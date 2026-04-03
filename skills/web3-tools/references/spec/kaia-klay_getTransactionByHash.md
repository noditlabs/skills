# kaia-klay_gettransactionbyhash

> klay_getTransactionByHash

- **Category**: Node API - Kaia (JSON-RPC)

## Supported Chains

Kaia (mainnet, kairos)

## Method

`klay_getTransactionByHash`

## Parameters

Array of parameters:

1. **Transaction Hash** (`string` (optional)): The transaction hash as a 64-character hexadecimal string.

## Returns

An object containing:
- `blockHash` (string): transaction block hash. confirmation transaction null
- `blockNumber` (string): transaction block number (hexadecimal). confirmation null
- `from` (string): transaction sender address
- `gas` (string): transaction gas limit (hexadecimal)
- `gasPrice` (string): (hexadecimal, peb )
- `hash` (string): transaction hash
- `input` (string): transaction input data (hexadecimal)
- `nonce` (string): sender transaction count (hexadecimal)
- `to` (string): transaction count address. contract creation null
- `transactionIndex` (string): transaction index (hexadecimal). confirmation null

## Example Request

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "klay_getTransactionByHash",
  "params": [
    "0xda148d856aef6d77d0b76c90ef1091ffe77afe9ee9b1c6cc23f28f042f198bd8"
  ]
}
```
