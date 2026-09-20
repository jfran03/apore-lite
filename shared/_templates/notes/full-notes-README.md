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
