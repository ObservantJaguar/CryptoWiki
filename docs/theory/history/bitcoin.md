---

---

# Bitcoin

**Bitcoin** is the first decentralized cryptocurrency, introduced in 2008 by the pseudonymous Satoshi Nakamoto via the Bitcoin whitepaper and launched in **January 2009** with the genesis block. It solved the double-spend problem without a trusted authority by combining proof-of-work, a distributed timestamped ledger, and economic incentives.

## Key innovations

- **Nakamoto consensus** — nodes follow the chain with the most accumulated proof-of-work.
- **Halving schedule** — block reward halves roughly every 4 years, capping supply at 21 million BTC.
- **UTXO model** — unspent transaction outputs; each coin is tracked as spendable output.
- **Decentralized issuance** — anyone can mine or run a full node; no issuer or central ledger.

## Timeline highlights

- **2009** — genesis block; first ever Bitcoin transaction between Nakamoto and Hal Finney.
- **2010** — first real-world purchase (the famous pizza, 10,000 BTC); Bitcoin reaches a market value.
- **2013** — first major price cycle; Bitcoin Foundation formed; altcoins begin.
- **2017** — SegWit activated; the Bitcoin Cash fork disputes block-size debate.
- **2021** — Taproot activated (Schnorr signatures, MAST), improving privacy and script flexibility.

## What to know technically

- PoW with SHA-256d mining → see [Proof of Work]({{ 'theory/consensus/pow' | relative_url }}).
- Address derivation uses SHA-256 + RIPEMD-160 → see [Address derivation]({{ 'theory/cryptography/addresses' | relative_url }}).
- UTXO spending and scripts — see [Bitcoin node software]({{ 'nodes/bitcoin' | relative_url }}).

Bitcoin's subsequent fork and scaling history produced a diverse family (Bitcoin Cash, Bitcoin SV, ordinal-based assets), covered under [alt node software]({{ 'nodes/alt-nodes' | relative_url }}).