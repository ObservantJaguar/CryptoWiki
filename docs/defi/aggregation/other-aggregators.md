---
layout: default
title: Other aggregators
parent: Aggregation and routing
grand_parent: Tools
---

# Other aggregators

Beyond 1inch and Paraswap, other routers and on-chain order protocols extend the aggregation space.

## Odos

- An aggregator emphasizing ultra-low slippage and gas-efficient routing.
- Routes across many EVM chains; unique "multi-hop" optimization.
- https://odos.xyz / https://docs.odos.xyz

## 0x Protocol

- An open protocol for decentralized exchange that also powers aggregator-style routing.
- **Open-source** (Apache-2.0) settlement layer; No protocol fees on the exchange.
- Powers 0x API used by many wallets and dApps.
- https://0x.org / https://github.com/0xProject

## KyberSwap

- Aggregates liquidity across Kyber's own pools and external DEXes on multiple chains.
- https://kyberswap.com

## Matching / intent protocols (emerging)

- **CoW Protocol** — an intent-based/trading "virtual order book" that batch-matches orders to reduce MEV. https://cow.fi
- **Uniswap X** — intent-based RFQ settlement for Uniswap. https://blog.uniswap.org

## Choosing

For most users, a leading aggregator (1inch/Paraswap) provides the best default execution. Intent-based protocols (CoW, Uniswap X) further reduce MEV and improve price for some trade types.