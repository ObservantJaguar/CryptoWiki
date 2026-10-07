---

---

# Hardware wallets

Hardware wallets are **cold storage** devices that keep private keys offline and generate signatures without exposing the keys to the connected computer or network. They are the recommended standard for self-custody of significant value.

## Why hardware

- Keys never leave the secure element/device.
- Signing happens inside the device; only the signed transaction is transmitted.
- PIN protection and optional passphrase add layers; an attacker needs both device and PIN/passphrase.

## Important practice

- Always verify the **seed recovery phrase** written down on a physical backup, never digital.
- Never enter your seed into any software or website, even for "verification".
- Buy from official channels; watch for tampering/fake devices.

## Featured devices

- [Ledger]({{ 'wallets/hardware/ledger' | relative_url }}) — Nano S/X.
- [Trezor]({{ 'wallets/hardware/trezor' | relative_url }}) — Model T / Safe series.
- [ColdCard]({{ 'wallets/hardware/coldcard' | relative_url }}) — air-gapped focused Bitcoin device.

See [Backup and key security]({{ 'guides/backup-security' | relative_url }}).