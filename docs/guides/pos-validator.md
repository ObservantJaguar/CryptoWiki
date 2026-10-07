---

---

# Guide: Setting up a PoS validator

Setting up a validator on a proof-of-stake network involves installing client software, generating validator keys, and (on Ethereum) running both an execution and a consensus client. This guide walks through the general flow using Ethereum as the concrete example.

## 1. Understand requirements

- **Ethereum** — stake 32 ETH, run an execution client + consensus client, keep them online 24/7.
- **Hardware** — 2+ cores, 8+ GB RAM, NVMe SSD with ~2 TB free for mainnet; network reliability matters.
- **Slashing risk** — signing contradictory messages loses stake; never run the same keys on two machines.

## 2. Install clients

Run one **execution client** and one **consensus client** from **different teams** for safety:

- Execution: [Geth]({{ 'nodes/ethereum/geth' | relative_url }}) / [Nethermind]({{ 'nodes/ethereum/nethermind' | relative_url }}) / [Erigon]({{ 'nodes/ethereum/erigon' | relative_url }})
- Consensus: [Lighthouse]({{ 'nodes/ethereum/lighthouse' | relative_url }}) / [Prysm]({{ 'nodes/ethereum/prysm' | relative_url }}) / [Teku]({{ 'nodes/ethereum/teku' | relative_url }}) / [Nimbus]({{ 'nodes/ethereum/nimbus' | relative_url }})

## 3. Generate validator keys

Use the official **Staking Deposit CLI** to generate a BIP-39 mnemonic and validator keys from the deposit contract:

```sh
./deposit new-mnemonic --chain mainnet
./deposit existing-mnemonic
```

You get:
- A mnemonic (back it up offline!),
- `validator_keys/` with keystore files,
- A `deposit_data.json` to send 32 ETH to the deposit contract.

## 4. Import keys and start the validator

Import keystores into your consensus client's validator client, set the graffiti, and start both clients:

```sh
# Example (Lighthouse)
lighthouse account validator import --directory validator_keys
lighthouse --network mainnet bn --http          # beacon node
lighthouse vc --network mainnet                  # validator client
```

Sync the beacon chain and execution client, deposit 32 ETH, then wait for activation (can take 1-2 days on mainnet).

## 5. Monitor and maintain

- Track your validator: status, attestation effectiveness, balance.
- Keep software updated and the machine online.
- Do not stop/restart with both validators active without care to avoid downtime penalties.

## 6. Alternatives

Not comfortable running infra? Use **liquid staking** ([Lido]({{ 'staking-mining/staking/lido' | relative_url }}), [Rocket Pool]({{ 'staking-mining/staking/rocket-pool' | relative_url }})) or a trusted service instead — no operational burden, at the cost of trust/distribution.

## Verification checklist

- Beacon node synced and peer-connected; validator appears in beacon chain status after deposit.
- Your validator's balance increases over time with effective rewards.
- No slashing events; uptime is high.

See [Validators and clients]({{ 'staking-mining/staking/validators' | relative_url }}) and [Consensus clients]({{ 'nodes/ethereum' | relative_url }}).