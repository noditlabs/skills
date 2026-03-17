# sui-suix_getAllBalances

> suix_getAllBalances

- **Category**: Node API - Sui (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/sui-suix_getAllBalances

## Supported Chains

Sui (mainnet, testnet)

## Method

`suix_getAllBalances`

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
  "method": "suix_getAllBalances",
  "params": [
    "0x94f1a597b4e8f709a396f7f6b1482bdcd65a673d111e49286c527fab7c2d0961"
  ]
}
```
