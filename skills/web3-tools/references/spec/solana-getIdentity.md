# solana-getIdentity

> getIdentity

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getIdentity

## Supported Chains

Solana (mainnet, devnet)

## Method

`getIdentity`

## Parameters

None - this method takes no parameters.

## Returns

An object containing:
- `identity` (string): The identity pubkey of the current node (as a base-58 encoded string)

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getIdentity"
}
```
