---

---

# Mnemonic phrases (BIP-39)

A **mnemonic phrase** (seed phrase, recovery phrase) is a human-readable sequence of words that encodes the entropy from which all wallet keys are derived. It is defined by **BIP-39** and is the standard backup format for most self-custody wallets.

## Structure

- A fixed wordlist of **2048 common English words**.
- Usually **12, 15, 18, 21, or 24 words** — the count encodes entropy (128, 160, 192, 224, or 256 bits).
- The last word carries a **checksum** so typos can be detected.

## Generation and use

1. Generate `ENT` bits of random entropy (e.g. 128 bits for 12 words).
2. Append a checksum of `ENT/32` bits (from SHA-256 of the entropy).
3. Split the bit string into 11-bit groups; each maps to a word in the wordlist.
4. The phrase seeds a BIP-32 master key (see [HD wallets]({{ 'theory/wallets-keys/hd-wallets' | relative_url }})).

## Security guidance

- **Write it down offline** and keep multiple physical copies.
- Never store it in plaintext in cloud notes, email, or screenshots.
- Any holder of the phrase controls all derived accounts.
- An optional **passphrase** (BIP-39 "25th word") adds protection but is not part of the phrase.

See [Backup and key security]({{ 'guides/backup-security' | relative_url }}) for full guidance.