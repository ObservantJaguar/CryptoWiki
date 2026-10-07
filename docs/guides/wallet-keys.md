---

---

# Guide: Creating a wallet and managing keys

This guide explains how to create a wallet, generate a mnemonic seed, and manage private keys safely. It covers both wallet software and raw key generation — for development and for self-custody.

## 1. Understand the model

- **Private key** = the secret that controls funds.
- **Mnemonic (seed phrase)** = human-readable backup of the key material (BIP-39).
- Hardware wallets keep keys offline; software wallets keep them local but online.

See [Wallets and keys]({{ 'theory/wallets-keys' | relative_url }}) for the theory.

## 2. Generate a mnemonic (BIP-39)

Using a trusted tool like the BIP-39 reference code, or a wallet's create-new-wallet flow, generate a 12- or 24-word seed. Example with the `bip39` CLI/node lib:

```sh
npx bip39 generate  # 12 words
```

**Critical:** generate the seed on an **offline, trusted machine** and write it down on paper — never onto a networked device or screenshot.

## 3. Derive keys and addresses

BIP-44 paths standardize derivation: `m/44'/0'/0'/0/0` (Bitcoin), `m/44'/60'/0'/0/0` (Ethereum). Libraries like ethers.js derive addresses from a mnemonic:

```js
import { ethers } from "ethers";
const wallet = ethers.Wallet.fromPhrase("<your mnemonic>");
console.log(wallet.address);
```

## 4. Create a wallet in practice

- **Software wallet** — install MetaMask/Electrum from the official site, follow "create wallet", back up the seed.
- **Hardware wallet** — initialize the device, write down the 24-word seed, verify it, set a PIN.

## 5. Never share keys

- Never enter a seed into a website, support chat, or "verification" tool.
- A legitimate service will never ask for your seed.
- Store the seed in a **physical**, fireproof location; consider a passphrase for extra security.

## 6. Test with minimal funds

Before trusting a wallet with real value, send a tiny amount to a derived address and confirm you can recover the wallet from the seed on a fresh install.

## Verification checklist

- You can regenerate the exact same addresses from the seed.
- You have a physical backup of the seed — and a tested restore path.

See [Backup and key security]({{ 'guides/backup-security' | relative_url }}) for hardening your setup.