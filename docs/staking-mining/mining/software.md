---
layout: default
title: Mining software
parent: Mining
grand_parent: Tools
---

# Mining software

Mining software controls the mining hardware (or CPU/GPU) and connects it to a pool or node. The choice depends on the algorithm and hardware type.

## CGMiner (asic / fpga)

- The classic, open-source mining program for FPGA/ASIC bitcoin miners (and others).
- **Open-source** (GPL) — Con Kolivas.
- CLI-based, supports many algorithms/hardware via drivers; has an RPC API and extensive tuning options.
- Mostly superseded by modern ASIC vendors, but historically foundational.
- https://github.com/ckolivas/cgminer

## T-Rex (GPU)

- A popular, feature-rich GPU miner supporting many algorithms (ethash, kawpow, etc.) with high performance and paid/limited versions.
- **Closed-source** binaries; free tier with a dev-fee.
- Popular for swift tuning, watchdog, and autodetect.
- https://github.com/trexminer/T-Rex

## BFGMiner (asic/gpu)

- Similar lineage to cgminer; open-source GPU/ASIC miner.
- https://github.com/luke-jr/bfgminer

## XVG/Litecoin/SHA-256/Scrypt tools

- Vendor ASIC software (e.g. Antminer/Whatsminer) or algorithms like **ccminer** (NVIDIA), **xmrig** (Monero/CPU), and **kawpowminer**.

## Choosing

Pick mining software based on:
- **Your hardware** (ASIC vs GPU vs CPU).
- **The algorithm** your target coin uses.
- **Payout preference** and dev-fee tolerance.

Ensure you download from official sources; many fake wallets/miners exist. See [Mining economics]({{ 'staking-mining/mining/economics' | relative_url }}).