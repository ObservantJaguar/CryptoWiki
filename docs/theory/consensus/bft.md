---

---

# BFT and PBFT family

The **Byzantine fault tolerance (BFT)** family models consensus as reaching agreement among nodes, some of which may behave arbitrarily (Byzantine), including lying or colluding. The goal is a protocol that achieves agreement and correct behavior even when up to a bounded fraction of participants are faulty.

## Byzantine faults

A node is *Byzantine* if it can deviate arbitrarily from the protocol: sending conflicting messages, stalling, or forging data. Classic distributed-systems results (e.g. the Byzantine Generals problem) show agreement is achievable only when at most one third of votes are faulty in synchronous settings.

## Practical Byzantine Fault Tolerance (PBFT)

PBFT is an early practical algorithm that reaches consensus in a view of `3f+1` or more replicas even when up to `f` are faulty, with message passing and a primary-backup scheme.

## Property and relation to blockchains

- **Deterministic finality** — once a round commits, the result is final (no probabilistic finality as in PoW).
- **Used by** — permissioned/chains and layer-1 protocols with BFT finality, e.g. Hyperledger Fabric, Hyperledger Besu (QBFT), CometBFT/Tendermint (Cosmos), and PBFT variants in private chains.

## Trade-offs

- BFT achieves finality fast but typically requires tighter network assumptions and a fixed/moderately sized validator set.

See [Proof of Authority (PoA)]({{ 'theory/consensus/poa' | relative_url }}), with which BFT engines are often combined in consortium chains.