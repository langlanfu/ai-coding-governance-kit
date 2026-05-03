# Codex-Style Agent Usage Policy

## Purpose

Codex-style agents can inspect files, edit code, run shell commands, execute tests, and sometimes operate autonomously. Their risk is broader than autocomplete because they may change many files, invoke tools, or perform network operations.

## Approved Uses

- Implementing scoped issues on non-production branches.
- Running local tests, formatters, and static analysis.
- Creating documentation, fixtures, and small migrations after review.
- Refactoring with clear acceptance criteria and rollback path.

## Required Boundaries

- Agents run with least privilege and only inside the intended repository or workspace.
- Shell access is limited to development commands unless explicitly approved.
- Network access is disabled by default or restricted to package registries and documented endpoints.
- Production credentials, deploy keys, cloud admin credentials, and customer data are not exposed to the agent.
- Every agent run should produce a run log with prompt, files touched, commands run, tests performed, and unresolved risks.

## Human Confirmation Required

A human must approve before the agent performs:

- Production deploys or infrastructure changes.
- DNS, domain, email, payment, billing, or account-management actions.
- Database writes outside disposable/local environments.
- Mass messaging, scraping, browser automation against third-party services, or customer data export.
- Installing new dependencies in production projects.

## Output Review

- Review diffs before execution in shared environments.
- Validate tests are meaningful, not merely adjusted to pass.
- Check for accidental secret exposure in code, logs, and prompts.
- Confirm rollback steps are documented for risky changes.
