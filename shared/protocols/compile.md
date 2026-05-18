# Protocol: Compile

> Read this file in full when the user says "compile", "compile this chapter", or "compile [chapter name]."
> Follow every step in order. Do not skip steps.
>
> **Academic integrity applies from step 1.** Extract only what the sources explicitly state. Do not supplement with pre-trained knowledge. Every claim must be traceable to a source file.

---

## Steps

### Step 1 — Identify the chapter

If not clear from context, ask:
> "Which chapter are you compiling? (domain and chapter name)"

Confirm the full path: `{domain-slug}/chapters/{N}-{chapter-slug}/`

### Step 2 — Read all sources

Read every file in `{chapter}/sources/`. For each file, note its exact filename — this becomes its citation identifier throughout the wiki.

If `sources/` is empty, stop and tell the user:
> "No sources found in `sources/`. Drop your materials there first, then say 'compile'."

### Step 3 — Extract and organize knowledge

From the sources, extract:
- Key concepts and their definitions (only as stated in the source)
- Important examples and case studies
- Relationships between concepts
- Common misconceptions (only if explicitly mentioned in the source)

Group extracted content by major topic. Each distinct topic becomes one wiki page. Do not create a topic page if the source only mentions it in passing — it must be substantively covered.

**Rule:** Only extract what the sources explicitly state. If something is implied but not stated, do not include it.

### Step 4 — Write wiki topic pages

For each major topic, create `{chapter}/wiki/{topic-slug}.md`:

```markdown
# {Topic Name}

## Definition
{definition — direct quote or close paraphrase from source}
> Source: {exact filename}

## Key Concepts
- **{concept name}:** {explanation}
  > Source: {exact filename}

## Examples
- {example as described in source}
  > Source: {exact filename}

## Common Misconceptions
- {misconception, only if source explicitly addresses it}
  > Source: {exact filename}

## Related Topics
- [{Related Topic}]({topic-slug}.md)
```

Every claim must have a `> Source: {exact filename}` line immediately below it. If a claim spans multiple sources, list all of them.

### Step 5 — Write wiki/_index.md

Create or overwrite `{chapter}/wiki/_index.md`:

```markdown
# Wiki Index — {Chapter Title}

**Last compiled:** {YYYY-MM-DD}
**Sources ingested:** {comma-separated list of filenames}
**Topics covered:**
- [{Topic Name}]({topic-slug}.md)
- ...

## Compile History

| Date | Action | Sources Added |
|------|--------|---------------|
| {YYYY-MM-DD} | initial compile | {filenames} |
```

### Step 6 — Generate question bank

Append questions to `{chapter}/progress/questions.md`. Rules:
- Minimum one question per key concept in the wiki
- Include a mix of types: `mcq`, `short-answer`, `conceptual`, `true-false`
- Include a mix of difficulties: `introductory`, `intermediate`, `advanced`
- Model answers must be derivable from `wiki/` content only — reference the relevant wiki page in the answer where helpful
- Assign sequential IDs starting from `Q001` (or continuing from the last ID if questions already exist)
- Use this exact format for each question:

```markdown
## Q{NNN}
**Status:** active
**Type:** {mcq | short-answer | conceptual | true-false}
**Difficulty:** {introductory | intermediate | advanced}
**Topic:** {topic-slug}
**Focus Area:** {specific concept or sub-topic}
**Question:** {question text}
**Answer:** {model answer — sourced from wiki only}
```

### Step 7 — Initialize ratings

For each new question added to `questions.md`, append a row to `{chapter}/progress/ratings.md`:

```
| {ID} | active | new | 0 | 0 | — | — |
```

Do not modify existing rows.

### Step 8 — Update CHAPTER.md

In `{chapter}/CHAPTER.md`:
- Set Compile Status to `compiled {YYYY-MM-DD}`
- Add each source filename to the Sources Ingested table with today's date
- Replace the Topics Covered placeholder with the list of topic slugs

### Step 9 — Update DOMAIN.md

In `{domain-slug}/DOMAIN.md`, update the chapter's Compile Status in the Chapter Index to `compiled {YYYY-MM-DD}`.

### Step 10 — Confirm

Tell the user:
> "Compiled. Wiki has {N} topic pages, question bank has {N} questions. Say 'quiz me on {Chapter Title}' to start a session."

---

## On Recompile

When the user adds new files to `sources/` and runs compile again:

1. Check `CHAPTER.md` Sources Ingested table — read only files not already listed there
2. Extract new knowledge and merge into existing wiki pages (add new sections, never overwrite)
3. Append new questions to `questions.md` with sequential IDs — do not modify existing questions
4. Append new rows to `ratings.md` for new questions only (status: `new`)
5. Append a new row to the Compile History in `wiki/_index.md`
6. Update `CHAPTER.md` Sources Ingested and Compile Status
7. Confirm: "Recompiled. Added {N} new topic sections and {N} new questions."
