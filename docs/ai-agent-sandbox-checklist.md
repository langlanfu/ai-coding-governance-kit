# AI Agent Sandbox Checklist

Use this checklist before allowing any AI agent to inspect files, run commands, use tools, browse websites, or modify code.

## Filesystem

- [ ] Agent is restricted to the intended project directory.
- [ ] Read-only mode is used when edits are not needed.
- [ ] `.env`, credentials, private keys, database dumps, logs, and customer exports are excluded.
- [ ] Destructive file operations require human confirmation.
- [ ] Backups or git checkpoints exist before broad edits.

## Network

- [ ] Network access is disabled by default or explicitly allowlisted.
- [ ] Package registry access is reviewed for dependency confusion and install scripts.
- [ ] No arbitrary outbound calls to unknown domains.
- [ ] No scraping, mass outreach, or third-party account automation without approval.

## Credentials

- [ ] No production credentials are available in the environment.
- [ ] Temporary credentials are scoped, time-limited, and revocable.
- [ ] Secrets are not pasted into prompts, files, logs, screenshots, or browser sessions.
- [ ] Credential exposure triggers incident response.

## Shell

- [ ] Shell commands are logged.
- [ ] High-risk commands require approval: delete, chmod/chown broad paths, package installs, migrations, deploys, cloud CLIs, git history rewrites.
- [ ] Commands run as a non-privileged user.
- [ ] No sudo unless explicitly approved and documented.

## Browser

- [ ] Browser automation uses test accounts where possible.
- [ ] No saved personal sessions or password-manager access.
- [ ] Purchases, account changes, messages, posts, and form submissions require human confirmation.
- [ ] Screenshots and downloaded files are reviewed for sensitive data.

## MCP Tools

- [ ] Each MCP tool has a documented purpose and permission level.
- [ ] Write-capable tools are disabled unless needed.
- [ ] Tool calls are logged with inputs and outputs where safe.
- [ ] Tools touching cloud, databases, GitHub, tickets, email, or payments require explicit scopes.

## GitHub Token

- [ ] Token has minimum repo scope and no organization admin rights unless necessary.
- [ ] Token cannot bypass branch protection.
- [ ] Agent cannot push to protected branches directly.
- [ ] PR creation is allowed only with visible diffs and reviewer assignment.

## CI/CD

- [ ] Agent cannot modify CI secrets.
- [ ] Workflow changes require human review.
- [ ] Deploy jobs require manual approval for production.
- [ ] Build logs are scanned for accidental secret disclosure.

## Databases

- [ ] Agent uses local, disposable, or sanitized databases by default.
- [ ] Production database access is prohibited unless explicitly approved.
- [ ] Destructive migrations require backup, dry run, and rollback plan.
- [ ] Customer data exports are prohibited without data owner approval.

## Production Environment

- [ ] Production deploys require human confirmation.
- [ ] DNS, payment, auth provider, cloud IAM, and infrastructure changes require human confirmation.
- [ ] Feature flags and rollback steps are prepared.
- [ ] Monitoring and alerting are checked after change.

## Log Retention

- [ ] Agent run logs include prompt, scope, tools, commands, changed files, tests, approvals, and risks.
- [ ] Logs redact secrets and customer data.
- [ ] Logs are retained according to team policy.
- [ ] Incident-related logs are preserved.
