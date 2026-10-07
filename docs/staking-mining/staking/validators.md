---
layout: default
title: Validators and clients
parent: Staking
grand_parent: Tools
---

# Validators and clients

To run a proof-of-stake validator you need **client software** that participates in consensus. On Ethereum, that means a consensus client (beacon chain) paired with an execution client.

## What a validator does

- **Proposes** blocks on a schedule.
- **Attests** (votes on) the correctness of proposed blocks.
- **Earns rewards** for participation; **gets slashed** for double-signing or equivocation.

## Ethereum consensus clients

- [Lighthouse]({{ 'nodes/ethereum/lighthouse' | relative_url }}) — Rust.
- [Prysm]({{ 'nodes/ethereum/prysm' | relative_url }}) — Go.
- [Teku]({{ 'nodes/ethereum/teku' | relative_url }}) — Java.
- [Nimbus]({{ 'nodes/ethereum/nimbus' | relative_url }}) — Nim.

Each pairs with an execution client ([Geth]({{ 'nodes/ethereum/geth' | relative_url }}), [Nethermind]({{ 'nodes/ethereum/nethermind' | relative_url }}), [Erigon]({{ 'nodes/ethereum/erigon' | relative_url }})) via the Engine API.

## Requirements

- **Hardware** — enough CPU/RAM for clients; NVMe storage recommended.
- **24/7 availability** — downtime loses rewards; prolonged downtime can lead to penalties.
- **Key management** — validator signing keys must be protected; slashing protection database prevents double-signing.

## Other networks

Solana, Polkadot, and Cardano validators use their own clients (see [Alternative network nodes]({{ 'nodes/alt-nodes' | relative_url }})).

See [Guide: Setting up a PoS validator]({{ 'guides/pos-validator' | relative_url }}) for a hands-on walkthrough.