# solana-getTokenAccountsByOwner

> getTokenAccountsByOwner

- **Category**: Node API - Solana (JSON-RPC)

## Supported Chains

Solana (mainnet, devnet)

## Method

`getTokenAccountsByOwner`

## Parameters

Array of parameters:

1. **Pubkey of Token Account** (`string` (required)): Pubkey of account owner to query, as base-58 encoded string
2. **Program** (`object` (required)): 

   - `mint` (string): Pubkey of the specific token Mint to limit accounts to, as base-58 encoded string
   - `programId` (string): Pubkey of the Token program that owns the accounts, as base-58 encoded string
3. **Configuration Object** (`object` (optional)): Optional configuration object.

   - `commitment` (string): block confirmation level. - finalized: cluster majority lockout finalized . cluster finalized recognized status . - confirmed: cluster majority vote . - processed: node . cluster . Enum: `processed`, `confirmed`, `finalized`.
   - `minContextSlot` (string): The minimum slot at which the request can be evaluated.
   - `dataSlice` (object): data . base58, base64, base64+zstd encoding data .
   - `encoding` (string): data encoding . - `base58` is slow and limited to less than 129 bytes of Account data. - `base64` will return base64 encoded data for Account data of any size. - `base64+zstd` compresses the Account data using Zstandard and base64-encodes the result. - `jsonParsed` encoding attempts to use program-specific state parsers to return more human-readable and explicit account state data. - If `jsonParsed` is requested but a parser cannot be found, the field falls back to base64 encoding, detectable when the data field is type <string>. Enum: `base58`, `base64`, `base64+zstd`, `jsonParsed`.

## Returns

An object containing:
- `context` (object): Solana network status data object.
- `value` (object): 

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getTokenAccountsByOwner",
  "params": [
    "A1TMhSGzQxMr1TboBKtgixKz1sS6REASMxPo1qsyTSJd",
    {
      "programId": "TokenkegQfeZyiNwAJbNbGKPFXCWuBvf9Ss623VQ5DA"
    },
    {
      "commitment": "finalized",
      "encoding": "jsonParsed"
    }
  ]
}
```
