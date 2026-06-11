# Overview

VeerTx hides the link between the sender and the receiver of a crypto payment. It does this with stealth addresses and a zero-knowledge privacy pool.

Here is the full flow in four steps.

## Step 1: The receiver sets up a link

The receiver connects a wallet and signs one message. This creates their private payment keys inside their browser. The keys never leave the device.

They pick a username and get a payment link:

```
veertx.com/pay/yourname
```

[SCREENSHOT: setup page showing the connected wallet and the chosen username]

## Step 2: The sender pays

The sender opens the link. They pick a token and an amount. VeerTx shows them a one-time deposit address.

The sender pays that address from any wallet, exchange, or app. They do not connect a wallet. They do not make an account.

[SCREENSHOT: pay page showing the amount, the fee breakdown, and the deposit address with a QR code]

## Step 3: The funds are made private

The payment is routed through a zero-knowledge privacy pool. This breaks the on-chain link between the deposit address and the receiver.

This step takes about 10 to 45 minutes. The delay is on purpose. It makes timing analysis harder.

## Step 4: The receiver claims

The receiver connects the same wallet they used at setup and signs to prove ownership. The funds are then swept to any wallet they choose.

[SCREENSHOT: claim page showing one or more payments ready to claim]

## What this looks like on-chain

- The sender sees a transfer to a random one-time address.
- The receiver claims from a different, unrelated address.
- There is no on-chain link between the two.

## Next

- [Supported chains](supported-chains.md)
- [Fees and limits](fees-and-limits.md)
- [Receive payments](../guides/receive-payments.md)
