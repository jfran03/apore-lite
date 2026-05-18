# apore-lite Design Spec
*2026-05-18*

## Overview

apore-lite is an LLM-powered tutoring harness. Claude AI chat is the runtime. The folder structure and markdown files define the system's behavior — scripts handle mechanical tasks that would be tedious to do by hand (PDF extraction, folder scaffolding, batch operations). No dedicated app, no API key required.

Two architectural principles govern the design:

- **Interpretable Context Methodology (ICM)** — folder structure replaces orchestration. Each domain and chapter folder contains a markdown file that defines Claude's role, its inputs, its rules, and its expected behavior. Claude reads the folder it's in and knows what to do.
- **Compiled Wiki (Karpathy analogy)** — raw source materials (PDFs, transcripts, pages) are immutable inputs. Claude compiles them into a structured wiki per chapter. The wiki is the grounding artifact Claude reads when tutoring. Sources are never edited after ingestion.

The learning loop is modeled after Anki's spaced repetition: Claude generates a question bank from the compiled wiki, tracks your difficulty ratings per question across sessions, surfaces hard and new questions first, and generates fresh questions once you've mastered the existing set.

---

## Folder Structure

> **Note:** The domain folders below (`biology/`, `calculus/`) are illustrative examples only. Actual domains are created by the user via the "new domain" protocol and will reflect whatever subjects you choose to study.

```
apore-lite/
├── CLAUDE.md                          ← system constitution (always read first)
├── {your-domain}/                     ← created via "new domain" protocol
│   ├── DOMAIN.md                      ← tutor role, domain scope, chapter index
│   └── chapters/
│       ├── 01-{chapter-name}/         ← created via "new chapter" protocol
│       │   ├── CHAPTER.md             ← chapter scope, compile status, instructions
│       │   ├── sources/               ← immutable raw inputs
│       │   ├── wiki/                  ← compiled knowledge artifact
│       │   └── progress/
│       │       ├── questions.md       ← question bank (generated from wiki)
│       │       ├── ratings.md         ← per-question spaced repetition state + wrong reasons
│       │       └── feedback.md        ← end-of-set ratings (difficulty, coverage, style)
│       └── 02-{chapter-name}/
│           └── ...
├── {another-domain}/
│   └── ...
└── shared/
    ├── protocols/
    │   ├── new-domain.md
    │   ├── new-chapter.md
    │   └── compile.md
    └── scripts/                       ← utility scripts (PDF extraction, scaffolding, etc.)
```

---

## Component Descriptions

### `CLAUDE.md` (root)
The system constitution. Read automatically by Claude when the workspace is opened. Contains:
- What apore-lite is and how it works
- A list of all active domains (updated as domains are added)
- How to respond to trigger phrases: "new domain", "new chapter", "compile", "quiz me"
- A pointer to `shared/protocols/` for detailed workflow instructions
- The two operating modes Claude must switch between:

**Question Generation Mode** — active when presenting questions from the bank. Claude surfaces one question at a time following the Anki priority order (new → hard → easy). This mode is strictly about presenting and evaluating answers. Claude does not volunteer explanations unprompted.

**Tutor Mode** — activated when the user asks a question *about* a generated question (e.g. "what does X mean?", "why is that the answer?", "can you explain this concept?"). Claude responds using the Socratic framework: it guides with follow-up questions rather than giving direct answers. Claude returns to Question Generation Mode once the user signals they are ready to continue.

**Skipping questions:** If the user says "it's too easy" or "it's too hard" at any point while a question is active, Claude skips the question immediately, logs it in `ratings.md` with the corresponding difficulty rating, and moves to the next question. No answer or explanation is required.

---

### Academic Integrity Rule (Hard Constraint)

**All feedback, hints, Socratic questions, generated questions, and answer evaluations must be grounded exclusively in the compiled wiki for the active chapter.** Claude must not draw on pre-trained knowledge to fill gaps, clarify concepts, or supplement what the sources say.

This applies to both modes:

- **In Question Generation Mode:** Questions and model answers are derived only from wiki content. If the wiki does not contain enough information to generate a question on a topic, that topic is excluded from the bank.
- **In Tutor Mode:** Every Socratic hint or follow-up question must trace back to a specific wiki page derived from the user's sources. Claude does not reason from general world knowledge.

