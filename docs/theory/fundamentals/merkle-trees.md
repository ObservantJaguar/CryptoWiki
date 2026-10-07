---

---

# Merkle trees

A **Merkle tree** (hash tree) is a data structure that commits to a set of leaf values with a single root hash, while allowing individual members to be verified without revealing the whole set.

## Structure

- **Leaves** — each leaf is the hash of a transaction (or other data item).
- **Internal nodes** — each internal node is the hash of its two children concatenated.
- **Root** — the top hash committing to all leaves.

A root with leaves `T1..T4` looks like:

```
       root = H(H(l1,l2), H(l3,l4))
        /                          \
  H(l1,l2)                       H(l3,l4)
   /     \                       /     \
  l1     l2                     l3     l4
```

(l1 = H(T1), l2 = H(T2), ...)

## Why they matter

- **Compact commitment** — the block header stores only the root, yet commits to every transaction.
- **Efficient verification** — to prove membership of one transaction you need only the hashes along its branch, about `log2(n)` values instead of all `n`.
- **Light-client support** — Simplified Payment Verification (SPV) clients confirm inclusion using Merkle proofs without downloading full blocks.
- **Mining layout** — multiple transactions can be committed before the final hash is computed, easing parallelization.