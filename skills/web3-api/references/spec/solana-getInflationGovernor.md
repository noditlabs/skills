# solana-getInflationGovernor

> Returns the current inflation governor

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getInflationGovernor

## Supported Chains
solana (mainnet, devnet)

## Method
`getInflationGovernor`

## Parameters
- **Configuration Object** (object, optional):
  - `commitment` (string, enum: `processed`, `confirmed`, `finalized`): How finalized a block is.

## Returns
An object containing:
- `foundation` (number): Percentage of total inflation allocated to the foundation.
- `foundationTerm` (integer): Duration of foundation pool inflation in years.
- `initial` (number): Initial inflation percentage from time 0.
- `taper` (number): Rate per year at which inflation is lowered.
- `terminal` (number): Terminal inflation percentage.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getInflationGovernor",
  "params": [{ "commitment": "finalized" }]
}
```
