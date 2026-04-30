# Hermit Team Template Specification

## Required file

Each template directory must contain `hermit-team.json`.

```json
{
  "schemaVersion": 1,
  "id": "products-team",
  "displayName": "产品生成小分队",
  "description": "...",
  "members": [],
  "skillPaths": [],
  "memoryPaths": [".claude/CLAUDE.md"],
  "tags": []
}
```

## Member fields

```json
{
  "name": "reviewer",
  "role": "代码审查",
  "workflowFile": "members/reviewer.md"
}
```

- `name` should be stable and CLI-safe.
- `role` should be user-facing and may use Chinese.
- `workflowFile` should point to a markdown workflow in the template directory.

## Skill paths

`skillPaths` points to directories containing `SKILL.md`.

Supported examples:

```json
[".claude/skills/code-review"]
```

## Design principles

- Templates define reusable team behavior, not one-off runtime state.
- Keep workflows concise and operational.
- Prefer explicit deliverables and quality gates.
- Do not include credentials.
- Do not assume a specific developer machine path.
