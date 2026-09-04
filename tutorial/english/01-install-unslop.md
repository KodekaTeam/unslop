# 01 - Install Unslop in a Project

## Objective

Make `AGENTS.md` and all Unslop skills available in the target repository.

## Target structure

```text
project/
|-- AGENTS.md
`-- .agents/
    `-- skills/
        |-- unslop-ui/
        |-- unslop-docs/
        `-- ...
```

## Steps

1. Copy the `.agents/` directory from the Unslop package into the target repository root.
2. If the project does not have an `AGENTS.md`, copy the package version.
3. If the project already has an `AGENTS.md`, merge the Unslop baseline without removing existing commands, domain rules, or project structure guidance.
4. Open Codex from the repository root or one of its descendants.
5. Inspect the available skills or try an explicit invocation:

```text
$unslop-docs Explain the available modes without changing any files.
```

## Avoid

- Do not place `.agents/skills` in a child directory that is outside the path from the working directory to the repository root.
- Do not blindly replace the project's existing `AGENTS.md`.
- Do not rename `SKILL.md` to `skill.md`; the entrypoint is case-sensitive.

## Expected result

Codex can discover skills named `unslop-*`, and the project baseline is read before the agent begins work.

For user-level installation, see [`../../INSTALL.md`](../../INSTALL.md).
