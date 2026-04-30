# HermitTeams

HermitTeams is the default team-template source for [Hermit](https://github.com/yancyuu/Hermit).

This repository is intentionally simple: every first-level directory that contains `hermit-team.json` is a team template. Enterprises can fork this repository, replace the templates with internal teams, and connect Hermit to their private GitHub, GitHub Enterprise, GitLab, Gitea, or other Git-compatible source.

## Templates

| Template | Purpose |
|---|---|
| `products-team` | Product discovery, PRD, requirement breakdown and engineering handoff. |
| `frontend-team` | UI implementation, interaction polish, component quality and accessibility review. |
| `code-review-team` | Code review, security review, test review and maintainability checks. |
| `incident-response-team` | Incident triage, production debugging, fix coordination and postmortem. |
| `content-team` | Product narrative, release notes, README, marketing and launch content. |

## Repository Contract

Hermit scans only repository-root children:

```text
<team-id>/
  hermit-team.json       required
  README.md              recommended
  members/*.md           member workflows
  .claude/CLAUDE.md      team operating memory
  .claude/skills/*       reusable skills
```

Do not put secrets or runtime state in templates.

Never commit:

- API keys or app secrets
- inbox files
- task runtime state
- transcripts
- launch-state files
- local machine paths that only work for one user

## How Enterprises Should Use This

1. Fork or mirror this repository into the company Git organization.
2. Create team templates for internal functions, services, and operating procedures.
3. Store reusable skills next to the teams that use them.
4. Review template changes through pull requests.
5. Connect Hermit to the repository as a team-template source.

The goal is to turn engineering process knowledge into versioned digital-team assets.
