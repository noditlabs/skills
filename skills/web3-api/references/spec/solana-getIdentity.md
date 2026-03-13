# solana-getIdentity

> Returns the identity pubkey for the current node

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getIdentity

## Supported Chains
solana (mainnet, devnet)

## Method
`getIdentity`

## Parameters
None.

## Returns
An object containing:
- `identity` (string): The identity pubkey of the current node (as a base-58 encoded string).

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getIdentity"
}
```
