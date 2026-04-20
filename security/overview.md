# Security & Transparency

## Trust Model

VeerTx is a privacy relay — not a fully trustless protocol. Understanding this distinction is important.

**What is trustless:**
- The ZK privacy pool (Privacy Cash) is a trustless, decentralized protocol
- Stealth key generation happens client-side in your browser — private keys never leave your device
- The receiver's claim is cryptographically verified — only the wallet that generated the stealth keys can claim funds

**What requires trusting VeerTx:**
- The server briefly holds custody of funds in a throwaway deposit wallet before routing to the ZK pool
- The server computes the stealth destination address using your public meta-address
- Ghost Memo encryption happens server-side — the server processes the memo before encrypting it
- We operate a strict no-logs policy, but this relies on trusting our infrastructure

**Our commitment:**
We are transparent about this architecture. VeerTx routes your funds through a trustless ZK pool, but the initial hop relies on our server infrastructure. We do not log IP addresses, do not link usernames to wallets on-chain, and do not retain memo content or sensitive personal data after processing.

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
