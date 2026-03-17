# sui-sui_tryMultiGetPastObjects

> sui_tryMultiGetPastObjects

- **Category**: Node API - Sui (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/sui-sui_tryMultiGetPastObjects

## Supported Chains

Sui (mainnet, testnet)

## Method

`sui_tryMultiGetPastObjects`

## Parameters

Array of parameters:

1. **past_objects** (`array` (required)): A vector of object and versions to be queried
2. **options** (`any` (optional)): 반환할 내용을 지정하는 옵션입니다.

## Returns

An array of objects. 

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "sui_tryMultiGetPastObjects",
  "params": [
    [
      {
        "objectId": "0x38b3186a7bb26a1ab2c982a0a9b482aa70f5a010fffc60f20194ef0f597474e8",
        "version": "4"
      },
      {
        "objectId": "0xceaf9ee4582d3a233101e322a22cb2a5bea2e681ea5af4e59bd1abb0bb4fcb27",
        "version": "12"
      }
    ],
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
