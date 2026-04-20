# How VeerTx Works

VeerTx breaks the on-chain link between sender and receiver using stealth addresses and a ZK privacy pool.

## The Flow

1. **Receiver sets up** — connects wallet, signs a message, gets a VeerLink (veertx.com/pay/username)
2. **Sender pays** — visits the link, sends SOL or USDC to a one-time deposit address. No wallet connection required.
3. **Funds anonymized** — routed through Privacy Cash ZK pool (10-45 minutes)
4. **Receiver claims** — connects wallet, signs to prove ownership, sweeps funds to any wallet

On-chain: sender sees a random deposit address. Receiver claims from a different stealth address. No link between them.
