# shared/scripts

Utility scripts that handle mechanical tasks Claude should not do inline.

## Planned Scripts

### extract-pdf.py
Extract plain text from a PDF and save it as a `.txt` file in the target chapter's `sources/` folder.

**Usage (planned):**
```bash
python shared/scripts/extract-pdf.py path/to/file.pdf biology/chapters/01-cells/sources/
```

**Why it exists:** Claude can read PDFs directly in some contexts, but a pre-extracted `.txt` file is faster to load, avoids encoding issues, and creates an explicit immutable artifact in `sources/` with a clear filename for citation.

---

Add new scripts here as they are built. Each entry should document: what it does, usage, and why it exists rather than being handled inline.
