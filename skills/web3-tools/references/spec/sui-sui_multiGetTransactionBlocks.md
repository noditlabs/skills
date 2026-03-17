# sui-sui_multiGetTransactionBlocks

> sui_multiGetTransactionBlocks

- **Category**: Node API - Sui (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/sui-sui_multiGetTransactionBlocks

## Supported Chains

Sui (mainnet, testnet)

## Method

`sui_multiGetTransactionBlocks`

## Parameters

Array of parameters:

1. **digests** (`array` (required)): A list of transaction digests.
2. **options** (`any` (optional)): Config options to control which fields to fetch

## Returns

An array of objects. 

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "sui_multiGetTransactionBlocks",
  "params": [
    [
      "EMqJqkQip6UaTkdff493ewAQNHGQFJwXDDn6m9CTgZzo",
      "Hn3B25vTQNTFAdThFkWvfkiAAUZxzwTaj4uEengu1ACX",
      "9vLSG9a4QcLcMdG1xCu6FRdXAjWWqvJHoHBCJfPMKkR9"
    ],
    {
      "showInput": true,
      "showRawInput": false,
      "showEffects": true,
      "showEvents": true,
      "showObjectChanges": false,
      "showBalanceChanges": false,
      "showRawEffects": false
    }
  ]
}
```
