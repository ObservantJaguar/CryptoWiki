---
layout: default
title: Hardhat
parent: Smart-contract frameworks
grand_parent: Tools
---

# Hardhat

**Hardhat** is a professional EVM development environment for Ethereum, built in JavaScript/TypeScript and running on Node.js. It provides local compilation, testing, deployment, and a rich ecosystem of plugins, making it a community-standard choice.

## What it is

- A **task runner** and **development environment** (not just a compiler).
- **Open-source** (MIT) — Nomic Foundation.
- Supports Solidity and Vyper; works on Linux/macOS; Windows supported via WSL/Linux containers.

## Key features

- **Hardhat Network** — a fast in-process Ethereum node for testing with instant mining, forking, and debugging.
- **Ethers.js/Graph TS bindings**; TypeScript-first workflows.
- **Hardhat Ignition** — declarative, reproducible deployments (replacing old deploy scripts).
- **Plugins** — many: `@nomicfoundation/hardhat-toolbox`, verify, gas-reporting, and more.
- **Console** — quick interactions via `hardhat console` REPL.
- Rich stack traces and error reporting for debugging.

## Getting started

```sh
npm init -y
npm install --save-dev hardhat
npx hardhat  # creates a sample project
```

## Resources

- Official site: https://hardhat.org
- Docs: https://hardhat.org/docs
- GitHub: https://github.com/NomicFoundation/hardhat

See [Deploying a smart contract]({{ 'guides/smart-contract-testnet' | relative_url }}).