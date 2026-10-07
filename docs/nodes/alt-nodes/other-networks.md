---
layout: default
title: Other networks
parent: Alternative network nodes
grand_parent: Tools
---

# Other networks

A brief reference to node software for further blockchain ecosystems. Details vary significantly; consult each project's documentation for exact binaries and requirements.

## Litecoin

- **Litecoin Core** — full node, a Bitcoin Core fork. https://litecoin.org / https://github.com/litecoin-project/litecoin

## Dogecoin

- **Dogecoin Core** — full node based on Litecoin/Bitcoin code. https://dogecoin.com / https://github.com/dogecoin/dogecoin

## Cardano

- **cardano-node** (Haskell) — Ouroboros PoS node. https://github.com/IntersectMBO/cardano-node

## Cosmos ecosystem

- **CometBFT / Tendermint** — consensus engine; each application chain runs its own node. https://github.com/cometbft/cometbft
- **Cosmos SDK** apps (including Cosmos Hub `gaiad`). https://github.com/cosmos/cosmos-sdk

## Polygon

- **heimdall + bor** — the Polygon PoS node pair (Tendermint-based + EVM fork). https://wiki.polygon.technology

## Binance Smart Chain

- **geth-based BSC node** — an EVM-compatible client. https://github.com/bnb-chain/bsc

## General guidance

Before running any node, consult the canonical docs, check hardware requirements, and enable only the ports/services you need. See [Security]({{ 'guides/backup-security' | relative_url }}) for hardening advice.