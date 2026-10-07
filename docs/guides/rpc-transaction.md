---

---

# Guide: First transaction over JSON-RPC

This guide shows how to make a transaction by talking to a node over **JSON-RPC** — using a local node or a hosted API — without a full wallet UI. It uses `curl` for Bitcoin (Core) and ethers.js for Ethereum.

## Bitcoin (bitcoin-cli / RPC)

With Bitcoin Core running and `server=1`:

```sh
# Create and fund an address on the node wallet
bitcoin-cli createwallet "test"
ADDR=$(bitcoin-cli getnewaddress)
bitcoin-cli generatetoaddress 101 "$ADDR"   # testnet/regtest only

# Send to a target address
TARGET=<recipient-address>
TXID=$(bitcoin-cli sendtoaddress "$TARGET" 0.01)
bitcoin-cli gettransaction "$TXID"          # confirm
```

Use `getrawtransaction`/`decoderawtransaction` for low-level inspection. On **testnet/regtest** you can mine to confirm instantly.

## Ethereum (JSON-RPC + ethers.js)

Use a local Geth node (`http://127.0.0.1:8545`) or a hosted provider.

```js
import { ethers } from "ethers";

const provider = new ethers.JsonRpcProvider("http://127.0.0.1:8545");
const signer = new ethers.Wallet(PRIVATE_KEY, provider);

const tx = await signer.sendTransaction({
  to: "0xRecipientAddress",
  value: ethers.parseEther("0.01"),
});
console.log("tx hash:", tx.hash);

const receipt = await tx.wait();   // wait for inclusion
console.log("status:", receipt.status); // 1 = success
```

## Sending via raw RPC (curl)

An unsigned Ethereum transfer can be constructed and broadcast with raw JSON-RPC:

```sh
curl -X POST -H "Content-Type: application/json" \
  --data '{"jsonrpc":"2.0","method":"eth_sendRawTransaction","params":["<signed-hex>"],"id":1}' \
  http://127.0.0.1:8545
```

The signed transaction is produced by a wallet library; the RPC call only **broadcasts** it.

## Gas and nonce (Ethereum)

- **Nonce** — increments per account per transaction (handled automatically by ethers).
- **Gas** — `limit` and `maxFeePerGas`/`maxPriorityFeePerGas`; set sensible values or let the library estimate.

## Safety

- Use **testnet** for your first attempt; never send real funds without testing.
- Confirm the recipient address carefully (checksums reduce typos).
- Never expose your RPC endpoint publicly.

## Verification

- Transaction appears on the mempool (`eth_getTransactionByHash`) then in a block.
- Receipt `status === 1` and the recipient balance increased.

See [Node APIs]({{ 'dev-tools/apis' | relative_url }}) and [Running a node]({{ 'guides/ethereum-node' | relative_url }}).