**When Claude cannot answer from the wiki alone**, it must say explicitly:
> "I can't address this from your provided sources. This would require me to draw on outside knowledge, which may not reflect what your course covers. Please refer to your source materials or ask your instructor."

**Citation requirement:** Any time Claude references content from the wiki in Tutor Mode or in answer evaluation, it must cite the originating source file (tracked in `wiki/_index.md` and `schema/provenance.md`). Format:
> "Based on [source filename], [content]."

This ensures you can trace every piece of information back to a document you provided.

### `DOMAIN.md`
Lives at the root of each domain folder. Defines:
- Domain name and subject scope
- Tutor persona for this domain (tone, depth, approach)
- Index of all chapters with their compile status
- Instruction to Claude: when working inside this domain, read the relevant chapter's `CHAPTER.md`, `wiki/`, and `progress/` before doing anything else

### `CHAPTER.md`
Lives at the root of each chapter folder. Defines:
- Chapter title, number, and topic description
- List of source files ingested (with dates)
- Key topics covered (derived at compile time, updated on recompile)
- Session instructions: read `wiki/` for grounding knowledge, read `progress/questions.md` and `progress/ratings.md` for session state before generating any questions

### `sources/`
Immutable after ingestion. Contains raw materials dropped in by the user: PDFs, plain-text transcripts, markdown dumps of web pages, handwritten note scans. Never edited. These are the source code — the wiki is compiled from them.

### `wiki/`
The compiled knowledge artifact for a chapter. Organized by topic. Written and updated by Claude during the compile step. Contains:
- `_index.md` — overview of topics covered and compile history
- One markdown file per major topic (e.g., `mitochondria.md`, `cell-membrane.md`)
- Each topic file: definition, key concepts, examples, common misconceptions, links to related topics
- Every claim in a topic file is attributed to its originating source file (e.g. `> Source: lecture-03-slides.pdf`) so citations during sessions are always traceable

### `progress/questions.md`
The question bank for a chapter. Generated by Claude from the wiki at compile time, and extended when the existing set is mastered. Format per question:

```
## Q001
**Status:** active | retired
**Type:** mcq | short-answer | conceptual | true-false
**Difficulty:** introductory | intermediate | advanced
**Topic:** cell-membrane
**Focus Area:** structure
**Question:** What is the role of cholesterol in the cell membrane?
**Answer:** Cholesterol regulates membrane fluidity — it prevents membranes from becoming too rigid at low temperatures and too fluid at high temperatures.
```

### `progress/ratings.md`
The spaced repetition state. Updated by Claude at the end of every session. Format per entry:

```
| ID   | Status | Difficulty | Times Seen | Times Correct | Last Seen  | Wrong Reason                        |
|------|--------|------------|------------|---------------|------------|-------------------------------------|
| Q001 | active | hard       | 3          | 1             | 2026-05-18 | confused fluidity with permeability |
| Q002 | active | new        | 0          | 0             | —          | —                                   |
| Q003 | active | easy       | 5          | 5             | 2026-05-15 | —                                   |
```

### `progress/feedback.md`
End-of-set feedback log. After each session, Claude prompts the user to optionally rate the overall set. Entries are appended and used to shape the next generated question set.

```
## 2026-05-18
**Difficulty feel:** too easy | about right | too hard
**Coverage gaps:** [topics the user felt were underrepresented]
**Style notes:** [e.g. "need more application questions", "too abstract", "want more MCQs"]
```

---

## Protocols

### `new-domain.md`
Triggered by: "I want a new domain" / "create a new domain"

Claude:
1. Asks: domain name and subject
2. Asks: what is the goal (exam prep, general mastery, skill development)?
3. Asks: what is the tutor tone/style for this domain (rigorous, conversational, Socratic)?
4. Creates the domain folder with `DOMAIN.md` pre-filled and an empty `chapters/` folder
5. Updates the domain list in root `CLAUDE.md`
6. Tells the user: "Domain created. Run 'new chapter' to add your first chapter."

### `new-chapter.md`
Triggered by: "I want a new chapter" / "add a chapter to [domain]"

Claude:
1. Asks: chapter number and title
2. Asks: brief description of what this chapter covers
3. Creates the chapter folder with `CHAPTER.md`, empty `sources/`, empty `wiki/`, and empty `progress/questions.md` and `progress/ratings.md`
4. Updates the chapter index in `DOMAIN.md`
5. Tells the user: "Chapter created. Drop your source materials into `sources/` then run 'compile'."

