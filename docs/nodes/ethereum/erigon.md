---
layout: default
title: Erigon
parent: Ethereum node software
grand_parent: Tools
---

# Erigon

**Erigon** is an Ethereum **execution client** focused on efficiency, low storage footprint, and extensibility. It forked from Geth with the goal of drastically reducing disk usage and sync time for full and archive nodes.

## What it is

- An execution-layer client for Ethereum mainnet and testnets.
- **Open-source** (LGPL-3.0) — developed by ErigonTech/Team Erigon.
- Requires significantly less storage than Geth, especially for archive data.

## Key features

- **Efficient storage model** — records state efficiently (Staged Sync, MDBX), reducing archive-node disk usage.
- **Fast sync** — staged synchronization importing blocks and state in batches.
- **Excellent for archive nodes** — historically the go-to client for RPC/archive use cases.
- **Rich RPC** including tracing (`trace_*`) and visibility into the state.
- **Modular sub-projects** — Erigon introduced components like Reth (Rust) and Erigon-style execution used by several rollups.

## Resources

- GitHub: https://github.com/erigontech/erigon
- Docs: https://erigon.gitbook.io/erigon/
- Community: https://t.me/erigon (external)

See [Guide: Running an Ethereum node]({{ 'guides/ethereum-node' | relative_url }}).