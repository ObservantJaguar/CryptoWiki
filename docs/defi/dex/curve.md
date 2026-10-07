---
layout: default
title: Curve Finance
parent: DEX and AMM
grand_parent: Tools
---

# Curve Finance

**Curve Finance** is a decentralized exchange optimized for trading **stablecoins** and other pegged assets. Its **Stableswap** invariant keeps slippage extremely low between assets of similar value, making it the preferred venue for stablecoin swaps and large institutional flows.

## How it works

- **Stableswap invariant** — a hybrid between constant-sum and constant-product that keeps prices near 1:1 for pegged assets.
- Pools hold multiple pegged assets (e.g. DAI, USDC, USDT).
- **Curve V2 / new pools** — adapt the invariant for slightly correlated (non-stable) pairs.

## Protocol details

- **Open-source** contracts.
- **CRV** — governance token; **veCRV** gauge weights direct emissions to pools.
- Deep liquidity in major stablecoin pairs; powering many yield farms.

## Key features

- **Low slippage** for pegged-asset swaps.
- **Liquidity pools** earning trading fees + CRV emissions.
- **Convex and Curve ecosystem** — yield aggregators built on Curve pools.
- Reliable deep liquidity relied on by aggregators (e.g. 1inch).

## Resources

- Official site: https://curve.fi
- Docs: https://curve.readthedocs.io
- GitHub: https://github.com/curvefi

See how aggregators route through Curve in [Aggregation and routing]({{ 'defi/aggregation' | relative_url }}).