# sui-sui_getObject

> sui_getObject

- **Category**: Node API - Sui (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/sui-sui_getObject

## Supported Chains

Sui (mainnet, testnet)

## Method

`sui_getObject`

## Parameters

Array of parameters:

1. **object_id** (`any` (required)): object ID.
2. **options** (`any` (optional)): 반환할 내용을 지정하는 옵션입니다.

## Returns

An object containing:
- `data` (object): 
- `error` (any): 

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "sui_getObject",
  "params": [
    "0x53e4567ccafa5f36ce84c80aa8bc9be64e0d5ae796884274aef3005ae6733809",
    {
      "showType": true,
      "showOwner": true,
      "showPreviousTransaction": true,
      "showDisplay": false,
      "showContent": true,
      "showBcs": false,
      "showStorageRebate": true
    }
  ]
}
```
