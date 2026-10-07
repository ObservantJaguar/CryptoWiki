---
layout: default
title: Ethereum explorers
parent: Block explorers
grand_parent: Tools
---

# Ethereum explorers

Web services for exploring the Ethereum blockchain and EVM-compatible chains — block/transaction data, token balances, contract verification, and gas metrics.

## Etherscan

- The canonical Ethereum block explorer (and its family: BscScan, PolygonScan, FTMScan, etc. for other EVM chains).
- Features: blocks and transactions, ERC-20/721 tracking, gas tracker, contract source verification, and a public API.
- **Vastly used**; proprietary service with freely accessible read endpoints.
- https://etherscan.io / https://docs.etherscan.io (API)

## Blockchair

- Multi-chain explorer with unified data and API across Bitcoin, Ethereum, and others.
- https://blockchair.com / https://blockchair.com/api

## Etherscan alternatives (self-hosted / open)

- **Otterscan** — an open-source explorer targeting the Erigon node. https://otterscan.io
- **Blockscout** — an open-source, multi-chain EVM explorer that many networks self-host; can run against your own node. https://www.blockscout.com / https://github.com/blockscout/blockscout

## Choosing

For EVM chains, Etherscan is the compatibility standard and most dApps link to it. For self-hosted/private or trustless environments, Blockscout or Otterscan integrate directly with a node you control.