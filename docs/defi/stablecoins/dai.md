---
layout: default
title: DAI (MakerDAO)
parent: Stablecoins
grand_parent: Tools
---

# DAI (MakerDAO)

**DAI** is a decentralized, **crypto-collateralized** stablecoin pegged to the US dollar, issued by the Maker Protocol. Unlike fiat-backed stablecoins, DAI is created from overcollateralized crypto positions (Vaults/CDPs) and does not depend on a central issuer holding dollars.

## How it works

1. A user locks collateral (e.g. ETH, wstETH) into a **Vault** (CDP).
2. The protocol mints DAI against the collateral up to a collateralization ratio (e.g. 150%+).
3. When the collateral ratio falls below threshold, the position is **liquidated**.
4. DAI is stabilized by a system of fees (stability fees) and the Maker governance.

## Protocol details

- **Open-source** smart contracts.
- **MKR** — governance token; the official decentralized stablecoin of the Maker ecosystem.
- Multiple collateral types via **debt ceilings** and governance-approved assets.
- **Dai Savings Rate (DSR)** — users can earn interest on DAI by locking it in the savings module.
- With MakerDAO's "Endgame" roadmap, the system has been transitioning (e.g. toward NewStable and NewGovToken).

## Key features

- Fully on-chain issuance; no reliance on bank reserves.
- Transparent, auditable collateral and liquidations.
- Widely used across DeFi as a neutral quote asset.

## Resources

- Official site: https://makerdao.com
- Docs: https://docs.makerdao.com
- GitHub: https://github.com/makerdao
- DAI stats: https://makerburn.com / see also https://makerdao.com/en/dai

Compare with fiat-backed **USDT/USDC** in [USDT and USDC]({{ 'defi/stablecoins/usdt-usdc' | relative_url }}).