

https://github.com/user-attachments/assets/098538df-e799-4e75-a764-4d9e9767e5f3

# apore-lite

An LLM-powered tutoring harness that turns your study materials into a personalized, grounded quiz system.

---

## How it works

You drop source files (HTML pages, PDFs, images) into a chapter folder. Claude reads them and compiles a **wiki** — a set of structured topic pages derived entirely from your sources. Every study session, every question, every hint is grounded exclusively in that wiki. Claude does not fill gaps with its pre-trained knowledge.

The folder structure is the architecture. Claude is the runtime. There is nothing to install.

---

## Prerequisites

- [Claude Code](https://claude.ai/code) (CLI) **or** [claude.ai](https://claude.ai) chat
- A Claude subscription (any tier)

That's it.

---

## Quick start

Open this repo in Claude Code, or paste the contents of `CLAUDE.md` into a claude.ai chat to load the system. Then:

### 1. Create a domain

Say: `new domain`

Claude will ask for the subject name, your goal (exam prep / general mastery / skill development), and preferred tutor style (rigorous / conversational / Socratic). It creates the domain folder and updates the active domains table in `CLAUDE.md`.

### 2. Add a chapter

Say: `new chapter`

Claude asks for the chapter number, title, and a brief topic description. It scaffolds the full chapter structure under `{domain}/chapters/{N}-{chapter-slug}/`.

### 3. Drop your sources

Copy your study materials into `{domain}/chapters/{N}-{chapter-slug}/sources/`.

Supported formats: HTML, plain text, images (PNG/JPG). PDFs work if they are not binary-only — use `shared/scripts/extract-pdf.py` (planned) to pre-extract text from heavy PDFs.

> The `sources/` folder is gitignored. Your materials stay local.

### 4. Compile

Say: `compile`

Claude reads every file in `sources/`, extracts key concepts, definitions, examples, and relationships, and writes one wiki page per major topic to `wiki/`. It then generates a question bank in `progress/questions.md` and initializes spaced repetition state in `progress/ratings.md`.

Every claim in the wiki has a `> Source: {filename}` line. Nothing is added from outside your materials.

### 5. Study

Say: `quiz me on [chapter title]`

Claude loads the wiki, question bank, ratings, and session feedback, then asks how you want to study (question type, difficulty, number of questions, focus area — or just say "just start"). The session begins.

---

## The discrete-math example

This repo ships with a working discrete math domain. Use it as a reference.

```
discrete-math/
├── DOMAIN.md                          ← subject scope, goal, tutor style, chapter index
└── chapters/
    └── 01-set-theory/
        ├── CHAPTER.md                 ← compile status, sources ingested, topics covered
        ├── sources/                   ← gitignored (your raw materials go here)
        ├── wiki/
        │   ├── _index.md              ← compile history, topic list
        │   ├── what-is-a-set.md
        │   ├── ways-to-describe-sets.md
        │   ├── special-sets.md
        │   ├── venn-diagrams.md
        │   ├── set-operations.md
        │   └── set-partitions.md
        └── progress/
            ├── questions.md           ← question bank (do not edit manually)
            ├── ratings.md             ← spaced repetition state (do not edit manually)
            └── feedback.md            ← session feedback log (do not edit manually)
```

**Sources ingested:** 6 HTML topic pages + 7 diagram images from a discrete math course site.

**Wiki output:** 6 topic pages, each with definitions, key concepts, examples, and source citations.

**Question bank:** Mixed types (MCQ, short-answer, true-false, conceptual), mixed difficulty (introductory → advanced).

**Example question (Q001):**
> True or False: The set {1, 2, 3} and the set {3, 2, 1} are different sets because their elements appear in a different order.
>
> *Answer:* False. A set is unordered — order doesn't matter. *(Based on what-is-a-set.md)*

---

## Study session behavior

### Question Generation Mode

Active during normal study. Claude surfaces one question at a time, following Anki priority order: `new` → `hard` → feedback gaps → `easy`. After a correct answer, it asks you to rate difficulty (easy / ok / hard). After a wrong answer, it asks what tripped you up, logs the reason, and generates 1–2 targeted follow-up questions from the wiki.

### Tutor Mode

Activated when you ask *about* a question — "what does X mean?", "why is that the answer?", "can you explain this?" Claude switches to Socratic mode: it guides you with questions rather than giving direct answers, and every hint cites a specific wiki page. It returns to Question Generation Mode when you say "got it", "next question", or similar.

### Spaced repetition and graduation

Your difficulty ratings are tracked in `ratings.md`. When all active questions have been rated `easy` three times consecutively, graduation triggers: the current set is retired, and Claude generates a new, harder question set from the same wiki. Coverage gaps from your session feedback shape the new set.

---

## Folder reference

```
apore-lite/
├── CLAUDE.md                          ← system instructions (the harness)
├── {domain}/
│   ├── DOMAIN.md                      ← domain config: scope, goal, tutor style
│   └── chapters/
│       └── {N}-{chapter}/
│           ├── CHAPTER.md             ← chapter config and compile status
│           ├── sources/               ← raw inputs (gitignored, never edited after drop-in)
│           ├── wiki/                  ← compiled knowledge (Claude's only grounding)
│           └── progress/
│               ├── questions.md       ← question bank
│               ├── ratings.md         ← spaced repetition state
│               └── feedback.md        ← session feedback log
└── shared/
    ├── protocols/                     ← step-by-step instructions Claude follows on trigger phrases
    ├── _templates/                    ← copied when creating new domains and chapters
    └── scripts/                       ← utility scripts (PDF extraction, etc.)
```

---

## Academic integrity

Every answer evaluation, Socratic hint, and generated question is grounded exclusively in the compiled wiki for the active chapter. Claude does not use pre-trained knowledge to fill gaps or supplement what your sources say.

If a concept isn't in the wiki, Claude says so and refers you back to your source materials. This keeps the system honest about what your course actually covers — not what Claude happens to know about the subject.

---

## Adding a new subject

The system is domain-agnostic. To add a new subject (biology, history, law, anything):

1. Say `new domain` and follow the prompts
2. Say `new chapter` for each chapter
3. Drop your sources and say `compile`
4. Say `quiz me on [chapter]` to start studying

Each domain is fully self-contained in its own folder.
