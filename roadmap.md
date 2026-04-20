# Roadmap

## Current Architecture
VeerTx currently operates as a trusted privacy relay. The server handles stealth address computation and memo encryption. We are transparent about this — see [Security & Transparency](security/overview.md).

## Planned: Client-Side ECDH (True Trustless Privacy)
The most significant planned upgrade is moving stealth address generation entirely to the sender's browser.

**What changes:**
- Sender's browser will compute the ECDH stealth address derivation locally
- Server will never see the link between sender and receiver
- Ghost Memo encryption will move to the browser — server receives only ciphertext

**What this achieves:**
- Server compromise or subpoena cannot expose sender/receiver relationships
- VeerTx becomes a true trustless privacy layer, not a trusted relay
- Privacy guarantees become cryptographic, not policy-based

This is a top architectural priority after the current version stabilizes.

## Planned: Multi-Chain Expansion
After Solana is fully stable and audited, expansion to:
- **Base** — low fees, large USDC volume, likely compatible with Privacy Pools protocol
- **Ethereum L1** — high-value transactions where fees are acceptable
- **More chains** — based on user demand

## Planned: Professional Security Audit
A third-party audit by a reputable firm (OtterSec, Cantina, or equivalent) is on the roadmap once the client-side ECDH migration is complete. Auditing the current architecture and the upgraded trustless version together.

## Planned: Burner Links
One-time payment links that self-destruct after a single use. Generate a link, get paid once, link permanently deleted.
