# Startup Team AI Policy Example

## Context

This example is for a small startup using Copilot, Cursor, terminal coding agents, and limited MCP integrations.

## Approved Uses

- Engineers may use approved AI tools for code suggestions, tests, documentation, and branch-scoped refactors.
- Agents may run local test commands and linters.
- MCP read-only access to issues and documentation is allowed.

## Approval Gates

Engineering lead approval is required for:

- Production deployment.
- CI/CD workflow changes.
- Database migration.
- New dependency in a critical service.
- Auth, billing, payment, or customer data changes.
- MCP write access to GitHub, cloud, or database systems.

## Data Rules

- No secrets or production data in prompts.
- Customer examples must be synthetic or approved anonymized samples.
- Logs must be redacted before AI use.

## PR Requirements

- AI-assisted PRs disclose tools used.
- Security-sensitive PRs require a second reviewer.
- Agent run logs are attached for autonomous changes.
- Rollback plan is required for production-impacting changes.

## Operations

Production deploys remain human-triggered. AI may draft a release checklist but may not independently execute deployment, DNS, payment, or customer data operations.
