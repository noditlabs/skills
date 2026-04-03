# optimism-eth_call

> eth_call

- **Category**: Node API - Optimism (JSON-RPC)

## Supported Chains

Optimism (mainnet, sepolia)

## Method

`eth_call`

## Parameters

Array of parameters:

1. **Call Object** (`object` (optional)): The transaction call object.

   - `from` (string): transaction from address input.
   - `to` (string): transaction to address input.
   - `gas` (string): transaction hex input . contract call 0x0 input .
   - `gasPrice` (string): hex input.
   - `value` (string): transaction value value.
   - `data` (string): execution transaction method signature hashvalue . ABI .
2. **Block Number or Hash or Tag** (`string` (optional)): A block identifier: block number (hex string, e.g. `"0x1"`), block hash (64-char hex, e.g. `"0x39008..."`), or block tag: `"latest"`, `"earliest"`, `"pending"`, `"safe"`, `"finalized"`.
3. **State Override Set** (`object` (optional)): contract , nonce, code, status chain value call value override . . * `balance`: balance override hex . * `nonce`: nonce value override hex . * `code`: EVM bytecode hex input . * `state`: status override key-value . key value hex . * `stateDiff`: status slot override key-value . state , slot .

## Returns

- **result** (`string`): hexadecimal string . 0x .

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
