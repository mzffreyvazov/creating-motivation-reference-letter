---
title: Program Research Guide (Reusable Prompt)
purpose: Prompt template for AI agents to research a target program for motivation letter tailoring
last_updated: 2026-02-03
---

# Program Research Guide (Reusable Prompt)

This file contains a **copy-paste prompt** you can give to another AI agent to research a target program (scholarship / university program / exchange / fellowship). The agent’s output will be used later to tailor a strong motivation letter.

## How to use

1. Copy the prompt in the next section.
2. Fill the placeholders in **[BRACKETS]**.
3. Give it to the research agent.
4. Save the agent’s result into `programs/` as a Markdown file:
	- `programs/[program-slug].md` (example: `programs/uni-of-sheffield-data-science.md`)

---

## Reusable Prompt (give to a research agent)

You are a research assistant. Your job is to produce a **Program Research Dossier** for a motivation letter writer.

### Context

- Applicant: **Müzəffər Eyvazov** (you do NOT need personal details; focus on program facts).
- Goal: gather accurate, relevant, **actionable** program info that can be used to tailor a compelling motivation letter.
- Output must be concise, structured, and source-backed.

### Target Program

- Program name: **[PROGRAM NAME]**
- Institution/Provider: **[UNIVERSITY / ORGANIZATION]**
- Degree/Type: **[MSc/PhD/Exchange/Scholarship/Fellowship/etc]**
- Track/Specialization (if any): **[TRACK]**
- Intake/Year: **[YEAR / TERM]**
- Campus/Location: **[CITY, COUNTRY]**
- Official program page (if known): **[URL]**

### Research Requirements (what to find)

Use **official sources first** (provider website, program handbook, admissions pages, scholarship pages). You may use secondary sources (rankings, forums, news) only to add context, never as the primary authority for requirements.

Collect and clearly present:

1. **One-paragraph overview**
	- What the program is, who it’s for, what it trains graduates to do.

2. **What the program values (selection signals)**
	- Keywords/phrases repeatedly emphasized (e.g., “research potential”, “impact”, “interdisciplinary”, “leadership”, “industry collaboration”, “social responsibility”).
	- What an ideal candidate looks like (as described by the provider).

3. **Curriculum structure and learning outcomes**
	- Core modules and typical electives (list a representative subset, not every single module unless small).
	- Thesis/capstone/research project expectations.
	- Practical components (labs, placements, industry projects, teaching assistantships).
	- Distinctive features (unique modules, centers, labs, partner companies).

4. **Faculty / labs / research groups relevant to Data Science / AI / Neuroscience / (or target area)**
	- 3–8 relevant labs, groups, institutes, or faculty pages.
	- What they work on, and why it’s relevant.

5. **Admissions & eligibility (hard requirements)**
	- Academic prerequisites (degree, GPA/classification, required background).
	- Language requirements (IELTS/TOEFL, minimum subscores).
	- Prerequisite courses or skills.
	- Required documents (CV, SoP, references, transcripts, portfolio, writing samples).
	- Any special requirements for scholarships tied to the program.

6. **Application process and deadlines**
	- Key deadlines (application, scholarship, references, deposit).
	- How applications are evaluated (criteria/rubric if available).
	- Whether rolling admissions exists and what that implies.

7. **Funding, tuition, and cost-of-living signals**
	- Tuition and fees (home/international if different).
	- Scholarships (eligibility, coverage, selection criteria).
	- If official cost-of-living guidance exists, summarize.

8. **Career outcomes & employability**
	- Typical roles, industries, placement stats (only if from credible sources).
	- Links to careers page, alumni outcomes, employability reports.

9. **Fit hooks for a motivation letter (MOST IMPORTANT)**
	- Identify 5–12 “hooks” that can be turned into letter content:
	  - program mission/values alignment
	  - module-to-goal mapping (module X supports goal Y)
	  - lab/research-group alignment
	  - unique facilities/centers
	  - industry partners, local ecosystem
	- For each hook: give a 1–2 sentence explanation + the best source link.

10. **Risks / ambiguities / things to confirm**
	- Anything conflicting across sources, unclear requirements, missing deadlines, etc.

### Source & Quality Rules

- Provide **links for every key claim** (requirements, deadlines, tuition, scholarship coverage, curriculum facts).
- Prefer:
  1) official provider pages
  2) official PDF handbooks/regulations
  3) official careers/employability pages
  4) reputable ranking bodies / government / recognized publications
- Avoid copying large text blocks. Summarize in your own words.
- Include **“as of” date** (today’s date) and note if pages are for a different year.

### Output Format (must follow exactly)

Return a single Markdown document using the template below.

#### Template

```md
# Program Research Dossier — [PROGRAM NAME] ([YEAR/TERM])

**Institution:** [UNIVERSITY / ORGANIZATION]  
**Program type:** [MSc/PhD/Scholarship/etc]  
**Location:** [CITY, COUNTRY]  
**Official pages (top 3):**
- [Title](URL)
- [Title](URL)
- [Title](URL)

## 1) Executive Summary (5–8 bullets)
- …

## 2) What the Program Optimizes For (Selection Signals)
- **Stated values:** …
- **Ideal candidate signals:** …
- **Evidence (links):** [Title](URL), …

## 3) Curriculum & Academic Experience
- **Structure:** (duration, credits, required components)
- **Core modules (representative):** …
- **Electives (representative):** …
- **Thesis/Capstone:** …
- **Distinctive elements:** …
- **Evidence (links):** …

## 4) Research Ecosystem (Labs/Groups/Faculty)
List 3–8 relevant options.
- **[Lab/Group/Professor]** — 1 sentence why relevant. [Link](URL)

## 5) Admissions & Eligibility (Hard Requirements)
- **Academic:** … [Link](URL)
- **Background/prereqs:** … [Link](URL)
- **Language:** … [Link](URL)
- **Documents:** … [Link](URL)
- **References:** … [Link](URL)

## 6) Application Process & Deadlines
- **Deadlines:** … [Link](URL)
- **Evaluation:** … [Link](URL)
- **Notes (rolling admissions, interviews, etc.):** …

## 7) Funding / Tuition / Costs
- **Tuition:** … [Link](URL)
- **Scholarships:** … [Link](URL)
- **Cost of living guidance:** … [Link](URL)

## 8) Career Outcomes
- **Common roles:** …
- **Outcome stats (only if credible):** … [Link](URL)
- **Evidence (links):** …

## 9) Motivation Letter Fit Hooks (5–12)
Each hook must include: *Hook → Why it matters → Evidence link*.
1. **Hook:** …  
	**Why it matters:** …  
	**Evidence:** [Title](URL)
2. …

## 10) Risks, Ambiguities, and To-Confirm Checklist
- …

## 11) Source List
- [Title](URL)
- …
```

### Final Checks Before You Submit

- Did you include links for all hard requirements and deadlines?
- Are the “Fit Hooks” specific enough to be used as motivation-letter paragraphs?
- Did you avoid unverified claims and large copied text?

---

## Optional Add-on: “One-page brief”

If time permits, also add a short section at the end:

- **One-page brief for letter writer:** 150–250 words summarizing the single best narrative angle for fit (values + curriculum + research + career outcomes), with 3 supporting links.

