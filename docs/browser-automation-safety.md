# Browser Automation Safety

## Purpose

Browser automation agents can log in, click buttons, submit forms, purchase items, post content, send messages, scrape websites, or change account settings. These actions may be externally visible and difficult to reverse.

## Default Rule

Browser automation is read-only unless a human explicitly approves the specific write action.

## Prohibited Without Approval

- Sending messages, emails, comments, posts, or connection requests.
- Purchasing, subscribing, refunding, bidding, or transferring funds.
- Changing account settings, passwords, MFA, API keys, roles, or permissions.
- Downloading, exporting, deleting, or bulk editing customer data.
- Scraping websites where terms, robots rules, or privacy obligations are unclear.
- Submitting government, legal, tax, HR, or compliance forms.

## Safe Practices

- Use test accounts and sandbox environments.
- Disable password-manager access and personal saved sessions.
- Record the task, target site, account used, and approved actions.
- Require a pre-submit pause before any form submission or irreversible click.
- Capture evidence for audit without exposing sensitive screenshots.

## Review Before Running

- [ ] Is the action reversible?
- [ ] Could it notify customers, vendors, or the public?
- [ ] Could it spend money or create a legal obligation?
- [ ] Could it access or expose customer data?
- [ ] Is the website authorized for automation?
