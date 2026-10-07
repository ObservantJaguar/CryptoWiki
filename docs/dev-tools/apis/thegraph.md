---
layout: default
title: The Graph
parent: Node APIs and indexers
grand_parent: Tools
---

# The Graph

**The Graph** is a decentralized indexing protocol for blockchain data. It lets developers define *subgraphs* that continuously index specific events and data, then query them through a fast GraphQL API — without operating their own indexing infrastructure.

## What it is

- A network of indexers, curators, and delegators serving indexed blockchain data.
- **Open-source** protocol and tooling.
- The **GRT** token powers the marketplace (indexers stake to serve queries).

## How it works

1. A developer defines a **subgraph** manifest (mappings from chain events to entities) in YAML + AssemblyScript or TypeScript.
2. Indexers process it and serve the subgraph's GraphQL endpoint.
3. Applications query the subgraph endpoint instead of raw chain data.

## Key features

- **GraphQL API** — ergonomic, typed queries over indexed entities.
- **Subgraph Studio** — deploy and manage subgraphs; The Graph Explorer for browsing.
- **Decentralized and open** — no single provider controls the data.
- **Hosted and decentralized networks** — transitions toward the decentralized network on Arbitrum.

## Resources

- Official site: https://thegraph.com
- Docs: https://thegraph.com/docs
- GitHub: https://github.com/graphprotocol/graph-node

Compare with centralized [hosted node APIs]({{ 'dev-tools/apis/hosted-apis' | relative_url }}).