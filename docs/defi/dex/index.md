---

---

# DEX and AMM

Decentralized exchanges (DEXes) let users trade directly through smart contracts without a central order book. Most modern DEXes use **Automated Market Makers (AMMs)**: liquidity pools priced algorithmically by a bonding curve rather than matched orders.

## Core concept

An AMM pool holds reserves of two (or more) tokens and sets prices by product-constant rules (e.g. `x*y = k` in Uniswap). Liquidity providers deposit both sides and earn trading fees; anyone can trade against the pool.

## Categories

- [Uniswap]({{ 'defi/dex/uniswap' | relative_url }}) — the original and largest AMM (constant-product).
- [Curve]({{ 'defi/dex/curve' | relative_url }}) — stablecoin-specialized, low-slippage Stableswap.
- [Other AMMs]({{ 'defi/dex/other-amms' | relative_url }}) — Balancer, PancakeSwap, SushiSwap, and weighted/multi-asset pools.