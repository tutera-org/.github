# Security Policy

We take the security of Tutera and its users seriously. This document explains how to report security issues and what to expect from us.

## Supported projects

This policy applies to all actively maintained repositories in the Tutera GitHub organization, including (but not limited to):

- `tutera-frontend`
- `tutera-backend`

Individual repositories may provide additional, project-specific security information.

---

## Reporting a vulnerability

If you believe you have found a security vulnerability, **do not** open a public GitHub issue.

Instead:

1. Use GitHub’s **private security advisory** feature on the affected repository, **or**
2. Contact the maintainers of the affected repository using the contact method specified in that repository (for example, a security contact email or issue template dedicated to security).

Please provide as much detail as possible, including:

- The affected repository and component (if known)
- A description of the vulnerability and its potential impact
- Steps to reproduce the issue
- Any proof-of-concept code or exploit details
- Any suggested mitigations if you have them

---

## Our commitment

When you report a vulnerability in good faith, we commit to:

- Acknowledging receipt of your report in a reasonable timeframe
- Investigating the issue thoroughly
- Working to confirm the impact and severity
- Taking appropriate steps to remediate the vulnerability
- Coordinating a responsible disclosure timeline with you when applicable

We will keep you informed of the status of your report as we work on a fix, within the bounds of what we can share.

---

## Public disclosure

We prefer coordinated disclosure. Once a fix is available and deployed (where applicable), we may:

- Publish a security advisory on GitHub for the affected repository
- Document the fix in release notes or changelogs

Please avoid sharing details of the vulnerability publicly until we have had reasonable time to address it.

---

## Scope and exclusions

This policy is focused on vulnerabilities in Tutera projects and infrastructure. It does **not** cover:

- Third-party services and libraries we depend on (though we encourage you to report those to their respective maintainers)
- Social engineering attacks against individual contributors or maintainers

If you are unsure whether something is in scope, you are still welcome to contact us; we can help route your report appropriately.