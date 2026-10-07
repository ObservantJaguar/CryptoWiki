---

---

# Hierarchical derivation (BIP-32/44)

**Hierarchical Deterministic (HD) wallets** derive an entire tree of private/public keys from a single master seed, so one backup (the [mnemonic]({{ 'theory/wallets-keys/mnemonics' | relative_url }})) protects every address the wallet will ever use.

## BIP-32

- Defines a **master key** from the BIP-39 seed via HMAC-SHA512.
- Child keys are derived deterministically from a parent key plus an index and a **chain code**.
- **Hardened** (`H`) derivation (index >= 2^31) prevents a leaked child key from revealing its siblings; non-hardened allows public-key-only derivation.
- Path notation: `m / purpose' / coin' / account' / change / index`.

## BIP-44 (multi-account)

- Standardizes the path layout so wallets interoperate:

```
m / 44' / coin_type' / account' / change / index
```

- `coin_type` separates networks (0' = Bitcoin, 60' = Ethereum, 501' = Solana, ...).
- `change` = 0 for receive addresses, 1 for internal/change addresses.

## Why it matters

- **Single backup** — the seed phrase regenerates every address.
- **Per-address privacy** — a fresh address per transaction without managing separate keys.
- **Interoperability** — any BIP-32/44 wallet can read the same key tree.

See [Private and public keys]({{ 'theory/wallets-keys/keys' | relative_url }}) and [Mnemonics]({{ 'theory/wallets-keys/mnemonics' | relative_url }}).