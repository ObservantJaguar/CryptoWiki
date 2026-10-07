---
layout: default
title: Teku (consensus client)
parent: Ethereum node software
grand_parent: Tools
---

# Teku (consensus client)

**Teku** is a Java implementation of the Ethereum **consensus layer**, developed by the ConsenSys teams. It is designed for enterprise-grade validity and compliance features.

## What it is

- A beacon chain client and validator client for Ethereum PoS.
- **Open-source** (Apache-2.0) — ConsenSys.
- Pairs with any execution client via the Engine API.

## Key features

- **Java/JVM portability** — runs on Windows, macOS, Linux; containers available.
- **Security and compliance** — rigorous focus on reporting and key handling for regulated operators.
- **Standard beacon API** and good metrics support.
- Built-in **validator client** with slashing protection.
- Frequently chosen by institutional stakers because of its audit-friendly design.

## Resources

- Official site: https://docs.teku.consensys.net
- GitHub: https://github.com/Consensys/teku
- Docs: https://docs.teku.consensys.net/

See [Guide: Setting up a PoS validator]({{ 'guides/pos-validator' | relative_url }}).