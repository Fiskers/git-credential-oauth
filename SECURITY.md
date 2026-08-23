# Security Policy

## Supported versions

Security fixes should target the latest released version and the default branch.

## Reporting a vulnerability

Do not disclose suspected vulnerabilities in a public issue.

Use GitHub's **Security** tab and **Report a vulnerability** when private
vulnerability reporting is available. Otherwise contact the upstream
maintainer through a verified private channel.

Include the affected version and platform, Git host, credential-store backend,
reproduction steps, impact, and a minimal proof of concept using a disposable
test account.

Never submit real authorization codes, access or refresh tokens, client
secrets, repository credentials, browser data, or unredacted logs. Revoke
tokens immediately if exposure is suspected.

## Sensitive areas

Changes involving these areas require particular review:

- OAuth authorization, device, redirect, and token-refresh flows;
- redirect URI validation, state parameters, PKCE, and browser callbacks;
- credential storage, retrieval, deletion, and logging;
- host detection and trust boundaries;
- token scopes and expiration;
- command-line and Git credential-protocol input.

Use least-privilege scopes, never log credentials, and treat host-provided
responses and credential-protocol input as untrusted.
