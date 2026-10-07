---
layout: default
title: Mining pools
parent: Mining
grand_parent: Tools
---

# Mining pools

A **mining pool** combines the hashrate of many miners so that blocks are found collectively and rewards are split among participants proportionally to their contributed shares. Solo mining finds blocks rarely; pools smooth out payouts.

## How a pool works

1. Miners connect to a pool server and receive work (a block template with a slightly higher target).
2. Each miner returns **shares** — near-valid block hashes that prove work performed.
3. When the pool finds a real block, its reward (block subsidy + fees) is distributed to miners based on shares submitted during a window.

## Reward schemes

- **PPS (Pay Per Share)** — fix payment per share, pool bears the variance risk.
- **FPPS (Full PPS)** — PPS incl. transaction fees.
- **PPLNS (Pay Per Last N Shares)** — proportional to a rolling window of shares (common).
- **Solo** — no pool; full reward if you find the block.

## Choosing a pool

Factors: **fee percentage**, **minimum payout**, **payout schedule**, **reliability/history**, and **stability of the operator**. Prefer pools with transparent payouts and good uptime. Avoid putting too much hashrate in one pool, a practice that threatens decentralization (51% concentration risk).

## Notable pools

- **ViaBTC, F2Pool, AntPool, Foundry** — major Bitcoin pools.
- **Ethermine, F2Pool** — closed post-merge but historically Ethereum pools.
- **2Miners** — multi-coin; **NiceHash** — hashrate marketplace.

For a hands-on guide, see [Mining economics and setup]({{ 'staking-mining/mining/economics' | relative_url }}).