# LaTeX Notes Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Give every apore-lite chapter a condensed, wiki-grounded LaTeX study guide that builds to PDF, plus a script that combines a domain's guides into one continuously-paginated book.

**Architecture:** A single style package (`apore-notes.sty`) defines five content boxes and a set of structural macros whose heading level depends on a package option, so one chapter source compiles correctly both standalone and as part of a combined book. Claude generates each chapter's `notes.tex` from `wiki/` under a strict wiki-only constraint. A stdlib-only Python script extracts each chapter's body from between fixed markers, concatenates them under one preamble, and runs `latexmk` once.

**Tech Stack:** LaTeX (`article`, `tcolorbox`, `amsmath`), `latexmk` + MiKTeX 25.12 / pdfTeX 4.23, Python 3.14 standard library only.

**Spec:** `docs/superpowers/specs/2026-09-19-latex-notes-design.md`

## Global Constraints

- **No git commands.** The user stages and commits. Never run `git add`, `git commit`, or any other git command during this plan.
- **No test files land in the repo.** Verification is by real builds and throwaway checks under the scratchpad directory (`C:\Users\jerom\AppData\Local\Temp\claude\C--Users-jerom-OneDrive-Desktop-Projects-apore-lite\29a9b915-e7d6-4830-bfb0-9f1d2a0a8415\scratchpad`).
- **Strict wiki-only content.** The hard constraint in root `CLAUDE.md` applies to all generated notes. Nothing appears that is not traceable to a wiki page and its cited source. No outside knowledge fills gaps.
- **`build_notes.py` uses the Python standard library only**: `argparse`, `re`, `shutil`, `subprocess`, `sys`, `datetime`, `pathlib`. No third-party imports.
- **LaTeX packages are limited to:** `geometry`, `amsmath`, `amssymb`, `amsthm`, `tcolorbox`, `enumitem`, `multicol`, `booktabs`, `xcolor`, `microtype`, `hyperref`. All exist in MiKTeX, TeX Live, and Overleaf.
- **Fixed filenames.** `notes.tex` / `notes.pdf` at chapter level; `full-notes.tex` / `full-notes.pdf` at domain level. Never repeat the domain or chapter name in the filename.
- **Body markers are exact:** `% >>> APORE BODY START` and `% <<< APORE BODY END`.
- **MiKTeX PATH.** This session's shell has a stale PATH. Every LaTeX command must be prefixed with:
  `$env:Path = "C:\Users\jerom\AppData\Local\Programs\MiKTeX\miktex\bin\x64\;$env:Path";`

---

## File Structure

| File | Action | Responsibility |
|---|---|---|
| `shared/_templates/notes/apore-notes.sty` | Create | All visual style, environments, structural macros, package options |
| `shared/_templates/notes/notes.tex` | Create | Chapter skeleton with markers and metadata placeholders |
| `shared/_templates/notes/full-notes-README.md` | Create | Explains the generated `full-notes/` folder |
| `shared/scripts/build_notes.py` | Create | Chapter discovery, body extraction, master assembly, `latexmk` invocation |
| `shared/protocols/notes.md` | Create | The step-by-step generation protocol Claude follows |
| `CLAUDE.md` | Modify | Trigger row + folder reference tree |
| `shared/protocols/compile.md` | Modify | Step 11 offering notes; recompile clause |
| `shared/_templates/CHAPTER.md` | Modify | `**Notes:**` status field |
| `shared/scripts/README.md` | Modify | `build_notes.py` entry |
| `.gitignore` | Modify | LaTeX build artifacts |

---

### Task 1: Style package

**Files:**
- Create: `shared/_templates/notes/apore-notes.sty`

**Interfaces:**
- Consumes: nothing
- Produces: package options `combined`, `toc`; macros `\notesmeta{subject}{chapter}{date}`, `\makenotestitle`, `\chapterhead{title}`, `\topic{name}`, `\subtopic{name}`, `\src{filename}`; environments `keydef{term}`, `formula{name}`, `method{name}`, `worked{name}`, `pitfall`; lists `steps`, `points`

- [ ] **Step 1: Write the style package**

