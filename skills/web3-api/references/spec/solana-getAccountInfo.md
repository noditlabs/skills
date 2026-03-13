# solana-getAccountInfo

> Returns all information associated with the account of provided Pubkey

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getAccountInfo

## Supported Chains
solana (mainnet, devnet)

## Method
`getAccountInfo`

## Parameters
- **Pubkey** (string, required): Pubkey of account to query, as base-58 encoded string.
- **Configuration Object** (object, optional):
  - `commitment` (string, enum: `processed`, `confirmed`, `finalized`): How finalized a block is at that point in time.
  - `encoding` (string, enum: `base58`, `base64`, `base64+zstd`, `jsonParsed`): Encoding format for Account data.
  - `dataSlice` (object): Request a slice of the account's data. Only available for base58, base64, or base64+zstd encodings.
    - `offset` (integer): Number of bytes to return.
    - `length` (integer): Byte offset from which to start reading.
  - `minContextSlot` (string): The minimum slot that the request can be evaluated at.

## Returns
An object containing:
- `context` (object): Metadata about the current state of the Solana network.
  - `apiVersion` (string): The API version used for the request.
  - `slot` (integer): The slot number at which the request was evaluated.
- `value` (object or null): If the account doesn't exist, result will be null. Otherwise:
  - `data` (array or object): Data associated with the account.
  - `executable` (boolean): Whether the account contains a program.
  - `lamports` (integer): Number of lamports assigned to this account.
  - `owner` (string): Base-58 encoded Pubkey of the program this account has been assigned to.
  - `rentEpoch` (integer): The epoch at which this account will next owe rent.
  - `space` (integer): The data size of the account.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getAccountInfo",
  "params": [
    "3fJ7AiixCoHhaYzaNn1nNoLZMQnrGSMDNmMN4ZNUMpEa",
    {
      "commitment": "processed",
      "encoding": "base58"
    }
  ]
}
```
