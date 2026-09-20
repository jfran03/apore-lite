# Design: LaTeX Notes per Chapter

**Date:** 2026-09-19
**Status:** approved, pending implementation plan

---

## 1. Purpose

Give every chapter a condensed, print-quality LaTeX study guide built from its
compiled `wiki/`. The guide is a problem-set companion: definitions, formulas,
procedures, and terse worked examples, scannable mid-problem. A Python script
combines a domain's chapter guides into one continuously-paginated book.

Claude generates the `.tex` from `wiki/`. The user then owns it and asks Claude
for edits.

### Goals

- One editable `.tex` per chapter, rendered to PDF by `latexmk`
- Strict wiki-only content, with a visible citation on every claim
- A combined per-domain PDF with unified TOC and continuous page numbers
- Portable across Windows and macOS; no dependency on any editor or extension

### Non-goals

- Generating notes from `sources/` directly. `wiki/` is the only input.
- Editing `progress/` state. Notes are read-only with respect to the quiz system.
- Cross-domain combined builds.
- Changes to `DOMAIN.md`.

---

## 2. Folder layout

```
{domain}/
├── DOMAIN.md
├── full-notes/                  ← generated; created on first combined build
│   ├── README.md
│   ├── apore-notes.sty
│   ├── full-notes.tex
│   └── full-notes.pdf
└── chapters/
    └── {N}-{slug}/
        ├── CHAPTER.md
        ├── sources/
        ├── wiki/
        ├── progress/
        └── notes/               ← created on demand
            ├── apore-notes.sty
            ├── notes.tex        ← user-editable source
            └── notes.pdf        ← build output
```

Filenames inside each folder are fixed: `notes.tex` / `notes.pdf` at chapter
level, `full-notes.tex` / `full-notes.pdf` at domain level. The path carries the
identity; the filename does not repeat it.

`apore-notes.sty` is **copied** into every notes folder rather than referenced
across directories. This costs a duplicated file and buys: `latexmk` works with
no `TEXINPUTS` configuration, any notes folder is portable to another machine or
to Overleaf as-is, and a chapter's build cannot break because a shared file moved.
The master copy is `shared/_templates/notes/apore-notes.sty`; every copy is
overwritten from the master on each generation or combined build.

---

## 3. `apore-notes.sty`

Loads only packages present in MiKTeX, TeX Live, and Overleaf:
`geometry`, `amsmath`, `amssymb`, `amsthm`, `tcolorbox`, `enumitem`, `multicol`,
`booktabs`, `xcolor`, `microtype`, `hyperref`.

### Package options

| Option | Effect |
|---|---|
| *(none)* | Standalone mode: title block, no table of contents |
| `combined` | Combined mode: heading levels demoted one step |
| `toc` | Force a table of contents on |

Standalone chapter builds default to no TOC — a condensed guide is too short to
earn one. The combined build passes `combined,toc`.

### Structural macros

| Macro | Standalone | Combined |
|---|---|---|
| `\notesmeta{subject}{chapter}{date}` | stores metadata | stores metadata |
| `\makenotestitle` | renders title block (+ TOC if `toc`) | same |
| `\chapterhead{title}` | no-op (title block already names it) | `\clearpage\section{title}` |
| `\topic{name}` | `\section{name}` | `\subsection{name}` |
| `\subtopic{name}` | `\subsection{name}` | `\subsubsection{name}` |

`\chapterhead` being a no-op in standalone mode is deliberate: the title block
rendered by `\makenotestitle` already carries the chapter name, so repeating it
would waste space at the top of a two-page guide.

### Content environments

| Environment | Signature | Contents |
|---|---|---|
| `keydef` | `{term}` | Definition, one or two lines |
| `formula` | `{name}` | Boxed equation or result |
| `method` | `{name}` | Numbered procedure steps |
| `worked` | `{name}` | One terse worked example |
| `pitfall` | *(none)* | A misconception the wiki explicitly states |

All five are `tcolorbox` environments sharing one visual system: distinct accent
colour per type, same geometry and typography.

### Citation macro

`\src{filename}` renders a small grey source marker. Every box carries one. This
is what makes the strict wiki-only constraint auditable in the rendered PDF, not
just in the generation process.

### Body markers

Every chapter `notes.tex` contains exactly one marker pair:

```latex
% >>> APORE BODY START
% <<< APORE BODY END
```

Everything between them is the extractable body. The build script relies on this
contract; a file missing either marker is a hard error (§7).

### Chapter file skeleton

```latex
\documentclass[11pt]{article}
\usepackage{apore-notes}
\notesmeta{Materials 204}{02 — Atomic Structure and Interatomic Bonding}{2026-09-19}
\begin{document}
\makenotestitle
% >>> APORE BODY START
\chapterhead{Atomic Structure and Interatomic Bonding}

\topic{...}
...
% <<< APORE BODY END
\end{document}
```

`\makenotestitle` sits **above** the start marker, so the per-chapter title block
is excluded from the combined book.

