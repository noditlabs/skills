# sui-suix_getStakes

> suix_getStakes

- **Category**: Node API - Sui (JSON-RPC)

## Supported Chains

Sui (mainnet, testnet)

## Method

`suix_getStakes`

## Parameters

Array of parameters:

1. **owner** (`any` (required)): Sui address.

## Returns

An array of objects. 

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "suix_getStakes",
  "params": [
    "0x9c76d5157eaa77c41a7bfda8db98a8e8080f7cb53b7313088ed085c73f866f21"
  ]
}
```
