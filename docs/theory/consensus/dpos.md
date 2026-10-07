---

---

# Delegated Proof of Stake (DPoS)

**Delegated Proof of Stake** is a stake-based consensus in which token holders vote to elect a small fixed set of **block producers** (delegates, witnesses, or validators). It trades some decentralization for high throughput and fast block times.

## How it works

1. Token holders vote with their stake for a candidate list of producers.
2. The top-ranked producers (often 21-121) are elected to produce blocks in a round-robin schedule.
3. Producers who misbehave or fail can be voted out in subsequent elections.
4. Delegation lets holders participate without running infrastructure.

## Trade-offs

- **High TPS and predictable block times** — a small producer set is fast.
- **Reduced decentralization** — the elected set concentrates power relative to PoW or open PoS.
- **Vote markets** — producers often campaign and pay voters, which can introduce governance capture risks.

## Usage

- **EOS, Tron, BitShares** — classic DPoS networks.
- Some sidechains and consortium chains adopt DPoS-like scheduling for throughput.

Compare with [Proof of Stake (PoS)]({{ 'theory/consensus/pos' | relative_url }}) and [Proof of Authority (PoA)]({{ 'theory/consensus/poa' | relative_url }}).