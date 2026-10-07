---

---

# Private and public keys

The **private key** is the fundamental secret that controls a blockchain identity and its funds. Everything else — public key, addresses, signatures — derives from it.

## Private key

- A random 256-bit integer (for secp256k1 networks), usually encoded in hex or WIF (Base58).
- **Must be kept secret.** Anyone holding it can sign transactions and spend all assets it controls.
- Cannot be recovered if lost — there is no reset mechanism on-chain.

## Public key

- Derived from the private key by elliptic-curve point multiplication: `pub = priv * G` (where G is the curve generator).
- One-way: recovering the private key from the public key is computationally infeasible.
- Not secret; used for verification and address derivation.

## Relationship to spending

```
private key  --(multiplication)-->  public key  --(hash)-->  address
    (secret)                              (shared)              (identifier)
                     signing                          verification
```

To spend, a wallet signs with the private key; the network verifies against the public key and checks the address.

## Practical notes

- **Backup the private key or its seed** — see [Mnemonics (BIP-39)]({{ 'theory/wallets-keys/mnemonics' | relative_url }}).
- Never paste a private key into web forms or chat; treat it as highly sensitive.
- Keys paired with [HD wallets]({{ 'theory/wallets-keys/hd-wallets' | relative_url }}) are derived from a single seed, so backing up the seed backs up all keys.