---

## 4. Content generation rules

Input is `wiki/` only. `sources/` is never read during notes generation.

1. One `\topic` per wiki topic page, ordered as listed in `wiki/_index.md`.
2. Within a topic, order content: definitions → formulas → methods → worked
   examples → pitfalls. Omit any category the wiki does not supply.
3. Map wiki content to environments:
   - A stated definition → `keydef`
   - An equation, identity, or named result → `formula`
   - A described step-by-step procedure → `method`
   - An example that demonstrates a procedure → `worked`, kept terse
   - Content under a wiki "Common Misconceptions" heading → `pitfall`
4. Examples that are purely illustrative, with no reusable technique, are dropped.
   At most one `worked` per `method`.
5. Narrative prose, transitions, and restatement are dropped. This is a condensed
   guide, not a rendering of the wiki.
6. Every environment gets a `\src{}` taken from the wiki's own `> Source:` line
   for that claim. Multiple sources are comma-separated in one `\src{}`.
7. Mathematical content is typeset properly: `\[...\]` for display, `$...$` for
   inline, `align` for multi-step derivations. Unicode symbols in the wiki
   (`∈`, `∉`, `∪`, `⊆`, …) are converted to their LaTeX equivalents.

### Academic integrity

The hard constraint from root `CLAUDE.md` applies without exception. Nothing
appears in a notes file that is not traceable to a wiki page and its cited source.
No outside knowledge fills gaps. No "not covered in sources" callouts — a gap is
simply absent. If a wiki topic page yields no definition, formula, method, or
pitfall, that topic produces no section.

---

## 5. Protocol: `shared/protocols/notes.md`

Written in the same step-by-step, numbered style as `compile.md`.

**Step 1 — Identify the chapter.** Confirm `{domain}/chapters/{N}-{slug}/`.

**Step 2 — Verify the wiki exists.** If `wiki/` is empty or missing `_index.md`,
stop: *"No compiled wiki found. Say 'compile' first, then I can generate notes."*

**Step 3 — Check for an existing `notes/notes.tex`.** If present, do not
overwrite. Ask which the user wants:
  - regenerate from scratch, replacing the file
  - append only topics not already present in the file
  - skip

**Step 4 — Create `notes/`** and copy `apore-notes.sty` from
`shared/_templates/notes/`, overwriting any existing copy.

**Step 5 — Read all of `wiki/`**, starting with `_index.md` for topic order.

**Step 6 — Write `notes/notes.tex`** from the skeleton in
`shared/_templates/notes/notes.tex`, applying §4. Fill `\notesmeta` with: the
`**Domain:**` field from `CHAPTER.md` as subject, the `# Chapter {N}: {Title}`
heading as chapter, and today's date.

**Step 7 — Build.** Run from the notes folder:

```
latexmk -pdf -interaction=nonstopmode -halt-on-error notes.tex
```

If `latexmk` is not on PATH, skip the build and tell the user the `.tex` is
ready and which engine to install (§9). This is not an error.

**Step 8 — Update `CHAPTER.md`.** Set `**Notes:** generated {YYYY-MM-DD}`,
inserting the field after `**Compile Status:**` if it is not already present.

**Step 9 — Confirm.** Report topic count, and the PDF path if it built.

### Appending on regeneration

When the user chooses "append only new topics", compare `\topic{...}` headings
already in the file against the topic list in `wiki/_index.md`, and insert only
the missing ones, in index order, before the end marker. Existing content is
never modified.

---

## 6. Trigger and protocol changes

### `CLAUDE.md`

Add one row to the Trigger Phrases table:

| Phrase | Protocol to read |
|---|---|
| "make notes" / "generate notes" / "notes for [chapter]" | `shared/protocols/notes.md` |

Add a `notes/` entry to the Folder Reference tree, and `full-notes/` under
`{domain}/`.

### `shared/protocols/compile.md`

Add **Step 11 — Offer notes**, after the existing Step 10 confirmation:

> Ask: *"Generate condensed study notes for this chapter?"*
> If yes, read `shared/protocols/notes.md` and follow it. If no, stop.

Add a matching line to the "On Recompile" section: after a recompile, if
`notes/notes.tex` exists, offer to append newly-added topics to it.

### `shared/protocols/new-chapter.md`

Unchanged. Empty `notes/` folders are not pre-created; the folder appears the
first time notes are generated.

---

## 7. `shared/scripts/build_notes.py`

Python 3, standard library only (`argparse`, `pathlib`, `re`, `shutil`,
`subprocess`, `sys`). No third-party dependencies.

### Usage

```bash
python shared/scripts/build_notes.py material204
python shared/scripts/build_notes.py material204 --chapters 1-3
python shared/scripts/build_notes.py material204 --chapters 1,3,5
python shared/scripts/build_notes.py material204 --no-build
```

### Behaviour

1. Validate `{domain}/chapters/` exists.
2. Collect chapters by scanning `{domain}/chapters/*/notes/notes.tex`, sorted by
   the numeric prefix of the chapter folder.
