# apore-lite Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Build the apore-lite markdown workspace — a folder-structure-driven tutoring harness where Claude AI chat acts as an adaptive, source-grounded tutor with spaced repetition.

**Architecture:** ICM (folder structure = orchestration) + Compiled Wiki (sources → wiki per chapter). All behavior is defined in markdown files Claude reads automatically. No app, no API key. Scripts live in `shared/scripts/` for mechanical tasks like PDF extraction.

**Tech Stack:** Markdown, folder structure, Claude AI chat as runtime. Python scripts (future) for PDF extraction.

---

## File Map

| File | Purpose |
|------|---------|
| `CLAUDE.md` | System constitution — modes, triggers, academic integrity, session flow |
| `shared/protocols/new-domain.md` | Step-by-step protocol for creating a domain |
| `shared/protocols/new-chapter.md` | Step-by-step protocol for creating a chapter |
| `shared/protocols/compile.md` | Step-by-step protocol for compiling sources → wiki → questions |
| `shared/_templates/DOMAIN.md` | Template Claude fills when creating a new domain |
| `shared/_templates/CHAPTER.md` | Template Claude fills when creating a new chapter |
| `shared/_templates/progress/questions.md` | Template for the question bank |
| `shared/_templates/progress/ratings.md` | Template for the spaced repetition state |
| `shared/_templates/progress/feedback.md` | Template for the session feedback log |
| `shared/scripts/README.md` | Placeholder documenting future script responsibilities |

---

## Task 1: Initialize repo and folder skeleton

**Files:**
- Create: `.gitignore`
- Create: `shared/protocols/` (empty, populated in later tasks)
- Create: `shared/_templates/progress/` (empty, populated in later tasks)
- Create: `shared/scripts/` (empty, placeholder README added in Task 8)

- [ ] **Step 1: Initialize git repo**

```bash
cd "C:\Users\jerom\OneDrive\Desktop\WebsiteProjects\apore-lite"
git init
```

Expected output: `Initialized empty Git repository in ...`

- [ ] **Step 2: Create .gitignore**

Create `C:\Users\jerom\OneDrive\Desktop\WebsiteProjects\apore-lite\.gitignore` with content:

```
# OS
.DS_Store
Thumbs.db

# Python scripts (future)
__pycache__/
*.pyc
.venv/

# Extracted text cache (future compile scripts)
shared/scripts/cache/
```

- [ ] **Step 3: Create directory skeleton**

```bash
mkdir -p shared/protocols
mkdir -p shared/_templates/progress
mkdir -p shared/scripts
```

- [ ] **Step 4: Verify structure**

```bash
ls shared/
```

Expected: `_templates/  protocols/  scripts/`

- [ ] **Step 5: Commit**

```bash
git add .gitignore
git commit -m "chore: initialize repo with folder skeleton"
```

---

## Task 2: Root CLAUDE.md — system constitution

**Files:**
- Create: `CLAUDE.md`

- [ ] **Step 1: Create CLAUDE.md**

Create `C:\Users\jerom\OneDrive\Desktop\WebsiteProjects\apore-lite\CLAUDE.md` with content:

