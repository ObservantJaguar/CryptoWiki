---

---

# Guide: Deploying a smart contract to a testnet

Deploying a smart contract to a testnet is the standard way to test before mainnet. This guide uses **Hardhat** (JS/TS) and **Foundry** (Rust) to compile and deploy a simple Solidity contract.

## Prerequisites

- A wallet with testnet ETH (free faucet) for gas.
- RPC endpoint / testnet (e.g. Sepolia) via a hosted API or local node.
- Node.js (for Hardhat) or foundry-up (for Foundry).

## 1. Hardhat

```sh
mkdir my-contract && cd my-contract
npm init -y
npm install --save-dev hardhat @nomicfoundation/hardhat-toolbox
npx hardhat init   # choose "create a JavaScript project"
```

Write a contract in `contracts/`, e.g.:

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

contract Hello {
    string public message;
    constructor(string memory _msg) { message = _msg; }
    function set(string memory _msg) public { message = _msg; }
}
```

Configure `hardhat.config.js` with your testnet RPC and a funded private key, then deploy:

```sh
npx hardhat run scripts/deploy.js --network sepolia
```

The script prints the deployed address; verify on the explorer (Etherscan) via `npx hardhat verify <address> <args>` after wiring the API key.

## 2. Foundry

```sh
curl -L https://foundry.paradigm.xyz | bash && foundryup
forge init my_contract && cd my_contract
```

Write the contract under `src/`, then create a deploy script:

```solidity
// script/Deploy.s.sol
import {Hello} from "../src/Hello.sol";
import {Script} from "forge-std/Script.sol";

contract Deploy is Script {
    function run() external {
        vm.startBroadcast();
        new Hello("hello");
        vm.stopBroadcast();
    }
}
```

Deploy to the testnet:

```sh
forge script script/Deploy.s.sol \
  --rpc-url $SEPOLIA_RPC_URL \
  --private-key $PRIVATE_KEY \
  --broadcast
```

## 3. Test first

Write and run tests before deploying — Hardhat: `npx hardhat test`; Foundry: `forge test`. This catches bugs cheaply.

## 4. Gotchas

- Keep your private key **out of version control** (use `.env` and `dotenv`/`forge install`).
- Testnet faucets are limited; request carefully.
- Check the chain/network ID matches your RPC to avoid deploying to the wrong chain.
- Verify the contract on the explorer so tools can display it.

## Verification checklist

- Deployment transaction succeeded (receipt status OK).
- Contract shows on the testnet explorer with source verified.
- You can call/read the contract via the explorer or a script.

See [Smart-contract frameworks]({{ 'dev-tools/frameworks' | relative_url }}) and [Libraries]({{ 'dev-tools/libraries' | relative_url }}).