3. Apply `--chapters` if given. The filter accepts comma-separated numbers and
   inclusive ranges, matched against the chapter folder's numeric prefix.
4. A selected chapter with no `notes/notes.tex` is a warning and is skipped. If
   the selection yields zero chapters, exit with an error.
5. Extract each chapter's body from between the §3 markers. A file missing either
   marker is a hard error naming the file — never a silent skip, since dropping a
   chapter from a study book without saying so is worse than failing.
6. Create `{domain}/full-notes/`. Copy `apore-notes.sty` from
   `shared/_templates/notes/`, overwriting. Copy
   `shared/_templates/notes/full-notes-README.md` to `README.md` only if absent.
7. Write the master `.tex`: preamble with `\usepackage[combined,toc]{apore-notes}`,
   then `\notesmeta{<domain name>}{Full Notes}{<today>}`, `\makenotestitle`, then
   each body in order. The domain name is read from the first `#` heading of
   `{domain}/DOMAIN.md`, falling back to the folder name if that file is missing
   or has no heading.
8. Run `latexmk -pdf -interaction=nonstopmode -halt-on-error <master>.tex` with
   the full-notes folder as working directory, unless `--no-build`.

### Output naming

The suffix is the sorted list of *selected* chapter numbers, each zero-padded to
two digits and joined by `-`. Ranges are expanded first, so the suffix never
looks like a range it is not.

| Invocation | Output |
|---|---|
| all chapters | `full-notes.tex` / `full-notes.pdf` |
| `--chapters 1-3` | `full-notes-ch01-02-03.tex` / `.pdf` |
| `--chapters 1,3,5` | `full-notes-ch01-03-05.tex` / `.pdf` |

A subset build never overwrites the complete book.

### Exit codes

| Code | Meaning |
|---|---|
| 0 | Success, PDF built (or `--no-build` and `.tex` written) |
| 1 | Usage or input error: unknown domain, no chapters selected, missing marker |
| 2 | `.tex` written, but `latexmk` is not on PATH — message names the engine to install |
| 3 | `latexmk` ran and failed — the last 20 lines of its output are printed |

Exit code 2 is distinct from 3 on purpose: a missing toolchain is a setup task,
a failed build is a content bug, and they need different responses.

---

## 8. Templates and git

### New template files

```
shared/_templates/notes/
├── apore-notes.sty
├── notes.tex
└── full-notes-README.md
```

`full-notes-README.md` explains: this folder is generated output; each chapter's
`notes/notes.tex` is the editable source; how to rebuild; how to scope a build to
specific chapters; and that edits made here are lost on the next run.

`shared/scripts/README.md` gains a `build_notes.py` entry following the existing
what / usage / why format. Its "Planned Scripts" heading becomes "Scripts", since
one now exists.

### `CHAPTER.md` template

Add `**Notes:** not generated` immediately after `**Compile Status:**`. Existing
chapter files gain the field when notes are first generated (§5, Step 8).

### `.gitignore`

Tracked: `.tex`, `.sty`, `.pdf`, `README.md`. The PDF is tracked deliberately so
notes stay readable on a machine with no TeX engine installed.

Appended:

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

---

## 9. Build environment

The only requirement is `latexmk` plus a TeX engine on PATH. Nothing in this
design depends on an editor or an extension.

- **Windows:** `winget install MiKTeX.MiKTeX` — ships `latexmk`, fetches packages
  on demand.
- **macOS:** MacTeX, or BasicTeX plus `tlmgr install latexmk`.
- **Optional:** VS Code's LaTeX Workshop extension (already installed on the
  Windows machine) runs the same `latexmk` on save, giving build-on-save and a
  side-by-side preview. `latexmk -pvc notes.tex` gives equivalent watch-rebuild
  behaviour in any terminal.

**Current state:** no TeX engine is installed on the Windows machine. LaTeX
Workshop 10.19.0 is present but has nothing to drive. Until an engine is
installed, generation produces `.tex` files that cannot be verified to build.

---

## 10. Verification

1. `apore-notes.sty` compiles standalone against a minimal document exercising
   all five environments, both structural modes, and `\src`.
2. Generate `notes.tex` for
   `material204/chapters/02-atomic-structure-and-interatomic-bonding/` and build
   it to PDF.
3. Generate a second chapter in the same domain, then run
   `build_notes.py material204` and confirm the combined PDF has a unified TOC,
   continuous page numbers, and working internal links.
4. Run `build_notes.py material204 --chapters 1-2` and confirm the subset output
   is written under its own name with `full-notes.pdf` untouched.
5. Exercise each error path: missing marker, unknown domain, empty selection,
   `latexmk` absent.
6. Spot-check the generated PDF against `wiki/` — every box traceable to a wiki
   claim, every `\src{}` matching the wiki's `> Source:` line, nothing present
   that the wiki does not state.

Step 2 onward requires a TeX engine (§9).
