# Level and sizing guide (ADO)

## Sources (Microsoft Learn)
- [Define features and epics](https://learn.microsoft.com/azure/devops/boards/backlogs/define-features-epics)
- [Best practices for Agile product management](https://learn.microsoft.com/azure/devops/boards/best-practices-agile-project-management)

## Hierarchy by process

| Process | Portfolio | Team-level requirement | Estimate field |
|---|---|---|---|
| Agile | Epic > Feature | User Story > Task (Bug) | Story Points |
| Scrum | Epic > Feature | Product Backlog Item > Task (Bug) | Effort |
| CMMI | Epic > Feature | Requirement > Task (Bug) | Size |
| Basic | Epic | Issue > Task | none |

Bugs: placement is a team setting ("Show bugs on backlogs and boards").

## Level definitions

| Level | Microsoft guidance | Typical sizing signal |
|---|---|---|
| Epic | Large initiative spanning multiple features, possibly several sprints or releases | Multiple features; often more than one team or release |
| Feature | Customer-facing value shipping as a coherent capability; one or more sprints; a shippable capability | Several stories; deliverable in one or a few sprints |
| Story / PBI / Requirement | Work scoped to a single iteration, with clear acceptance criteria | Finishable by one team in one sprint |
| Task | Developer work that fits within an iteration | Hours to a couple of days (heuristic) |

Microsoft states the iteration boundary (story/task within a sprint; feature/epic one or more sprints). Finer numbers (e.g. task in hours-to-days, feature within a quarter) are common Agile heuristics, not Microsoft requirements.

## Triage questions
- Goal or outcome across teams/releases → Epic.
- Capability a customer can use, shippable on its own → Feature.
- One slice of behavior, testable, fits a sprint → Story.
- Implementation step with no standalone user value → Task.

## Too big / too small
- Story that will not fit a sprint: split by workflow step, rule variation, data variation, or happy path then edge cases; keep each slice user-visible.
- Feature with one story: probably just a Story. Epic with one feature: probably just a Feature.
- Feature that cannot ship until all children finish and is not valuable earlier: fine, but check it is not an Epic.
- Reduce size variability by breaking large items down (Microsoft portfolio-backlog rationale).

## Estimation notes
- Estimates live on requirements; Forecast needs them (or use 1 per item to forecast by count).
- Features/Epics may carry relative Effort/Size; use whatever unit the team uses.
