---
layout: default
title: Foundry
parent: Smart-contract frameworks
grand_parent: Tools
---

# Foundry

**Foundry** is a fast, modern toolchain for Ethereum smart-contract development written largely in Rust. It prioritizes speed, testing rigor, and a CLI-first workflow, and has become the preferred framework for many serious Solidity teams.

## What it is

- A suite of binaries: **forge** (build/test/deploy), **cast** (RPC CLI), **anvil** (local node), **chisel** (REPL).
- **Open-source** (MIT/Apache) — maintained by Paradigm and the community.
- Solidity-focused; compiles and tests at native speed.

## Key features

- **Forge** — blazing-fast compile/test with fuzzing, invariant testing, and cheatsheets.
- **Anvil** — a fast local node (EVM) for testing and forking mainnet.
- **Cast** — command-line interaction with contracts and RPC.
- **Chisel** — an interactive Solidity REPL for quick math/behavior checks.
- **Solidity-native scripting** — deploy scripts written in Solidity rather than JS/TS.
- Excellent for fork testing and fuzzing workflows.

## Getting started

```sh
curl -L https://foundry.paradigm.xyz | bash   # installs foundryup
foundryup
forge init my_project && cd my_project
forge build
forge test
```

## Resources

- Official site: https://getfoundry.sh
- Docs: https://book.getfoundry.sh
- GitHub: https://github.com/foundry-rs/foundry

Compare with [Hardhat]({{ 'dev-tools/frameworks/hardhat' | relative_url }}); see [Deploying a smart contract]({{ 'guides/smart-contract-testnet' | relative_url }}).