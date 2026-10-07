---
layout: default
title: Lido
parent: Staking
grand_parent: Tools
---

# Lido

**Lido** is the largest liquid-staking protocol. Users deposit ETH (and other staked assets) and receive a liquid token (**stETH**) that appreciates as the underlying stake earns rewards — while independent node operators run the validators.

## What it is

- A **liquid-staking** DAO-governed protocol on Ethereum (and other chains: wstETH on L2s, stSOL on Solana, stMATIC on Polygon, etc.).
- **Open-source** smart contracts.
- **LDO** — governance token.

## How it works

1. User stakes ETH through Lido; the protocol mints **stETH** 1:1 to the deposit.
2. Lido's curated operators run validators; rewards accrue to stETH balances over time.
3. stETH is **rebasing** — its balance grows (or shrinks) with protocol yield, giving liquidity + yield simultaneously.

## Key features

- **Liquid while staking** — stETH can be used in DeFi (lending, LP) while earning.
- **wstETH** — the non-rebasing, wrapped form widely used as a DeFi collateral.
- **Curated vs. dual governance** — balance of security and decentralization.
- Extremely deep liquidity and DeFi integration.

## Trade-offs

- **Concentration risk** — Lido is the dominant staking provider, which raises centralization concerns in the Ethereum ecosystem.
- **Governance risk** — the protocol can be changed by LDO holders.
- **Smart-contract risk** — audited but complex.

## Resources

- Official site: https://lido.fi
- Docs: https://docs.lido.fi
- GitHub: https://github.com/lidofinance

See [Rocket Pool]({{ 'staking-mining/staking/rocket-pool' | relative_url }}) and [Liquid staking derivatives]({{ 'staking-mining/staking/lsd' | relative_url }}).