# Incident Response for AI-Assisted Development

## When to Use This Playbook

Use this process when an AI tool may have caused or contributed to:

- Secret exposure.
- Unauthorized production change.
- Customer data exposure or misuse.
- Destructive file, database, or infrastructure operation.
- Unapproved external communication or browser action.
- Malicious, vulnerable, or license-incompatible code merged from AI output.

## Immediate Actions

1. Stop the agent/session/tool run.
2. Preserve logs, prompts, diffs, command history, and tool call records.
3. Revoke exposed credentials and rotate affected secrets.
4. Disable risky tool permissions or tokens.
5. Notify the project owner and security contact.
6. If production is affected, activate the normal incident process.

## Triage Questions

- What data or system was accessed?
- Was the action read-only or write/destructive?
- Were secrets exposed to a third-party AI provider, logs, or repository?
- Did the agent use browser, MCP, shell, GitHub, CI/CD, database, or cloud tools?
- Is customer notification, legal review, or vendor notification required?

## Containment

- Revert commits or disable features.
- Roll back deployments using the approved rollback plan.
- Lock or rotate tokens used by the agent.
- Freeze affected automation until review is complete.

## Recovery

- Patch vulnerable code.
- Restore data from backups if needed.
- Re-run tests and security checks.
- Validate monitoring and alerts.

## Post-Incident Review

- Root cause.
- Missing sandbox control.
- Prompt or policy failure.
- Tool permission adjustment.
- Training or documentation update.
- Follow-up owner and due date.
