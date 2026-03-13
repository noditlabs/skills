# eth_call

> Executes a read-only contract method call without creating a transaction on the blockchain. Commonly used to read the current state of a smart contract. No state changes occur from the call.

- **Category**: Node API (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/eth_call

## Supported Chains
arbitrum, arc, avalanche, base, bnb, ethereum, giwa, kaia, luniverse, optimism, polygon (common EVM method)

## Method
`eth_call`

## Parameters
Array of 2-3 items:

1. **Call Object** (`object`): The transaction call object.
   - `from` (`string`, optional): The sender address.
   - `to` (`string`, required): The contract address to call.
   - `gas` (`string`, optional): Gas limit in hex.
   - `gasPrice` (`string`, optional): Gas price in hex.
   - `value` (`string`, optional): Value to send in hex.
   - `data` (`string`, optional): The encoded method signature and parameters (ABI-encoded).

2. **Block Identifier** (`string`): Block number (hex), block hash (64-char hex), or block tag (`"latest"`, `"earliest"`, `"pending"`, `"safe"`, `"finalized"`).

3. **State Override Set** (`object`, optional): Override account balance, nonce, code, or storage state for the simulation.
   - `balance` (`string`): Override balance in hex.
   - `nonce` (`string`): Override nonce in hex.
   - `code` (`string`): Fake EVM bytecode in hex.
   - `state` (`object`): Key-value pairs to override storage state.
   - `stateDiff` (`object`): Key-value pairs to override individual storage slots.

## Returns
- **result** (`string`): The return value of the executed contract method, ABI-encoded as a hex string.

## Example Request
```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_call",
  "params": [
    {
      "to": "0xA0b86991c6218b36c1d19D4a2e9Eb0cE3606eB48",
      "data": "0x70a08231000000000000000000000000d8dA6BF26964aF9D7eEd9e03E53415D37aA96045"
    },
    "latest"
  ]
}
```
