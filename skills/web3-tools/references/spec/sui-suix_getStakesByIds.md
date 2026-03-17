# sui-suix_getStakesByIds

> suix_getStakesByIds

- **Category**: Node API - Sui (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/sui-suix_getStakesByIds

## Supported Chains

Sui (mainnet, testnet)

## Method

`suix_getStakesByIds`

## Parameters

Array of parameters:

1. **staked_sui_ids** (`array` (required)): Array of staked SUI IDs

## Returns

An array of objects. 

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "suix_getStakesByIds",
  "params": [
    [
      "0x378423de90ed03b694cecf443c72b5387b29a731d26d98108d7abc4902107d7d",
      "0x6a8e0f8fea6fda5488462e58724c034462b6064a08845e2ae2942fe7c4ee816d"
    ]
  ]
}
```
