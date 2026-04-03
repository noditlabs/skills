# solana-getMultipleAccounts

> getMultipleAccounts

- **Category**: Node API - Solana (JSON-RPC)

## Supported Chains

Solana (mainnet, devnet)

## Method

`getMultipleAccounts`

## Parameters

Array of parameters:

1. **Pubkeys** (`array` (required)): An array of Pubkeys to query, as base-58 encoded strings (up to a maximum of 100)
2. **Configuration Object** (`object` (optional)): Optional configuration object.

   - `commitment` (string): block confirmation level. - finalized: cluster majority lockout finalized . cluster finalized recognized status . - confirmed: cluster majority vote . - processed: node . cluster . Enum: `processed`, `confirmed`, `finalized`.
   - `minContextSlot` (string): The minimum slot at which the request can be evaluated.
   - `dataSlice` (object): data . base58, base64, base64+zstd encoding data .
   - `encoding` (string): data encoding . - `base58` is slow and limited to less than 129 bytes of Account data. - `base64` will return base64 encoded data for Account data of any size. - `base64+zstd` compresses the Account data using Zstandard and base64-encodes the result. - `jsonParsed` encoding attempts to use program-specific state parsers to return more human-readable and explicit account state data. - If `jsonParsed` is requested but a parser cannot be found, the field falls back to base64 encoding, detectable when the data field is type <string>. Enum: `base58`, `base64`, `base64+zstd`, `jsonParsed`.

## Returns

An object containing:
- `context` (object): Solana network status data object.
- `value` (array): 

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getMultipleAccounts",
  "params": [
    [
      "vines1vzrYbzLMRdu58ou5XTby4qAqVRLmqo36NKPTg",
      "4fYNw3dojWmQ4dXtSGE9epjRGy9pFSx62YypT7avPYvA"
    ],
    {
      "encoding": "base58",
      "commitment": "finalized"
    }
  ]
}
```
