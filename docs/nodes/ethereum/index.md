---

---

# Ethereum node software

Ethereum post-Merge runs a **two-client architecture**: an *execution client* (EV) processes transactions and state, and a *consensus client* (CL) implements the PoS beacon chain. Engineers typically run one client of each type that does not share the same client team, for diversity.

## Executing clients

- [Geth (Go Ethereum)]({{ 'nodes/ethereum/geth' | relative_url }}) — the most widely used execution client.
- [Nethermind]({{ 'nodes/ethereum/nethermind' | relative_url }}) — high-performance C# execution client.
- [Erigon]({{ 'nodes/ethereum/erigon' | relative_url }}) — an efficient, modular execution client (also known as Erigon2/Turbo-Geth lineage).

## Consensus clients

Run alongside an execution client to run the beacon chain and finality. Provisionally noted here:

- **Lighthouse** (Rust), **Prysm** (Go), **Teku** (Java), **Nimbus** (Nim) — the main PoS consensus clients.

See [Guide: Running an Ethereum node]({{ 'guides/ethereum-node' | relative_url }}) for a practical setup.