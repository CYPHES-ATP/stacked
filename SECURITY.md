# Security Policy

CYPHES is an agentic coding environment. Treat every tool execution, file edit, shell command, network request, credential flow, and model-provider integration as security-sensitive.

## Supported Versions

During Phase 1, only the current `main` branch is supported. Formal version support begins with the first public alpha release.

## Reporting A Vulnerability

Please do not open a public issue for vulnerabilities.

Report security concerns privately to the project maintainers. If a dedicated CYPHES security address is not yet published, contact the repository owner through GitHub and request a private disclosure channel.

Include:

- A short description of the issue.
- Steps to reproduce.
- Impact and affected surfaces.
- Logs, receipts, or screenshots if useful.
- Suggested fix, if known.

## Security Priorities

- Tool permissions fail closed.
- Credentials must not be exposed to model context unless explicitly required and approved.
- Provider keys must be kept out of logs, receipts, screenshots, and issue templates.
- Receipts should capture audit facts without leaking secrets.
- File edits and shell commands should remain reviewable by the user.
- Contributions must not introduce copied proprietary source or leaked code.

## Out Of Scope For Public Issues

Do not post:

- API keys or provider tokens.
- Private repository code.
- Prompt contents containing secrets.
- Exploit details before maintainers have acknowledged the report.
