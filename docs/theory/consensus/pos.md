---

---

# Proof of Stake (PoS)

**Proof of Stake** is a consensus mechanism in which the right to propose and attest blocks is weighted by the economic stake a validator locks up. Sybil resistance comes from capital, not computational work, giving PoS networks much lower energy consumption than PoW.

## How it works

1. Validators deposit a stake (e.g. ETH, or network tokens) to activate.
2. The protocol deterministically selects which validators propose and attest each slot/block, weighted by stake.
3. Validators who behave honestly earn rewards; those who equivocate or misbehave are **slashed** (lose part of their stake).
4. The chain follows the fork supported by the most stake-weighted attestations.

## Properties

- **Low energy cost** compared with PoW.
- **Slashing** penalties provide strong economic disincentives against misbehavior.
- **Entry/exit mechanics** (bonding periods) manage the validator set.

## Notable implementations

- **Ethereum** — post-Merge (2022) uses Gasper/Casper FFG; validators stake 32 ETH.
- **Solana, Cardano, Polkadot (NPoS), Tezos** — all use stake-based variants.

See [Proof of Work (PoW)]({{ 'theory/consensus/pow' | relative_url }}) for the work-based alternative, and the [staking domain]({{ 'staking-mining/staking' | relative_url }}) for validator software and services.