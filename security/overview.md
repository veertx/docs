# Security & Transparency

## Trust Model

VeerTx is a privacy relay, not a fully trustless protocol. Understanding this distinction is important.

**What is trustless:**
- The ZK privacy pool (Privacy Cash) is a trustless, decentralized protocol
- Stealth key generation happens entirely client-side — your wallet signature and the private keys it derives never leave your browser. Only the derived public meta-address is sent to VeerTx. Private keys never touch our infrastructure at any point.
- The receiver's claim is cryptographically verified - only the wallet that generated the stealth keys can claim funds

**What requires trusting VeerTx:**
- The server briefly holds custody of funds in a throwaway deposit wallet before routing to the ZK pool
  Because funds pass through a server-generated deposit wallet first, a theoretical breach of our backend during that window could result in loss of funds before they reach the ZK pool.
- The server computes the stealth destination address using your public meta-address
- Ghost Memo encryption happens server-side. The server processes the memo before encrypting it
- We operate a strict no-logs policy, but this relies on trusting our infrastructure
- The server stores the ephemeral public key generated during ECDH, this key is fetched by the receiver's browser to complete the stealth key derivation during claim

**Our commitment:**
We are transparent about this architecture. VeerTx routes your funds through a trustless ZK pool, but the initial hop relies on our server infrastructure. We do not log IP addresses, do not link usernames to wallets on-chain. Unencrypted memo content is never retained in memory, and encrypted memos are permanently wiped 24 hours after being claimed.

## What VeerTx Never Does
- Never has access to your main wallet's private keys or your stealth receiver keys
- Never requires senders to connect a wallet
- Never stores unencrypted memos
- Never links your username to your wallet on-chain
- Never logs IP addresses or links them to on-chain identities
- Never exposes sweep transactions unnecessarily, we use dedicated RPC endpoints separate from public endpoints

## Audits
Professional third-party audit is on the roadmap. Currently all security review is internal. Bug reports welcome, contact us on X @VeerTx or open a ticket on Discord: https://discord.gg/tNf5pDVVCe

## Ghost Memo Security
Messages encrypted with AES-256-GCM before storage. Auto-deleted 24 hours after claim. Memo content is never logged.
