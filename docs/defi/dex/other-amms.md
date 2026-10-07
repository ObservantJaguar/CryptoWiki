---
layout: default
title: Other AMMs
parent: DEX and AMM
grand_parent: Tools
---

# Other AMMs

Beyond Uniswap and Curve, the AMM ecosystem includes weighted, multi-asset, and chain-native variants. Each adapts the core pooling idea for different use cases.

## Balancer

- **Weighted pools** — allow arbitrary weights and up to 8 assets in one pool.
- Enables custom portfolio construction and index-like pools.
- V2 introduced programmable pool architecture (Composable Stable Pools, Boosted Pools).
- **BAL** governance token. https://balancer.fi / https://github.com/balancer/balancer-v2-monorepo

## PancakeSwap

- AMM DEX on BNB Smart Chain (and other EVM chains), forks Uniswap V2/V3 with added features (farms, lotteries, prediction markets).
- **CAKE** token; very high volume on BSC. https://pancakeswap.finance

## SushiSwap

- Forked from Uniswap V2 with revenue-redistribution features and a multi-chain presence.
- **SUSHI** token; known for its "chef" farm contracts. https://www.sushi.com

## Kyberswap (Kyber Network)

- Aggregates liquidity across AMMs (KyberSwap Elastic + Classic) on multiple chains.
- **KNC** token. https://kyberswap.com

## How to pick

Choose based on asset type (stablecoins → Curve; general pairs → Uniswap-like; weighted/multi-asset → Balancer), chain usage, and liquidity depth. Aggregators (see [Aggregation]({{ 'defi/aggregation' | relative_url }})) automatically route to the best venue.