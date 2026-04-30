# Secure Skill Usage

Use this skill when selecting or executing Skills in a team or enterprise setting.

## Security Model

Skills are reusable instructions and workflows, but they can also introduce execution risk.

Prefer:

- API-based Skills for production and shared environments.
- Sandboxed or containerized execution for risky operations.
- Explicit permission boundaries.
- Environment variables or secret stores for credentials.

Avoid:

- Hardcoded credentials.
- Unreviewed CLI Skills in team or production environments.
- Skills that write outside the project boundary.
- Hidden network or filesystem side effects.

## Review Checklist

- Does the Skill need filesystem access?
- Does it execute shell commands?
- Does it access secrets?
- Can it run in a sandbox?
- Is the output auditable and reversible?

If the answer is unclear, require review before use.
