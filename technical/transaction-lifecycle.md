# Transaction Lifecycle

Full flow:
Sender → Deposit Address → Fee Extraction → Privacy Cash ZK Pool → Stealth Address → Receiver Claim

## Step 1: Deposit Address
Sender visits veertx.com/pay/username. Server generates a fresh throwaway Solana keypair. Sender sends funds from any wallet or exchange.

## Step 2: Webhook Detection
Helius RPC webhook detects the incoming transaction. VeerTx validates and records it.

## Step 3: Fee Extraction
1.5% fee deducted before routing.

## Step 4: Privacy Cash ZK Pool
Funds routed through Privacy Cash zero-knowledge privacy pool. Anonymization takes 10-45 minutes. On-chain link between deposit and destination is broken.

## Step 5: Stealth Address Derivation
Server computes the one-time stealth destination using the receiver's public meta-address and a fresh ephemeral keypair.

## Step 6: Withdrawal
Funds withdrawn from Privacy Cash pool to the stealth address. Receiver notified via Telegram if enabled.

## Step 7: Claim
Receiver connects wallet, signs to prove ownership, browser derives stealth private key, sweep transaction executed.
