# solana-getTokenAccountsByOwner

> Returns all SPL Token accounts by token owner

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getTokenAccountsByOwner

## Supported Chains
solana (mainnet, devnet)

## Method
`getTokenAccountsByOwner`

## Parameters
- **Pubkey of Token Account** (string, required): Pubkey of account owner to query, as base-58 encoded string.
- **Program** (object, required):
  - `mint` (string): Pubkey of the specific token Mint to limit accounts to.
  - `programId` (string): Pubkey of the Token program that owns the accounts.
- **Configuration Object** (object, optional):
  - `commitment` (string, enum: `processed`, `confirmed`, `finalized`): How finalized a block is.
  - `minContextSlot` (string): The minimum slot that the request can be evaluated at.
  - `dataSlice` (object): Request a slice of the account's data.
  - `encoding` (string, enum: `base58`, `base64`, `base64+zstd`, `jsonParsed`): Encoding format for Account data.

## Returns
An object containing:
- `context` (object): Metadata about the current state of the Solana network.
- `value` (array): Array of objects with `pubkey` and `account` fields containing token account data.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getTokenAccountsByOwner",
  "params": [
    "A1TMhSGzQxMr1TboBKtgixKz1sS6REASMxPo1qsyTSJd",
    { "programId": "TokenkegQfeZyiNwAJbNbGKPFXCWuBvf9Ss623VQ5DA" },
    { "commitment": "finalized", "encoding": "jsonParsed" }
  ]
}
```
