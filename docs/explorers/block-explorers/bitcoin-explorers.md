---
layout: default
title: Bitcoin explorers
parent: Block explorers
grand_parent: Tools
---

# Bitcoin explorers

Web services for exploring the Bitcoin blockchain — viewing blocks, transactions, addresses, mempool, and miner activity.

## Blockstream.info

- Block explorer for Bitcoin (and Liquid) by Blockstream. **Open-source** (MIT), runs on self-hosted infrastructure but can also be self-hosted.
- Features: transaction view, mempool page, historical charts, raw data, and an API.
- https://blockstream.info / https://github.com/Blockstream/esplora

## mempool.space

- Community-run, open-source Bitcoin explorer emphasizing the mempool and fee estimation.
- **Open-source** (MIT).
- Features: live mempool visualization, fee rates, block data, and a full API for programmatic access.
- https://mempool.space / https://github.com/mempool/mempool

## Blockchair

- Multi-chain explorer (Bitcoin, Ethereum, and more) with a unified API and many advanced filters.
- **Free with limits**, partly open tools; not fully open-source.
- https://blockchair.com / https://blockchair.com/api

## Choosing

All explorers read the same public data; differences are in UX, mempool focus, and API. For programmatic use, mempool.space and Blockstream offer well-documented public APIs. For trustless data, run your own node (see [Bitcoin Core]({{ 'nodes/bitcoin/bitcoin-core' | relative_url }})).