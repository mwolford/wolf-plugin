---
name: backlog-scoping
description: Coaches an idea into the right ADO work item level (Epic, Feature, Story/PBI, Task) and the right size. Use when the user has a raw idea and does not know what level it is, says "is this an epic or a story", "how big is this", "scope this", "break this down", "too big", "roll this up", or wants to decompose or consolidate work across the hierarchy.
license: MIT
---

# Backlog scoping coach

Takes an idea of unknown size and lands it at the right level of the Azure DevOps hierarchy, then sizes or splits it. Level/size guidance: [level-and-sizing-guide.md](references/level-and-sizing-guide.md). Safety rules: [ado-safety.md](../backlog-readiness/references/ado-safety.md).

## Process

1. **Capture the idea** in the user's words. Do not reformat yet.
2. **Identify the ADO process** (Agile, Scrum, CMMI, Basic). Read it from ADO if connected; otherwise ask once. It determines type names.
3. **Triage the level** by asking at most three questions at a time, drawn from:
   - Who is the user or customer, and what outcome changes for them?
   - How many teams or releases would this touch?
   - Could one team finish it in a single sprint? Could it ship on its own and be useful?
   - Is it a goal/initiative, a capability, a slice of behavior, or a unit of work?
4. **Recommend a level** with a one-line reason and the signals that drove it. State confidence; if borderline, give both options and the deciding question.
5. **Check size** against the guide. If too big, propose a split one level down (Epic→Features, Feature→Stories, Story→smaller Stories by vertical slice, not by layer). If too small, propose rolling up under an existing parent.
6. **Check the parent chain**: suggest an existing parent to link, or flag a missing one. Never invent one.
7. **Hand off**: write the item with `backlog-story-coach`, lint with `backlog-hygiene`, check Definition of Ready with `backlog-readiness`.

## Output

**What I understand** (1–3 lines)
**Recommended level**: Level, confidence, why
**Size check**: fits / too big / too small, and why
**Suggested breakdown or parent** (titles only, no estimates)
**Questions to settle next** (up to three, numbered)

## Rules

- Do not invent estimates, points, dates or owners; ask or leave blank.
- Split vertically (user-visible slices), not by technical layer, unless the item is an Architectural-value-area Feature.
- Tasks do not replace Stories; if a "Task" has user value, it is a Story.
- Time ranges in the guide are heuristics, not Microsoft requirements; say so if the user asks for the source.
- Never create or update ADO items without explicit approval, shown field by field.