```latex
% apore-notes.sty: condensed study-guide style for apore-lite
% Generated notes are wiki-grounded; every box carries a \src{} citation.
\NeedsTeXFormat{LaTeX2e}
\ProvidesPackage{apore-notes}[2026/09/19 apore-lite condensed notes style]

\newif\ifapore@combined \apore@combinedfalse
\newif\ifapore@toc      \apore@tocfalse
\DeclareOption{combined}{\apore@combinedtrue}
\DeclareOption{toc}{\apore@toctrue}
\DeclareOption*{\PackageWarning{apore-notes}{Unknown option '\CurrentOption'}}
\ProcessOptions\relax

\RequirePackage[margin=1in]{geometry}
\RequirePackage{amsmath}
\RequirePackage{amssymb}
\RequirePackage{amsthm}
\RequirePackage{xcolor}
\RequirePackage[most]{tcolorbox}
\RequirePackage{enumitem}
\RequirePackage{multicol}
\RequirePackage{booktabs}
\RequirePackage{microtype}
\RequirePackage[hidelinks]{hyperref}

% --- palette -------------------------------------------------------------
\definecolor{aporeDef}{HTML}{2563EB}
\definecolor{aporeFormula}{HTML}{7C3AED}
\definecolor{aporeMethod}{HTML}{059669}
\definecolor{aporeWorked}{HTML}{D97706}
\definecolor{aporePitfall}{HTML}{DC2626}
\definecolor{aporeMuted}{HTML}{6B7280}

% --- document metadata ---------------------------------------------------
\def\apore@subject{}
\def\apore@chapter{}
\def\apore@date{}
\newcommand{\notesmeta}[3]{%
  \def\apore@subject{#1}\def\apore@chapter{#2}\def\apore@date{#3}%
}

\newcommand{\makenotestitle}{%
  \begin{center}
    {\Large\bfseries\apore@chapter\par}
    \vspace{3pt}
    {\normalsize\apore@subject\par}
    \vspace{3pt}
    {\footnotesize\color{aporeMuted}Condensed study notes\quad$\cdot$\quad compiled \apore@date\par}
  \end{center}
  \vspace{2pt}\hrule\vspace{12pt}
  \ifapore@toc\tableofcontents\vspace{12pt}\fi
}

% --- structure -----------------------------------------------------------
% Heading level depends on build mode, so one chapter source compiles both
% standalone and as part of the combined book.
\ifapore@combined
  \setcounter{tocdepth}{2}
  \newcommand{\chapterhead}[1]{\clearpage\section{#1}}
  \newcommand{\topic}[1]{\subsection{#1}}
  \newcommand{\subtopic}[1]{\subsubsection{#1}}
\else
  \setcounter{tocdepth}{1}
  % No-op: \makenotestitle already names the chapter.
  \newcommand{\chapterhead}[1]{\relax}
  \newcommand{\topic}[1]{\section{#1}}
  \newcommand{\subtopic}[1]{\subsection{#1}}
\fi

% --- citation ------------------------------------------------------------
\newcommand{\src}[1]{{\footnotesize\color{aporeMuted}\textsf{Source: #1}}}

% --- lists ---------------------------------------------------------------
\newlist{steps}{enumerate}{1}
\setlist[steps]{leftmargin=*,itemsep=2pt,topsep=3pt,label=\arabic*.}
\newlist{points}{itemize}{1}
\setlist[points]{leftmargin=*,itemsep=2pt,topsep=3pt,label=\textbullet}

% --- content boxes -------------------------------------------------------
\tcbset{aporebox/.style={
  breakable, enhanced, arc=0pt, outer arc=0pt,
  boxrule=0pt, leftrule=2.5pt,
  colback=white, colbacktitle=white,
  fonttitle=\bfseries\small,
  boxsep=0pt, left=9pt, right=6pt, top=5pt, bottom=5pt,
  titlerule=0pt, toptitle=2pt, bottomtitle=3pt,
  before skip=9pt, after skip=9pt
}}

\newtcolorbox{keydef}[1]{aporebox,colframe=aporeDef,coltitle=aporeDef,title={Definition: #1}}
\newtcolorbox{formula}[1]{aporebox,colframe=aporeFormula,coltitle=aporeFormula,title={#1}}
\newtcolorbox{method}[1]{aporebox,colframe=aporeMethod,coltitle=aporeMethod,title={Method: #1}}
\newtcolorbox{worked}[1]{aporebox,colframe=aporeWorked,coltitle=aporeWorked,title={Example: #1}}
\newtcolorbox{pitfall}{aporebox,colframe=aporePitfall,coltitle=aporePitfall,title={Watch out}}

% --- body spacing --------------------------------------------------------
\setlength{\parindent}{0pt}
\setlength{\parskip}{4pt}

\endinput
```

`steps` and `points` are additions beyond the spec's §3 table. They exist because `method` bodies need a compact numbered list and `keydef` bodies need compact bullets; without them every generated file would repeat the same `enumitem` options inline.

- [ ] **Step 2: Build a fixture in standalone mode**

Write `<scratchpad>/styletest/fixture.tex` and copy the `.sty` next to it:

