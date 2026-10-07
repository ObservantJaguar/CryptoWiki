---

---

# Hash functions (SHA-256, Keccak, RIPEMD-160)

Cryptographic hash functions are the workhorses of blockchain construction. They bind block data, derive addresses, and provide the commitments that make chains tamper-evident. The general role is covered in [Hashing]({{ 'theory/fundamentals/hashing' | relative_url }}).

## SHA-256

- The **Secure Hash Algorithm 256-bit** from the SHA-2 family (NIST).
- Produces a 256-bit digest.
- Used by **Bitcoin** for block hashing and transaction IDs (`double-SHA256`), and widely across many chains.

## SHA-3 / Keccak

- **Keccak** is the original sponge-based function; **SHA-3** is the NIST-standardized variant (with different padding).
- Produces configurable digest sizes; Ethereum uses **Keccak-256**.
- Used by **Ethereum** for KECCAK256 hashing of transaction data, storage, and as the hashing of addresses and Merkle structures.

> Note: Ethereum's `keccak256` is the original Keccak, not the NIST SHA-3 padding variant. Tooling that claims "SHA-3" frequently implements Keccak — check the precise variant.

## RIPEMD-160

- A 160-bit hash from the RIPEMD family.
- Used by **Bitcoin** in the Base58Check address derivation (`HASH160 = RIPEMD160(SHA256(pubkey))`).
- Legacy origin: designed in 1996 as a European alternative to the SHA family.

## Layering

Ethereum/Bitcoin derive addresses by composing hashes:

- Bitcoin: `address = RIPEMD160(SHA256(public_key))`.
- Ethereum: `address = last 20 bytes of Keccak256(public_key)`.

See [Address derivation]({{ 'theory/cryptography/addresses' | relative_url }}).