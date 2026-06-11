# Security process

Every meaningful change to VeerTx goes through review before it reaches users. This page describes that process in plain terms.

## Review before deploy

Changes that touch payments, cryptography, or user data get extra scrutiny:

- The change is planned and written down before any code is touched.
- An independent review checks the approach for security and design problems before code is written.
- The change is reviewed again as code, one piece at a time.
- The affected flow is tested before and after it goes live.

Nothing that touches funds ships on a hunch.

## Standards we use

- The OWASP Top 10 as a primary checklist for web security.
- Constant-time comparisons for secret checks, to avoid timing attacks.
- Standard, well-reviewed cryptographic libraries for all signature checks.
- Strong HTTP security headers and a content security policy.
- A network layer in front of the site for DDoS protection and filtering.

## Money-path safety

The payment pipeline is built to be safe even when things go wrong:

- On-chain receipts are treated as the source of truth for whether a payment landed.
- The system avoids any action that could move funds twice.
- If a step is unclear, the system waits and retries rather than guessing.
- There is no automatic refund path that could be tricked into double spending.

## Honesty about limits

We document our trust model and known limits openly rather than hiding them. See [Privacy model](../technical/privacy-model.md) and [Security overview](overview.md).

## More

- [Audits](audits.md)
- [Security overview](overview.md)
