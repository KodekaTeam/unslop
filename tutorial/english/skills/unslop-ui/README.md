# Using `unslop-ui`

This skill builds, redesigns, or refines product interfaces using project evidence, realistic content, functional states, and deliberate visual composition.

## When to use it

Use it to implement pages, components, dashboards, product flows, or redesigns that require UI code changes. Use `unslop-ui-audit` for read-only reports and `unslop-logic` for nonvisual behavior changes.

## Workflow

1. Study the users, primary tasks, design owners, components, tokens, and existing patterns.
2. Establish a visual thesis and hierarchy before adding decorative details.
3. Build with semantic structure, realistic content, and loading, empty, error, and success states.
4. Ensure controls actually work and connect to the intended behavior.
5. Critique the result at page, component, and detail levels, then test primary interactions and viewports.

When the project has no governing visual direction, the skill can shortlist two or three suitable styles, explain their fit and risks, and select one primary direction before implementation. Color references are mapped to semantic body, component, typography, interaction, and state tokens; palette order alone does not determine usage.

## Prompt examples

```text
$unslop-ui Build a team settings page that follows the existing design system. Include loading, empty, error, and success states.
```

```text
$unslop-ui Redesign this dashboard to clarify its decision hierarchy without changing the API contract.
```

## Suitable combinations

- Add `unslop-responsive` for adaptation across sizes.
- Add `unslop-accessibility` for deeper accessibility checks.
- Add `unslop-copy` when product text is also being designed.
- Add `unslop-logic` when APIs or application behavior also change.
- Use `unslop-docs` after a durable change that alters project context.

## Result checks

The interface should fit the product rather than resemble a generic template. Its hierarchy, content, states, and interactions should be complete. Preserve the existing design system where applicable, and do not invent data, features, or social proof.
