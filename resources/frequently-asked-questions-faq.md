---
description: >-
  Here are the most common questions about routing payments through the VeerTx
  Privacy Pool.
---

# Frequently Asked Questions (FAQ)

### Is VeerTx non-custodial?&#x20;

Yes. VeerTx does not act as a bank or hold user funds long-term. Funds deposited into a temporary routing address are automatically swept into the smart routing pool and securely routed to the destination wallet once the randomized delay is complete and the user executes the claim.

### **What happens if a sender deposits less than 0.7 SOL or 50 USDC?**

Deposits under the 0.7 SOL or 50 USDC minimums won't be processed by the privacy pool and will fail to route automatically. If a sender accidentally sends below the minimum, open a support ticket and our team will manually recover the funds and return them to the sender's wallet.

### What happens if someone sends more than 20 SOL or 2000 USDC?&#x20;

For security and liquidity reasons, the pool enforces strict maximums of 10 SOL and 1000 USDC. Deposits exceeding these limits risk de-anonymizing the pool and will be paused by the protocol. A manual intervention by our support team will be required to return or process the funds.

### Can I send other SPL tokens like USDT or BONK?&#x20;

Currently, VeerTx strictly supports native SOL and USDC transfers. We are actively developing the infrastructure to support additional SPL tokens in future updates, but sending any token other than SOL or USDC to a temporary deposit address right now will result in a permanent loss of funds.

### Why hasn't my payment arrived yet?&#x20;

If the sender has confirmed the deposit on the blockchain, please remember that VeerTx utilizes a randomized 10 to 45-minute routing delay. This is a mandatory security feature to prevent timing analysis attacks. Additionally, remember that funds do not appear in your wallet automatically, you must visit your VeerTx Claim Page to securely withdraw them once the delay is over. If 60 minutes have passed and the funds are not showing as "Ready" on your Claim Page, please contact support.

### Is my original wallet completely hidden?&#x20;

Yes. The sender only ever sees the temporary deposit address. When you claim the funds, your wallet history will only show an incoming transfer from the VeerTx Privacy Pool, completely severing the on-chain link between you and the sender.

### Which wallets work with VeerTx?

Phantom, Solflare, Backpack, MetaMask, and any other wallet that supports the Solana network. On mobile, connect via WalletConnect to use your preferred wallet from any device.
