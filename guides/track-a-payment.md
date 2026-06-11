# Track a payment

After you send a payment, you can follow its progress. This is useful if you want to confirm the payment went through.

## The tracker

When you send a payment, the pay page turns into a tracker. It shows three steps:

1. **Sent** - the deposit was received.
2. **Anonymizing** - the funds are passing through the privacy pool (about 10 to 45 minutes).
3. **Claimed** - the receiver has the funds.

[SCREENSHOT: receipt page showing the three-step tracker]

## Coming back later

You do not need to keep the tab open. The tracker lives at a link like this:

```
veertx.com/receipt?address=...
```

Open that link any time to check the status again. When you return to the pay page, a small banner can point you back to a payment in progress.

## What the tracker shows and hides

The tracker is built to protect privacy.

- It shows the status and the amount you sent.
- It does not show the receiver's wallet.
- It does not show where the funds end up.
- Once the payment is claimed, the tracker hides the amount and shows a clean shareable card with no private details.

[SCREENSHOT: claimed receipt card with all three steps complete]

## If a payment looks stuck

- The privacy step can take up to 45 minutes. This is normal.
- Some exchanges are slow to send. The deposit address waits up to 24 hours.
- If you sent less than the exact total, the payment may not be detected. Check the amount you sent against the total on the pay page.
