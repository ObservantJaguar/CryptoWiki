---

---

# Guide: Wallet backup and key security

Securing your keys is the single most important task in self-custody. This guide covers backup strategies, threat models, and operational best practices.

## Core principle

**Your seed phrase (or private key) IS the money.** Anyone who obtains it can take everything. Back it up rigorously and treat it like the highest-value secret you own.

## 1. Build a solid backup

- **Write the seed on paper** (multiple copies) and store in fireproof/waterproof, physically separate locations (e.g. safe + bank deposit box).
- **Do not** store the seed in plaintext on a phone, laptop, or cloud (screenshots, notes apps, email).
- Optionally use a **steel backup** (engraved metal tiles) for disaster durability.
- Split the seed across locations if desired (e.g. Shamir, or a passphrase) for defense in depth.

## 2. Use the BIP-39 passphrase

- A passphrase ("25th word") changes the derived keys from the same mnemonic.
- It protects against a stolen seed backup — but if forgotten, funds are lost, so back it up separately.

## 3. Practice key hygiene

- **Never** enter your seed into a website, "verification" tool, or support chat.
- Be wary of **phishing** — double-check URLs and app sources.
- Use a dedicated **hardware wallet** for significant value; keep hot wallets for small, everyday balances.
- Keep software wallets and browser extensions updated.

## 4. Isolate and diversify

- Separate "cold" (long-term) from "hot" (active) balances.
- For organizations: multi-sig (e.g. 2-of-3) and hardware security modules reduce single points of failure.
- Consider a **dummy "burner" wallet** with tiny funds for risky interactions.

## 5. Recovery testing

- **Test your restore** — from the seed alone (on a fresh device), confirm you can reproduce your addresses.
- Do this before entrusting real funds, and repeat after major changes.

## 6. Threat model quick reference

| Threat | Mitigation |
|---|---|
| Stolen seed backup | Passphrase, split storage, hardware wallet |
| Malware / phishing | Hardware wallet, seed hygiene, cold storage |
| Lost device / disaster | Multiple physical backups, steel plate |
| Human error | Test restores, checklists |
| Social engineering | Never share seed, verify identity |

## 7. If something goes wrong

- If you suspect a seed/phrase leak, **move funds immediately** to a new key created on a clean device.
- There is no support that can recover keys; only prevention and backups protect you.

## Related

- [Creating a wallet and managing keys]({{ 'guides/wallet-keys' | relative_url }})
- [Wallets and keys (theory)]({{ 'theory/wallets-keys' | relative_url }})
- [Hardware wallets]({{ 'wallets/hardware' | relative_url }})