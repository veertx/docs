# Fees and limits

VeerTx shows every fee before the sender pays. Nothing is hidden. The receiver always gets the exact amount that was requested.

## How fees work

When you set an amount, that is the amount the receiver gets. VeerTx adds the fees on top, so the sender pays a little more. This is called exact settlement. The receiver is never short.

The pay page shows an itemized breakdown. It has these lines:

- **Receiver gets** - the amount you entered.
- **VeerTx fee (1%)** - our fee.
- **Privacy Cash fee (0.35%)** - the privacy pool percentage fee.
- **Privacy Cash flat fee** - a small fixed pool fee (see table below).
- **Network buffer** - a small reserve for on-chain costs (see table below).
- **You send (total)** - what the sender pays.
- **Effective cost** - the total fee as a percentage of the amount sent.

[SCREENSHOT: pay page fee breakdown showing each line and the total]

## Fee parts by chain

| Chain  | Token | VeerTx fee | Privacy Cash % | Flat pool fee   | Network buffer |
|--------|-------|------------|----------------|-----------------|----------------|
| Solana | SOL   | 1%         | 0.35%          | 0.006 SOL       | 0.004 SOL      |
| Solana | USDC  | 1%         | 0.35%          | about 0.56 USDC | none           |
| Base   | ETH   | 1%         | 0.35%          | 0.00025 ETH     | 0.0003 ETH     |
| Base   | USDC  | 1%         | 0.35%          | about 0.56 USDC | none           |

The flat and percentage pool fees are charged by the privacy pool, not by VeerTx. VeerTx passes them through at cost.

## Worked example

You want a friend to receive **10 SOL**. The pay page shows this:

| Line                    | Amount       |
|-------------------------|--------------|
| Receiver gets           | 10 SOL       |
| VeerTx fee (1%)         | ~0.1015 SOL  |
| Privacy Cash fee (0.35%)| ~0.0351 SOL  |
| Privacy Cash flat fee   | 0.006 SOL    |
| Network buffer          | 0.004 SOL    |
| **You send (total)**    | **~10.1466 SOL** |
| Effective cost          | ~1.47%       |

The receiver gets exactly 10 SOL. The sender pays about 10.1466 SOL.

## Effective cost goes down as the amount goes up

The flat fees stay the same no matter the size. So small payments cost more in percentage terms, and large payments cost less.

- A 1 SOL payment costs about 2.4% in total.
- A 10 SOL payment costs about 1.5% in total.

## Limits

These are the smallest and largest amounts the receiver can be set to get.

| Chain  | Token | Minimum  | Maximum   |
|--------|-------|----------|-----------|
| Solana | SOL   | 1 SOL    | 50 SOL    |
| Solana | USDC  | 50 USDC  | 5000 USDC |
| Base   | ETH   | 0.05 ETH | 5 ETH     |
| Base   | USDC  | 50 USDC  | 5000 USDC |

If you enter an amount outside these limits, the pay page will tell you.

## Important

Send the exact total shown on the pay page. If the sender sends less than the total, the payment may not go through. The pay page always shows the exact amount to send.

## Next

- [Send a payment](../guides/send-a-payment.md)
- [Privacy model](../technical/privacy-model.md)
