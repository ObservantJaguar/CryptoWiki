---

---

# Public-key cryptography

Public-key (asymmetric) cryptography uses a **key pair**: a private key that must be kept secret and a public key that can be shared. Blockchains use these pairs for ownership: possession of the private key authorizes spending or executing operations tied to the address.

## Key pair

- **Private key** — a random secret (usually 256 bits). Anyone holding it controls the associated funds/identity.
- **Public key** — derived from the private key via elliptic-curve multiplication (one-way: public does not reveal private).
- **Controlled by** — the user; no trusted third party is required to prove ownership.

## What it enables

- **Signing** — the private key signs transactions; the public key verifies the signature.
- **Addresses** — a hashed form of the public key becomes the on-chain address.
- **Encryption (less common on-chain)** — used in some protocols and communication layers.

## Security implications

- **Secrecy** — loss or theft of the private key means irreversible loss of the associated assets.
- **No recovery** — there is no central authority to reset or recover a private key; that is why [wallet backups]({{ 'theory/wallets-keys' | relative_url }}) matter.

See [Signatures]({{ 'theory/cryptography/signatures' | relative_url }}) and [Hash functions]({{ 'theory/cryptography/hash-functions' | relative_url }}).