```latex
\documentclass[11pt]{article}
\usepackage{apore-notes}
\notesmeta{Test Subject}{01. Fixture Chapter}{2026-09-19}
\begin{document}
\makenotestitle
% >>> APORE BODY START
\chapterhead{Fixture Chapter}
\topic{First Topic}
\begin{keydef}{Test Term}
A term defined for the fixture. \src{fixture.html}
\end{keydef}
\begin{formula}{Quadratic Formula}
\[ x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a} \]
\src{fixture.html}
\end{formula}
\begin{method}{Solving a Quadratic}
\begin{steps}
\item Put the equation in standard form.
\item Apply the formula above.
\end{steps}
\src{fixture.html}
\end{method}
\begin{worked}{Solve $x^2-3x+2=0$}
$a=1$, $b=-3$, $c=2$, so $x = 1$ or $x = 2$. \src{fixture.html}
\end{worked}
\begin{pitfall}
Forgetting the $\pm$ drops a root. \src{fixture.html}
\end{pitfall}
\subtopic{A Subtopic}
\begin{points}
\item First point.
\item Second point.
\end{points}
% <<< APORE BODY END
\end{document}
```

Run:

```powershell
$env:Path = "C:\Users\jerom\AppData\Local\Programs\MiKTeX\miktex\bin\x64\;$env:Path"; latexmk -pdf -interaction=nonstopmode -halt-on-error fixture.tex
```

Expected: exit 0, `fixture.pdf` exists. No TOC (standalone default), no duplicated chapter heading under the title block.

- [ ] **Step 3: Build the same fixture in combined mode**

Copy `fixture.tex` to `fixture-combined.tex`, changing only the package line to `\usepackage[combined,toc]{apore-notes}`.

Run the same `latexmk` command on it.

Expected: exit 0. The PDF now has a table of contents, "Fixture Chapter" as a numbered `\section` on its own page, and "First Topic" as a `\subsection` beneath it.

- [ ] **Step 4: Confirm both PDFs and read the log**

Confirm both PDFs exist and are non-empty. Grep the `.log` files for `LaTeX Warning: Reference` and `Overfull \hbox` exceeding 20pt; fix the style if either appears. Do not proceed with a package that emits errors.

---

### Task 2: Templates

**Files:**
- Create: `shared/_templates/notes/notes.tex`
- Create: `shared/_templates/notes/full-notes-README.md`

**Interfaces:**
- Consumes: `apore-notes.sty` macros from Task 1
- Produces: the skeleton Task 4's protocol fills in, and the README Task 3's script copies

- [ ] **Step 1: Write the chapter skeleton**

`shared/_templates/notes/notes.tex`:

```latex
% apore-lite condensed study notes.
% Generated from this chapter's wiki/. Safe to edit by hand.
% Replace SUBJECT, CHAPTER and DATE below. Keep both APORE BODY markers
% exactly as they are: shared/scripts/build_notes.py extracts the text
% between them when building the combined domain PDF.
\documentclass[11pt]{article}
\usepackage{apore-notes}

\notesmeta{SUBJECT}{CHAPTER}{DATE}

\begin{document}
\makenotestitle
% >>> APORE BODY START
\chapterhead{CHAPTER TITLE}

% <<< APORE BODY END
\end{document}
```

- [ ] **Step 2: Write the full-notes README template**

`shared/_templates/notes/full-notes-README.md`:

```markdown
# full-notes/

**This folder is generated. Do not edit anything in it by hand.**

`full-notes.tex` is assembled by `shared/scripts/build_notes.py` from every
chapter's `notes/notes.tex` in this domain. Any edit you make here is
overwritten the next time the script runs.

## Where to edit instead

Each chapter's notes live at `chapters/{N}-{slug}/notes/notes.tex`. That is the
editable source. Edit there, then rebuild.

## Rebuilding

From the repository root:

```bash
python shared/scripts/build_notes.py {domain}
```

To scope a build to specific chapters, useful when an exam covers only part of
the domain:

```bash
python shared/scripts/build_notes.py {domain} --chapters 1-3
python shared/scripts/build_notes.py {domain} --chapters 1,3,5
```

A scoped build writes its own file (`full-notes-ch01-02-03.pdf`) and never
overwrites the complete `full-notes.pdf`.

Add `--no-build` to write the `.tex` without running `latexmk`.

## Requirements

`latexmk` plus a TeX engine on PATH: MiKTeX on Windows, MacTeX or BasicTeX on
macOS. No editor or extension is required.
```

- [ ] **Step 3: Verify the skeleton compiles**

Copy `notes.tex` and `apore-notes.sty` into `<scratchpad>/skeletontest/`, substitute the three placeholders with test values, and build with the Task 1 `latexmk` command.

Expected: exit 0, a one-page PDF with just the title block. An empty body must not error.

---

### Task 3: `build_notes.py`

**Files:**
- Create: `shared/scripts/build_notes.py`

**Interfaces:**
- Consumes: the body markers and `apore-notes.sty` options from Task 1; `full-notes-README.md` from Task 2
- Produces: CLI `python shared/scripts/build_notes.py <domain> [--chapters SPEC] [--no-build]`; exit codes 0 / 1 / 2 / 3

- [ ] **Step 1: Write the script**

