# solana-getInflationGovernor

> getInflationGovernor

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getInflationGovernor

## Supported Chains

Solana (mainnet, devnet)

## Method

`getInflationGovernor`

## Parameters

Array of 0-1 item(s). . 1. Configuration Object ( )

## Returns

An object containing:
- `foundation` (number): Percentage of total inflation allocated to the foundation
- `foundationTerm` (integer): Duration of foundation pool inflation in years
- `initial` (number): Initial inflation percentage from time 0
- `taper` (number): Rate per year at which inflation is lowered. (Rate reduction is derived using the target slot time in genesis config)
- `terminal` (number): Terminal inflation percentage

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getInflationGovernor",
  "params": [
    {
      "commitment": "finalized"
    }
  ]
}
```
