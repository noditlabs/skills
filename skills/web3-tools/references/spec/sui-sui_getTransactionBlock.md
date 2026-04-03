# sui-sui_getTransactionBlock

> sui_getTransactionBlock

- **Category**: Node API - Sui (JSON-RPC)

## Supported Chains

Sui (mainnet, testnet)

## Method

`sui_getTransactionBlock`

## Parameters

Array of parameters:

1. **digest** (`any` (required)): The digest of the queried transaction
2. **options** (`any` (optional)): 반환할 내용을 지정하는 옵션입니다.

## Returns

An object containing:
- `balanceChanges` (['array', 'null']): 
- `checkpoint` (string): 
- `confirmedLocalExecution` (['boolean', 'null']): 
- `digest` (object): A representation of a 32 byte digest
- `effects` (any): 
- `errors` (array): 
- `events` (['array', 'null']): 
- `objectChanges` (['array', 'null']): 
- `rawEffects` (array): 
- `rawTransaction` (string): Base64 encoding.

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "sui_getTransactionBlock",
  "params": [
    "Hay2tj3GcDYcE3AMHrej5WDsHGPVAYsegcubixLUvXUF",
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