```python
#!/usr/bin/env python3
"""Combine a domain's per-chapter LaTeX notes into a single PDF.

Reads every chapter's notes/notes.tex, extracts the text between the APORE
body markers, concatenates the bodies under one preamble, and runs latexmk.

See docs/superpowers/specs/2026-09-19-latex-notes-design.md
"""

from __future__ import annotations

import argparse
import re
import shutil
import subprocess
import sys
from datetime import date
from pathlib import Path

BODY_START = "% >>> APORE BODY START"
BODY_END = "% <<< APORE BODY END"

EXIT_OK = 0
EXIT_INPUT = 1
EXIT_NO_LATEXMK = 2
EXIT_BUILD_FAILED = 3

REPO_ROOT = Path(__file__).resolve().parents[2]
TEMPLATE_DIR = REPO_ROOT / "shared" / "_templates" / "notes"


class InputError(Exception):
    """Unusable input: bad selection, missing markers, nothing to build."""


def parse_chapter_selection(spec):
    """Expand a selection string such as "1-3,7" into {1, 2, 3, 7}."""
    numbers = set()
    for part in spec.split(","):
        part = part.strip()
        if not part:
            continue
        if "-" in part:
            low, _, high = part.partition("-")
            try:
                low_n, high_n = int(low), int(high)
            except ValueError:
                raise InputError("invalid chapter range: %r" % part)
            if low_n > high_n:
                raise InputError("reversed chapter range: %r" % part)
            numbers.update(range(low_n, high_n + 1))
        else:
            try:
                numbers.add(int(part))
            except ValueError:
                raise InputError("invalid chapter number: %r" % part)
    if not numbers:
        raise InputError("empty chapter selection: %r" % spec)
    return numbers


def chapter_number(folder_name):
    """Leading digits of a chapter folder name, or None."""
    match = re.match(r"^(\d+)", folder_name)
    return int(match.group(1)) if match else None


def discover_chapters(domain_dir):
    """All numbered chapter folders in a domain, ordered by number."""
    chapters_dir = domain_dir / "chapters"
    if not chapters_dir.is_dir():
        raise InputError("no chapters/ folder in %s" % domain_dir)
    found = []
    for child in sorted(chapters_dir.iterdir()):
        if not child.is_dir():
            continue
        number = chapter_number(child.name)
        if number is not None:
            found.append((number, child))
    found.sort(key=lambda pair: pair[0])
    return found


def select_chapters(chapters, wanted):
    """Filter chapters to those with notes. Returns (selected, warnings)."""
    selected = []
    warnings = []
    for number, chapter_dir in chapters:
        if wanted is not None and number not in wanted:
            continue
        notes_tex = chapter_dir / "notes" / "notes.tex"
        if not notes_tex.is_file():
            warnings.append(
                "chapter %02d (%s): no notes/notes.tex, skipped"
                % (number, chapter_dir.name)
            )
            continue
        selected.append((number, notes_tex))
    if wanted is not None:
        present = {number for number, _ in chapters}
        for number in sorted(wanted - present):
            warnings.append("chapter %02d: not found in this domain" % number)
    return selected, warnings


def extract_body(tex_path):
    """Text between the body markers.

    A missing marker is fatal rather than a skip: silently dropping a chapter
    from a study book is worse than refusing to build it.
    """
    text = tex_path.read_text(encoding="utf-8")
    start = text.find(BODY_START)
    end = text.find(BODY_END)
    if start == -1:
        raise InputError("%s: missing marker %r" % (tex_path, BODY_START))
    if end == -1:
        raise InputError("%s: missing marker %r" % (tex_path, BODY_END))
    if end < start:
        raise InputError("%s: end marker precedes start marker" % tex_path)
    return text[start + len(BODY_START):end].strip("\n")


def domain_display_name(domain_dir):
    """First '# ' heading of DOMAIN.md, falling back to the folder name."""
    domain_md = domain_dir / "DOMAIN.md"
    if domain_md.is_file():
        for line in domain_md.read_text(encoding="utf-8").splitlines():
            if line.startswith("# "):
                return line[2:].strip()
    return domain_dir.name


def output_stem(numbers, is_subset):
    """Base filename. Ranges are expanded, so a suffix never fakes a range."""
    if not is_subset:
        return "full-notes"
    return "full-notes-ch" + "-".join("%02d" % n for n in numbers)


def build_master_tex(domain_name, bodies, today):
    """Assemble the combined document source."""
    header = "\n".join([
        "% Generated by shared/scripts/build_notes.py. Do not edit by hand.",
        "% Edit each chapter's notes/notes.tex instead, then rebuild.",
        "\\documentclass[11pt]{article}",
        "\\usepackage[combined,toc]{apore-notes}",
        "",
        "\\notesmeta{%s}{Full Notes}{%s}" % (domain_name, today),
        "",
        "\\begin{document}",
        "\\makenotestitle",
        "",
    ])
    return header + "\n" + "\n\n".join(bodies) + "\n\n\\end{document}\n"


def copy_assets(out_dir):
    """Refresh the style package and the README from the templates.

    Both are overwritten every run. The README itself states that edits here
    are lost on the next build, so keeping a stale copy would make the folder
    contradict its own instructions.
    """
    sty_src = TEMPLATE_DIR / "apore-notes.sty"
    if not sty_src.is_file():
        raise InputError("missing template: %s" % sty_src)
    shutil.copyfile(sty_src, out_dir / "apore-notes.sty")
    readme_src = TEMPLATE_DIR / "full-notes-README.md"
    if readme_src.is_file():
        shutil.copyfile(readme_src, out_dir / "README.md")


def run_latexmk(tex_name, cwd):
    """Build the PDF. Returns an exit code."""
    if shutil.which("latexmk") is None:
        return EXIT_NO_LATEXMK
    result = subprocess.run(
        ["latexmk", "-pdf", "-interaction=nonstopmode", "-halt-on-error", tex_name],
        cwd=str(cwd),
        capture_output=True,
        text=True,
    )
    if result.returncode != 0:
        tail = (result.stdout + result.stderr).splitlines()[-20:]
        for line in tail:
            print(line, file=sys.stderr)
        return EXIT_BUILD_FAILED
    return EXIT_OK


def resolve_domain(name):
    """Accept a domain folder name or a path to one."""
    candidate = REPO_ROOT / name
    if candidate.is_dir():
        return candidate.resolve()
    direct = Path(name)
    if direct.is_dir():
        return direct.resolve()
    raise InputError("unknown domain: %s" % name)


def main(argv=None):
    parser = argparse.ArgumentParser(
        description="Combine a domain's chapter notes into one PDF."
    )
    parser.add_argument("domain", help="domain folder name, e.g. material204")
    parser.add_argument(
        "--chapters", help="chapter selection, e.g. 1-3 or 1,3,5"
    )
    parser.add_argument(
        "--no-build",
        action="store_true",
        help="write the .tex but do not run latexmk",
    )
    args = parser.parse_args(argv)

    try:
        domain_dir = resolve_domain(args.domain)
        wanted = parse_chapter_selection(args.chapters) if args.chapters else None
        chapters = discover_chapters(domain_dir)
        selected, warnings = select_chapters(chapters, wanted)
        for warning in warnings:
            print("warning: %s" % warning, file=sys.stderr)
        if not selected:
            raise InputError("no chapters with notes/notes.tex were selected")
        bodies = [extract_body(path) for _, path in selected]
        out_dir = domain_dir / "full-notes"
        out_dir.mkdir(parents=True, exist_ok=True)
        copy_assets(out_dir)
    except InputError as error:
        print("error: %s" % error, file=sys.stderr)
        return EXIT_INPUT

    stem = output_stem([n for n, _ in selected], wanted is not None)
    tex_path = out_dir / (stem + ".tex")
    tex_path.write_text(
        build_master_tex(
            domain_display_name(domain_dir), bodies, date.today().isoformat()
        ),
        encoding="utf-8",
    )
    print("wrote %s (%d chapters)" % (tex_path, len(selected)))

    if args.no_build:
        return EXIT_OK

    status = run_latexmk(tex_path.name, out_dir)
    if status == EXIT_NO_LATEXMK:
        print(
            "error: latexmk not found on PATH. Install MiKTeX "
            "(Windows: winget install MiKTeX.MiKTeX) or MacTeX/BasicTeX (macOS).",
            file=sys.stderr,
        )
    elif status == EXIT_BUILD_FAILED:
        print("error: latexmk failed for %s" % tex_path.name, file=sys.stderr)
    else:
        print("built %s" % (out_dir / (stem + ".pdf")))
    return status


if __name__ == "__main__":
    sys.exit(main())
```

