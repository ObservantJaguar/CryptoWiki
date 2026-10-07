---

---

# Guide: Running an Ethereum node (geth)

Running an Ethereum node typically means running an **execution client** (Geth) and optionally a **consensus client** (Lighthouse/Prysm) for full mainnet participation. This guide covers the execution side with Geth on Linux/macOS/Windows.

## 1. Install Geth

Download from **https://geth.ethereum.org/downloads** or build from source.

```sh
# Most Linux/macOS via package manager
sudo apt install ethereum   # Debian/Ubuntu (official repo)
brew install ethereum       # macOS
```

Windows: use the release `.zip`/installer from the official downloads page.

## 2. Choose a sync mode

Geth offers **snap** (default; fastest, one-shot) and **full** (validate all state, more storage) sync. For most operators, snap sync is appropriate.

```sh
geth --syncmode snap
```

Full sync needs a lot of storage and time; archive mode (`--gcmode=archive` or `--state.scheme=path`) is only for archive use.

## 3. First run (mainnet)

```sh
geth --http --http.api eth,net,web3 --http.addr 127.0.0.1 --http.port 8545
```

- `--http` enables the JSON-RPC server.
- Bind to `127.0.0.1` by default for security — do not expose 8545 publicly.
- You can also run with `--authrpc` for the Engine API (needed by consensus clients) and `--datadir` to set the data location.

## 4. Wait for sync

The first sync takes time and tens of GB of disk. Watch progress:

```sh
geth attach http://127.0.0.1:8545
> eth.blockNumber
> eth.syncing
```

`eth.syncing` returns `false` when fully synced.

## 5. Test the RPC

```sh
curl -X POST -H "Content-Type: application/json" \
  --data '{"jsonrpc":"2.0","method":"eth_blockNumber","params":[],"id":1}' \
  http://127.0.0.1:8545
```

Expect a hex response like `{"result":"0x12c...","id":1}`.

## 6. Add a consensus client (optional, for validating)

To run a full PoS node, pair Geth with a consensus client. See [Validators and clients]({{ 'staking-mining/staking/validators' | relative_url }}) and the [PoS validator guide]({{ 'guides/pos-validator' | relative_url }}).

## Security

- Keep the RPC port **local** — exposing 8545 invites abuse (fund draining via signed transactions).
- Use a firewall and only open ports required for p2p (30303).
- Store the data directory on fast storage; update Geth regularly.

## Verification checklist

- `eth.blockNumber` advances and `eth.syncing` is `false`.
- `eth_peerCount` / `net_peerCount` > 0.
- Logs show no repeat sync errors.

See [Ethereum node software]({{ 'nodes/ethereum' | relative_url }}).