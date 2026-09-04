# Unslop Project Guidance

Use this file as a portable baseline. Instructions supplied by the user and rules closer to the edited file take precedence.

## Working contract

- Read the relevant project documentation and trace the affected implementation before choosing a solution.
- Preserve established architecture, naming, visual language, and product behavior unless the task explicitly changes them.
- Make the smallest coherent change that resolves the requested outcome. Do not bundle speculative cleanup.
- Treat claims, sample data, controls, routes, and success states as product behavior: they must be real, clearly marked as examples, or honestly unavailable.
- Verify the changed behavior with the narrowest meaningful checks. State what was not verified.

## Session context bootstrap

Before implementation, debugging, refactoring, release, or maintenance work, establish durable project context when the files exist:

1. Read the repository-root `README.md` and `docs/README.md`.
2. Read `docs/structure-of-app/PROJECT_CONTEXT.md`, `ARCHITECTURE.md`, and `DECISIONS.md`.
3. Follow links from `docs/README.md` only to the timeline, guide, build, history, audit, roadmap, or research documents relevant to the current task.

Missing documentation must not block ordinary work. Do not load the entire documentation tree by default. Resolve conflicts in favor of current code, configuration, tests, and newer accepted decisions, then flag stale documentation.

After a material change, update durable documentation only when project context, architecture, an accepted decision, operational commands, release behavior, or maintenance history actually changed. Use `unslop-docs` for substantial documentation creation, reconstruction, or synchronization.

## Skill routing

Codex discovers the skills under `.agents/skills`. Load only the entries that materially affect the task:

- Build, redesign, or visually refine an interface: `.agents/skills/unslop-ui/SKILL.md`
- Audit an existing interface and prepare evidence-backed recommendations: `.agents/skills/unslop-ui-audit/SKILL.md`
- Repair responsive behavior or mobile layout: `.agents/skills/unslop-responsive/SKILL.md`
- Check accessibility, keyboard use, focus, contrast, or inclusive states: `.agents/skills/unslop-accessibility/SKILL.md`
- Write or revise product-facing prose: `.agents/skills/unslop-copy/SKILL.md`
- Clean up code comments without changing behavior: `.agents/skills/unslop-comments/SKILL.md`
- Implement or review application, API, state, and business rules: `.agents/skills/unslop-logic/SKILL.md`
- Reduce over-engineering in a coding change: `.agents/skills/unslop-lean/SKILL.md`
- Create, reconstruct, or synchronize durable project documentation: `.agents/skills/unslop-docs/SKILL.md`

Common combinations:

- UI implementation: `unslop-ui`, plus `unslop-responsive` or `unslop-accessibility` only when those concerns are substantial.
- UI audit: `unslop-ui-audit`; add accessibility only when the user requests an accessibility review.
- Full-stack feature: `unslop-ui` for presentation and `unslop-logic` for behavior. Do not make the UI skill govern domain logic.
- Comment-only cleanup: `unslop-comments` alone.

## Delivery baseline

- Connect every reported problem to an observed file, runtime path, rendered state, or explicit product contract.
- Do not invent product direction to make a result look polished.
- Keep expected loading, empty, error, validation, permission, and success states coherent with the task.
- Preserve semantic structure, keyboard access, visible focus, readable contrast, and reflow where UI is affected.
- Report changed files, checks run, and remaining risk without ceremonial checklists for untouched areas.
