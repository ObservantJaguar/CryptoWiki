---
layout: default
title: USDT and USDC
parent: Stablecoins
grand_parent: Tools
---

# USDT and USDC

**USDT (Tether)** and **USDC (USD Coin)** are the two dominant **fiat-collateralized** stablecoins, each pegged 1:1 to the US dollar. They are the most widely used stablecoins for trading pairs, settlement, and on/off-ramps across all major chains.

## USDT (Tether)

- Issued by **Tether** (iFinex).
- The largest stablecoin by market cap; the universal quote asset on most exchanges.
- **Proprietary** smart contracts; issued natively on Ethereum (ERC-20), Tron (TRC-20), and multiple other chains.
- Backed by a reserve portfolio held by Tether; transparency reports published periodically.
- Common choice for trading because of deep liquidity and wide adoption, including retail flows.

## USDC (USD Coin)

- Issued by **Circle** (via Centre consortium and now Circle Internet Financial).
- The **regulated** Ethereum & multi-chain stablecoin; fully reserved and audited by a firm each month.
- Available widely on Ethereum, Solana, Arbitrum, Optimism, Base (native), and others.
- **Open-source** ERC-20 implementation (Base58/Rebase variants for multi-chain).
- Favored by DeFi protocols and institutional users for regulatory clarity.

## Key comparison

| | USDT | USDC |
|---|---|---|
| Issuer | Tether | Circle |
| Reserve model | Fiat + equivalents, periodic attestation | Fiat-backed, monthly audits |
| Regulatory posture | Global, less granular | Highly regulated (US) |
| Native chains | Ethereum, Tron, Solana, ... | Ethereum, Solana, Base, ... |

Both are **proprietary** at the issuer level. Unlike [DAI]({{ 'defi/stablecoins/dai' | relative_url }}), users do not directly observe the reserves on-chain.

## Resources

- Tether: https://tether.to / https://github.com/TetherTech  (does not fully publish smart contracts)
- Circle USDC: https://www.circle.com/usdc / https://github.com/circlefin/stablecoin-evm