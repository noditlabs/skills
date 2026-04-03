# sui-sui_multiGetObjects

> sui_multiGetObjects

- **Category**: Node API - Sui (JSON-RPC)

## Supported Chains

Sui (mainnet, testnet)

## Method

`sui_multiGetObjects`

## Parameters

Array of parameters:

1. **object_ids** (`array` (required)): The IDs of the queried objects
2. **options** (`any` (optional)): 반환할 내용을 지정하는 옵션입니다.

## Returns

An array of objects. 

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "sui_multiGetObjects",
  "params": [
    [
      "0x77b3482580ee8d5bdc5b824808df54bfec4fc817622e5add0e48f749f01def98",
      "0x9060d87664c26a3f9a509228c21b16dc6797cf787c839a07edc03e6338421091",
      "0xb37379c527753c5c8ab783f697e7b61439368cd75ebe63d633af32ffb4a022d1",
      "0xee309e94ff5c9f6b02c5637f018f6ea7bed8f6c3d80f2a595c2305e12dd6d07c",
      "0x29bc7c8d230db3b417edb1184cf075da5e934f672d3da3e003d989075efaecc7"
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
