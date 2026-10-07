---

---

# Proof of Authority (PoA)

**Proof of Authority** is a consensus mechanism in which a pre-authorized set of known, trusted validators produces blocks. There is no mining and no stake-based election; authority comes from the validators' real-world identity and reputation.

## How it works

1. A genesis or governance rule defines an allowed set of validator addresses.
2. Validators sign and produce blocks in a rotating schedule.
3. A validator could create forks or censor, but damages its real-world reputation if caught — hence "authority" as the Sybil cost.

## Properties

- **Very high throughput** — no mining, no staking overhead.
- **Low latency** — near-instant finality among the known validator set.
- **Trust assumption** — centralization is explicit and by design.

## Usage

- **Ethereum testnets** and dev networks such as Goerli (Clique), Polygon PoS testnets, and Kovan used PoA engines.
- **Private and consortium chains** (Hyperledger Besu QBFT, Geth Clique) commonly use PoA.

See also [BFT / PBFT family]({{ 'theory/consensus/bft' | relative_url }}), with which PoA engines often overlap.