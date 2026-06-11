# Roadmap

This is where VeerTx is heading. Items are not in strict order, and plans can change.

## Done

- **Solana live.** Private SOL and USDC payments on mainnet.
- **Base live.** Private ETH and USDC payments on mainnet.
- **One link, many chains.** A single username can receive on more than one chain.
- **Private message support.** Optional encrypted messages with a payment.
- **Payment tracker.** Senders can follow a payment through to claim.

## Planned: stronger privacy

The biggest planned upgrade moves more of the work into the browser.

Today, the one-time address for an incoming payment is worked out on the VeerTx side. The plan is to move that computation to the sender and receiver, so that VeerTx infrastructure can no longer see the link between them.

What this would achieve:

- A server problem or legal demand could not expose who paid whom.
- Privacy would become a cryptographic guarantee, not a policy promise.

## Planned: reduce the amount fingerprint

Because the receiver gets the exact amount requested, the amount can act as a hint that links a deposit to a withdrawal. We plan to reduce this. See [Privacy model](technical/privacy-model.md) for the full explanation.

## Planned: more chains

After the current chains are fully stable, we plan to expand to more networks based on demand. Ethereum main network is on the list.

## Planned: burner links

One-time payment links that work once and then expire. Generate a link, get paid once, and the link is gone.

## Planned: agent payments

An API and an MCP server so applications and AI agents can pay privately. See [Agent API](developers/agent-api.md).

## Planned: professional audit

A third-party audit by a reputable firm, with the results published.
