# kaia-klay_gettransactionbyblocknumberandindex

> klay_getTransactionByBlockNumberAndIndex

- **Category**: Node API - Kaia (JSON-RPC)

## Supported Chains

Kaia (mainnet, kairos)

## Method

`klay_getTransactionByBlockNumberAndIndex`

## Parameters

Array of parameters:

1. **Block Number or Tag** (`string` (optional)): . - : hexadecimal string (ex. "0x1") - : enum (ex. "latest", "earliest", "pending") - `earliest`: chain oldest . - `latest`: chain , finalized (reorgs) . latest status . - `pending`: , transaction . transaction status confirmation .
2. **Transaction Index** (`string` (optional)): transaction index transaction . transaction index hexadecimal string .

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
  "method": "klay_getTransactionByBlockNumberAndIndex",
  "params": [
    "0x1076B5A",
    "0x0"
  ]
}
```
