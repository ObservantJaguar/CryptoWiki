---

---

# Blocks and chaining

A **block** is the fundamental unit of a blockchain: a container of transactions (or other state changes) plus metadata that links it to the rest of the chain.

## Anatomy of a block

Most blocks contain:

- **Header** — structural metadata: previous-block hash, timestamp, and consensus-specific fields (e.g. nonce in proof-of-work, or proposal round in proof-of-stake).
- **Body** — the list of transactions or state transitions committed by this block.
- **Block hash** — a hash of the header (and, in a Merkle-tree design, an implicit commitment to the body) that acts as the block's identifier.

## The hash chain

Each header stores the hash of the previous block's header. Because the previous hash is itself part of the header, changing any earlier block changes every subsequent hash — which is what makes the chain tamper-evident.

```
+--------+   +--------+   +--------+
| Block1 |-->| Block2 |-->| Block3 |
| h(B1)  |   | h(B2)  |   | h(B3)  |
|        |   | prev:B1|   | prev:B2|
+--------+   +--------+   +--------+
```

## Forking

When nodes propose conflicting extensions, the chain temporarily *forks*. The consensus mechanism determines which fork becomes canonical (typically the one with the most accumulated work or stake). This is covered in the [consensus domain]({{ 'theory/consensus' | relative_url }}).