# Send a payment

This guide shows you how to pay someone through their VeerTx link. You do not need an account or a connected wallet.

## What you need

- The receiver's VeerTx link, for example `veertx.com/pay/yourname`.
- A wallet, exchange, or app that can send the token you want to pay with.

## Steps

### 1. Open the link

Open the receiver's link in your browser.

[SCREENSHOT: pay page showing the receiver username at the top]

### 2. Pick the chain and token

Pick the chain (Solana or Base) and the token. Only chains the receiver has linked can be selected.

### 3. Enter the amount

Type the amount the receiver should get. The page shows a full fee breakdown:

- Receiver gets
- VeerTx fee (1%)
- Privacy Cash fee (0.35%)
- Privacy Cash flat fee
- Network buffer
- You send (total)

The receiver gets the exact amount you entered. The total is what you pay. See [Fees and limits](../how-it-works/fees-and-limits.md) for details.

[SCREENSHOT: pay page with an amount entered and the fee breakdown open]

### 4. Add a private message (optional)

You can attach a short private message, up to 140 characters. Only the receiver can read it. It is removed 24 hours after they claim. To add one, open the "Add a private message" section.

### 5. Send the exact total

The page shows a one-time deposit address and a QR code. Send the exact total shown.

- Send from any wallet, exchange, or app.
- Do not send less than the total. If you do, the payment may not go through.
- Send the right token on the right chain.

[SCREENSHOT: deposit address with QR code and the exact amount to send]

### 6. Done

Once you send, the page starts tracking the payment. You can keep the tab open to watch progress, or save the link to check later. See [Track a payment](track-a-payment.md).

## What you see on-chain

You see a transfer to a random one-time address. That address has no on-chain link to the receiver's wallet. You never see where the funds end up.

## Common mistakes

- **Sending the receiver amount instead of the total.** Always send the "You send (total)" figure.
- **Wrong chain.** USDC on Solana and USDC on Base are not the same. Match the chain shown.
- **Closing too early on exchanges.** Some exchanges take time to send. That is fine. The deposit address waits up to 24 hours.
