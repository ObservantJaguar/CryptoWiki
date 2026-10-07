---
layout: default
title: Uniswap
parent: DEX and AMM
grand_parent: Tools
---

# Uniswap

**Uniswap** is the pioneering decentralized exchange built on an **Automated Market Maker (AMM)** model. Its V2 constant-product formula and V3 concentrated liquidity have made it the largest DEX by volume on Ethereum and many EVM chains.

## How it works

- **V2** — pools with two reserves follow `x * y = k`; price is the ratio of reserves.
- **V3** — **concentrated liquidity** lets LPs provide liquidity within custom price ranges, improving capital efficiency; introduces tick-based mechanics.
- **V4 (in development)** — hooks system and singleton pools for customization.

## Protocol details

- **Open-source** smart contracts (GPL for V2/V3 core; BSL initially for V4, later open).
- **UNI** — the governance token; holders vote on protocol upgrades.
- Deployed to Ethereum and dozens of EVM L1s/L2s (Polygon, Arbitrum, Optimism, etc.).
- **Uniswap Labs** — the interface; the protocol itself is governed by community.

## Key features

- Permissionless creation of pools and seamless token swaps.
- Extremely deep liquidity in major pairs; reliable oracles via V2 TWAP.
- Audited, battle-tested contracts (with past v1/v2 audits).

## Resources

- Official site: https://uniswap.org
- Docs: https://docs.uniswap.org
- GitHub: https://github.com/Uniswap

Read about the liquidity-pool economics in [stablecoins and liquidity]({{ 'defi/stablecoins' | relative_url }}).