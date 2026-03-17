# solana-getVersion

> getVersion

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getVersion

## Supported Chains

Solana (mainnet, devnet)

## Method

`getVersion`

## Parameters

None - this method takes no parameters.

## Returns

An object containing:
- `solana-core` (string): Software version of solana-core
- `feature-set` (integer): Unique identifier of the current software's feature set

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getVersion"
}
```
