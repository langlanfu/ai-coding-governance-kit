# One-Page AI Coding Governance Checklist

## Universal Rules

- [ ] Never paste secrets, tokens, API keys, passwords, private keys, session cookies, or production credentials into AI tools.
- [ ] Use synthetic or redacted data instead of customer data.
- [ ] Treat AI output as untrusted until reviewed and tested by a human.
- [ ] Keep AI-assisted changes small, auditable, and reversible.

## Tool Boundaries

- [ ] Copilot/inline suggestions: review before accepting security-sensitive code.
- [ ] Codex-style agents: sandbox filesystem, shell, network, tokens, and branch permissions.
- [ ] Claude Code/terminal agents: log commands and require approval for destructive or production-adjacent actions.
- [ ] Cursor/AI IDEs: exclude secrets, logs, dumps, and private configuration from context.
- [ ] MCP tools: assign permission levels and disable high-impact tools by default.
- [ ] Browser automation: read-only unless a human approves the exact write action.

## Human Approval Required

- [ ] Production deploy or rollback.
- [ ] DNS, domain, SSL/TLS, email, identity provider, or cloud IAM change.
- [ ] Payment, billing, refund, subscription, or account-management action.
- [ ] Customer data export, deletion, migration, or bulk update.
- [ ] Database writes outside local/sandbox environments.
- [ ] CI/CD workflow or secret changes.
- [ ] Mass outreach, posting, scraping, or browser form submission.

## Sandbox Coverage

- [ ] Filesystem restrictions.
- [ ] Network allowlist or disabled network.
- [ ] No production credentials.
- [ ] Shell command logging and approval gates.
- [ ] Browser session isolation.
- [ ] MCP tool permission review.
- [ ] GitHub token least privilege.
- [ ] CI/CD production approval.
- [ ] Database isolation.
- [ ] Log retention and redaction.

## PR Review

- [ ] AI use disclosed.
- [ ] Tests and verification documented.
- [ ] No secrets or customer data in diff.
- [ ] Security/data/infra owners review high-risk changes.
- [ ] Rollback plan documented for production-impacting work.
