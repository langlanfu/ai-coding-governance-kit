# MCP Tool Permission Policy

## Purpose

Model Context Protocol (MCP) tools can connect AI assistants to files, databases, browsers, issue trackers, cloud systems, source control, and internal services. MCP increases usefulness but also expands the blast radius of mistakes.

## Permission Levels

### Level 0: No Tool

The assistant can only reason over provided text. Use for sensitive analysis when no system access is required.

### Level 1: Read-Only Tool

The assistant may read approved resources such as selected files, documentation, or issue metadata. It cannot modify state.

### Level 2: Limited Write Tool

The assistant may create drafts, branches, comments, local files, or test records. It cannot affect production, customers, billing, credentials, or protected branches.

### Level 3: High-Impact Tool

The assistant can affect production, databases, accounts, payments, cloud infrastructure, CI/CD secrets, DNS, external messaging, or customer data. Level 3 requires explicit human approval per action and should be rare.

## Approval Rules

- Every MCP server must have an owner and documented purpose.
- Tools are disabled by default and enabled per task.
- Write tools must log inputs, outputs, target resource, and actor.
- High-impact tools require human confirmation and rollback plan.
- Secrets must be injected through secure tool configuration, never pasted into prompts.

## Examples

- GitHub read-only issue search: Level 1.
- Creating a PR from a feature branch: Level 2.
- Modifying branch protection or repository secrets: Level 3.
- Querying a sanitized development database: Level 1 or 2 depending on writes.
- Updating production customer records: Level 3.
