# kaia-kaia_getblocktransactioncountbynumber

> kaia_getBlockTransactionCountByNumber

- **Category**: Node API - Kaia (JSON-RPC)

## Supported Chains

Kaia (mainnet, kairos)

## Method

`kaia_getBlockTransactionCountByNumber`

## Parameters

Array of parameters:

1. **Block Number or Tag** (`string` (optional)): . - : hexadecimal string (ex. "0x1") - : enum (ex. "latest", "earliest", "pending") - `earliest`: chain oldest . - `latest`: chain , finalized (reorgs) . latest status . - `pending`: , transaction . transaction status confirmation .
2. **Include Transactions** (`boolean` (optional)): transaction . true transaction result is returned.

## Returns

- **result** (`string`): An integer encoded as a hexadecimal string (e.g., `'0x1a'`).

## Example Request

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "kaia_getBlockTransactionCountByNumber",
  "params": [
    "0x1076B5A"
  ]
}
```
