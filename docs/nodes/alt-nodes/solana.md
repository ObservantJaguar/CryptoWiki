---
layout: default
title: Solana
parent: Alternative network nodes
grand_parent: Tools
---

# Solana

Solana is a high-throughput, proof-of-stake blockchain known for its **Proof of History (PoH)** clock and single-client implementation. Node operators run either a **validator** (consensus-producing) or an **RPC node** (serving clients).

## Node software

- **solana-validator** — the core binary for running a validator or RPC node.
- **agave-validator** — the community-maintained (fork) successor used in current mainnet.
- **Jito client** — an alternative validator with MEV/block-engine capabilities.
- Reference docs: https://docs.anza.xyz (Anza maintains Agave) and https://solana.com/developers

## Key concepts

- **Proof of History** — a verifiable time-ordering mechanism that reduces consensus messaging overhead.
- **Leader schedule** — validators are assigned blocks in a rotating schedule.
- **Stake-weighted consensus** — validators vote with stake; rewards and slashing apply.

## Requirements

High TPS demands relatively powerful hardware and low-latency networking; validators typically run on dedicated servers with NVMe storage. See [Guide: Setting up a PoS validator]({{ 'guides/pos-validator' | relative_url }}) for the general pattern; Solana specifics vary by client.