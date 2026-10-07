---
layout: default
title: ColdCard
parent: Hardware wallets
grand_parent: Tools
---

# ColdCard

**ColdCard** (by Coinkite) is a hardware wallet focused almost exclusively on Bitcoin, built around maximal security and **air-gapped** operation. It is a favorite among privacy-conscious Bitcoin users and power users.

## What it is

- A Bitcoin-only hardware wallet with a strong emphasis on offline (air-gapped) signing.
- **Open-source firmware** and open hardware design.
- Operates via buttons and a small display; supports **PSBT** (Partially Signed Bitcoin Transactions) for offline signing.

## Key features

- **Air-gapped operation** — sign on the device with QR codes or microSD; no USB signing required if you prefer.
- **Secure boot / secure element** and verified firmware.
- **BIP-39**, passphrases, and multi-sig (PSBT/Descriptor wallets) support.
- **ColdCard Mk4** current model; supports both USB-C and legacy microSD workflows.
- Rust-based firmware, reproducible builds.

## Resources

- Official site: https://coldcard.com
- Docs: https://coldcard.com/docs/
- GitHub: https://github.com/Coldcard  (firmware) / https://github.com/Coldcard/firmware

See [Backup and key security]({{ 'guides/backup-security' | relative_url }}).