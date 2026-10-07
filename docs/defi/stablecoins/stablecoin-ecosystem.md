---
layout: default
title: Stablecoin ecosystem
parent: Stablecoins
grand_parent: Tools
---

# Stablecoin ecosystem

Stablecoins do not exist in isolation — they power lending, liquidity provision, and DeFi yields. This page covers the on-chain infrastructure around them.

## Lending protocols

- **Aave / Compound** — let users deposit stablecoins and borrow against them, or lend for yield.
- **Curve pools** — provide deep stablecoin liquidity with minimal slippage (see [Curve]({{ 'defi/dex/curve' | relative_url }})).
- **Lido/mStable-style vaults** — yield-bearing wrappers on top of stable positions.

## Yield sources

- **DAI Savings Rate (DSR)** — earn on DAI via Maker's savings module.
- **Protocol yield** — Curve gauge emissions, Convex pools, and LP rewards.
- **Real-world assets (RWAs)** — tokenized treasuries increasingly back some stablecoins/usdc-like products.

## Risk considerations

- **De-pegging** — fiat-backed stablecoins can deviate from 1:1 during stress (reserve doubts, market panics); DAI can be subject to collateral volatility.
- **Collateral quality** — fiat-backed rely on issuer solvency; crypto-backed rely on collateralization ratios.
- **Smart-contract risk** — pools and vaults are code and can be exploited.
- **Regulatory risk** — stablecoin issuers increasingly face licensing (e.g. MiCA in the EU).

## Engineering perspective

When building, treat stablecoin assumptions conservatively: monitor de-pegs, prefer audited/insured pools, and test integration on testnets. See [Smart-contract development]({{ 'dev-tools' | relative_url }}) and [Security]({{ 'guides/backup-security' | relative_url }}).