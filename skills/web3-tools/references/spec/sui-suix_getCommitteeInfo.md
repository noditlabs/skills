# sui-suix_getCommitteeInfo

> suix_getCommitteeInfo

- **Category**: Node API - Sui (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/sui-suix_getCommitteeInfo

## Supported Chains

Sui (mainnet, testnet)

## Method

`suix_getCommitteeInfo`

## Parameters

Array of parameters:

1. **epoch** (`string` (optional)): The epoch of interest. If None, default to the latest epoch

## Returns

An object containing:
- `epoch` (string): 
- `validators` (array): 

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "suix_getCommitteeInfo",
  "params": [
    "5000"
  ]
}
```
