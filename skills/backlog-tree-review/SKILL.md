---
name: backlog-tree-review
description: Read-only review of an Azure DevOps Epic tree (Epic → Features → optionally Stories). Flags level mismatches, technical Features, placeholder shells, overlaps and inconsistent iterations, lints each item, and coaches how to break a monolithic Epic into smaller outcome-focused, time-boxed Epics. Use when asked to "review this epic", "review my backlog tree", "is this epic too big", "break up this epic", or "are these features the right level".
license: MIT
---

# Backlog tree review (ADO, read-only)

Walk one Epic and its children, report problems, and propose a restructure. Never write to ADO; follow `../backlog-readiness/references/ado-safety.md`.

## Process
1. Get the Epic ID (ask if missing). Fetch the Epic with `azure-devops-wit_work_item` `get` + `expand=Relations`, then children with `get_batch` (requires `project`; use `fields` OR `expand`, not both). Go to Stories only if asked or if Features look oversized.
2. Run the checks in [references/tree-review-checklist.md](references/tree-review-checklist.md) on every item.
3. Run the Epic-scope check: is this a monolith? Use the heuristics in `../backlog-scoping/references/level-and-sizing-guide.md`.
4. If monolithic, propose a split into smaller Epics by outcome/value slice, and regroup Features under them.
5. Present findings and the proposal. Ask before anything else.

## Output
1. **Tree summary** – Epic, child count, iteration/date spread.
2. **Findings table** – Item | Issue | Proposed fix or re-level.
3. **Epic scope verdict** – Monolith? Why (evidence).
4. **Proposed restructure** – New Epics (outcome-style title, success measure to confirm), Features under each, Features to re-level (enabler/Task/Story), merge or drop candidates. Order by dependency/value, not by invented dates.
5. **Questions** – Missing facts (owners, validation status, dates).

## Rules
- Read-only. Offer updates only as a list for explicit approval.
- Don't invent estimates, dates, owners or measures; phrase them as questions.
- Split Epics by outcome, never by technical layer or team.
- Time-box ranges are heuristics, not Microsoft requirements.
- Titles: Verb + outcome, no prefixes. Field rules: `../backlog-hygiene/references/hygiene-rules.md`.
- Follow-ups: `backlog-scoping` (single item), `backlog-hygiene` (wording), `backlog-readiness` (ready/split), `backlog-story-coach` (rewrite).
