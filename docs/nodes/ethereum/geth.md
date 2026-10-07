---
layout: default
title: Geth (Go Ethereum)
parent: Ethereum node software
grand_parent: Tools
---

# Geth (Go Ethereum)

**Geth** is the flagship execution client for Ethereum, written in Go. It is the most populous and commonly used client, capable of running a full node, an archive node, a miner (pre-merge), and exposing JSON-RPC for dApps and tooling.

## What it is

- The reference **execution layer (EL)** implementation for Ethereum mainnet and testnets.
- **Open-source** (LGPL-3.0) — developed by the Go Ethereum team.
- Handles transaction execution, state, mempool, and JSON-RPC serving.

## Key features

- **Fast and full sync modes** — snap, full, and historical archive.
- **JSON-RPC API** — `eth_*`, `net_*`, `web3_*`, `debug_*`, `txpool_*` endpoints.
- **Developer tooling** — a built-in JavaScript console and a Go testnet (`--dev`).
- **Engine API** — the EL side of the CL-EL interface (`engine_*`) used by consensus clients.
- **Light client** support via LES (deprecated) and experimental modes.

## Resources

- Official site: https://geth.ethereum.org
- GitHub: https://github.com/ethereum/go-ethereum
- Docs: https://geth.ethereum.org/docs/

See [Guide: Running an Ethereum node]({{ 'guides/ethereum-node' | relative_url }}).