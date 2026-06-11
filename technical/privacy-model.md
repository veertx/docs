# Privacy model

VeerTx is honest about what it does and does not protect. This page explains the trust model in plain terms.

## What is trustless

- **The privacy pool.** The zero-knowledge pool that breaks the on-chain link is a separate, decentralized protocol. VeerTx does not control it.
- **Your private keys.** Your stealth key set is created from your own wallet signature, inside your browser. The keys never leave your device. VeerTx never has them.
- **Your claim.** Only the wallet that set up your account can compute the keys needed to claim. No one else can take your funds, including VeerTx.

## What you trust VeerTx for

- **A brief custody window.** Each payment first lands at a one-time deposit wallet before it enters the privacy pool. During that short window, the funds depend on VeerTx infrastructure.
- **Stealth address computation.** The one-time address for each incoming payment is worked out on the VeerTx side from your public meta-address.
- **No-logs policy.** VeerTx does not log IP addresses and does not link your username to your wallet on-chain. This is a policy backed by how the system is built, but it still asks you to trust that policy.

## What VeerTx never does

- Never holds your main wallet keys or your stealth claim keys.
- Never requires senders to connect a wallet.
- Never links your username to your wallet on-chain.
- Never logs IP addresses tied to on-chain identities.
- Never keeps private message content after the 24-hour window following a claim.

## The amount fingerprint limit

There is one known limit you should understand.

Because the receiver gets the exact amount requested, the amount that goes in and the amount that comes out are closely related. A determined observer who is watching both sides could try to match a deposit to a withdrawal by amount and timing.

The privacy pool breaks the direct on-chain link, and the 10 to 45 minute delay makes timing harder. But the amount itself can act as a hint. This is true across the whole product, on every chain.

We are upfront about this. Reducing the amount fingerprint is on the roadmap. See [Roadmap](../roadmap.md).

## Where this is heading

The long-term goal is to move more of the work into the sender's and receiver's browsers, so that even VeerTx infrastructure cannot see the link between sender and receiver. This would turn the trust points above into cryptographic guarantees. See [Roadmap](../roadmap.md).

## Related

- [Security overview](../security/overview.md)
- [Audits](../security/audits.md)
