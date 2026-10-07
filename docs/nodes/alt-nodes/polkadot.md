---
layout: default
title: Polkadot
parent: Alternative network nodes
grand_parent: Tools
---

# Polkadot

Polkadot is a heterogeneous **parachain network** built on Substrate. It operates a relay chain secured by validators, with multiple parachains running their own executions. The node software is based on the **Substrate** framework.

## Node software

- **polkadot** — the full node for the Polkadot relay chain.
- **kton** (or `polkadot-parachain`) — full node for parachains.
- **cargo/rust toolchain** — Substrate nodes are Rust and built/run via `cargo`.
- Reference: https://wiki.polkadot.network and https://github.com/paritytech/polkadot

## Key concepts

- **NPoS (Nominated Proof of Stake)** — nominators back validators; minimal staking requirements.
- **Parachains** — individual chains connected via the relay chain and XCM messages.
- **Roles** — validators, collators (parachain block producers), fishermen/verifiers.
- **Substrate** — the modular framework shared across many chains in the ecosystem.

## Running a node

A relay/parachain node can be compiled from source or run as a packaged binary. Hardware requirements are moderate. See [Guide: Setting up a PoS validator]({{ 'guides/pos-validator' | relative_url }}) for the general validator workflow.