# Security overview

This page is a short summary of how VeerTx protects you. For the full trust model, see [Privacy model](../technical/privacy-model.md).

## The short version

- Your private keys are made in your browser and stay there. VeerTx never has them.
- Senders never connect a wallet, so there is nothing to leak on their side.
- Funds pass through a decentralized zero-knowledge privacy pool that VeerTx does not control.
- There is a brief window where a payment sits at a one-time deposit wallet before the pool. That window relies on VeerTx infrastructure. We are open about this.

## What VeerTx never does

- Never holds your main wallet keys or your claim keys.
- Never requires senders to connect a wallet.
- Never stores unencrypted private messages.
- Never links your username to your wallet on-chain.
- Never logs IP addresses tied to on-chain identities.

## Private messages

The optional private message a sender can attach is encrypted before it is stored. Only the receiver can read it. It is permanently removed 24 hours after the payment is claimed. The content is never logged and never sent in Telegram alerts.

## Reporting a problem

If you find a security issue, please tell us.

- Discord: https://discord.gg/tNf5pDVVCe
- Email: hello@veertx.com

We welcome responsible disclosure.

## More

- [Audits](audits.md)
- [Security process](security-process.md)
- [Privacy model](../technical/privacy-model.md)
