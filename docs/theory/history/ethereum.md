---

---

# Ethereum and smart contracts

**Ethereum** is a general-purpose, programmable blockchain proposed by Vitalik Buterin in 2013 and launched in **July 2015**. Unlike Bitcoin's simple script, Ethereum runs arbitrary programs — **smart contracts** — in a decentralized virtual machine.

## Key innovations

- **EVM (Ethereum Virtual Machine)** — a stack-based, Turing-complete (gas-limited) execution environment.
- **Gas** — a metered cost per computation that prevents infinite loops and pays validators.
- **Account model** — stateful accounts (EOA + contract accounts) instead of UTXOs; balances and storage live in a global state.
- **Smart contracts** — immutable programs deployed on-chain, typically written in Solidity or Vyper and deployed as bytecode.

## Timeline highlights

- **2015** — Frontier mainnet launch (PoW, Ethash).
- **2016** — The DAO incident leads to a hard fork (Ethereum vs Ethereum Classic).
- **2017** — ERC-20 token standard standardizes fungible tokens; ICO wave begins.
- **2019-2020** — formal scaling roadmap; the Beacon Chain (PoS) launches in late 2020.
- **2022** — the **Merge** switches mainnet from PoW to PoS (Gasper/Beacon Chain), cutting energy use massively.
- **2023-2025** — proto-danksharding (EIP-4844, "blobs") lowers L2 rollup costs.

## What to know technically

- Consensus is now [Proof of Stake]({{ 'theory/consensus/pos' | relative_url }}).
- Address hashing uses **Keccak-256** → see [Hash functions]({{ 'theory/cryptography/hash-functions' | relative_url }}).
- Execution and node software are catalogued under [Ethereum node software]({{ 'nodes/ethereum' | relative_url }}).