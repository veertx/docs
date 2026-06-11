# Depositing SOL or USDC

When someone clicks your VeerTx payment link, they are taken to a secure, single-use deposit portal. This page is designed to make sending private payments as easy as a standard Solana network transfer, without exposing the receiver's actual wallet.

### Step 1: The Deposit Interface&#x20;

The sender will see a clean interface where they can select their preferred asset (SOL or USDC) and view a Temporary Deposit Address. This is an intermediary wallet created exclusively for this specific transaction. It acts as a secure bridge to the VeerTx Privacy Pool. The sender can either copy this text address directly or scan the provided QR code using their mobile wallet.

### Step 2: Transferring the Funds&#x20;

The sender can use any standard Solana wallet (such as Phantom, Solflare, or Backpack) or centralized exchange account to initiate the transfer.

* Important Note on Limits: VeerTx currently supports transactions between 0.7 and 20 SOL, or 50 and 2000 USDC. Senders must ensure their deposit falls strictly within these ranges.

The sender simply transfers the desired amount of SOL or USDC to the temporary address displayed on their screen.

### Step 3: Confirmation and Sweeping&#x20;

Because VeerTx is built natively on Solana, network confirmation takes only a few seconds. Once the sender broadcasts the transaction:

* Our Helius infrastructure instantly detects the incoming SOL or USDC.
* The deposit interface updates to confirm the funds have been successfully received.
* The SOL or USDC is immediately swept from the temporary address into the secure Privacy Pool, effectively severing the on-chain link to the sender's wallet.

At this point, the sender's job is completely finished. The funds are now securely mixing in the pool, waiting for the automated routing delay to finish before being sent to the final destination.

### Tracking Your Payment

After you send a payment, VeerTx gives you a private receipt link. You can use this link to check if your transfer is "Pending" or successfully "Claimed" by the receiver.

To protect the receiver's privacy, the receipt will never show their final wallet address or the exact time they withdrew the funds.

### Ghost Memos&#x20;

VeerTx allows senders to attach an anonymous message to their deposit without compromising on-chain privacy.

Because we do not use on-chain memos (which would permanently link the sender's wallet to the message), we built an ephemeral, off-chain messaging layer.

**• AES-256-GCM Encryption:** Memos are never stored in plain text. They are securely encrypted at the database level the moment the deposit is generated.&#x20;

**• Zero On-Chain Footprint:** The memo data lives entirely off-chain in the VeerTx middleware layer.&#x20;

**• Strict 24-Hour TTL (Time-To-Live):** Memos are not kept permanently. An automated background worker securely nullifies and deletes the encrypted memo exactly 24 hours after the receiver executes their claim.&#x20;

**• XSS Protection:** The frontend strictly uses secure text DOM insertion to prevent any malicious script injection from sender to receiver.
