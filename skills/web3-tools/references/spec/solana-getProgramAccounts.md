# solana-getProgramAccounts

> getProgramAccounts

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getProgramAccounts

## Supported Chains

Solana (mainnet, devnet)

## Method

`getProgramAccounts`

## Parameters

Array of parameters:

1. **Pubkey of program** (`string` (required)): Base-58 encoded Pubkey of the program to query
2. **Configuration Object** (`object` (optional)): Optional configuration object.

   - `commitment` (string): block confirmation level. - finalized: cluster majority lockout finalized . cluster finalized recognized status . - confirmed: cluster majority vote . - processed: node . cluster . Enum: `processed`, `confirmed`, `finalized`.
   - `minContextSlot` (string): The minimum slot at which the request can be evaluated.
   - `withContext` (boolean): Wrap the result in an RpcResponse JSON object
   - `encoding` (string): data encoding . - `base58` is slow and limited to less than 129 bytes of Account data. - `base64` will return base64 encoded data for Account data of any size. - `base64+zstd` compresses the Account data using Zstandard and base64-encodes the result. - `jsonParsed` encoding attempts to use program-specific state parsers to return more human-readable and explicit account state data. - If `jsonParsed` is requested but a parser cannot be found, the field falls back to base64 encoding, detectable when the data field is type <string>. Enum: `base58`, `base64`, `base64+zstd`, `jsonParsed`.
   - `dataSlice` (object): data . base58, base64, base64+zstd encoding data .
   - `filters` (array): 4 filter object result filter .

## Returns

An array of objects. 

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getProgramAccounts",
  "params": [
    "4Nd1mBQtrMJVYVfKf2PJy9NZUZdTAsp7D4xWLs4gDB4T",
    {
      "commitment": "finalized",
      "filters": [
        {
          "dataSize": 17
        },
        {
          "memcmp": {
            "offset": 4,
            "bytes": "3Mc6vR"
          }
        }
      ]
    }
  ]
}
```