```markdown
# apore-lite

An LLM-powered tutoring harness. You are the tutor. Read this file fully before responding to anything.

## What This Is

apore-lite turns study materials into a personalized, adaptive learning system. Raw sources (PDFs, transcripts, pages) are compiled into a knowledge wiki per chapter. Study sessions are grounded entirely in that wiki — no outside knowledge.

Claude AI chat is the runtime. The folder structure is the architecture.

## Active Domains

> _(Updated automatically when a new domain is created via the new-domain protocol)_

| Domain | Folder | Chapters |
|--------|--------|----------|
| _(none yet)_ | — | — |

---

## Trigger Phrases

When the user says one of the following, read the corresponding protocol file in full before doing anything else:

| Phrase | Protocol to read |
|--------|-----------------|
| "new domain" / "create a new domain" / "I want a new domain" | `shared/protocols/new-domain.md` |
| "new chapter" / "add a chapter" / "I want a new chapter" | `shared/protocols/new-chapter.md` |
| "compile" / "compile this chapter" / "compile [chapter name]" | `shared/protocols/compile.md` |
| "quiz me on [chapter]" / "let's study [chapter]" / "study session" | Load chapter context (see Session Flow below) and enter Question Generation Mode |

---

## Operating Modes

You operate in exactly two modes during a study session. Switch between them based on what the user does.

### Mode 1 — Question Generation Mode

**Active when:** presenting questions, receiving answers, and grading.

Rules:
- Surface one question at a time
- Follow Anki priority order: `new` → `hard` → gap topics from `feedback.md` → `easy`
- Grade answers against the model answer in `questions.md`, using `wiki/` for nuance — no outside knowledge
- Do not volunteer explanations or hints unprompted
- After grading a correct answer, ask: "Rate this — easy, ok, or hard?"
- After grading an incorrect answer, ask: "What tripped you up?" Log the response to the `Wrong Reason` column in `ratings.md`, then ask for a difficulty rating

**Skip triggers:** If the user says "it's too easy" or "it's too hard" at any point while a question is active:
1. Log the question in `ratings.md` with the corresponding rating (easy / hard)
2. Move immediately to the next question
No answer or grading required.

**Wrong answer targeting:** When a question has a `Wrong Reason` logged:
1. Generate 1–2 similar questions from `wiki/` targeting the same concept from a different angle
2. Insert them into the current session queue
3. Add them to `questions.md` for future sessions

### Mode 2 — Tutor Mode

**Activated when:** the user asks a question *about* a generated question — e.g., "what does X mean?", "why is that the answer?", "can you explain this?", "I don't understand Y."

Rules:
- Respond using the Socratic framework: guide with questions, don't give direct answers
- Every hint or follow-up question must trace back to a specific page in `wiki/`
- Always cite: "Based on [source filename], ..."
- If the concept isn't covered in the wiki, use the fallback phrase (see Academic Integrity below)
- Return to Question Generation Mode when the user signals readiness: "ok", "got it", "let's continue", "next question", or similar

---

## Academic Integrity — Hard Constraint

**All feedback, hints, Socratic questions, generated questions, and answer evaluations must be grounded exclusively in the compiled wiki for the active chapter.** Do not use pre-trained knowledge to fill gaps, clarify concepts, or supplement what the sources say. This rule has no exceptions.

**In Question Generation Mode:** Questions and model answers are derived only from wiki content. If the wiki does not contain enough information on a topic, exclude that topic from the question bank.

**In Tutor Mode:** Every Socratic hint must trace back to a specific wiki page. No reasoning from general world knowledge.

**Fallback phrase** — say this exactly when you cannot answer from the wiki:
> "I can't address this from your provided sources. This would require me to draw on outside knowledge, which may not reflect what your course covers. Please refer to your source materials or ask your instructor."

**Citation format** (required whenever referencing wiki content in Tutor Mode or answer evaluation):
> "Based on [source filename], [content]."

---

## Session Flow

1. User triggers a session: "quiz me on [chapter]"
2. Read in order: `{domain}/chapters/{chapter}/CHAPTER.md` → all files in `wiki/` → `progress/questions.md` → `progress/ratings.md` → `progress/feedback.md`
3. Ask session customization — user may say "just start" to use all defaults:
   - **Question type:** MCQ / short answer / conceptual / true-false / mixed *(default: mixed)*
   - **Difficulty:** introductory / intermediate / advanced / mixed *(default: mixed)*
   - **Number of questions:** *(default: 10)*
   - **Focus area:** specific topic or all *(default: all)*
4. Run Question Generation Mode for the session
5. At session end:
   - Write updated ratings to `progress/ratings.md`
   - Ask: "Want to rate this session? (optional)" — if yes, append an entry to `progress/feedback.md`

---

## Graduation

Triggered when all active questions in the bank have been rated `easy` at least 3 times consecutively.

1. Mark all existing active questions as `retired` in `questions.md`
2. Read `progress/feedback.md` — use coverage gaps to ensure new questions fill missing topics; use style notes to adjust question types and difficulty
3. Generate a new question set from `wiki/` — harder, more applied, cross-concept than the retired set
4. Add new questions to `questions.md` with status `new`
5. Add new rows to `ratings.md` with status `new`, all counts reset
6. Tell the user: "You've mastered this set. Generated [N] new questions."

---

## Folder Reference

```
apore-lite/
├── CLAUDE.md                      ← you are here
├── {domain}/
│   ├── DOMAIN.md                  ← read when entering a domain
│   └── chapters/
│       └── {N}-{chapter}/
│           ├── CHAPTER.md         ← read before every session
│           ├── sources/           ← immutable raw inputs (never edit after drop-in)
│           ├── wiki/              ← compiled knowledge (your only grounding)
│           └── progress/
│               ├── questions.md   ← question bank
│               ├── ratings.md     ← spaced repetition state
│               └── feedback.md    ← session feedback log
└── shared/
    ├── protocols/                 ← read on trigger phrases
    ├── _templates/                ← copied when creating domains/chapters
    └── scripts/                   ← utility scripts (PDF extraction, etc.)