### `compile.md`
Triggered by: "compile [chapter]" / "compile this chapter"

Claude:
1. Reads all files in `sources/`
2. Extracts key concepts, definitions, examples, and relationships
3. Writes wiki topic files into `wiki/` (one file per major topic)
4. Updates `wiki/_index.md` with the topic list and compile date
5. Generates an initial question bank in `progress/questions.md` — one question per key concept minimum, mix of recall, application, and conceptual questions
6. Initializes `progress/ratings.md` with all questions marked as `new`, 0 times seen
7. Updates `CHAPTER.md` with compile status and list of topics covered

On recompile (new sources added): Claude merges new knowledge into existing wiki pages, adds new questions to the bank without removing existing ones, and logs the update in `wiki/_index.md`.

---

## The Anki Session Loop

Triggered by: "quiz me on [chapter]" / "let's study [chapter]"

**Session customization (at session start):**
Claude asks the user to optionally specify:
- **Question type:** MCQ, short answer, conceptual, true/false, or mixed (default: mixed)
- **Difficulty:** introductory, intermediate, advanced, or mixed (default: mixed)
- **Number of questions:** how many to go through this session (default: 10)
- **Focus area:** specific topic within the chapter, or all topics (default: all)

If the user says "just start" or similar, Claude uses defaults and applies the Anki priority order.

**Load:**
Claude reads `CHAPTER.md` → `wiki/` → `progress/questions.md` → `progress/ratings.md` → `progress/feedback.md`.

**Priority order for question selection:**
1. `new` questions matching session filters (never seen)
2. `hard` questions matching session filters (seen, rated hard or answered incorrectly)
3. Questions flagged in `feedback.md` as covering a gap topic
4. `easy` questions (cycle back occasionally to verify retention)

**Per question:**
1. Claude presents the question
2. User answers (or says "skip" / "I don't know")
3. Claude grades the answer against the stored answer, using the wiki for nuance
4. If the user got it wrong, Claude asks: "What tripped you up?" — the user's response is logged to the `Wrong Reason` field in `ratings.md`
5. User rates difficulty: **easy**, **ok**, or **hard** (or uses the skip phrases "too easy" / "too hard")
6. Claude updates the in-session state

**Wrong answer targeting:**
If a question has a `Wrong Reason` logged, Claude generates 1–2 similar questions on the spot (drawn from the wiki, targeting the same concept from a different angle) and inserts them into the current session queue. These are also added to `questions.md` for future sessions.

**End of session:**
1. Claude writes updated ratings to `progress/ratings.md`
2. Claude prompts: "Want to rate this session? (optional)" — if yes, records difficulty feel, coverage gaps, and style notes to `progress/feedback.md`
3. Feedback is applied to the next session's question selection and to the next graduation set

**Graduation:**
When all active questions have been rated `easy` at least 3 times consecutively, Claude:
1. Marks the existing question set as `retired` in `questions.md`
2. Reads `progress/feedback.md` to inform the new set — fills coverage gaps, adjusts style and difficulty
3. Generates a new set of questions from the wiki — harder, more applied, cross-concept
4. Adds them to `questions.md` with status `new`
5. Resets their entries in `ratings.md`
6. Notifies the user: "You've mastered this set. Generated [N] new questions."

---

## Data Flow Summary

```
User drops PDFs/transcripts
        ↓
    sources/  (immutable)
        ↓  compile
     wiki/  (compiled knowledge)
        ↓  generate
 questions.md  (question bank, typed + difficulty-tagged)
        ↓  session (customized: type, difficulty, count, focus)
  ratings.md  (spaced repetition state + wrong reasons)
  feedback.md  (coverage gaps, style, difficulty feel)
        ↓  wrong answer detected
  similar questions generated on the spot → added to bank
        ↓  graduation
  feedback.md informs new set → harder, gap-filling questions generated
```

---

## What Claude Does vs. What the User Does

| Action | Who |
|--------|-----|
| Drop source materials into `sources/` | User |
| Trigger compile | User |
| Trigger new domain / new chapter | User |
| Trigger a study session | User |
| Rate question difficulty | User |
| Resolve wiki contradictions | User |
| Compile wiki from sources | Claude |
| Generate and extend question bank | Claude |
| Track and update ratings | Claude |
| Prioritize questions per session | Claude |
| Generate graduation questions | Claude |
