---
layout: default
title: Electrum
parent: Software wallets
grand_parent: Tools
---

# Electrum

**Electrum** is a lightweight, fast, and battle-tested Bitcoin wallet first released in 2011. It does not download the whole blockchain — it synchronizes with servers holding the chain while keeping private keys on the user's device.

## What it is

- A **lightweight Bitcoin hot wallet** where keys stay local (client-side).
- **Open-source** (MIT) — one of the oldest and most audited Bitcoin wallets.
- Works on desktop (Windows/macOS/Linux) and mobile (Android).

## Key features

- **SPV security model** — clients verify block headers and transactions against servers without full sync.
- **Two-factor and multisig** (PSBT/descriptors) support.
- **Cold storage integration** — designed to pair with hardware wallets and air-gapped signing.
- **Electrum protocol** for server communication and plugins (including for advanced users).
- Deterministic keys (BIP-32/44) with seed backup.

## Security notes

Choose your server carefully and treat the seed as precious. Electrum's offline/cold-signing modes are a strong reason power users choose it.

## Resources

- Official site: https://electrum.org
- GitHub: https://github.com/spesmilo/electrum
- Docs: https://electrum.readthedocs.io/

See [Backup and key security]({{ 'guides/backup-security' | relative_url }}).