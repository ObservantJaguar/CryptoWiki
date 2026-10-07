---

---

# Hashing

A **cryptographic hash function** maps an arbitrary-length input to a fixed-length digest with properties that make it central to blockchain design.

## Required properties

- **Deterministic** — the same input always yields the same digest.
- **Quick to compute** — the digest is cheap to produce.
- **Preimage resistance** — given a digest, it is infeasible to find any input producing it.
- **Second-preimage resistance** — given an input, it is infeasible to find a different input with the same digest.
- **Collision resistance** — it is infeasible to find any two distinct inputs with the same digest.
- **Avalanche effect** — a tiny change in the input produces an unrecognizably different digest.

## Role in blockchains

- **Block identifiers** — each block's hash serves as its unique ID and as the link in the chain.
- **Commitments** — a Merkle root (see [Merkle trees]({{ 'theory/fundamentals/merkle-trees' | relative_url }})) is a single hash committing to many transactions.
- **Address/type conversions** — e.g. SHA-256 and RIPEMD-160 are layered to derive Bitcoin addresses from public keys.
- **Difficulty and mining** — in proof-of-work, a block is valid only if its hash falls below a target, which drives the difficulty mechanism.

Common blockchain hash functions are discussed in the [cryptography domain]({{ 'theory/cryptography' | relative_url }}).