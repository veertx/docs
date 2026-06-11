# Sender Receipts

To solve the UX problem of sender confirmation without compromising receiver privacy, VeerTx utilizes a Zero-Knowledge Receipt Tracker.

* How it works: When a sender deposits funds, they receive a unique tracking URL based on their one-time deposit address (`/receipt?address=...`).
* Privacy Guarantee: The endpoint strictly returns a binary PENDING or CLAIMED status. It mathematically cannot expose the receiver's destination wallet or withdrawal transaction signature.
* Timing Attack Mitigation: To prevent on-chain timing correlation attacks, the system introduces a randomized 5 to 15-minute delay after the receiver withdraws their funds before the public receipt status flips to CLAIMED.
