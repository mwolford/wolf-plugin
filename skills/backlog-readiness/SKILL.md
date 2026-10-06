---
name: backlog-readiness
description: Assess whether an Azure DevOps work item is ready for sprint planning, and handle splitting and sequencing. Use when the user asks "is this ready", "definition of ready", "review this story/feature", "should this be split", "what depends on what", "do we need a spike", or "sequence these items".
license: MIT
---

# Backlog Readiness

Assess readiness, splits and sequencing. Follow `references/ado-safety.md`. Never mark an item Ready from generated text alone; unresolved decisions need explicit user confirmation.

## Definition of Ready
Rate each Clear / Partial / Missing / N/A: outcome and consumer; scope and exclusions; correct level; acceptance criteria; dependencies and sequencing; data/system ownership; testability; terminology consistency; unresolved decisions. No numeric score unless the user supplies a scoring model.

## Split
See splitting signals in `../backlog-hygiene/references/hygiene-rules.md`. Propose child items that are each independently valuable and testable, with a one-line outcome each. Don't assign points.

## Sequence
Identify dependencies (new data sources, contract changes, access/environment, other teams, migrations), spikes for material unknowns, ordering and delivery risks. Present estimates only as questions for the team.

## Output
**Bottom line**: Ready / Ready with minor edits / Needs refinement + one sentence why.
**Strong as written**: only meaningful strengths.
**Questions that block readiness**: unresolved product/architecture decisions.
**Delivery considerations**: split, spike, dependencies, order.
**Proposed revision**: ADO-ready draft with assumptions labeled (field-by-field if updating).
Distinguish facts, user decisions and suggestions. Send wording problems to `backlog-hygiene`.
