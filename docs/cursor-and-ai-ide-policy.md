# Cursor and AI IDE Policy

## Purpose

AI IDEs such as Cursor combine editor context, chat, codebase search, refactoring, and sometimes command execution. The main governance challenge is controlling which files enter context and preventing broad automatic edits from bypassing review.

## Approved Uses

- Local code explanations and refactoring suggestions.
- Generating tests from selected files.
- Documentation and comment improvements.
- Assisted navigation across unfamiliar repositories.

## Context Rules

- Do not index or attach files containing secrets, credentials, private keys, production dumps, customer data, or confidential client materials unless explicitly approved.
- Prefer selected-file or selected-snippet context for sensitive repositories.
- Use synthetic examples instead of real user data.
- Exclude generated artifacts, logs, environment files, and private configuration from AI context where possible.

## Edit Rules

- Use small, reviewable changes.
- Inspect all AI-applied diffs before committing.
- Do not allow the IDE to make production configuration, CI/CD, dependency, or auth changes without PR review.
- Avoid accepting large rewrites where the reviewer cannot explain the behavior.

## Team Recommendations

- Maintain a repository-level AI usage note describing allowed files and prohibited data.
- Add `.env`, secrets, logs, dumps, and private fixtures to ignore/exclusion settings.
- Require manual test execution for AI-generated changes.
