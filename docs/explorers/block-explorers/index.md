---

---

# Block explorers

Block explorers are web services that index a blockchain and let you search blocks, transactions, addresses, and token balances through a browser or API. They are the primary "user interface" for raw chain data.

## Categories

- [Bitcoin explorers]({{ 'explorers/block-explorers/bitcoin-explorers' | relative_url }}) — Blockstream.info, Blockchair, mempool.space.
- [Ethereum explorers]({{ 'explorers/block-explorers/ethereum-explorers' | relative_url }}) — Etherscan and ecosystem explorers.

## Practical notes

- Explorers are **read-only** — they never touch your keys or sign.
- They rely on third-party indexing; for trustless access, query your own full node via [RPC]({{ 'guides/rpc-transaction' | relative_url }}).