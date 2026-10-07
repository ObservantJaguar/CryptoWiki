---
layout: default
title: MetaMask
parent: Software wallets
grand_parent: Tools
---

# MetaMask

**MetaMask** is a software wallet available as a browser extension and mobile app, most commonly used for Ethereum and any EVM-compatible chain. It manages accounts, signs transactions, and connects dApps via the wallet standard.

## What it is

- A hot/software wallet storing keys locally in the browser's encrypted storage (or mobile secure enclave).
- **Open-source** — the core client is MIT-licensed; proprietary elements exist around certain services.
- Standard choice for interacting with DeFi, NFTs, and web3 dApps.

## Key features

- **Multi-chain EVM** — Ethereum, Polygon, BSC, Arbitrum, Optimism, and custom RPC networks.
- **dApp connectivity** — injects `window.ethereum` for EIP-1193 compatibility.
- **Built-in swap** (MetaMask Swap) and fiat onramp/analytics.
- **Snaps** — a modular plugin system (MetaMask Snaps) extending features.
- **Ledger/Trezor hardware integration** via hardware wallets in the app.

## Security notes

As a hot wallet, MetaMask is exposed to phishing and malicious dApps. Use it with a dedicated low-balance account and cold storage for the bulk of funds. Never enter your seed into anything but the official app.

## Resources

- Official site: https://metamask.io
- Docs: https://docs.metamask.io
- GitHub: https://github.com/MetaMask

See [Backup and key security]({{ 'guides/backup-security' | relative_url }}).