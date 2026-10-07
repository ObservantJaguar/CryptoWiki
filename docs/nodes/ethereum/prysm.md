---
layout: default
title: Prysm (consensus client)
parent: Ethereum node software
grand_parent: Tools
---

# Prysm (consensus client)

**Prysm** is a Go implementation of the Ethereum **consensus layer**, developed by Prysmatic Labs (part of Offchain Labs). It was among the first consensus clients to launch with the Beacon Chain and ships with an integrated validator client and a web UI.

## What it is

- A beacon node + validator client pair for the Ethereum PoS layer.
- **Open-source** (GPL-3.0) — Prysmatic Labs.
- Connects to an execution client through the Engine API to run a full PoS node.

## Key features

- **Single binary & CLI** — `beacon-chain` and `validator` commands with a shared config.
- **Built-in web UI** — a dashboard for node and validator health.
- **Validator client** — key management, duty scheduling, slashing protection.
- **Prometheus metrics** and RPC/HTTP beacon endpoints.
- Long production track record since the Beacon Chain genesis (2020).

## Resources

- Official site: https://docs.prylabs.network
- GitHub: https://github.com/prysmaticlabs/prysm
- Docs: https://docs.prylabs.network/docs/

See [Guide: Setting up a PoS validator]({{ 'guides/pos-validator' | relative_url }}).