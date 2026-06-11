# Stealth addresses

Stealth addresses are the core idea that lets you publish one link and still keep your wallet private. This page explains the concept in plain terms.

## The problem

A normal wallet address is fixed. If you post it to get paid, anyone can look it up on-chain and see your full balance and history. Sharing one address links everything together.

## The idea

A stealth address scheme gives you two parts:

- A **public meta-address**. This is safe to share. It is what your VeerTx link points to.
- A **private key set** that only you hold. It stays in your browser.

From your public meta-address, a fresh one-time address can be worked out for each payment. Each payment lands at a different address. Only you can compute the private key for those addresses, using your private key set.

So:

- The world sees a different address for every payment.
- None of them are your real wallet.
- Only you can claim from them.

## How VeerTx uses it

1. **At setup**, your wallet signs one message. This creates your private key set inside your browser and produces your public meta-address. The private keys never leave your device.

2. **When a payment comes in**, a fresh one-time address is derived from your public meta-address. The sender pays into the flow, and the funds end up at that one-time address after the privacy step.

3. **At claim time**, your browser uses your private key set to compute the one-time private key and sweep the funds. This happens on your device.

## Why this is safe for you

- Your private keys are derived from your own wallet signature and stay in your browser.
- VeerTx only ever sees your public meta-address, which is safe to share by design.
- Even if you receive a hundred payments, an outside observer cannot group them or trace them back to a single owner.

## Two chains, two schemes

Solana and Base use different cryptography under the hood, so VeerTx uses a stealth scheme suited to each chain. The user experience is the same on both: connect, sign once, share your link, claim later.

## Related

- [Payment lifecycle](payment-lifecycle.md)
- [Privacy model](privacy-model.md)
