# Helius Webhooks & Sweeping

For a privacy router to work seamlessly, it needs to detect on-chain deposits the exact second they happen. To achieve this, VeerTx integrates enterprise-grade infrastructure from Helius to handle real-time network monitoring and automated fund sweeping for both SOL and USDC.

### Enterprise-Grade Detection&#x20;

When a user generates a VeerTx payment link, a unique, temporary deposit address is created. Because Solana moves at the speed of light, we cannot rely on slow, manual indexers to check if a user has paid. Instead, we use Helius Webhooks.

* **Real-Time Monitoring:** Helius actively listens to the Solana blockchain for us.
* **Instant Triggers:** The moment a SOL or USDC transaction hits your specific temporary deposit address, Helius fires a secure webhook to our backend.
* **Zero Missed Payments:** This ensures that even during times of massive network congestion on Solana, your deposit is instantly recognized and credited.

### The Sweeping Mechanism&#x20;

Once the Helius webhook confirms the deposit is valid, the VeerTx sweeping protocol automatically kicks in.

* Isolation: The SOL or USDC sits briefly in the temporary, isolated deposit wallet.
* The Sweep: Our backend securely signs a transaction to move the exact deposited amount (minus standard network fees) directly into the main Privacy Pool.
* Preparation for Output: Once the sweep is complete, the temporary wallet is abandoned, and the funds are mixed into the pool liquidity, ready to be distributed to the receiver.
