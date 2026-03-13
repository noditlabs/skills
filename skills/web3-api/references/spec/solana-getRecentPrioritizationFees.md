# solana-getRecentPrioritizationFees

> Returns a list of prioritization fees from recent blocks

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getRecentPrioritizationFees

## Supported Chains
solana (mainnet, devnet)

## Method
`getRecentPrioritizationFees`

## Parameters
- **Account addresses** (array of strings, optional): An array of Account addresses (up to 128), as base-58 encoded strings. If provided, the response will reflect a fee to land a transaction locking all of the provided accounts as writable.

## Returns
An array of objects, each containing:
- `slot` (integer): Slot in which the fee was observed.
- `prioritizationFee` (integer): The per-compute-unit fee paid by at least one successfully landed transaction, in micro-lamports.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getRecentPrioritizationFees",
  "params": [["CxELquR1gPP8wHe33gZ4QxqGB3sZ9RSwsJ2KshVewkFY"]]
}
```
