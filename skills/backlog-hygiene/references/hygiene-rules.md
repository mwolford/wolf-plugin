# Backlog Hygiene Rules

## Title
- Names one capability, behavior, or outcome.
- Avoids implementation-only wording unless the item is a technical enabler.
- Uses the same terminology as the parent and neighboring items.
- Avoids unexplained acronyms.

## Description
- States the problem or opportunity before the proposed solution.
- Identifies the consumer or decision maker.
- States the expected outcome.
- Separates current state, desired state, and constraints.
- Includes explicit exclusions when scope could be misunderstood.

## Acceptance criteria
- Each criterion is independently verifiable.
- Criteria describe observable behavior or evidence.
- Criteria do not repeat the description.
- Criteria avoid subjective terms such as intuitive, easy, useful, robust, or fast without a measurable definition.
- Error, empty-state, permission, and freshness behavior are included only when relevant.
- Implementation tasks are not disguised as acceptance criteria.

## Splitting signals
Consider splitting when an item contains:
- Multiple user personas with different outcomes.
- Multiple independent workflows.
- Multiple systems that can deliver value separately.
- Research plus production implementation.
- Temporary and target-state solutions.
- Several major clauses joined by "and."
- Acceptance criteria that form separate deliverable groups.

## Dependency signals
Ask about dependencies when the item requires:
- A new authoritative data source.
- A schema or contract change.
- Access, identity, or environment setup.
- Another team's decision or deliverable.
- Migration or temporary mapping.
- A spike to resolve a material unknown.

## Product versus engineering responsibility
Product typically owns:
- Problem, consumer, outcome, priority, scope, acceptance, and tradeoffs.

Engineering typically owns:
- Technical design, implementation tasks, estimates, capacity commitment, and detailed sequencing.

Architecture may guide:
- System boundaries, ownership, integration patterns, target state, temporary exceptions, and technical risk.
