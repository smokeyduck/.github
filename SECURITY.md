# Security Policy

Security reports are handled privately. Please do not open a public issue,
discussion or pull request for a vulnerability.

## Reporting a vulnerability

Report privately through GitHub Security Advisories on the affected repository:

- [Report a vulnerability](https://github.com/hungtqce180632/hungtqce180632/security/advisories/new)

If advisories are unavailable for a repository, email **security@winsell.vn**
with the details.

Include as much of the following as you can:

- type of issue (authentication bypass, injection, privilege escalation, etc.)
- affected repository, version or commit
- steps to reproduce, ideally a minimal proof of concept
- impact: what an attacker gains
- any known mitigations

## What to expect

| Stage | Target |
| --- | --- |
| Acknowledgement | within 3 business days |
| Triage and severity assessment | within 7 business days |
| Fix released | depends on severity; critical issues are expedited |
| Public advisory | after a fix is available, credit given to the reporter unless anonymity is requested |

## Scope

In scope:

- authentication, authorization and session handling
- injection (SQL, command, template, XSS)
- insecure deserialization, file upload and path traversal
- secret exposure
- SSRF and privilege escalation between tenants

Out of scope:

- findings that require an already-compromised host
- denial of service through volumetric abuse
- reports against third-party dependencies without a demonstrated impact on our code
- missing hardening headers with no exploitable consequence

## Hardening already in place

- Secret scanning and push protection on public repositories
- Dependabot alerts and automated security updates
- `rel="ugc nofollow noopener noreferrer"` on user-generated links
- File upload validated by magic bytes, not by MIME type
- Short-lived JWT access tokens plus rotating refresh tokens in HttpOnly cookies

## License

Contributions are licensed under the MIT License, the same license as the
repository you contribute to.
