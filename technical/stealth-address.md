# Stealth Address Cryptography

VeerTx uses a dual-key stealth address scheme based on Ed25519 elliptic curve cryptography. All key derivation happens client-side in the browser. Private keys never touch VeerTx servers.

## Key Generation (Receiver Side)

When a receiver sets up their account, their wallet signs a fixed message:

VeerTx: Generate my stealth payment keys

The 64-byte Ed25519 signature is split into two 32-byte seeds:
- Bytes 0-31 → Scan seed
- Bytes 32-63 → Spend seed

Each seed is SHA-256 hashed, then used to derive an Ed25519 keypair via TweetNaCl:

scanKeypair  = nacl.sign.keyPair.fromSeed(SHA256(scanSeed))
spendKeypair = nacl.sign.keyPair.fromSeed(SHA256(spendSeed))

The public meta-address stored in VeerTx database:
base58(scanPublicKey) + ":" + base58(spendPublicKey)

Private keys remain in the browser only, used later during claim.

## One-Time Stealth Address Generation (Server Side)

When funds arrive, the server computes a one-time stealth destination using ECDH:

1. Generate random ephemeral private key
2. Derive ephemeral public key
3. ECDH: multiply receiver's scan public key by ephemeral scalar → shared point
4. SHA-512 the shared point → derive extended key
5. Add derived point to receiver's spend public key → stealth address

sharedPoint = scanPubKey × ephemeralScalar
derived     = getExtendedKey(SHA512(sharedPoint)[0:32])
stealthAddr = derived.point + spendPubKey

The ephemeral public key is stored with the transaction and required for claim.

## Claim (Receiver Side)

The receiver's browser reconstructs the stealth private key:

1. Recover shared point: scanPrivKey × ephemeralPubKey
2. Derive the same extended key as the server
3. Add derived scalar to spend private key → stealth private key
4. Sign sweep transaction to move funds to any wallet

Only the holder of scan and spend private keys can compute the stealth private key.
