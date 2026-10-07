---
layout: default
title: web3.js
parent: Libraries and SDKs
grand_parent: Tools
---

# web3.js

**web3.js** is one of the oldest and most established JavaScript libraries for Ethereum. It provides a broad API for accounts, contracts, providers, and utilities, and remains used widely in legacy and production codebases.

## What it is

- A comprehensive Ethereum JavaScript API.
- **Open-source** (LGPL-3.0 / MIT) — maintained by the Web3.js team (ChainSafe).
- Version 4.x is the modern release (modular, TypeScript).

## Key features

- **Accounts** — create/sign transactions, work with private keys and mnemonics.
- **Contract** — instantiate and call deployed contracts from ABI.
- **Providers** — HTTP/WebSocket/Web3 provider; node connectivity.
- **Ethers-compatible choices** — v4 is fully tree-shakeable, improved types.

## Quick example

```js
import Web3 from "web3";
const web3 = new Web3("http://127.0.0.1:8545");
const bal = await web3.eth.getBalance("0x...");
console.log(web3.utils.fromWei(bal, "ether"));
```

## Choosing between them

- **ethers.js** — generally preferred for new projects (type safety, security, active velocity).
- **web3.js** — still used in many existing products and educational materials; fine for maintenance or familiarity.

Both are valid; ethers.js is recommended for greenfield work. See [ethers.js]({{ 'dev-tools/libraries/ethers' | relative_url }}).

## Resources

- Docs: https://docs.web3js.org
- GitHub: https://github.com/web3/web3.js
- npm: https://www.npmjs.com/package/web3