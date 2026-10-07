---

---

# What is a blockchain

A **blockchain** is a distributed, append-only ledger in which data is organized into blocks that are cryptographically linked to form a chain. Copies of the ledger are maintained independently by many nodes, and no single party controls the whole history.

## Core properties

- **Decentralization** — no single operator holds the authoritative copy; consensus decides which chain is canonical.
- **Immutability** — altering a past block breaks the hash chain and is detectable by any node.
- **Transparency** — the ledger is public and independently verifiable.
- **Tamper-evidence** — every block commits to all previous blocks via hashes, so a change is immediately visible.

## How history is formed

Each new block references the hash of the previous block, forming a chain from the *genesis block* to the tip. A node accepts a block that extends its current best chain; competing extensions are resolved by the consensus mechanism.

See [Blocks and chaining]({{ 'theory/fundamentals/blocks-chaining' | relative_url }}) for the block structure, and the [consensus domain]({{ 'theory/consensus' | relative_url }}) for how nodes agree on the canonical chain.