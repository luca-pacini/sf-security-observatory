# Security Policy

This repository is a public portfolio landing page for Salesforce Security Observatory.

## Security posture

The project concept follows these boundaries:

- Read-only security scanning.
- No automatic remediation.
- No token revocation.
- No API blocking.
- No permission removal.
- No endpoint changes.
- Sanitised evidence only.
- Least-privilege setup.
- Named Credentials for callouts.

## Sensitive data handling

The public repository must not contain:

- Access tokens.
- Refresh tokens.
- Session IDs.
- Auth URLs.
- Passwords.
- Private keys.
- Certificate bodies.
- Client secrets.
- Consumer secrets.
- Raw sensitive headers.
- Real scan output.
- Real org IDs.
- Real sandbox or production URLs.
- Real usernames or personal data.

## Reporting issues

If you notice accidental exposure of sensitive information, raise it through GitHub issue reporting or contact the repository owner directly.

Do not include secrets or sensitive data in a public issue.

## Implementation publication

Implementation code will only be published after sanitisation and final review.
