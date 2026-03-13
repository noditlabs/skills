# solana-getRecentPerformanceSamples

> Returns a list of recent performance samples, in reverse slot order

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getRecentPerformanceSamples

## Supported Chains
solana (mainnet, devnet)

## Method
`getRecentPerformanceSamples`

## Parameters
- **Number of samples** (integer, optional): Number of samples to return (maximum 720).

## Returns
An array of objects, each containing:
- `slot` (integer): Slot in which sample was taken at.
- `numTransactions` (integer): Number of transactions processed during the sample period.
- `numSlots` (integer): Number of slots completed during the sample period.
- `samplePeriodSecs` (integer): Number of seconds in a sample window.
- `numNonVoteTransactions` (integer): Number of non-vote transactions processed.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getRecentPerformanceSamples",
  "params": [2]
}
```
