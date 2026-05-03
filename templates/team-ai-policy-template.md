# Team AI Policy Template

Use this as a starting point and customize it for your organization, clients, and regulatory environment.

## 1. Scope

This policy applies to AI-assisted development tools used on company or client work, including code completion, chat assistants, coding agents, AI IDEs, MCP tools, browser automation, and CI-integrated agents.

## 2. Approved Tools

| Tool | Approved Use | Restrictions | Owner |
|---|---|---|---|
| GitHub Copilot | Code suggestions and tests | No secrets or customer data in chat | Engineering lead |
| Codex-style agent | Scoped branch work | Sandbox required; no production access | Repo owner |
| Claude Code | Analysis and refactoring | Log non-trivial runs | Repo owner |
| Cursor/AI IDE | Local editing | Exclude sensitive files | Developer |
| MCP tools | Controlled integrations | Per-tool permission level | Security/engineering |
| Browser automation | Read-only research by default | Human approval for submissions | Task owner |

## 3. Data Rules

- Never paste secrets, tokens, API keys, passwords, private keys, or session cookies into AI tools.
- Do not provide customer data unless approved by the data owner and covered by vendor review.
- Use synthetic or redacted examples whenever possible.

## 4. Human Approval Gates

Human confirmation is required for production deploys, DNS, payments, customer data operations, database writes, CI/CD secret changes, infrastructure changes, mass outreach, and browser form submissions.

## 5. Review Requirements

AI-assisted code must be reviewed, tested, and attributable to a human owner. Security-sensitive changes require independent review.

## 6. Logging

Autonomous or semi-autonomous agent runs must record the task, prompt, scope, tools, commands, changed files, tests, approvals, and rollback plan.

## 7. Exceptions

Exceptions must include reason, owner, expiration date, compensating controls, and approval record.
