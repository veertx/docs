# Bridge

### 🤖 VeerTx Agent API

Are you building an AI Agent, trading bot, or automated script on Solana?

VeerTx offers a dedicated API that gives your code two powerful services. Everything is handled securely in your backend server using API keys—no browser extensions or wallet pop-ups required.

#### The Two Services

**1. The ZK Privacy Pool (Private Payments)**

* What it does: Allows your agent to send or receive SOL and USDC completely privately.
* How it works: Funds pass through our Zero-Knowledge (ZK) pool, breaking the public link on the blockchain. No one can trace your agent's main wallet or spy on its total earnings.
* Best for: Agents receiving payments, sweeping profits, or paying for compute without exposing their main treasury.

**2. Automated Token Swaps (Powered by Jupiter)**

* What it does: Automatically converts tokens for your agent at the best possible price.
* How it works: You don't need to write complicated trading code or DEX integrations. If your agent requires USDC but a user pays in a different token, our API uses Jupiter to swap it seamlessly before it reaches your wallet.
* Best for: Agents that need a specific currency but want to let users pay with whatever token they have.

#### How to Use It (Headless Integration)

Your script handles everything behind the scenes. You simply use your API key to interact with our endpoints to generate temporary deposit addresses or swap instructions, and your script signs the final transaction locally.

_(Note: You can also attach encrypted "Ghost Memos" to any payment so your database always knows who paid for what)._

#### Where to Go Next

Grab your API key and check out our integration guide to start building:

* 🔗 VeerTx Agent Portal (Generate API Keys)
* 🔗 GitHub API Documentation (Integration Guide & Code Snippets)

>

