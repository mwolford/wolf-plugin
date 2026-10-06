---
name: backlog-hygiene
description: Lint the wording, consistency and testability of Azure DevOps work items. Use when the user asks to "check hygiene", "lint this story", "check wording/terminology consistency", "clean up acceptance criteria", or compare titles and terms across a Feature and its child items.
license: MIT
---

# Backlog Hygiene

Mechanical, surgical lint. Fix wording; do not change the item's intended outcome. Follow `../backlog-readiness/references/ado-safety.md`.

## Checks
Apply `references/hygiene-rules.md` plus:
- One term per concept across title, description, criteria and linked items; flag synonyms.
- Unfamiliar acronyms defined.
- Active voice, specific verbs.
- Vague words need a measurable meaning: improve, enhance, support, optimize, easy, seamless, real-time, intelligent.
- No bundled requirements hidden behind "and" or slashes.
- Titles match the pattern of neighboring items.
- Parent and child outcomes align.
- Acceptance criteria don't prescribe code structure unless a true constraint.

## Cross-item consistency
When given a Feature/Epic (or several items), read the children and build a short terminology table (term, variants found, recommended). Report mismatches in title patterns and parent/child outcomes.

## Output
**Findings** — table: item/field | issue | suggested fix (quote the original text).
**Terminology** — only if variants were found.
**Proposed edits** — field-by-field, current -> proposed, minimal changes only.
Don't comment on readiness or scope; point to `backlog-readiness` for that.