- [ ] **Step 2: Check the pure functions from the scratchpad**

Write a throwaway script at `<scratchpad>/check_build_notes.py` that imports the module by path and asserts:

```python
import sys
from pathlib import Path

sys.path.insert(0, r"C:\Users\jerom\OneDrive\Desktop\Projects\apore-lite\shared\scripts")
import build_notes as bn

assert bn.parse_chapter_selection("1-3") == {1, 2, 3}
assert bn.parse_chapter_selection("1,3,5") == {1, 3, 5}
assert bn.parse_chapter_selection("2") == {2}
assert bn.parse_chapter_selection("1-2,5") == {1, 2, 5}
for bad in ("", "x", "3-1", "1-x"):
    try:
        bn.parse_chapter_selection(bad)
    except bn.InputError:
        pass
    else:
        raise AssertionError("expected InputError for %r" % bad)

assert bn.chapter_number("02-atomic-structure") == 2
assert bn.chapter_number("notes") is None

assert bn.output_stem([1, 2], False) == "full-notes"
assert bn.output_stem([1, 2, 3], True) == "full-notes-ch01-02-03"
assert bn.output_stem([1, 3, 5], True) == "full-notes-ch01-03-05"

tmp = Path(r"<scratchpad>") / "bodytest"
tmp.mkdir(parents=True, exist_ok=True)
good = tmp / "good.tex"
good.write_text(
    "preamble\n%s\nBODY LINE\n%s\ntrailer\n" % (bn.BODY_START, bn.BODY_END),
    encoding="utf-8",
)
assert bn.extract_body(good) == "BODY LINE"

bad = tmp / "bad.tex"
bad.write_text("no markers here\n", encoding="utf-8")
try:
    bn.extract_body(bad)
except bn.InputError:
    pass
else:
    raise AssertionError("expected InputError for missing markers")

print("all checks passed")
```

