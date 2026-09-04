# 07 - Combine Skills

Combine skills according to the concerns actually present, not according to the number of files touched.

## Common combinations

| Task | Primary skill | Add when relevant |
| --- | --- | --- |
| Build a new page | `unslop-ui` | `unslop-responsive`, `unslop-accessibility`, `unslop-copy` |
| Read-only visual audit | `unslop-ui-audit` | `unslop-accessibility` when requested |
| Full-stack feature | `unslop-logic` + `unslop-ui` | `unslop-docs` when durable knowledge changes |
| Mobile layout repair | `unslop-responsive` | `unslop-accessibility` for keyboard, touch, or focus |
| Implementation simplification | `unslop-lean` | `unslop-logic` when behavior is also analyzed |
| Comment cleanup | `unslop-comments` | UI or logic skills are unnecessary |
| Maintenance documentation | `unslop-docs` | A domain skill only when needed to understand the related change |

## Combined prompt examples

```text
$unslop-ui $unslop-responsive

Reimplement the checkout header with a clearer hierarchy while keeping
navigation usable on narrow screens. Preserve existing routes, design
tokens, and checkout behavior.
```

```text
$unslop-logic $unslop-docs

Add idempotency to the payment webhook with relevant tests. After it is
verified, update only the architecture and decision documentation changed
by this mechanism.
```

## Avoid mode conflicts

Do not combine the read-only `unslop-ui-audit` workflow with a prompt that requests direct implementation. Audit first, or use `unslop-ui` when the change has already been decided.
