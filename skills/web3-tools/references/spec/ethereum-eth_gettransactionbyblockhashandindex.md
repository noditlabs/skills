# ethereum-eth_gettransactionbyblockhashandindex

> eth_getTransactionByBlockHashAndIndex

- **Category**: Node API - Ethereum (JSON-RPC)

## Supported Chains

Ethereum (mainnet, sepolia, hoodi)

## Method

`eth_getTransactionByBlockHashAndIndex`

## Parameters

Array of parameters:

1. **Block Hash** (`string` (optional)): The block hash as a 64-character hexadecimal string.
2. **Transaction Index** (`string` (optional)): transaction index transaction . transaction index hexadecimal string .

## Returns

An object containing:
- `blockHash` (string): transaction block hash. confirmation transaction null
- `blockNumber` (string): transaction block number (hexadecimal). confirmation null
- `from` (string): transaction sender address
- `gas` (string): transaction gas limit (hexadecimal)
- `gasPrice` (string): (hexadecimal, wei )
- `maxPriorityFeePerGas` (string): fee (EIP-1559, hexadecimal)
- `maxFeePerGas` (string): fee (EIP-1559, hexadecimal)
- `hash` (string): transaction hash
- `input` (string): transaction input data (hexadecimal)
- `nonce` (string): sender transaction count (hexadecimal)

## Example Request

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_getTransactionByBlockHashAndIndex",
  "params": [
    "0x59f63e3840e0f4a1659074c1a4021e881a268a52d31958688da1d66bfbf6d2ca",
    "0x0"
  ]
}
```
