---
layout: default
title: Nimbus (consensus client)
parent: Ethereum node software
grand_parent: Tools
---

# Nimbus (consensus client)

**Nimbus** is a Nim implementation of the Ethereum **consensus layer**, developed by the Status research team. It is engineered for low resource usage, making it a popular choice for validators on lightweight or constrained hardware (including Raspberry Pi).

## What it is

- A beacon client and validator client for Ethereum PoS.
- **Open-source** (Apache-2.0 / MIT, dual) — Status.
- Connects to an execution client through the Engine API.

## Key features

- **Minimal memory footprint** — designed to run comfortably on small devices.
- **Fast sync** and low bandwidth use.
- **Built-in validator client** with slashing protection.
- **Metrics and logging** suitable for embedded deployment.
- Actively maintained and upgraded through the PoS roadmap.

## Resources

- GitHub: https://github.com/status-im/nimbus-eth2
- Docs: https://nimbus.guide/
- Status project: https://status.app (project site)

See [Guide: Setting up a PoS validator]({{ 'guides/pos-validator' | relative_url }}).