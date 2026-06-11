# Receiving Funds

Once the sender has deposited SOL or USDC into the temporary address, the VeerTx protocol begins the anonymization process.

### The Routing Delay&#x20;

Instantaneous transfers are a massive vulnerability for privacy on a public ledger. If a sender deposits 5 SOL and exactly three seconds later 5 SOL is sent to your wallet, blockchain analysts can easily link the two transactions together using timing analysis. To combat this, VeerTx introduces a randomized routing delay. Funds sit securely in the Privacy Pool for a random interval between 10 and 45 minutes. During this time, your funds are continuously mixed with other network activity, creating a deep anonymity set that obscures the original source.

### The Claim Process&#x20;

Once the randomized timer expires, the protocol flags your funds as ready. You simply navigate to your personal VeerTx Claim Page. Here, you will see a unified dashboard of your pending payments. With a single click of the "Claim" button, the exact amount of SOL or USDC (minus the 1.5% protocol fee) is routed directly from the VeerTx Privacy Pool to your destination wallet. Because the funds are pulled from our central liquidity, your wallet's transaction history will only show a transfer from the pool, completely hiding the person who actually paid you.

### Verification&#x20;

You will receive the SOL or USDC directly in your primary Solana wallet. The on-chain link is now officially severed. You have successfully received a private payment on a public blockchain, and your financial data remains entirely secure.