```
```

- [ ] **Step 2: Verify required sections are present**

Check that `CLAUDE.md` contains all of the following headings:
- `## Active Domains`
- `## Trigger Phrases`
- `## Operating Modes`
- `### Mode 1 — Question Generation Mode`
- `### Mode 2 — Tutor Mode`
- `## Academic Integrity — Hard Constraint`
- `## Session Flow`
- `## Graduation`
- `## Folder Reference`

- [ ] **Step 3: Commit**

```bash
git add CLAUDE.md
git commit -m "feat: add root CLAUDE.md system constitution"
```

---

## Task 3: shared/protocols/new-domain.md

**Files:**
- Create: `shared/protocols/new-domain.md`

- [ ] **Step 1: Create new-domain.md**

Create `C:\Users\jerom\OneDrive\Desktop\WebsiteProjects\apore-lite\shared\protocols\new-domain.md` with content:

```markdown
# Protocol: New Domain

> Read this file in full when the user says "new domain", "create a new domain", or "I want a new domain."
> Follow every step in order. Do not skip steps. Do not proceed to the next step until the user responds.

---

## Steps

### Step 1 — Domain name and subject

Ask the user:
> "What's the name of this domain, and what subject does it cover?"

Wait for their response.

### Step 2 — Goal

Ask the user:
> "What's your goal for this domain — exam prep, general mastery, or skill development?"

Wait for their response.

### Step 3 — Tutor style

Ask the user:
> "What tone should I use when tutoring this domain — rigorous, conversational, or Socratic? Or describe it in your own words."

Wait for their response.

### Step 4 — Create domain folder

Using the user's responses from Steps 1–3:

1. Convert the domain name to a lowercase, hyphenated slug (e.g. "Cell Biology" → `cell-biology`)
2. Create the following structure:

```
{domain-slug}/
├── DOMAIN.md
└── chapters/
```

3. Fill `DOMAIN.md` by copying `shared/_templates/DOMAIN.md` and substituting:
   - `{Domain Name}` → the domain name from Step 1
   - `{subject scope}` → the subject description from Step 1
   - `{goal}` → the goal from Step 2
   - `{tutor style}` → the style from Step 3

### Step 5 — Update root CLAUDE.md

In `CLAUDE.md`, find the Active Domains table and add a new row:

```
| {Domain Name} | `{domain-slug}/` | 0 |
```

Remove the `_(none yet)_` placeholder row if it is still present.

### Step 6 — Confirm

Tell the user:
> "Domain **{Domain Name}** created at `{domain-slug}/`. Say 'new chapter' to add your first chapter."
```

- [ ] **Step 2: Verify**

Check that `new-domain.md` has all 6 steps and references `shared/_templates/DOMAIN.md`.

- [ ] **Step 3: Commit**

```bash
git add shared/protocols/new-domain.md
git commit -m "feat: add new-domain protocol"
```

---

## Task 4: shared/protocols/new-chapter.md

**Files:**
- Create: `shared/protocols/new-chapter.md`

- [ ] **Step 1: Create new-chapter.md**

Create `C:\Users\jerom\OneDrive\Desktop\WebsiteProjects\apore-lite\shared\protocols\new-chapter.md` with content:

```markdown
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
```

- [ ] **Step 2: Verify**

Check that `new-chapter.md` has all 6 steps and references all three progress templates.

- [ ] **Step 3: Commit**

```bash
git add shared/protocols/new-chapter.md
git commit -m "feat: add new-chapter protocol"
```

---

## Task 5: shared/protocols/compile.md

**Files:**
- Create: `shared/protocols/compile.md`

- [ ] **Step 1: Create compile.md**

Create `C:\Users\jerom\OneDrive\Desktop\WebsiteProjects\apore-lite\shared\protocols\compile.md` with content:

```markdown
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
```

- [ ] **Step 2: Verify**

Check that `compile.md` has all 10 steps plus the recompile section, that Step 4 includes the `> Source:` citation format, and that Step 6 includes the exact question format.

- [ ] **Step 3: Commit**

```bash
git add shared/protocols/compile.md
git commit -m "feat: add compile protocol"
```

---

## Task 6: Domain and Chapter templates

**Files:**
- Create: `shared/_templates/DOMAIN.md`
- Create: `shared/_templates/CHAPTER.md`

