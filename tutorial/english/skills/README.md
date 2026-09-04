# Per-Skill Tutorials

This index covers every skill available in `.agents/skills/`. Select the skill that most directly owns the work, and add another only when the task genuinely crosses responsibility boundaries.

| Skill | Use it for | Guide |
| --- | --- | --- |
| `unslop-accessibility` | Semantics, keyboard use, focus, contrast, status, and zoom | [Open](unslop-accessibility/README.md) |
| `unslop-comments` | Auditing or refining comments without changing code behavior | [Open](unslop-comments/README.md) |
| `unslop-copy` | User-facing product and marketing copy | [Open](unslop-copy/README.md) |
| `unslop-docs` | Documentation bootstrapping, synchronization, reconstruction, and handoff | [Open](unslop-docs/README.md) |
| `unslop-lean` | The smallest solution that remains complete and correct | [Open](unslop-lean/README.md) |
| `unslop-logic` | APIs, state, data, validation, and business rules | [Open](unslop-logic/README.md) |
| `unslop-responsive` | Reflow, overflow, adaptive navigation, and touch targets | [Open](unslop-responsive/README.md) |
| `unslop-ui` | Building or refining product interfaces | [Open](unslop-ui/README.md) |
| `unslop-ui-audit` | Read-only visual audits with prioritized findings | [Open](unslop-ui-audit/README.md) |

## Invocation

Use explicit invocation when a particular skill must be selected:

```text
$unslop-responsive Fix the catalog page layout on narrow viewports.
```

For implicit routing, describe the objective and task boundaries concretely. Codex selects skills from their descriptions. Do not invoke every skill at once; see the [combination guide](../07-combine-skills.md).

Tutorials are user-facing guidance. Runtime behavior remains governed by `AGENTS.md` and each skill's `SKILL.md`.
