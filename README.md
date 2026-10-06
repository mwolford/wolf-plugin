# wolf-plugin

Personal GitHub Copilot plugin for housing and authoring my own skills.

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

All four need an ADO MCP connection to read items; updates require explicit approval (`skills/backlog-readiness/references/ado-safety.md`).

## Adding a new skill

1. Copy `templates/SKILL.md` to `skills/<skill-name>/SKILL.md` (folder name = `name` in frontmatter).
2. Edit `SKILL.md` — write a clear `description` with trigger phrases.
3. Put supporting docs in `skills/<skill-name>/references/` and link relatively.
4. Reinstall/update the plugin and restart Copilot.
