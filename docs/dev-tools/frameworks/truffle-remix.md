---
layout: default
title: Truffle and Remix
parent: Smart-contract frameworks
grand_parent: Tools
---

# Truffle and Remix

Two foundational tools in EVM development: **Truffle** was the original mainstream framework, and **Remix** (the browser IDE) remains the fastest way to prototype a contract without installing anything.

## Truffle

- An early (2015) development framework for Ethereum/Solidity: compilation, migration scripts, testing.
- **Open-source** (MIT). Development is now largely superseded by Hardhat/Foundry; Truffle was archived as of 2023-24.
- Key ideas that remain influential: the **migration/deploy script** pattern and testable artifact structure.

## Remix

- A browser-based **IDE** for Solidity (also Vyper, Solidity Playground).
- **Open-source** (MIT) — run at https://remix.ethereum.org or install locally.
- Features: in-browser compile, deploy to any network (via provider/injected), debugger with advanced stack traces, plugin marketplace.

## When to use

- **Remix** — quick prototyping, learning Sandbox, verifying single contracts.
- **Hardhat/Foundry** — serious development, testing, and deployment pipelines.
- Truffle is legacy-downstream; choose Hardhat/Foundry for new work.

## Resources

- Remix: https://remix.ethereum.org / https://github.com/ethereum/remix-project
- Truffle: https://www.trufflesuite.com / https://github.com/trufflesuite/truffle (archived)