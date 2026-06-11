# The Privacy Pool

The Privacy Pool is the core engine that powers VeerTx. It acts as the secure middle layer between the sender and the receiver, ensuring that funds can move across the Solana network without leaving a traceable path.

### The Standard Transfer (A to B)&#x20;

In a normal Solana transaction, Wallet A sends SOL or USDC directly to Wallet B. This creates a permanent, visible line on the blockchain connecting the two entities. Anyone analyzing the chain can see exactly who paid whom, and at what time.

### The VeerTx Transfer (A to Pool to B)&#x20;

VeerTx fundamentally changes this routing structure. When a payment is initiated through our platform, the process looks like this:

* Temporary Deposit Address: The sender deposits funds into a randomly generated, single-use wallet address.
* The Sweep: Once the deposit is confirmed, the funds are automatically swept into the VeerTx Privacy Pool.
* The Distribution: The receiver is then paid directly from the main Privacy Pool (or one of its distributed output wallets).

Because the receiver gets their SOL or USDC from the pool and not the sender's original wallet, the on-chain link is permanently severed.

### The Anonymity Set&#x20;

The strength of the Privacy Pool comes from its volume. As more users process transactions through VeerTx, the funds are continuously mixed within the pool. When a receiver claims their payment, the SOL or USDC they receive is mathematically indistinguishable from any other SOL or USDC in the pool. This "anonymity set" means blockchain sleuths cannot accurately determine which input corresponds to which output.

### Non-Custodial Routing&#x20;

It is important to note that the Privacy Pool is designed for routing, not storage. VeerTx is a non-custodial protocol. Funds are swept and distributed automatically based on the generated payment links. We do not operate as a bank, and funds only remain in the pool for the duration of the routing delay.
