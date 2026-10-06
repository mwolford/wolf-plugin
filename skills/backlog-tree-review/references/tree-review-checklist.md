# Tree review checklist

## Per item
- Right level? Use the triage questions in the sizing guide.
- Title is Verb + outcome; description is HTML and free of stray AI/chat text.
- Acceptance criteria present (Feature/Story); Epic has measurable success measures.
- Hygiene field rules (Risk, Priority, Value Area, dates, iteration, AC, dependency comments).

## Feature-level smells
- **Technical Feature**: titled by tooling/infrastructure (Terraform, CI/CD, containers) with no user value → re-level as Enabler, or Tasks under a value Feature.
- **Placeholder shell**: noun title, no AC, "to be validated" → needs scope or removal.
- **Implementation detail** in the title/description (storage, file formats) → move to Tasks/notes.
- **Overlap**: two Features covering the same capability → merge or draw a boundary.
- Feature with one Story → probably a Story; Feature that can't ship before all siblings → check it isn't part of another Epic.

## Tree consistency
- Child iteration/dates fall inside the parent's; generic iteration (e.g. root only) vs parent's quarter.
- Missing Priority on siblings; mixed area paths (flag only).
- Dependencies between Features documented.

## Epic monolith signals (heuristics)
- Roughly more than 6–8 Features, or children spanning several quarters/releases.
- More than one distinct customer outcome or user group.
- No single success measure covers all Features.
- Several Features are unrelated placeholders awaiting validation.
- In-scope list reads as a feature list rather than an outcome.

## Splitting an Epic
- One outcome and one measurable success measure per new Epic.
- Target roughly one quarter or one release per Epic (heuristic).
- Group Features by outcome/value slice; put shared enablers in the first Epic that needs them.
- Park unvalidated placeholders in a backlog/"Later" Epic instead of the active one.
