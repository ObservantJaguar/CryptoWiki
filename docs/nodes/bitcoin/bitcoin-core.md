---
layout: default
title: Bitcoin Core
parent: Bitcoin node software
grand_parent: Tools
---

# Bitcoin Core

**Bitcoin Core** is the reference and most widely used full node for the Bitcoin network. Running it (`bitcoind` daemon, `bitcoin-qt` GUI) validates the entire blockchain, relays transactions, and provides an RPC interface for wallet and chain operations.

## What it is

- A full-featured **SPV-to-full node** implementation combining the P2P network, validation, mempool, wallet, and RPC server in one daemon.
- **Open-source** (MIT-style) — the canonical specification of Bitcoin's rules.
- Available on Windows, macOS, and Linux; a large portion of the Bitcoin hash power and full-node count run Bitcoin Core.

## Key features

- **Full validation** — independently verifies every block and transaction since genesis.
- **RPC interface** — JSON-RPC over HTTP (and a CLI) for wallet, chain, and mempool APIs.
- **Wallet module** — optional built-in BIP-32 wallet with seed and address management.
- **Mining interface** — `miner` RPC (`getblocktemplate`) to connect to mining software.
- **Indexers** — optional txindex/coinstatsindex for faster queries.

## Resources

- Official site: https://bitcoincore.org
- GitHub: https://github.com/bitcoin/bitcoin
- Documentation: https://bitcoin.org/en/bitcoin-core/

See [Guide: Running a full Bitcoin node]({{ 'guides/bitcoin-node' | relative_url }}) for setup.