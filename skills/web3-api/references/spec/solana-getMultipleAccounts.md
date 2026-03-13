# solana-getMultipleAccounts

> Returns the account information for a list of Pubkeys

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getMultipleAccounts

## Supported Chains
solana (mainnet, devnet)

## Method
`getMultipleAccounts`

## Parameters
- **Pubkeys** (array of strings, required): An array of Pubkeys to query, as base-58 encoded strings (up to a maximum of 100).
- **Configuration Object** (object, optional):
  - `commitment` (string, enum: `processed`, `confirmed`, `finalized`): How finalized a block is.
  - `minContextSlot` (string): The minimum slot that the request can be evaluated at.
  - `dataSlice` (object): Request a slice of the account's data.
  - `encoding` (string, enum: `base58`, `base64`, `base64+zstd`, `jsonParsed`): Encoding format for Account data.

## Returns
An object containing:
- `context` (object): Metadata about the current state of the Solana network.
- `value` (array): Array of account objects, each with `data`, `executable`, `lamports`, `owner`, `rentEpoch`, and `space` fields.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getMultipleAccounts",
  "params": [
    ["vines1vzrYbzLMRdu58ou5XTby4qAqVRLmqo36NKPTg", "4fYNw3dojWmQ4dXtSGE9epjRGy9pFSx62YypT7avPYvA"],
    { "encoding": "base58", "commitment": "finalized" }
  ]
}
```
