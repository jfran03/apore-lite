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

Then verify the file has all 6 steps, and that Step 4 references `shared/_templates/DOMAIN.md`.