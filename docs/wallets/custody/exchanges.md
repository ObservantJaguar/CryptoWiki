---
layout: default
title: Exchanges (custodial)
parent: Custody
grand_parent: Tools
---

# Exchanges (custodial)

Centralized cryptocurrency exchanges are the most common **custodial** service: users deposit funds into exchange accounts, and the exchange holds the associated private keys in its own wallets. Trading, staking, and fiat on/off-ramps are provided against account balances.

## How it works

1. User creates an account and completes **KYC** (identity verification).
2. Deposits are credited to an internal ledger; the exchange controls the actual on-chain funds.
3. Trades update account balances without moving coins on-chain for each order.
4. Withdrawals move real assets from exchange wallets to a user-provided address.

## Featured exchanges

These are illustrative; there are many. All are **proprietary** and subject to jurisdictional regulation.

- **Binance** — largest by volume. https://www.binance.com
- **Coinbase** — US-based, regulated public company. https://www.coinbase.com
- **Kraken** — long-running US/EU exchange. https://www.kraken.com
- **OKX / Bybit** — major global derivatives and spot exchanges. https://www.okx.com / https://www.bybit.com

> **License:** Proprietary — not open source.

## Risks

- **Counterparty risk** — if the exchange fails, goes insolvent, or is hacked, user funds may be lost (history includes bankruptcies such as Mt. Gox and FTX).
- **Regulatory risk** — a service can freeze withdrawals or accounts by jurisdiction.
- **Withdrawal limits** — withdrawals may be paused during stress.

## Good practice

Keep only **trading balances** on exchanges; the majority of long-term holdings belong in [self-custody]({{ 'wallets' | relative_url }}). Verify a service's regulatory status and security track record before depositing.