---
layout: default
title: Rocket Pool
parent: Staking
grand_parent: Tools
---

# Rocket Pool

**Rocket Pool** is a **decentralized** liquid-staking protocol for Ethereum designed to lower the barrier to solo staking. Users can stake with as little as any amount of ETH and receive **rETH**, but the network is operated by permissionless node operators who put up 8 ETH each plus collateral.

## What it is

- A **liquid-staking** protocol emphasizing permissionless decentralization.
- **Open-source** smart contracts (GPL) — a community/governance DAO.
- **RPL** — the collateral and governance token.

## How it works

1. ETH is pooled and allocated to **node operators** who run validators (they stake 8 ETH + RPL collateral per validator; the remaining 24 ETH comes from the pool).
2. In exchange for ecosystem ETH, users receive **rETH**, a liquid token that grows in value as rewards accrue.
3. Because operators are permissionless, anyone with hardware can run infra and earn — unlike Lido's curated set.

## Key features

- **rETH** — non-rebasing, transferable liquid token representing ETH plus accrued rewards.
- **Permissionless node operation** — strong decentralization stance.
- **Smoothing pools and minipools** — options for operators of different deposit sizes.
- **Low minimums for stakers** — start with a small ETH amount.

## Trade-offs

- **Market liquidity for rETH** is thinner than stETH.
- **Token price discovery** — rETH trades at a variable premium/discount to DAR (deposited ETH).

## Resources

- Official site: https://rocketpool.net
- Docs: https://docs.rocketpool.net
- GitHub: https://github.com/rocket-pool

See [Lido]({{ 'staking-mining/staking/lido' | relative_url }}) and [Liquid staking derivatives]({{ 'staking-mining/staking/lsd' | relative_url }}).