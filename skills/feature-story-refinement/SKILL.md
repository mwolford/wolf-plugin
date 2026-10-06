---
name: feature-story-refinement
description: Refine an Azure DevOps Feature into independently valuable Stories or PBIs with a product owner. Use when asked to "break this Feature into stories", "refine this Feature with the PO", or check whether proposed child stories cover a Feature's acceptance criteria.
license: MIT
---

# Feature-to-Story refinement

Turn a confirmed Feature outcome into reviewable, user-visible slices. Follow [ADO safety](../backlog-readiness/references/ado-safety.md); use [level guidance](../backlog-scoping/references/level-and-sizing-guide.md) for the project's work item type and size. If the work is not yet a scoped Feature, use `backlog-scoping` first.

## Process

1. **Read the source.** Get the Feature's title, description, acceptance criteria, state and existing child items, plus relevant dependencies. Identify the ADO process (Agile: User Story; Scrum: Product Backlog Item; CMMI: Requirement; Basic has no Feature level by default). If ADO access is unavailable, ask for the Feature and current children rather than claiming coverage.
2. **Find decisions.** Extract the Feature's consumer, outcome, success evidence, boundaries, and each acceptance criterion. Ask the PO up to three questions at a time about missing behavior, scope exclusions, business rules, or tradeoffs; ask engineering/architecture about material system ownership, contracts, access, migration and delivery unknowns. Label unanswered decisions as blockers or assumptions; do not invent requirements.
3. **Slice vertically.** Propose the smallest useful, testable increments by workflow, persona outcome, rule variation or data variation. Each slice must produce observable value and fit one team's sprint as a sizing check, not a promise. Put implementation steps under Stories as potential Tasks only when needed. If research is required to choose a solution, propose a time-boxed spike with the decision it must resolve; do not disguise research as a delivery Story.
4. **Check coverage.** Map every Feature acceptance criterion to one or more proposed or existing Stories. Mark anything uncovered, ambiguous, or covered only by an assumption. Compare proposed Stories with existing children to avoid duplicates. Identify dependencies and a suggested delivery order without inventing estimates, dates, owners or priority.
5. **Draft and hand off.** For each proposed item, show title (verb + outcome), consumer/outcome, scope and exclusions, and independently verifiable acceptance criteria. Use `backlog-story-coach` for detailed item drafting, `backlog-hygiene` for wording, and `backlog-readiness` when a readiness verdict is requested. Keep unresolved PO decisions visible for confirmation.

## Output

**Feature understanding**: verified outcome and constraints; missing decisions.
**Questions for the PO**: up to three, before finalizing disputed behavior.
**Story proposals**: existing vs new, each with outcome, boundaries, observable acceptance criteria and known dependencies.
**Coverage**: Feature criterion | existing/proposed Story | covered / gap / needs PO decision.
**Delivery considerations**: suggested order, technical unknowns, spike if needed.

Treat this as a proposal. For ADO creation or edits, show each field and its proposed value (and current value for edits), then wait for explicit approval before writing. Do not change the Feature's acceptance criteria to make the coverage table pass without a PO decision.
