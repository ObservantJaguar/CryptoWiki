---

---

# Signatures (ECDSA, EdDSA)

A **digital signature** proves that a message (transaction) was authorized by the holder of a private key, without revealing the key. Signatures provide authentication, integrity, and non-repudiation on-chain.

## ECDSA

The **Elliptic Curve Digital Signature Algorithm** is used by Bitcoin, Ethereum, and many other chains.

- Curve: secp256k1 (`y^2 = x^3 + 7` over a finite field).
- Output: a pair `(r, s)` plus a recovery bit that lets the public key be reconstructed from a signature.
- Properties: ~65-72 bytes per signature; historical and very widely deployed.
- Known weakness: **nonce reuse** (reusing `k`) leaks the private key — clients must use deterministic nonces (RFC 6979).

## EdDSA / Ed25519

The **Edwards-curve Digital Signature Algorithm** is a modern alternative used by Solana, Cardano, Stellar, and newer protocols (and Ed448/Schnorr variants).

- Curve: Ed25519 (`x^2 + y^2 = 1 + d*x^2*y^2` over a prime field).
- Deterministic nonces by design, single-pass verification, small and fast signatures.
- No recovery bit in the base scheme (variant Ed25519ph / aggregation extend it).

## In practice

- Transactions are signed with the sender's private key and verified with their public key on-chain.
- Signature schemes matter for wallet compatibility and aggregated signatures (BLS) in PoS networks.

See [Hash functions]({{ 'theory/cryptography/hash-functions' | relative_url }}) and [Address derivation]({{ 'theory/cryptography/addresses' | relative_url }}).