---

---

# Proof of Work (PoW)

**Proof of Work** is a consensus mechanism in which a node (miner) must expend computational effort to propose a valid block. The cost of work is the Sybil resistance: an attacker must control a majority of hash rate, not merely a majority of cheap identities.

## How it works

1. The miner assembles a candidate block and computes its hash.
2. The block is valid only if the hash is below a network-wide **target** (difficulty).
3. The miner searches a **nonce** (and header fields) until the target is met.
4. The winning block is broadcast; other nodes verify the hash and adopt it as part of the longest/heaviest chain.

## Properties

- **Tamper-evidence** — rewriting history requires redoing the work for that block and all successors.
- **51% requirement** — an attacker would need a majority of hash power to reliably reorg the chain.
- **Energy cost** — high electricity consumption is the primary criticism.

## Usage

- **Bitcoin** and its forks use SHA-256d PoW.
- **Litecoin** and Dogecoin use Scrypt.
- **Ethereum** used Ethash PoW until its Merge to PoS in 2022.

See [Proof of Stake (PoS)]({{ 'theory/consensus/pos' | relative_url }}) for the leading alternative, and the [mining domain]({{ 'staking-mining/mining' | relative_url }}) for mining software.