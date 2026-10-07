# Security policy

## Supported version

This policy covers the published 2.5.1 security maintenance distribution. Earlier 2.5.0 downloads are superseded by 2.5.1.

## Reporting a vulnerability

Do not disclose a vulnerability, exploit, credential, personal information or sensitive local path in a public issue.

Use **Security → Advisories → Report a vulnerability** in this repository. The repository owner must enable GitHub private vulnerability reporting before announcing the release. If that button is temporarily unavailable, open a public issue containing only a request for a private contact route and withhold all technical details.

Include the affected version, browser or Windows package, reproducible steps, expected and observed behaviour, security impact and the SHA-256 of the affected file. Remove personal data, tokens, local paths and unrelated logs before submitting evidence.

## Scope

Useful reports include unintended network requests, path traversal or local-server exposure, unsafe import handling, cross-site scripting, dependency vulnerabilities that affect the distributed build, disclosure of local game data, or a mismatch between a published file and its recorded SHA-256.

The educational model's assumptions and disagreements about simulated values are not security vulnerabilities. Do not test against systems or data you do not own or have permission to use.

## Response and updates

The maintainer will validate the report, identify affected release hashes and, when needed, publish a new version or advisory. A published `2.5.1` asset or tag is never replaced in place; corrected binaries receive a new version such as `2.5.2`.

No fixed response-time commitment is offered.