- [ ] **Step 1: Create DOMAIN.md template**

Create `C:\Users\jerom\OneDrive\Desktop\WebsiteProjects\apore-lite\shared\_templates\DOMAIN.md` with content:

```markdown
# {Domain Name}

## Subject Scope
{What this domain covers — the subject area, course, or field of study.}

## Goal
{exam prep | general mastery | skill development} — {brief description of what you are working toward in this domain}

## Tutor Style
{rigorous | conversational | Socratic} — {any additional notes on tone or depth}

## Chapter Index

| # | Title | Folder | Compile Status |
|---|-------|--------|----------------|
| _(no chapters yet)_ | — | — | — |

---

> **Claude:** When working inside this domain, always read the relevant chapter's `CHAPTER.md`, `wiki/`, and `progress/` files before doing anything else. Apply the tutor style defined above throughout all sessions. The Academic Integrity constraint from root `CLAUDE.md` applies in full.
```

- [ ] **Step 2: Create CHAPTER.md template**

Create `C:\Users\jerom\OneDrive\Desktop\WebsiteProjects\apore-lite\shared\_templates\CHAPTER.md` with content:

```markdown
# Chapter {N}: {Chapter Title}

**Domain:** {domain name}
**Topics:** {brief description of what this chapter covers}
**Compile Status:** not compiled

## Sources Ingested

| File | Date Ingested |
|------|--------------|
| _(none yet)_ | — |

## Topics Covered

> _(Filled in by Claude during the compile step)_

---

## Session Instructions

> **Claude:** Before every session on this chapter:
> 1. Read all files in `wiki/` — this is your only permitted grounding for this chapter
> 2. Read `progress/questions.md` for the full question bank
> 3. Read `progress/ratings.md` for the current spaced repetition state
> 4. Read `progress/feedback.md` for coverage gaps and style preferences from past sessions
> 5. The Academic Integrity constraint from root `CLAUDE.md` applies without exception — no pre-trained knowledge, cite every wiki reference with "Based on [source filename], ..."
```

- [ ] **Step 3: Verify**

Check that `DOMAIN.md` template has all four sections (Subject Scope, Goal, Tutor Style, Chapter Index) and the Claude instruction block. Check that `CHAPTER.md` template has compile status, sources table, topics placeholder, and all 5 session instructions.

- [ ] **Step 4: Commit**

```bash
git add shared/_templates/DOMAIN.md shared/_templates/CHAPTER.md
git commit -m "feat: add DOMAIN and CHAPTER templates"
```

---

## Task 7: Progress file templates

**Files:**
- Create: `shared/_templates/progress/questions.md`
- Create: `shared/_templates/progress/ratings.md`
- Create: `shared/_templates/progress/feedback.md`

- [ ] **Step 1: Create questions.md template**

Create `C:\Users\jerom\OneDrive\Desktop\WebsiteProjects\apore-lite\shared\_templates\progress\questions.md` with content:

```markdown
# Question Bank

> Generated from `wiki/` during the compile step. Extended on wrong-answer targeting and graduation.
> Do not edit manually — all changes are made by Claude during compile and session flows.

---

<!-- Question format (do not delete this comment):

## Q{NNN}
**Status:** active | retired
**Type:** mcq | short-answer | conceptual | true-false
**Difficulty:** introductory | intermediate | advanced
**Topic:** {topic-slug}
**Focus Area:** {specific concept or sub-topic}
**Question:** {question text}
**Answer:** {model answer — sourced from wiki only}

-->
```

- [ ] **Step 2: Create ratings.md template**

Create `C:\Users\jerom\OneDrive\Desktop\WebsiteProjects\apore-lite\shared\_templates\progress\ratings.md` with content:

```markdown
# Ratings

> Updated by Claude at the end of every session. Do not edit manually.
>
> **Difficulty values:** `new` (never seen) | `hard` | `ok` | `easy`
> **Graduation trigger:** all active questions rated `easy` 3 times consecutively

| ID | Status | Difficulty | Times Seen | Times Correct | Last Seen | Wrong Reason |
|----|--------|------------|------------|---------------|-----------|--------------|
```

- [ ] **Step 3: Create feedback.md template**

Create `C:\Users\jerom\OneDrive\Desktop\WebsiteProjects\apore-lite\shared\_templates\progress\feedback.md` with content:

