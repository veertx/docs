# Payment lifecycle

This page walks through what happens from the moment a sender pays to the moment the receiver has the funds.

## The full path

```
Sender  ->  one-time deposit address  ->  fee taken  ->  privacy pool  ->  stealth address  ->  receiver claim
```

## Step 1: Deposit address

The sender opens the receiver's link and enters an amount. A fresh one-time deposit address is created for that payment. The sender pays it from any wallet, exchange, or app. No wallet connection is needed.

## Step 2: Detection

The payment is detected on-chain through an RPC provider. VeerTx checks it and records that funds arrived.

## Step 3: Fee

The VeerTx fee (1%) is taken before the funds enter the privacy pool. The privacy pool also charges its own small fees. All fees are shown to the sender up front. See [Fees and limits](../how-it-works/fees-and-limits.md).

## Step 4: Privacy pool

The funds are routed through a zero-knowledge privacy pool. This is the step that breaks the on-chain link between the deposit address and the receiver. It takes about 10 to 45 minutes. The delay is intentional and helps resist timing analysis.

## Step 5: Stealth address

A fresh one-time stealth address is worked out from the receiver's public meta-address. This is where the funds will land for the receiver.

## Step 6: Withdrawal

The funds move from the privacy pool to the stealth address. If the receiver has Telegram alerts on, they get a message that funds are ready.

## Step 7: Claim

The receiver connects their wallet and signs to prove ownership. Their browser computes the one-time private key for the stealth address and sweeps the funds to a wallet of their choice.

## Notes on reliability

- The deposit address waits up to 24 hours, so slow senders and exchanges still work.
- Payments stay claimable for 7 days after they are ready.
- The receiver does not need to keep a browser tab open. The privacy and withdrawal steps run on their own.

## Related

- [Stealth addresses](stealth-addresses.md)
- [Privacy model](privacy-model.md)
