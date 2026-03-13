# solana-getProgramAccounts

> Returns all accounts owned by the provided program Pubkey

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getProgramAccounts

## Supported Chains
solana (mainnet, devnet)

## Method
`getProgramAccounts`

## Parameters
- **Pubkey of program** (string, required): Base-58 encoded Pubkey of the program to query.
- **Configuration Object** (object, optional):
  - `commitment` (string, enum: `processed`, `confirmed`, `finalized`): How finalized a block is.
  - `minContextSlot` (string): The minimum slot that the request can be evaluated at.
  - `withContext` (boolean): Wrap the result in an RpcResponse JSON object.
  - `encoding` (string, enum: `base58`, `base64`, `base64+zstd`, `jsonParsed`): Encoding format for Account data.
  - `dataSlice` (object): Request a slice of the account's data.
  - `filters` (array): Filter results using up to 4 filter objects.

## Returns
An array of objects, each containing:
- `pubkey` (string): The account Pubkey as base-58 encoded string.
- `account` (object): Account data with `data`, `executable`, `lamports`, `owner`, `rentEpoch`, and `space` fields.

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
      "filters": [{ "dataSize": 17 }, { "memcmp": { "offset": 4, "bytes": "3Mc6vR" } }]
    }
  ]
}
```
