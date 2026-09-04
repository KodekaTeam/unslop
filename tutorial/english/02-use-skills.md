# 02 - Use Skills

## Explicit invocation

Prefix a skill name with `$` when you need to ensure that a particular workflow is selected:

```text
$unslop-ui Refine this settings page while preserving the existing design system.
```

```text
$unslop-docs Bootstrap persistent documentation for this repository.
```

```text
$unslop-ui-audit Audit the checkout page as read-only work and report evidence-backed findings.
```

Explicit invocation is useful for documentation bootstrapping, audits that must remain read-only, or tasks where neighboring skills could plausibly match.

## Implicit invocation

Codex can select a skill from its description when the request is specific:

```text
Fix horizontal overflow and mobile navigation on the dashboard page.
```

This request should route to `unslop-responsive` without naming it directly.

## Write outcome-oriented prompts

Include:

- the desired result;
- the project area in scope;
- constraints that must be preserved;
- initial evidence or files, when known;
- important verification requirements.

Example:

```text
$unslop-logic Fix duplicate invoice creation when a webhook is retried.
Preserve the current API contract and add a regression test to the existing test suite.
```

## Avoid

- invoking every skill "just in case";
- using a skill name instead of explaining the objective;
- selecting `unslop-ui-audit` when direct implementation is required;
- using `unslop-comments` for a change that also modifies executable behavior.
