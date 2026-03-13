# solana-getVersion

> Returns the current Solana version running on the node

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getVersion

## Supported Chains
solana (mainnet, devnet)

## Method
`getVersion`

## Parameters
None.

## Returns
An object containing:
- `solana-core` (string): Software version of solana-core.
- `feature-set` (integer): Unique identifier of the current software's feature set.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getVersion"
}
```
