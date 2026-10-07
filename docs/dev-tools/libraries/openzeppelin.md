---
layout: default
title: OpenZeppelin
parent: Libraries and SDKs
grand_parent: Tools
---

# OpenZeppelin

**OpenZeppelin** provides the canonical set of **audited, reusable smart-contract libraries** for Ethereum and EVM chains — ERC standards, access control, security utilities — plus tools for upgrades and testing. It is the foundation of thousands of production contracts.

## What it is

- **OpenZeppelin Contracts** — a modular Solidity library with battle-tested implementations of ERC-20, ERC-721, ERC-1155, access control, pausable, reentrancy guard, and more.
- **OpenZeppelin Defender** — a platform for managing, monitoring, and upgrading contract operations.
- **Open-source** (MIT) — OpenZeppelin.

## Key features

- **Standard implementations** — audited, widely reused (SafeERC20, Ownable, AccessControl, etc.).
- **Upgrades** — the transparent/proxy patterns (UUPS, Transparent) via `@openzeppelin/contracts-upgradeable`.
- **Hardhat/Foundry integrations** — deployment plugins.
- **Defender** — automated deployment, ops, and monitoring for production contracts.
- **Modern standards** — support for ERC-4626, EIP-2981, EIP-712, etc.

## Example

```solidity
import "@openzeppelin/contracts/token/ERC20/ERC20.sol";
import "@openzeppelin/contracts/access/Ownable.sol";

contract MyToken is ERC20, Ownable {
    constructor() ERC20("MyToken", "MTK") Ownable(msg.sender) {}
}
```

## Resources

- Official site: https://www.openzeppelin.com
- Docs: https://docs.openzeppelin.com
- GitHub: https://github.com/OpenZeppelin/openzeppelin-contracts

See [Deploying a smart contract]({{ 'guides/smart-contract-testnet' | relative_url }}).