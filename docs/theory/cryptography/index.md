---
layout: default
title: Cryptography in crypto
parent: Theory
nav_order: 3
has_children: true
---

# Cryptography in crypto

Blockchains rest on public-key cryptography: asymmetric algorithms that give each user a **private key** (secret) and a **public key** (shareable), enabling signatures and address derivation without sharing secrets.

## Categories

- [Public-key cryptography]({{ 'theory/cryptography/public-key' | relative_url }}) — asymmetric key pairs and how they are used.
- [Signatures]({{ 'theory/cryptography/signatures' | relative_url }}) — ECDSA, EdDSA/Ed25519, and how transactions are authorized.
- [Hash functions]({{ 'theory/cryptography/hash-functions' | relative_url }}) — SHA-256, Keccak/SHA-3, RIPEMD-160 in blockchain roles.
- [Address derivation]({{ 'theory/cryptography/addresses' | relative_url }}) — how addresses are computed from public keys.