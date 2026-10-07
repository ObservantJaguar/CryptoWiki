---

---

# Guide: Running a full Bitcoin node

Running your own Bitcoin full node gives you independent verification of the entire chain, private transaction broadcasting, and a JSON-RPC interface. This guide uses **Bitcoin Core** on Linux/macOS and notes Windows-specific steps.

## 1. Install Bitcoin Core

Download the official binaries from **https://bitcoincore.org/bin/** (never from other sources) and verify the SHA-256 checksums and signatures.

```sh
# Linux/macOS (example via tarball)
tar -xzf bitcoin-*.tar.gz
sudo install -m 0755 -o root -g root -t /usr/local/bin bitcoin-*/bin/*
```

Windows: run the `.exe` installer.

## 2. Configure the daemon

Create `~/.bitcoin/bitcoin.conf` (Linux/macOS) or `%AppData%\Bitcoin\bitcoin.conf` (Windows):

```conf
server=1          # enable RPC server
rpcuser=bitcoin
rpcpassword=<strong-random-password>
txindex=0         # 1 only if you need historic txid lookups
daemon=1          # run in background (Linux)
# Optional: limit bandwidth / storage
# datadir=/mnt/ssd/bitcoin
```

Keep the RPC password strong and never expose the RPC port publicly.

## 3. Start and sync

```sh
bitcoind
```

Initial full sync downloads the whole blockchain (several hundred GB) and takes days on slow hardware. Check progress:

```sh
bitcoin-cli getblockchaininfo | grep -E 'blocks|headers|verificationprogress'
```

`verificationprogress` near `1.0` means fully synced.

## 4. Use the RPC

With the daemon running and `server=1`:

```sh
bitcoin-cli getinfo                  # basic info
bitcoin-cli getbalance               # wallet balance
bitcoin-cli getnewaddress            # new receiving address
```

## 5. Security

- Put the chain data on an SSD with enough free space (plan for growth).
- Do **not** expose the RPC port (8332) to the internet.
- If you want remote access, use SSH tunneling or a properly authenticated reverse proxy, not raw RPC.
- Keep the node software updated.

## Verification checklist

- `bitcoin-cli getblockchaininfo` shows `"blocks"` advancing and `verificationprogress` close to 1.
- `bitcoin-cli getnetworkinfo` shows active connections to peers.
- The daemon logs no sync or rpc errors.

See [Bitcoin Core]({{ 'nodes/bitcoin/bitcoin-core' | relative_url }}) and [RPC transactions]({{ 'guides/rpc-transaction' | relative_url }}).