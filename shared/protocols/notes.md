# Protocol: Notes

> Read this file in full when the user says "make notes", "generate notes", or "notes for [chapter]."
> Follow every step in order. Do not skip steps.
>
> **Academic integrity applies from step 1.** `wiki/` is the only permitted input. Never read `sources/` during notes generation. The wiki is already the compiled, citation-bearing record of those sources. Every line you write must be traceable to a wiki page.

---

## Steps

### Step 1: Identify the chapter

If not clear from context, ask:
> "Which chapter am I making notes for? (domain and chapter name)"

Confirm the full path: `{domain-slug}/chapters/{N}-{chapter-slug}/`

### Step 2: Verify the wiki exists

Check that `{chapter}/wiki/` exists and contains `_index.md`.

If it does not, stop and tell the user:
> "No compiled wiki found. Say 'compile' first, then I can generate notes."

### Step 3: Check for existing notes

If `{chapter}/notes/notes.tex` already exists, **do not overwrite it.** Ask:
> "Notes already exist for this chapter. Regenerate from scratch, append only new topics, or skip?"

- **regenerate**: replace the file entirely, continue from Step 4
- **append**: follow the "On Append" section at the bottom of this file instead
- **skip**: stop here

### Step 4: Create the notes folder

Create `{chapter}/notes/` if it does not exist.

Copy `shared/_templates/notes/apore-notes.sty` into `{chapter}/notes/`, overwriting any existing copy. The style package is duplicated per folder on purpose: it makes every notes folder build with no path configuration and stay portable to another machine or to Overleaf.

### Step 5: Read the wiki

Read `{chapter}/wiki/_index.md` first. Its **Topics covered** list is the section order for the document. Then read every topic page it lists.

### Step 6: Write notes.tex

Copy `shared/_templates/notes/notes.tex` to `{chapter}/notes/notes.tex` and fill the placeholders:

- `SUBJECT` → the domain's display name: the first `# ` heading of `{domain-slug}/DOMAIN.md`, falling back to the `**Domain:**` field in `CHAPTER.md` if that file has no heading. `build_notes.py` resolves the name the same way, so the standalone and combined documents always agree.
- `CHAPTER` → the `# Chapter {N}: {Title}` heading from `CHAPTER.md`, as `{N}. {Title}`
- `DATE` → today's date, `YYYY-MM-DD`
- `CHAPTER TITLE` → the chapter title alone, without the number

Keep both `% >>> APORE BODY START` and `% <<< APORE BODY END` markers exactly as they are. `shared/scripts/build_notes.py` extracts everything between them when building the combined domain PDF; a missing marker makes that build fail.

Then write the body between the markers, following these rules.

**Structure**

- One `\topic{...}` per wiki topic page, in `_index.md` order
- Use `\subtopic{...}` only where a wiki page has genuinely distinct sub-sections
- Within a topic, order content: definitions → formulas → methods → worked examples → pitfalls
- Omit any category the wiki does not supply. Do not invent a heading to fill a slot.

**Mapping wiki content to environments**

| Wiki content | Environment |
|---|---|
| A stated definition | `\begin{keydef}{term}` |
| An equation, identity, or named result | `\begin{formula}{name}` |
| A described step-by-step procedure | `\begin{method}{name}`, steps in a `steps` list |
| An example demonstrating a procedure | `\begin{worked}{name}`, terse, at most one per method |
| Content under a wiki "Common Misconceptions" heading | `\begin{pitfall}` |

Use the `points` list for compact bullets inside any box.

**What to cut**

This is a condensed guide for use during problem sets, not a rendering of the wiki. Drop:

- Narrative prose, transitions, and restatement
- Examples that are purely illustrative and teach no reusable technique
- Any topic that yields no definition, formula, method, or pitfall; it produces no section at all

**Citations**

Every environment carries a `\src{...}` taken from the wiki's own `> Source:` line for that claim. Where a claim spans several sources, list them comma-separated inside one `\src{}`. This is what makes the wiki-only constraint auditable in the rendered PDF.

**Long filenames.** When a chapter's source filenames are long enough to swamp the page, define short keys instead of repeating them. Put a source key at the top of the chapter body, immediately after `\chapterhead`, mapping each key to its exact filename:

```latex
\begin{keydef}{Sources}
\begin{points}
\item \textbf{Full deck}: \texttt{F26-D2L-Chapter 2- ... (full).pdf}
\item \textbf{Pre-lecture}: \texttt{before lecture-Chapter 2 - ....pdf}
\end{points}
\end{keydef}
```

Then cite as `\src{Full deck, slide 44}`. Keep any slide or problem number the wiki records. It is what makes a claim checkable. Never invent a key that the key box does not define.

**Math**

Typeset mathematics properly. This is the reason the notes are LaTeX at all:

- `\[ ... \]` for display equations, `$ ... $` inline
- `align` for multi-step derivations
- Convert Unicode symbols from the wiki to LaTeX: `∈` → `\in`, `∉` → `\notin`, `∪` → `\cup`, `∩` → `\cap`, `⊆` → `\subseteq`, `≤` → `\leq`, `≥` → `\geq`, `×` → `\times`, `→` → `\to`, `−` → `-`

**Hard constraint**

Nothing appears in the file that the wiki does not state. No outside knowledge fills a gap, clarifies a definition, or completes a derivation. A gap is simply absent, so do not add "not covered in sources" callouts.

### Step 7: Build the PDF

From `{chapter}/notes/`, run:

```
latexmk -pdf -interaction=nonstopmode -halt-on-error notes.tex
```

If `latexmk` is not on PATH, skip the build. This is not an error. Tell the user:
> "The .tex is ready but there's no TeX engine on PATH. Install MiKTeX (Windows: `winget install MiKTeX.MiKTeX`) or MacTeX/BasicTeX (macOS), then the PDF will build on save or with `latexmk -pdf notes.tex`."

If the build fails, read the `.log` file, fix the LaTeX, and rebuild. Do not report success on a failed build.

### Step 8: Update CHAPTER.md

In `{chapter}/CHAPTER.md`, set:

```
**Notes:** generated {YYYY-MM-DD}
```

If the field is not present, insert it immediately after the `**Compile Status:**` line.

### Step 9: Confirm

Tell the user:
> "Notes generated: {N} topics, {M} pages at `{path to notes.pdf}`."

If the build was skipped, name the `.tex` path instead and repeat the install hint from Step 7.

---

## On Append

When the user chose "append only new topics" in Step 3:

1. Read the existing `notes/notes.tex` and collect every `\topic{...}` heading already present
2. Compare against the **Topics covered** list in `wiki/_index.md`
3. Write only the missing topics, in `_index.md` order, inserted immediately before the `% <<< APORE BODY END` marker
4. **Never modify existing content.** The user may have edited it; those edits are theirs to keep.
5. Rebuild (Step 7) and update `CHAPTER.md` (Step 8)

---

## Combining a Domain

Each chapter's `notes.pdf` stands alone. To read several chapters as one document with continuous page numbers, a single table of contents, and working cross-links, run from the repository root:

```bash
python shared/scripts/build_notes.py {domain-slug}
python shared/scripts/build_notes.py {domain-slug} --chapters 1-3
python shared/scripts/build_notes.py {domain-slug} --chapters 1,3,5
```

Add `--no-build` to write the `.tex` without running `latexmk`.

Output lands in `{domain-slug}/full-notes/`, which is **generated**, so never edit it by hand. A scoped build writes its own file (`full-notes-ch01-02-03.pdf`) and never overwrites the complete `full-notes.pdf`.