Run: `python <scratchpad>/check_build_notes.py`
Expected: `all checks passed`, exit 0.

- [ ] **Step 3: Check the error paths through the CLI**

```powershell
python shared/scripts/build_notes.py no-such-domain; "exit=$LASTEXITCODE"
python shared/scripts/build_notes.py material204 --chapters 99; "exit=$LASTEXITCODE"
```

Expected: both print an `error:` line to stderr and exit 1. The second also warns that chapter 99 was not found.

- [ ] **Step 4: Delete the throwaway check script**

Remove `<scratchpad>/check_build_notes.py` and `<scratchpad>/bodytest`. Nothing from this task's verification belongs in the repo, and the scratchpad should not accumulate stale scripts.

---

### Task 4: Notes protocol

**Files:**
- Create: `shared/protocols/notes.md`

**Interfaces:**
- Consumes: templates from Tasks 1–2, the script from Task 3
- Produces: the procedure the trigger row in Task 5 points at

- [ ] **Step 1: Write the protocol**

Match the voice and numbered-step structure of `shared/protocols/compile.md` exactly: a blockquote header stating when to read it, `### Step N:` headings, and blockquoted lines for anything Claude says to the user.

Content, in order:

1. **Header blockquote**: read in full on "make notes" / "generate notes" / "notes for [chapter]"; follow every step in order; academic integrity applies from step 1; `wiki/` is the only permitted input and `sources/` is never read.
2. **Step 1: Identify the chapter.** Ask if unclear; confirm the path `{domain}/chapters/{N}-{slug}/`.
3. **Step 2: Verify the wiki.** If `wiki/` is missing or has no `_index.md`, stop with: *"No compiled wiki found. Say 'compile' first, then I can generate notes."*
4. **Step 3: Check for existing notes.** If `notes/notes.tex` exists, never overwrite silently. Ask which of: regenerate from scratch / append only topics not already present / skip.
5. **Step 4: Create `notes/`** and copy `shared/_templates/notes/apore-notes.sty` into it, overwriting any existing copy.
6. **Step 5: Read the wiki.** `_index.md` first, for topic order; then every topic page.
7. **Step 6: Write `notes/notes.tex`** from `shared/_templates/notes/notes.tex`. Fill `\notesmeta` with the `**Domain:**` field from `CHAPTER.md`, the `# Chapter {N}: {Title}` heading, and today's date. Then apply the content rules, reproduced in full in the protocol:
   - One `\topic` per wiki topic page, in `_index.md` order
   - Within a topic: definitions → formulas → methods → worked examples → pitfalls; omit absent categories
   - Definition → `keydef`; equation or named result → `formula`; step-by-step procedure → `method`; example demonstrating a procedure → `worked`, terse, at most one per `method`; wiki "Common Misconceptions" content → `pitfall`
   - Drop purely illustrative examples, narrative prose, transitions, restatement
   - Every environment carries a `\src{}` from the wiki's own `> Source:` line; multiple sources comma-separated in one `\src{}`
   - Typeset math properly: `\[...\]` display, `$...$` inline, `align` for multi-step work; convert Unicode symbols (`∈`, `∉`, `∪`, `⊆`, `≤`, `≥`, `×`, `→`) to LaTeX equivalents
   - A topic yielding no definition, formula, method or pitfall produces no section
8. **Step 7: Build.** From the notes folder: `latexmk -pdf -interaction=nonstopmode -halt-on-error notes.tex`. If `latexmk` is absent, skip the build, report the `.tex` is ready, and name the engine to install per platform. This is not an error.
9. **Step 8: Update `CHAPTER.md`.** Set `**Notes:** generated {YYYY-MM-DD}`, inserting the field immediately after `**Compile Status:**` if absent.
10. **Step 9: Confirm.** Report the topic count and the PDF path if it built.
11. **Closing section: "On Append".** When the user chose append: compare `\topic{...}` headings already in the file against the `_index.md` topic list, insert only missing topics in index order before the end marker, and never modify existing content.
12. **Closing section: "Combining a Domain".** Point at `python shared/scripts/build_notes.py {domain}` with the `--chapters` and `--no-build` flags, and note that `full-notes/` is generated output.

