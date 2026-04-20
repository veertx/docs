# Security & Transparency

## Trust Model

VeerTx separates client-side cryptography (open and verifiable) from backend infrastructure (closed to protect business logic).

Open and verifiable:
- All stealth key derivation happens in the browser
- Frontend source code publicly available on GitHub
- Standard Ed25519 ECDH — auditable by any cryptographer

Closed source:
- Backend relayer and routing logic
- Database architecture
- Fee infrastructure

## What VeerTx Never Does
- Never has access to your private keys
- Never requires senders to connect a wallet
- Never stores unencrypted memos
- Never links your username to your wallet on-chain
- Never logs IP addresses or links them to on-chain identities
- Never exposes sweep transactions to public mempool tracking — we use custom RPC routing

## Audits
Professional third-party audit is on the roadmap. Currently all security review is internal. Bug reports welcome — contact us on X @VeerTx.

## Ghost Memo Security
Messages encrypted with AES-256-GCM before storage. Auto-deleted 24 hours after claim. Memo content is never logged.
