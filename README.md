# wolf-plugin

Personal GitHub Copilot plugin for Azure DevOps backlog coaching.

## Install

```
copilot plugin install mwolford/wolf-plugin
```

Or for local development:

```
copilot plugin install ./path/to/wolf-plugin
```

## Skills

| Skill | Purpose |
|---|---|
| `backlog-scoping` | Coaches an idea to the right Epic/Feature/Story/Task level and size (ADO-based). |
| `backlog-story-coach` | Interviews you while creating/refining an ADO work item (max 3 questions at a time). |
| `backlog-hygiene` | Lints wording, terminology consistency and testability; field-by-field fixes. |
| `backlog-readiness` | Definition of Ready verdict, splitting and sequencing. |
| `backlog-tree-review` | Read-only Epic tree review: level mismatches, technical Features, and splitting a monolithic Epic into time-boxed Epics. |

All five need an ADO MCP connection to read items; updates require explicit approval (`skills/backlog-readiness/references/ado-safety.md`).

## Agent

| Agent | Purpose |
|---|---|
| `product-owner` | Coordinates the backlog skills to scope, draft, refine, and review ADO work items while leaving product decisions to you. |

The agent is defined in `agents/product-owner.agent.md`. Select it with `/agent` in Copilot CLI (or choose it from the installed plugin's agents in the Copilot app). It uses only the skills needed for the request and proposes field-by-field edits for approval before changing ADO items. Backlog prioritization and cross-backlog triage do not yet have dedicated skills.

## Adding a new skill

1. Copy `templates/SKILL.md` to `skills/<skill-name>/SKILL.md` (folder name = `name` in frontmatter).
2. Edit `SKILL.md` — write a clear `description` with trigger phrases.
3. Put supporting docs in `skills/<skill-name>/references/` and link relatively.
4. Reinstall/update the plugin and restart Copilot.

## Install (marketplace)

```bash
copilot plugin marketplace add mwolford/wolf-plugin
copilot plugin install wolf-plugin@wolf-plugins
```

In the Copilot app, add the marketplace `mwolford/wolf-plugin`, then install `wolf-plugin`.
