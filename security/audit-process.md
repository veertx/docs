# Security Review Process

## How VeerTx Approaches Security

Every major change to VeerTx goes through a three-layer review process before deployment.

**Layer 1 — Planning with Claude**
All features and fixes are planned in Claude before any code is written. Architecture decisions, edge cases, and security implications are discussed and documented in MEMORY.md before touching the codebase.

**Layer 2 — Gemini Architecture Review**
Before any change that touches critical infrastructure — payment pipelines, cryptographic flows, database schema, authentication routes — a detailed brief is sent to Gemini for independent architecture and security review. No code is written until Gemini approves the approach.

**Layer 3 — Claude Code Implementation**
All file edits are made by Claude Code in VS Code. Every change is shown before saving. Changes are never combined — one file at a time, confirmed before moving to the next.

## Pre-Deploy Checklist

Before any backend change goes to production:
- Gemini architecture approval received
- Change shown in Claude Code before saving
- Git push to private GitHub repo
- Git pull on server
- PM2 restart and status check
- Manual test of affected flow

## Security Tools Used

- **OWASP Top 10:2025** — primary audit framework
- **Claude Code owasp-security skill** — automated code review
- **Gemini** — independent architecture and security review
- **nacl (TweetNaCl)** — all cryptographic signature verification
- **crypto.timingSafeEqual** — constant-time secret comparison
- **Helmet.js** — HTTP security headers and CSP
- **Cloudflare** — DDoS protection, WAF, DNS

## Known Limitations

VeerTx is honest about its trust model. Full details at [Security & Transparency](./overview.md).
