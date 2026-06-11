# FAQ

## What is VeerTx?

VeerTx is a private payment tool. You share one link, people pay through it, and your wallet stays hidden on-chain. See [Welcome](README.md).

## Is there a token?

No. VeerTx has no token tied to using the product. Be careful of anyone claiming otherwise.

## Do senders need an account or a wallet connection?

No. Senders just open the link, pick an amount, and pay the address shown from any wallet, exchange, or app.

## What chains and tokens are supported?

Solana (SOL and USDC) and Base (ETH and USDC) are live. See [Supported chains](how-it-works/supported-chains.md).

## What are the fees?

A 1% VeerTx fee, plus the privacy pool's own fees (0.35% and a small flat fee), plus a small network buffer. Everything is shown before the sender pays, and the receiver always gets the exact amount requested. See [Fees and limits](how-it-works/fees-and-limits.md).

## What are the limits?

| Chain  | Token | Minimum  | Maximum   |
|--------|-------|----------|-----------|
| Solana | SOL   | 1 SOL    | 50 SOL    |
| Solana | USDC  | 50 USDC  | 5000 USDC |
| Base   | ETH   | 0.05 ETH | 5 ETH     |
| Base   | USDC  | 50 USDC  | 5000 USDC |

## How long until I can claim?

A payment takes about 10 to 45 minutes to pass through the privacy pool. After that it is ready to claim, and it stays claimable for 7 days.

## Can I claim with an empty wallet?

Yes. For a standard claim you do not need funds in your wallet. Your ability to claim is tied to your setup signature.

## Can someone else claim my payments?

No. Only the wallet that set up your account can compute the keys needed to claim. VeerTx cannot claim for you or move your funds.

## Does VeerTx see my private message?

The message is encrypted, readable only by the receiver, and removed 24 hours after claim. It is never logged and never sent in Telegram alerts.

## Is VeerTx fully trustless?

Not yet. The privacy pool and your keys are trustless, but there is a brief window where a payment sits at a one-time deposit wallet that relies on VeerTx infrastructure. We are open about this. See [Privacy model](technical/privacy-model.md).

## What is the amount fingerprint limit?

Because you get the exact amount requested, the amount can hint at a link between a deposit and a withdrawal. The pool breaks the direct on-chain link and the delay helps, but the amount is still a clue. Reducing this is on the roadmap.

## I sent a payment but nothing shows up. What now?

- Make sure you sent the exact total shown, not just the receiver amount.
- Make sure you used the right chain and token.
- The privacy step can take up to 45 minutes. Exchanges can be slow to send. The deposit address waits up to 24 hours.

## How do I report a bug or get help?

- Discord: https://discord.gg/tNf5pDVVCe
- Email: hello@veertx.com
