# Limits & Fees

To maintain the security, liquidity, and speed of the privacy pool, VeerTx enforces strict parameters on all transactions. Understanding these limits is crucial for ensuring your funds route successfully.

### Transaction Limits (SOL & USDC)&#x20;

Currently, the protocol only processes deposits between 0.1 and 10 SOL, or between 5 and 1000 USDC.

* **Minimum (0.7 SOL or 50 USDC):** Deposits below these thresholds will not trigger the automated sweeping webhook, as they are uneconomical to process after standard Solana network fees.
* **Maximum (20 SOL or 2000 USDC):** Deposits above these maximums risk draining the pool's immediate liquidity and reducing the anonymity set for other users. Keeping transactions within this range ensures mathematical indistinguishability for everyone.
* **Note:** If a sender deposits an amount outside of these limits, the transaction will fail to route automatically and will require manual support intervention.

### The Protocol Fee (1.5%)&#x20;

VeerTx charges a flat 1.5% fee on all successful transfers. This fee is completely seamless. It is automatically deducted from the final output amount before it is sent to the receiving destination wallet. The sender does not need to calculate or add extra SOL or USDC to their deposit to cover this fee.

What does the fee cover?

* Enterprise-grade Helius RPC infrastructure and real-time webhooks.
* Automated backend sweeping and relayer network costs.
* Continuous liquidity balancing and security maintenance within the Privacy Pool.

### Routing Delays (10 - 45 Minutes)&#x20;

As a core protocol rule, no transaction is ever processed instantly. Every deposit is subject to a randomized 10 to 45-minute delay. This is not a network lag; it is a designed security feature. This delay ensures all incoming funds are thoroughly mixed with other network activity, guaranteeing that malicious actors cannot use timing analysis to de-anonymize our users.
