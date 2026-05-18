# Protocol: New Chapter

> Read this file in full when the user says "new chapter", "add a chapter", or "I want a new chapter."
> Follow every step in order. Do not skip steps. Do not proceed to the next step until the user responds.

---

## Steps

### Step 1 — Confirm domain

If the domain is not clear from context, ask:
> "Which domain is this chapter for?"

Wait for their response.

### Step 2 — Chapter number and title

Ask:
> "What's the chapter number and title? (e.g. '3 — Cellular Respiration')"

Wait for their response.

### Step 3 — Topic description

Ask:
> "Briefly describe what this chapter covers — what are the main topics or concepts?"

Wait for their response.

### Step 4 — Create chapter folder

Using the user's responses:

1. Convert the chapter title to a lowercase, hyphenated slug (e.g. "Cellular Respiration" → `cellular-respiration`)
2. Left-pad the chapter number with a zero if single digit (e.g. 3 → `03`)
3. Create the following structure inside `{domain-slug}/chapters/`:

```
{N}-{chapter-slug}/
├── CHAPTER.md
├── sources/
├── wiki/
└── progress/
    ├── questions.md
    ├── ratings.md
    └── feedback.md
```

4. Fill `CHAPTER.md` by copying `shared/_templates/CHAPTER.md` and substituting:
   - `{N}` → the chapter number
   - `{Chapter Title}` → the chapter title from Step 2
   - `{domain name}` → the domain name
   - `{topic description}` → the description from Step 3

5. Copy `shared/_templates/progress/questions.md` → `progress/questions.md`
6. Copy `shared/_templates/progress/ratings.md` → `progress/ratings.md`
7. Copy `shared/_templates/progress/feedback.md` → `progress/feedback.md`

### Step 5 — Update DOMAIN.md

In `{domain-slug}/DOMAIN.md`, find the Chapter Index table and add a new row:

```
| {N} | {Chapter Title} | `chapters/{N}-{chapter-slug}/` | not compiled |
```

Remove the `_(no chapters yet)_` placeholder row if it is still present.

Also increment the Chapters count in root `CLAUDE.md`'s Active Domains table for this domain.

### Step 6 — Confirm

Tell the user:
> "Chapter **{N} — {Chapter Title}** created. Drop your source materials into `{domain-slug}/chapters/{N}-{chapter-slug}/sources/`, then say 'compile' when ready."
