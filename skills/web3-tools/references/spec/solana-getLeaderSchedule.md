# solana-getLeaderSchedule

> getLeaderSchedule

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getLeaderSchedule

## Supported Chains

Solana (mainnet, devnet)

## Method

`getLeaderSchedule`

## Parameters

Array of 0-2 item(s). . 1. Epoch ( ) 2. Configuration Object ( )

## Returns

An object. epoch null , object is returned. key validator (base-58 encoding ) . - Values are arrays of leader slot indices relative to the first slot in the requested epoch

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getLeaderSchedule",
  "params": [
    null,
    {
      "commitment": "processed",
      "identity": "dv2eQHeP4RFrJZ6UeiZWoc3XTtmtZCUKxxCApCDcRNV"
    }
  ]
}
```
