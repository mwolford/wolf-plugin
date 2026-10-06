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

## Title convention
Verb + outcome at every level (Epic, Feature, Story). No `[Product]` prefix, no noun-phrase titles. Put "As a... I want... so that..." in the story description.

## Description format
HTML for all work items. Flag Markdown descriptions.

## Per-level field conventions
1. Risk required at Epic, Feature, Story.
2. Priority and Value Area required at all three.
3. Epic and Feature need Start and Target dates; stories don't.
4. A story committed to work sits on a sprint-level iteration, not a quarter node. Features may use a month or quarter.
5. Acceptance Criteria lives in its field only, not duplicated in the description. Epics may use "Success measures".
6. Dependency links carry an explanatory comment.
7. A story whose parent isn't the expected Feature is a question, not an error.

Notes: a story with no tasks is fine until sprint planning. Area-path inconsistency across levels is flagged only. To choose missing values, use `../../backlog-story-coach/references/field-value-guide.md`.
