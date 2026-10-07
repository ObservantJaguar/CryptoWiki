---
layout: default
title: Consensus mechanisms
parent: Theory
nav_order: 2
has_children: true
---

# Consensus mechanisms

Consensus is the set of rules by which independent nodes agree on a single canonical version of the ledger. Each mechanism balances decentralization, security, and performance differently.

## Categories

- [Proof of Work (PoW)]({{ 'theory/consensus/pow' | relative_url }}) — work "burned" as a Sybil cost; used by Bitcoin and legacy Ethereum.
- [Proof of Stake (PoS)]({{ 'theory/consensus/pos' | relative_url }}) — economic stake as a Sybil cost; used by modern Ethereum.
- [Delegated Proof of Stake (DPoS)]({{ 'theory/consensus/dpos' | relative_url }}) — elected block producers.
- [Proof of Authority (PoA)]({{ 'theory/consensus/poa' | relative_url }}) — trusted named validators; common in testnets and private chains.
- [BFT / PBFT family]({{ 'theory/consensus/bft' | relative_url }}) — Byzantine fault-tolerant agreement protocols.