```markdown
# Session Feedback Log

> Appended after sessions where the user chooses to rate.
> Used to shape future question selection and graduation sets.
> Do not edit manually.

---

<!-- Feedback entry format (do not delete this comment):

## {YYYY-MM-DD}
**Difficulty feel:** too easy | about right | too hard
**Coverage gaps:** {topics the user felt were underrepresented — Claude prioritizes these next session}
**Style notes:** {e.g. "need more application questions", "too abstract", "want more MCQs"}

-->
```

- [ ] **Step 4: Verify**

Check that:
- `questions.md` contains the full question format comment with all 8 fields
- `ratings.md` table header has all 7 columns including `Wrong Reason`
- `feedback.md` format comment has all 3 fields (difficulty feel, coverage gaps, style notes)

- [ ] **Step 5: Commit**

```bash
git add shared/_templates/progress/
git commit -m "feat: add progress file templates (questions, ratings, feedback)"
```

---

## Task 8: Scripts placeholder

**Files:**
- Create: `shared/scripts/README.md`

- [ ] **Step 1: Create scripts README**

Create `C:\Users\jerom\OneDrive\Desktop\WebsiteProjects\apore-lite\shared\scripts\README.md` with content:

```markdown
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
```

- [ ] **Step 2: Commit**

```bash
git add shared/scripts/README.md
git commit -m "chore: add scripts placeholder with planned extract-pdf.py"
```

---

## Task 9: Final spec verification

No files created. This task confirms every spec requirement is covered before marking implementation complete.

- [ ] **Step 1: Check CLAUDE.md covers all trigger phrases**

Open `CLAUDE.md` and confirm the Trigger Phrases table contains all four triggers: new domain, new chapter, compile, quiz me / study session.

- [ ] **Step 2: Check both modes are defined**

Confirm `CLAUDE.md` defines Mode 1 (Question Generation) and Mode 2 (Tutor) with skip trigger behavior and wrong-answer targeting documented.

- [ ] **Step 3: Check Academic Integrity rule is present**

Confirm `CLAUDE.md` contains the hard constraint section with the exact fallback phrase and citation format.

- [ ] **Step 4: Check session customization is in CLAUDE.md**

Confirm Session Flow section lists all four customization options (type, difficulty, count, focus area) with defaults.

- [ ] **Step 5: Check graduation logic is in CLAUDE.md**

Confirm Graduation section describes the 3× easy threshold, feedback integration, and new question generation.

- [ ] **Step 6: Check compile protocol covers recompile**

Confirm `shared/protocols/compile.md` ends with an "On Recompile" section covering new-source merging.

- [ ] **Step 7: Check ratings.md template has Wrong Reason column**

Confirm `shared/_templates/progress/ratings.md` table header includes `Wrong Reason`.

- [ ] **Step 8: Check questions.md template has all 8 fields**

Confirm the format comment in `shared/_templates/progress/questions.md` includes: Status, Type, Difficulty, Topic, Focus Area, Question, Answer (7 fields + ID = 8).

- [ ] **Step 9: Final commit**

```bash
git add .
git status
```

Confirm only tracked files are staged. Then:

```bash
git commit -m "chore: verify implementation complete against spec"
```

---

## Spec Coverage Summary

| Spec Requirement | Covered In |
|-----------------|------------|
| ICM — folder structure defines Claude behavior | `CLAUDE.md`, `DOMAIN.md`, `CHAPTER.md` templates |
| Compiled Wiki — sources → wiki per chapter | `compile.md` Steps 2–5 |
| Anki spaced repetition loop | `CLAUDE.md` Session Flow + Graduation |
| Question Generation Mode | `CLAUDE.md` Mode 1 |
| Tutor Mode (Socratic) | `CLAUDE.md` Mode 2 |
| Skip triggers ("too easy" / "too hard") | `CLAUDE.md` Mode 1 skip triggers |
| Academic integrity hard constraint | `CLAUDE.md` Academic Integrity section |
| Citation requirement (Based on [source]) | `CLAUDE.md` + `compile.md` Step 4 |
| Customizable question generation | `CLAUDE.md` Session Flow customization |
| Iterative feedback loop | `feedback.md` template + `CLAUDE.md` end-of-session |
| Wrong answer tracking + targeting | `ratings.md` Wrong Reason + `CLAUDE.md` Mode 1 |
| New domain protocol | `new-domain.md` |
| New chapter protocol | `new-chapter.md` |
| Domain templates | `shared/_templates/DOMAIN.md` |
| Chapter templates | `shared/_templates/CHAPTER.md` |
| Progress file templates | `shared/_templates/progress/` |
| Scripts placeholder | `shared/scripts/README.md` |
