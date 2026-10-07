---
layout: default
title: Nethermind
parent: Ethereum node software
grand_parent: Tools
---

# Nethermind

**Nethermind** is a fast, high-performance Ethereum **execution client** written in C#. It offers good sync speeds, memory efficiency, and rich debugging/diagnostics, making it a popular choice for validators and node operators.

## What it is

- A full-featured Ethereum execution-layer client for mainnet and testnets.
- **Open-source** (LGPL-3.0) — developed by Nethermind and grants.
- Also powers some layer-2 and rollup execution environments via its modularity.

## Key features

- **Fast sync** with a goal of low storage footprint and quick block import.
- **Full JSON-RPC** plus advanced `debug_*` tracing used by analysers (e.g. for MEV research).
- **Tracing and diagnostics** — rich `trace_*` RPC for transaction-level debugging.
- **Engine API** for consensus-client integration; health/metrics endpoints.
- **Built-in staking tooling** hints and validator diagnostics.

## Resources

- Official site: https://www.nethermind.io
- GitHub: https://github.com/NethermindEth/nethermind
- Docs: https://docs.nethermind.io/

See [Guide: Running an Ethereum node]({{ 'guides/ethereum-node' | relative_url }}).