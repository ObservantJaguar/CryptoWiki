---

---

# Address derivation

An **address** is a short, network-specific identifier that others use to send funds or interact with a contract. It is derived deterministically from the public key, which in turn derives from the private key.

## Bitcoin

1. `public_key` (uncompressed/compressed 33-65 bytes).
2. `HASH160 = RIPEMD160( SHA256(public_key) )` — 20 bytes.
3. Encode with Base58Check (or Bech32 for SegWit), adding a version byte and a 4-byte checksum.

Result examples: legacy `1...`, SegWit-v0 `bc1...` (Bech32).

## Ethereum

1. `public_key` as a 64-byte uncompressed point.
2. `keccak256(public_key)` — take the **last 20 bytes**.
3. Optionally checksummed with EIP-55 mixed-case capitalization.

Result example: `0x8Ba1fDa...`.

## Key takeaways

- **Derivation is one-way** — you cannot go from address back to keys.
- **Different standards for the same key** — the same private key produces different addresses per network convention.
- **With the private key, addresses can always be re-derived** — which is why backing up keys (see [Wallets and keys]({{ 'theory/wallets-keys' | relative_url }})) is the true source of ownership.