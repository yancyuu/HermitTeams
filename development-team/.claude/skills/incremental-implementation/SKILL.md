# Incremental Implementation

Use this skill when turning an approved spec or plan into code.

## Principles

- One coherent task at a time.
- Keep changes scoped to the behavior under implementation.
- Prefer existing project patterns over new abstractions.
- Use Git, task comments and tests as persistent memory.
- Clear AI context between unrelated tasks; do not carry stale assumptions.

## Implementation Loop

1. Read only the relevant files and symbols.
2. Make the smallest safe code change.
3. Run focused validation.
4. Record result and remaining risk.
5. Move to the next task only after the current one is complete.

## Completion Criteria

- Code compiles or the failure is explained.
- Focused tests or equivalent validation are run.
- User-visible behavior is summarized.
- Any follow-up work is explicitly captured.
