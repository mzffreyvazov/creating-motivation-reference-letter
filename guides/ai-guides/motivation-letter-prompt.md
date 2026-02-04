---
title: Motivation Letter Master Prompt (Reusable)
purpose: Reusable prompt that guides the AI to research this workspace and synthesize a program-tailored motivation letter
last_updated: 2026-02-03
---

# Motivation Letter Master Prompt (Reusable)

Copy-paste the prompt below and fill the placeholders in **[BRACKETS]**.

---

## Reusable Prompt (give to the AI assistant)

You are my AI assistant working inside my VS Code workspace `creating-motivation-reference-letter/`.

**Purpose:** Research the relevant documents in this workspace and combine them into a **compelling, program-tailored motivation letter**.

### 1) Non-negotiable rules

- **No hallucinations.** Only state specific facts about me (projects, roles, awards, dates, skills, grades) if they exist in my files or I provide them in this chat.
- If a needed detail is missing, ask targeted questions (max **8**) before writing.
- Don’t copy sentences from example letters; use them only for structure and inspiration.
- Prefer specific evidence over generic claims; avoid clichés.

### 2) Inputs (fill these)

- Target program: **[PROGRAM NAME]**
- Institution: **[UNIVERSITY / ORGANIZATION]**
- Degree/type: **[MSc/PhD/Scholarship/Exchange/etc]**
- Intake/year: **[YEAR / TERM]**
- Letter audience: **[Admissions committee / Scholarship committee / Specific department]**
- Required format constraints (if any):
  - Word/character limit: **[LIMIT or “none given”]**
  - Required prompts/questions to answer: **[PASTE PROMPT(S) or “none”]**
  - Required themes (if any): **[THEMES or “none”]**
- Program dossier (required): **[programs/PROGRAM-SLUG.md]**
- Motivation writing guide (required; provided in `programs/`): **[programs/MOTIVATION-GUIDE.md]**
  - This guide contains the writing rules/structure to follow for this application.
- Program deadline (for metadata): **[YYYY-MM-DD or TBD]**
- Application status (for metadata): **[planned/researching/preparing/submitted/etc]**

If any required program file is missing, stop and ask me whether to (a) create it first or (b) proceed with limited info.

### 3) Workspace sources you MUST consult (minimum set)

Read only what you need, but ground the letter in:

1) Program-specific guidance and facts
- **[programs/MOTIVATION-GUIDE.md]** (the writing guide to follow)
- **[programs/PROGRAM-SLUG.md]** (program facts, fit hooks, requirements)

2) My background (facts + voice)
- `muzeffer-info/cv/` (facts)
- `muzeffer-info/motivation-letters-muzeffer/` (voice and prior framing)

3) Style calibration (optional but helpful)
- `motivation-letters-example/` (structure ideas; do not copy)

If there are multiple CV versions, prefer the most recent/complete one, but resolve any conflicts explicitly.

### 4) What you must produce (deliverables)

Produce BOTH:

1) **Final motivation letter** (ready to submit)
2) **Builder notes** (not part of the letter): evidence map + assumptions + open questions

Save the final letter as:
- Folder: `muzeffer-info/motivation-letters-muzeffer/`
- Filename: `muzeffer-motivation-letter-[program-slug]-[year].md`

### 5) Required writing standard: frontmatter + statuses

When creating the motivation letter file, you MUST follow the workspace rule in `.github/skills/SKILL.md`:

- Add YAML frontmatter at the very top with keys:
  - `university`, `program`, `program_deadline`, `application_status`, `writing_status`
- Use only the allowed values for `application_status` and `writing_status`.

Default recommendation unless I specify otherwise:
- `application_status: preparing`
- `writing_status: draft`

### 6) How to build the letter (short)

1) Extract building blocks
- 6–10 proof points from my CV (impact, projects, research, leadership).
- 5–12 fit hooks from the program dossier (modules, labs, values, outcomes).
- Create at least 6 pairings: proof point → fit hook.

2) Ask what’s missing (max 8 questions)
- Only ask for info that materially changes the letter (word limit, required prompts, key project to highlight).

3) Write and refine
- Draft an outline (bullets), then the letter.
- Ensure each paragraph has a job: intent, preparation, fit, trajectory, close.

### 7) Letter style requirements

- Language: professional academic English.
- Tone: confident, specific, humble; no over-claims.
- Length: default **650–900 words** unless a strict limit is given.
- Structure: 4–6 paragraphs, each with a clear purpose.

### 8) Output format (must follow)

Return in Markdown with exactly these sections.

```md
---
university: [UNIVERSITY / ORGANIZATION]
program: [PROGRAM NAME]
program_deadline: [YYYY-MM-DD or TBD]
application_status: [planned|researching|preparing|submitted|under_review|interview|accepted|rejected|waitlisted|deferred|withdrawn]
writing_status: [not_started|outline|draft|revising|proofreading|final|submitted]
---

# Motivation Letter — [PROGRAM NAME] ([YEAR/TERM])

**Applicant:** Müzəffər Eyvazov  
**Program:** [PROGRAM NAME] — [INSTITUTION]  
**Intake:** [YEAR/TERM]  
**Date:** [TODAY’S DATE]  

Dear [Admissions/Selection Committee / Specific Name],

[Paragraph 1: intent + program match in one clear angle.]

[Paragraph 2: preparation proof — strongest evidence + what it taught me.]

[Paragraph 3: program fit — named curriculum/labs/values + why they matter.]

[Paragraph 4: research/professional direction — what I want to do and why this program is the bridge.]

[Paragraph 5 (optional): community/leadership + closing with confident readiness.]

Sincerely,  
Müzəffər Eyvazov
```

If you need to ask questions: ask up to 8, then wait.

