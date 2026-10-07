---

---

# Hot and cold wallets

Wallets are classified by where keys live and how exposed they are to the internet. The distinction is about **key custody**, not just the app used.

## Hot wallets

- Keys stored on a device connected to the network (desktop, mobile, browser extension, exchange).
- **Convenient** — fast signing and trading.
- **Higher attack surface** — malware, phishing, and compromised extensions can steal keys.

## Cold wallets

- Keys stored offline and used only transiently to sign.
- Includes **hardware wallets** (Ledger, Trezor, ColdCard) and paper/air-gapped setups.
- **Lower risk** — keys never leave the offline device; only signed (and optionally blind/annotated) transactions are exported.

## Custodial vs self-custody

- **Self-custody** — you control the private keys/seed; no third party can spend or freeze your funds.
- **Custodial** — an exchange or service holds keys on your behalf; you control the *account*, not the keys (see [Custody]({{ 'wallets/custody' | relative_url }})).

## Tooling

Hardware and software wallet products are catalogued under [Wallets]({{ 'wallets' | relative_url }}); full backup guidance is in [Backup and key security]({{ 'guides/backup-security' | relative_url }}).