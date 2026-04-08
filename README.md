# 👻 VeerTx

**The Non-Custodial Privacy Payment Router for Solana.**

VeerTx allows users and AI agents to send and receive SOL and USDC privately. By decoupling the sender's wallet from the receiver's wallet, VeerTx ensures that on-chain transaction history cannot be used to dox earnings, holdings, or payment networks.

🌐 **App:** [veertx.com](https://veertx.com)  
🤖 **Agent API:** [agents.veertx.com](https://agents.veertx.com) *(In Development)*

---

## 📖 Table of Contents
- [Overview](#overview)
- [How It Works (High Level)](#how-it-works-high-level)
- [Consumer Payment Links](#consumer-payment-links)
- [Agent API & SDK (Upcoming)](#agent-api--sdk-upcoming)
- [Security & Privacy](#security--privacy)

---

## 🔍 Overview

On public blockchains like Solana, sending funds directly from Wallet A to Wallet B leaves a permanent, traceable link. For creators, freelancers, and AI agents, this lack of financial privacy is a critical vulnerability. 

VeerTx solves this by acting as a non-custodial middleware layer. We utilize a secure routing pool to anonymize the flow of funds, ensuring that the sender and receiver never interact directly on-chain.

### Key Features
* **Multi-Token Support:** Native SOL and SPL USDC.
* **Non-Custodial:** VeerTx never holds private keys. Funds are swept programmatically to the end-user.
* **No Account Required:** purely Web3 native. No emails, no KYC, no passwords.
* **Agent Ready:** Built with autonomous AI trading and intent-execution in mind.

---

## ⚙️ How It Works (High Level)

To protect user privacy, the exact smart contract configurations and routing mechanics remain closed-source. However, the conceptual flow is entirely verifiable on-chain:

1. **Generation:** A recipient generates a unique VeerTx Payment Link.
2. **Deposit:** The sender deposits SOL or USDC via the link. These funds are routed into the VeerTx Privacy Pool.
3. **Anonymization:** The protocol breaks the deterministic link between the inbound deposit and the outbound destination.
4. **Claim:** The funds become available for the recipient to claim to their desired destination wallet.

*Note: Senders can verify their deposit was successfully processed via our zero-knowledge Receipt Tracker, which confirms deposit status without revealing the recipient's withdrawal address.*

---

## 🔗 Consumer Payment Links

For human users (creators, freelancers, DAOs), VeerTx operates entirely in the browser. 

* **Supported Wallets:** Phantom (Current), Multi-Wallet Adapter (Coming Soon).
* **Notifications:** Opt-in Telegram alerts for deposits and successful claims.
* **Fees:** A flat 1.5% routing fee is applied to transactions for pool maintenance and RPC costs.

---

## 🤖 Agent API & SDK (Upcoming)

*This repository will soon host the public SDKs (TypeScript & Python) for the VeerTx Agent API.*

The Agent API is designed for AI developers building autonomous agents on Solana. It allows agents to execute trades, swaps (via Jupiter), and transfers without the developer needing to build custom infrastructure or expose user funds.

**Features of the upcoming SDK:**
* Strictly non-custodial intent execution.
* Local transaction signing (Session Keys).
* Strict IP and API Key rate limiting.
* Built-in idempotency protection.

---

## 🛡️ Security & Privacy

VeerTx is designed with a "trust-minimized" architecture. 

* **No Web2 Linkage:** We do not log IP addresses to on-chain identities. 
* **Database Minimization:** Internal routing states are strictly used for transaction completion and are never exposed via public APIs.
* **On-Chain Footprint:** We utilize custom RPC routing to prevent mempool tracking of our sweep workers.

### 🔒 Open Source & Safety
To protect our users and maintain the integrity of our privacy pools, the core backend routing logic and database schemas are kept strictly private. This repository serves as our public documentation hub and the future home for our open-source Developer SDKs.

### Support
If you encounter an issue with a transaction or have a question about integrating the upcoming Agent API, please reach out via our official support channels on [veertx.com](https://veertx.com).
