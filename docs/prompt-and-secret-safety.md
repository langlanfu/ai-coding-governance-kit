# Prompt and Secret Safety

## Non-Negotiable Rule

Never paste secrets into AI tools. This includes API keys, OAuth tokens, cloud credentials, database passwords, SSH keys, private keys, session cookies, recovery codes, production environment files, customer credentials, and proprietary keys.

## Unsafe Prompt Examples

- "Here is my production `.env`; debug this." Replace with redacted variable names and error messages.
- "Use this GitHub token to create a PR." Use a scoped tool integration instead, and never expose the token in text.
- "Analyze this customer export." Use synthetic or approved anonymized data.

## Safer Prompting Pattern

1. State the goal.
2. Provide minimal relevant code.
3. Redact sensitive values using placeholders such as `<REDACTED_DB_URL>`.
4. Describe environment behavior without exposing credentials.
5. Ask for a plan before allowing edits or commands.

## Redaction Checklist

- [ ] Tokens and keys removed.
- [ ] User emails, names, addresses, and identifiers replaced with synthetic values.
- [ ] Logs trimmed to relevant lines.
- [ ] Internal URLs and hostnames reviewed before sharing externally.
- [ ] Screenshots checked for sidebars, browser tabs, tokens, and account details.

## If a Secret Is Exposed

1. Stop the run.
2. Revoke or rotate the secret immediately.
3. Preserve relevant logs without further spreading the secret.
4. Notify the project owner/security contact.
5. Review whether downstream systems were accessed.
