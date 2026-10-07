---

---

# Aggregation and routing

DeFi **aggregators** route a single trade across multiple liquidity venues (DEXes, AMMs, bridges, and sometimes order books) to get the best price and lowest slippage. They solve the fragmentation problem of scattered liquidity.

## Why aggregators

- Liquidity is spread across many pools and chains.
- A single-user swap can be split into multiple sub-swaps for better execution.
- Aggregators search for the optimal path in real time.

## Categories

- [1inch Network]({{ 'defi/aggregation/1inch' | relative_url }}) — leading Ethereum/EVM aggregator with its own DEXs.
- [Paraswap]({{ 'defi/aggregation/paraswap' | relative_url }}) — open-source aggregator with GasToken and limit orders.
- [Other aggregators]({{ 'defi/aggregation/other-aggregators' | relative_url }}) — Odos, 0x, and on-chain routing.