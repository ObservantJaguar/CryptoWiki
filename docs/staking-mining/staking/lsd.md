---
layout: default
title: Liquid staking derivatives
parent: Staking
grand_parent: Tools
---

# Liquid staking derivatives (LSDs)

**Liquid staking derivatives (LSDs)** are tokens that represent a staked position. They let stakers keep liquidity in DeFi while the underlying capital is locked in a validator — the LSD carries the staking yield and can be traded, lent, or used as collateral.

## How LSDs work

1. Underlying asset (e.g. ETH) is deposited into a staking protocol.
2. The protocol issues a derivative (e.g. **stETH**, **rETH**, **sfrxETH**) representing principal + accrued rewards.
3. The derivative can be transferred freely; its value grows (rebasing) or is reflected in its traded price (non-rebasing).

## Common LSDs

- **stETH (Lido)** — the largest; rebasing, from [Lido]({{ 'staking-mining/staking/lido' | relative_url }}).
- **rETH (Rocket Pool)** — non-rebasing, minted from [Rocket Pool]({{ 'staking-mining/staking/rocket-pool' | relative_url }}).
- **sfrxETH (Frax)** — the frxETH variant with Frax's flexible model.
- **cbETH (Coinbase)** — custodial LSD from Coinbase.

## Design differences

| | Rebase vs. apprec | Custody | Distribution |
|---|---|---|---|
| stETH | Rebase (balance grows) | Protocol (curated ops) | Very deep |
| rETH | Appreciates in price | Permissionless nodes | Moderate |
| sfrxETH | Appreciates in price | Centralized (Frax) | Moderate |

## Risks

- **De-peg risk** — derivatives can trade below underlying value during stress.
- **Liquidity** — thinner for smaller LSDs.
- **Protocol risk** — slashing, hacks, or governance changes.
- **Custody/centralization** — some LSDs are custodial.

## In DeFi

LSDs are a preferred collateral in lending markets and an ingredient in sophisticated yield strategies; monitor de-pegs and protocol health before use.