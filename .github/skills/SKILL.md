---
name: motivation-letter-frontmatter-and-statuses
description: Standardize YAML frontmatter metadata for motivation letters, including consistent application and writing status values.
---

# Motivation letter frontmatter + statuses

## Goal
Standardize YAML frontmatter for motivation letters and keep `application_status` and `writing_status` consistent across files.

## When to use
- When creating a new motivation letter markdown file.
- When updating existing motivation letters to include metadata.

## Frontmatter template
Add this at the very top of the markdown file:

```yaml
---
university: <University Name>
program: <Program Name>
program_deadline: <YYYY-MM-DD | TBD>
application_status: <see allowed values>
writing_status: <see allowed values>
---
```

Notes:
- Keep keys snake_case.
- Prefer ISO date `YYYY-MM-DD` for `program_deadline`; use `TBD` if unknown.

## Allowed values

### application_status
Use one of:
- `planned` — intend to apply, not started
- `researching` — checking requirements, contacting referees
- `preparing` — collecting docs, polishing materials
- `submitted`
- `under_review`
- `interview` — interview / assessment stage
- `accepted`
- `rejected`
- `waitlisted`
- `deferred`
- `withdrawn`

### writing_status
Use one of:
- `not_started`
- `outline`
- `draft`
- `revising`
- `proofreading`
- `final`
- `submitted` — only if the letter itself was uploaded/sent

## Example

```yaml
---
university: University of Sheffield
program: MSc Data Science
program_deadline: TBD
application_status: preparing
writing_status: draft
---
```
