---
layout: default
title: Mining economics and setup
parent: Mining
grand_parent: Tools
---

# Mining economics and setup

Mining is capital-intensive. This page covers the practical economics and setup considerations — it is technical guidance, not financial advice.

## Core variables

- **Hardware cost** — ASICs (e.g. Antminer, Whatsminer) dominate Bitcoin; GPUs for altcoins.
- **Hashrate & efficiency** — measured in J/TH (ASIC) or MH/J (GPU); efficiency drives profitability.
- **Electricity price** — the single biggest operational cost.
- **Pool fees and payout** — PPS/PPLNS choice affects income variance.
- **Network difficulty** — rises with total hashrate, cutting each machine's share.
- **Coin price** — revenue is `reward * price`; volatile.

## Simple P&L model

```
Revenue = (your_hashrate / network_hashrate) * blocks_per_day * block_reward * price
Profit  = Revenue - (power_consumption_kW * hours * electricity_price) - overhead
```

## Setup basics

1. **Choose a coin/algorithm** compatible with your hardware.
2. **Pick a pool** (see [Mining pools]({{ 'staking-mining/mining/pools' | relative_url }})).
3. **Configure mining software** with your wallet address.
4. **Monitor** temperature, hash rate, and rejected shares.
5. **Secure** your earnings wallet address and never expose mining credentials.

## Realities

- **Post-Merge Ethereum**: no longer minable on GPUs (PoS). Altcoin GPU mining continues on other PoW chains.
- **Difficulty adjustments** mean early profits tend to normalize as hash rate follows.
- Beware **scams** promising guaranteed mining returns (cloud-mining fraud is common).

See [Mining software]({{ 'staking-mining/mining/software' | relative_url }}) for tool choices. This page is informational, not investment advice.