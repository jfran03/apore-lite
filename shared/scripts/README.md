# shared/scripts

Utility scripts that handle mechanical tasks Claude should not do inline.

## Scripts

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

### extract-pdf.py _(planned)_
Extract plain text from a PDF and save it as a `.txt` file in the target chapter's `sources/` folder.

**Usage (planned):**
```bash
python shared/scripts/extract-pdf.py path/to/file.pdf biology/chapters/01-cells/sources/
```

**Why it exists:** Claude can read PDFs directly in some contexts, but a pre-extracted `.txt` file is faster to load, avoids encoding issues, and creates an explicit immutable artifact in `sources/` with a clear filename for citation.

---

Add new scripts here as they are built. Each entry should document: what it does, usage, and why it exists rather than being handled inline.
