# Audits

VeerTx takes security reviews seriously. This page explains how we audit and where to read the reports.

## Public audit reports

We publish audit reports on the live security page:

```
veertx.com/security
```

The reports there are written for the public. They are sanitized by design, which means they describe findings and fixes without exposing code, secrets, or operational detail. Check that page for the most recent report.

## The veer-audit process

Security reviews for VeerTx run through a process we call veer-audit. In general terms, it works like this:

- Code is reviewed against well-known security standards, including the OWASP Top 10.
- Findings are classified by severity.
- Fixes are made and verified.
- A sanitized version of the report is published to the security page so anyone can read what was checked and what was fixed.

This runs on an ongoing basis, not just once.

## Key and secret hygiene

VeerTx follows good practice for the keys and secrets that protect the system.

- Encryption keys and secrets are rotated when needed, and the system is built so a rotation can happen cleanly.
- Secrets are kept out of public code.
- Sensitive values are never written to logs.

We do not publish operational detail about keys, for obvious reasons. The point is that key hygiene is part of the routine, not an afterthought.

## Professional third-party audit

A professional third-party audit is planned. We will publish the results when it is done.

## Reporting a problem

Found something? Please reach out.

- Discord: https://discord.gg/tNf5pDVVCe
- Email: hello@veertx.com

## More

- [Security overview](overview.md)
- [Security process](security-process.md)
