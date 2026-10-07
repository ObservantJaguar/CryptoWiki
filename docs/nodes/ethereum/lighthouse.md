---
layout: default
title: Lighthouse (consensus client)
parent: Ethereum node software
grand_parent: Tools
---

# Lighthouse (consensus client)

**Lighthouse** is a Rust implementation of the Ethereum **consensus layer** (beacon chain), developed by Sigma Prime. It is one of the most widely used consensus clients and popular for validators, offering excellent performance and good tooling.

## What it is

- A beacon client that tracks the beacon chain, produces/attests blocks (via a validator client), and drives finality.
- **Open-source** (Apache-2.0) — Sigma Prime.
- Runs alongside an execution client (Geth/Nethermind/Erigon) via the Engine API.

## Key features

- **High performance and low resource use** — a common choice for large validator sets.
- **Validator client** — manages keys, proposes/attests, and handles duties with a built-in slashing protection database.
- **TLS-encrypted HTTP beacon API** + rich metrics (Prometheus).
- **Clean, well-documented** config and many testnet/mainnet aids.
- Supports **distributed validator technology (DVT)** integrations.

## Resources

- Official site: https://lighthouse.sigmaprime.io
- GitHub: https://github.com/sigp/lighthouse
- Book: https://lighthouse-book.sigmaprime.io/

See [Guide: Setting up a PoS validator]({{ 'guides/pos-validator' | relative_url }}).