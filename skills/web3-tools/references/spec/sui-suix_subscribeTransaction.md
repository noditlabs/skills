# sui-suix_subscribeTransaction

> suix_subscribeTransaction

- **Category**: Node API - Sui (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/sui-suix_subscribeTransaction

## Supported Chains

Sui (mainnet, testnet)

## Method

`suix_subscribeTransaction`

## Parameters

Array of parameters:

1. **filter** (`any` (required)): The filter criteria for the transaction stream

## Returns

- **result**: The response from processing a transaction or a certified transaction

## Example Request

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "suix_subscribeTransaction"
}
```
