# Using `unslop-responsive`

This skill improves how interfaces adapt to available space: reflow, overflow, navigation, content order, content-driven breakpoints, zoom, and touch targets.

## When to use it

Use it when layouts break, content is clipped, tables become unusable, navigation grows crowded, or components are merely scaled down instead of recomposed. Do not use it for a broad visual redesign when responsiveness is not the primary problem.

## Workflow

1. Reproduce the failure with realistic viewports and content.
2. Find the owner of the width, overflow, min-content, or constraint causing the problem.
3. Recompose according to content priority instead of shrinking everything.
4. Introduce local scrolling only where it is intentional.
5. Test wide, near-breakpoint, and narrow viewports, as well as zoom, long text, touch, and keyboard use.

## Prompt examples

```text
$unslop-responsive Fix this dashboard between 320px and 768px. Prioritize reflow and do not hide the primary action.
```

```text
$unslop-responsive Keep the transaction table usable on mobile with local scrolling and clear headers.
```

## Suitable combinations

- Pair with `unslop-ui` when building or redesigning a page.
- Pair with `unslop-accessibility` for zoom, keyboard, reading order, and target size.
- Pair with `unslop-copy` when realistic text length is part of layout testing.

## Result checks

The page should not scroll horizontally unless explicitly intended. Important content must remain available, touch targets must remain usable, and reading and focus order must make sense. Breakpoints should respond to content needs rather than customary device numbers.
