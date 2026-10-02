# Security

This document defines the baseline security expectations for all packages in the repository.

## Core rules

- Treat all external input as untrusted.
- Validate and sanitize data at boundaries.
- Use least privilege for users, services, tokens, and file access.
- Never commit secrets, credentials, private keys, or tokens.
- Prefer secure defaults and explicit opt-in for risky behavior.

## Authentication and authorization

- Require authentication for protected actions.
- Enforce authorization on the server side for every sensitive operation.
- Keep permission checks close to the resource being accessed.
- Do not rely on obscurity, client-side controls, or hidden routes.

## Data handling

- Minimize the collection and retention of sensitive data.
- Mask or redact secrets and personal data in logs.
- Encrypt sensitive data in transit and, where appropriate, at rest.
- Use safe file handling and avoid writing untrusted paths directly to disk.

## Dependencies and supply chain

- Keep dependencies up to date.
- Prefer well-maintained libraries with a clear security track record.
- Review changes to lock files and transitive upgrades.
- Remove unused dependencies and packages.

## Common attack surfaces

- Protect against injection by using parameterized APIs and validated inputs.
- Prevent SSRF, path traversal, and deserialization issues through explicit allow-lists and safe primitives.
- Set sane timeouts for network and I/O calls.
- Avoid executing untrusted code or shell commands unless strictly necessary.

## Operational guidance

- Log security-relevant events without exposing secrets.
- Keep alerts actionable and avoid noisy false positives.
- Use secure configuration for production, staging, and local development.
- Review security impact as part of every substantial change.