- [ ] **Step 2: Verify the protocol is self-contained**

Re-read the file and confirm an agent with no other context could follow it: every path is exact, every user-facing line is quoted verbatim, and the content rules are present in full rather than referencing the spec.

---

### Task 5: Wire-up

**Files:**
- Modify: `CLAUDE.md`
- Modify: `shared/protocols/compile.md`
- Modify: `shared/_templates/CHAPTER.md`
- Modify: `shared/scripts/README.md`
- Modify: `.gitignore`

**Interfaces:**
- Consumes: `shared/protocols/notes.md` from Task 4, `build_notes.py` from Task 3
- Produces: nothing downstream

- [ ] **Step 1: Add the trigger row to `CLAUDE.md`**

In the Trigger Phrases table, after the "compile" row:

```markdown
| "make notes" / "generate notes" / "notes for [chapter]" | `shared/protocols/notes.md` |
```

- [ ] **Step 2: Update the Folder Reference tree in `CLAUDE.md`**

Add `notes/` under the chapter tree and `full-notes/` under the domain:

```
├── {domain}/
│   ├── DOMAIN.md                  ← read when entering a domain
│   ├── full-notes/                ← generated: combined domain PDF (build_notes.py)
│   └── chapters/
│       └── {N}-{chapter}/
│           ├── CHAPTER.md         ← read before every session
│           ├── sources/           ← immutable raw inputs (never edit after drop-in)
│           ├── wiki/              ← compiled knowledge (your only grounding)
│           ├── notes/             ← LaTeX study guide (notes.tex / notes.pdf)
│           └── progress/
```

Keep the existing `progress/` sub-entries and the `shared/` block unchanged.

- [ ] **Step 3: Add Step 11 to `shared/protocols/compile.md`**

After the existing Step 10, before the `---` preceding "On Recompile":

```markdown
### Step 11: Offer notes

Ask:
> "Generate condensed study notes for this chapter?"

If yes, read `shared/protocols/notes.md` in full and follow it. If no, stop.
```

- [ ] **Step 4: Add the recompile clause to `shared/protocols/compile.md`**

Append to the numbered list in the "On Recompile" section:

```markdown
8. If `notes/notes.tex` exists, offer to append the newly-added topics to it, following the "On Append" section of `shared/protocols/notes.md`. Never regenerate it without asking.
```

- [ ] **Step 5: Add the Notes field to `shared/_templates/CHAPTER.md`**

Immediately after the `**Compile Status:** not compiled` line:

```markdown
**Notes:** not generated
```

- [ ] **Step 6: Document the script in `shared/scripts/README.md`**

Change the `## Planned Scripts` heading to `## Scripts`, and add above the existing `extract-pdf.py` entry:

```markdown
### build_notes.py
Combine a domain's per-chapter LaTeX notes into one continuously-paginated PDF.

**Usage:**
```bash
python shared/scripts/build_notes.py material204
python shared/scripts/build_notes.py material204 --chapters 1-3
python shared/scripts/build_notes.py material204 --no-build
```

**Why it exists:** Each chapter's `notes/notes.tex` builds on its own, but studying
for an exam means reading several chapters as one document with continuous page
numbers, a single table of contents, and working cross-links. Merging finished
PDFs gives none of those, so the script concatenates the LaTeX bodies and runs one
real build. Output lands in `{domain}/full-notes/`, which is generated, so edit the
chapter sources instead.

Exit codes: `0` success, `1` bad input, `2` `.tex` written but `latexmk` missing,
`3` `latexmk` ran and failed.
```

Leave the `extract-pdf.py` entry and the closing paragraph untouched.

- [ ] **Step 7: Append build artifacts to `.gitignore`**

```
# LaTeX build artifacts
*.aux
*.fdb_latexmk
*.fls
*.log
*.out
*.synctex.gz
*.toc
```

- [ ] **Step 8: Confirm no tracked file is newly ignored**

The repo has no existing `.aux`, `.log`, `.toc` or similar files, so these patterns cannot orphan tracked content. Confirm by listing files matching those extensions across the repo before relying on the change. Use the Glob tool, not git.

---

### Task 6: End-to-end verification

**Files:**
- Create: `material204/chapters/01-introduction/notes/` (`apore-notes.sty`, `notes.tex`, `notes.pdf`)
- Create: `material204/chapters/02-atomic-structure-and-interatomic-bonding/notes/` (same three)
- Create: `material204/full-notes/` (`README.md`, `apore-notes.sty`, `full-notes.tex`, `full-notes.pdf`)
- Modify: both chapters' `CHAPTER.md`

