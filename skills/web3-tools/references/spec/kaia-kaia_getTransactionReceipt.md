# kaia-kaia_gettransactionreceipt

> kaia_getTransactionReceipt

- **Category**: Node API - Kaia (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/kaia-kaia_gettransactionreceipt

## Supported Chains

Kaia (mainnet, kairos)

## Method

`kaia_getTransactionReceipt`

## Parameters

Array of parameters:

1. **Transaction Hash** (`string` (optional)): The transaction hash as a 64-character hexadecimal string.

## Returns

An object containing:
- `blockHash` (string): transaction block hash
- `blockNumber` (string): transaction block number (hexadecimal)
- `contractAddress` (string): contract creation transaction creation contract address, null
- `effectiveGasPrice` (string): (hexadecimal, peb )
- `from` (string): transaction sender address
- `gas` (string): transaction gas limit (hexadecimal)
- `gasPrice` (string): (hexadecimal, peb )
- `gasUsed` (string): transaction (hexadecimal)
- `logs` (array): transaction execution event
- `logsBloom` (string): event Bloom filter (2048 , hexadecimal)

## Example Request

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "kaia_getTransactionReceipt",
  "params": [
    "0xda148d856aef6d77d0b76c90ef1091ffe77afe9ee9b1c6cc23f28f042f198bd8"
  ]
}
```
