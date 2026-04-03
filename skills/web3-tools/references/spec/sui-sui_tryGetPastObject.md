# sui-sui_tryGetPastObject

> sui_tryGetPastObject

- **Category**: Node API - Sui (JSON-RPC)

## Supported Chains

Sui (mainnet, testnet)

## Method

`sui_tryGetPastObject`

## Parameters

Array of parameters:

1. **object_id** (`any` (required)): object ID.
2. **version** (`any` (required)): The version of the queried object. If None, default to the latest known version
3. **options** (`any` (optional)): 반환할 내용을 지정하는 옵션입니다.

## Returns

- **result**: The object exists and is found with this version | The object does not exist | The object is found to be deleted with this version

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "sui_tryGetPastObject",
  "params": [
    "0x11af4b844ff94b3fbef6e36b518da3ad4c5856fa686464524a876b463d129760",
    4,
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