**Interfaces:**
- Consumes: everything from Tasks 1–5
- Produces: the first real notes in the repo

- [ ] **Step 1: Generate notes for `material204` chapter 01**

Follow `shared/protocols/notes.md` end to end for
`material204/chapters/01-introduction/`. Read `wiki/_index.md` first for topic
order, then every topic page. Apply the content rules strictly: wiki-only.

- [ ] **Step 2: Build chapter 01 and inspect**

```powershell
$env:Path = "C:\Users\jerom\AppData\Local\Programs\MiKTeX\miktex\bin\x64\;$env:Path"; latexmk -pdf -interaction=nonstopmode -halt-on-error notes.tex
```

Expected: exit 0, `notes.pdf` created. Read the PDF back and confirm every box
carries a `\src{}` whose filename matches a `> Source:` line in that chapter's
wiki, and that nothing appears which the wiki does not state.

- [ ] **Step 3: Generate and build notes for `material204` chapter 02**

Same procedure against
`material204/chapters/02-atomic-structure-and-interatomic-bonding/`. This
chapter has denser formula content, so it exercises `formula` and `method` more
heavily than chapter 01.

- [ ] **Step 4: Run the combined build**

```powershell
$env:Path = "C:\Users\jerom\AppData\Local\Programs\MiKTeX\miktex\bin\x64\;$env:Path"; python shared/scripts/build_notes.py material204
```

Expected: exit 0. `material204/full-notes/` contains `README.md`,
`apore-notes.sty`, `full-notes.tex`, `full-notes.pdf`. Open the PDF and confirm:
a table of contents listing both chapters and their topics, continuous page
numbering across the chapter boundary, each chapter starting on a fresh page,
and working internal links from the TOC.

- [ ] **Step 5: Run a subset build**

```powershell
$env:Path = "C:\Users\jerom\AppData\Local\Programs\MiKTeX\miktex\bin\x64\;$env:Path"; python shared/scripts/build_notes.py material204 --chapters 1
```

Expected: exit 0, `full-notes-ch01.pdf` and `full-notes-ch01.tex` created,
`full-notes.pdf` byte-identical to before this step. Confirm the timestamp on
`full-notes.pdf` is unchanged.

- [ ] **Step 6: Confirm the missing-marker error path**

Copy chapter 01's `notes.tex` to the scratchpad, delete its end marker in the
copy, then temporarily point a scratch domain tree at it, or simpler, verify by
reading `extract_body` was exercised in Task 3 Step 2 and confirm here only that
a chapter folder lacking `notes/notes.tex` produces a warning and is skipped:

```powershell
python shared/scripts/build_notes.py calculus275 --no-build
```

`calculus275` has three chapters and no notes at all, so expected output is three
skip warnings followed by `error: no chapters with notes/notes.tex were selected`
and exit 1.

- [ ] **Step 7: Update both `CHAPTER.md` files**

Set `**Notes:** generated {today}` in each, inserted after `**Compile Status:**`.

- [ ] **Step 8: Report, do not commit**

Summarise for the user: files created, PDF page counts, and the exact set of
paths they will want to stage. Run no git commands.

---

## Self-Review

**Spec coverage:**

| Spec section | Task |
|---|---|
| §2 Folder layout | Tasks 3, 6 |
| §3 Style package, options, macros, environments, markers | Task 1 |
| §3 Chapter skeleton | Task 2 |
| §4 Content generation rules | Task 4 Step 1 item 7; applied in Task 6 |
| §5 Protocol steps 1–9 and On Append | Task 4 |
| §6 CLAUDE.md, compile.md, new-chapter.md unchanged | Task 5 Steps 1–4 |
| §7 Script behaviour, output naming, exit codes | Task 3 |
| §8 Templates, CHAPTER.md field, scripts README, .gitignore | Tasks 2, 5 |
| §9 Build environment | Global Constraints; Task 3 Step 1 error message |
| §10 Verification | Tasks 1, 3, 6 |

**Type consistency:** `BODY_START` / `BODY_END` are defined once in Task 3 Step 1
and match the literals in Tasks 1 and 2 exactly. `output_stem(numbers, is_subset)`,
`extract_body(tex_path)`, `parse_chapter_selection(spec)`, `chapter_number(name)`
and `InputError` are used in Task 3 Step 2 under the same names and signatures
they are defined with. The package options `combined` and `toc` are declared in
Task 1 and consumed by `build_master_tex` in Task 3.

**Deviation from spec, recorded:** §10 verification step 1 called for a fixture
exercising both modes; Task 1 Steps 2–3 do this but keep the fixture in the
scratchpad rather than the repo, per the user's instruction that no test files
land in the codebase. §10 step 5's full error-path sweep is reduced in Task 6
Step 6 to the paths reachable without fabricating a broken chapter in the repo;
the marker paths are covered by Task 3 Step 2 instead.
