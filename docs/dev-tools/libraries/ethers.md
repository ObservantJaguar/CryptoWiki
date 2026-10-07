---
layout: default
title: ethers.js
parent: Libraries and SDKs
grand_parent: Tools
---

# ethers.js

**ethers.js** is a JavaScript/TypeScript library for interacting with the Ethereum blockchain. It is the modern standard for dApp frontends and Node scripts, offering a clean, secure API for wallets, contracts, providers, and utilities.

## What it is

- A complete library for EVM development: provider, signer, contract, and utilities.
- **Open-source** (MIT) — maintained by the Ethers community and Richard Moore.
- Version 6 (`ethers`) is current; v5 was ubiquitous previously.

## Key features

- **Provider abstraction** — connect to any Ethereum-compatible RPC (Infura, Alchemy, local geth).
- **Signer** — manage accounts/private keys, sign transactions and typed data (EIP-712).
- **Contract interfaces** — type-safe interaction with deployed contracts via ABIs.
- **Utilities** — address checksumming, big-number handling (`BigInt`), units conversion.
- **TypeScript-first** — excellent type definitions and ESM/CJS support.

## Quick example

```js
import { ethers } from "ethers";
const provider = new ethers.JsonRpcProvider("http://127.0.0.1:8545");
const balance = await provider.getBalance("0x..."); // BigInt in wei
console.log(ethers.formatEther(balance));
```

## Resources

- Official site / docs: https://docs.ethers.org
- GitHub: https://github.com/ethers-io/ethers.js
- npm: https://www.npmjs.com/package/ethers

See [First transaction over JSON-RPC]({{ 'guides/rpc-transaction' | relative_url }}).