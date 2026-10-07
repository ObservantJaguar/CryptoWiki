---
layout: default
title: Hosted node APIs
parent: Node APIs and indexers
grand_parent: Tools
---

# Hosted node APIs

Hosted node providers (Infura, Alchemy, QuickNode) offer managed, production-grade access to Ethereum and other chains over JSON-RPC — letting dApps call `eth_*` endpoints and use webhooks without running or maintaining full nodes.

## What they are

- Managed infrastructure: JSON-RPC endpoints, WebSockets, higher-level APIs, and analytics.
- **Commercial SaaS** — free tiers + paid plans; these are **proprietary** services (you trust the provider), unlike running your own node.
- Important for scaling dApps that cannot afford node ops.

## The main providers

- **Alchemy** — JSON-RPC, webhooks, NFT APIs, and a large developer platform. https://www.alchemy.com
- **Infura** — long-running Ethereum/IPFS/Filecoin gateway provider by ConsenSys. https://www.infura.io
- **QuickNode** — high-performance multi-chain endpoints with add-ons (history, tracing, token APIs). https://www.quicknode.com

## Key features

- **JSON-RPC/WebSockets** for standard `eth_*` calls.
- **Analytics** dashboards for request volume and errors.
- **Enhanced APIs** — mempool, token balances, NFT metadata, ENS (provider-specific).
- **Webhooks** — event-driven subscriptions (Alchemy/QuickNode).
- Elastic scaling for high-traffic dApps.

## Trade-offs

- **Trust & decentralization** — these are centralized; a node provider outage or policy can affect your app.
- **Downtime** — outages have historically hit dApps relying on a single provider.
- **Mitigation** — use multiple providers or run your own node as the base layer for critical paths. See [Node software]({{ 'nodes' | relative_url }}).

## Resources

- Alchemy docs: https://docs.alchemy.com
- Infura docs: https://docs.infura.io
- QuickNode docs: https://www.quicknode.com/docs