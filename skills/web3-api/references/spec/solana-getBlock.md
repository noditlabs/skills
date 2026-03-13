# solana-getBlock

> Returns identity and transaction information about a confirmed block in the ledger

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getBlock

## Supported Chains
solana (mainnet, devnet)

## Method
`getBlock`

## Parameters
- **Slot number** (integer, required): The slot number (uint64).
- **Configuration Object** (object, optional):
  - `commitment` (string, enum: `processed`, `confirmed`, `finalized`): How finalized a block is.
  - `encoding` (string, enum: `json`, `jsonParsed`, `base58`, `base64`): Encoding format for each returned transaction.
  - `transactionDetails` (string, enum: `full`, `accounts`, `signatures`, `none`, default: `full`): Level of transaction detail to return.
  - `maxSupportedTransactionVersion` (integer, default: 0): Set to 0 to fetch all transactions including Versioned.
  - `rewards` (boolean, default: true): Whether to populate the rewards array.

## Returns
An object containing:
- `blockHeight` (integer): The number of blocks beneath this block.
- `blockTime` (integer): Estimated production time as Unix timestamp, or null.
- `blockhash` (string): The blockhash of the block, as base-58 encoded string.
- `parentSlot` (integer): The slot index of the parent block.
- `previousBlockhash` (string): The blockhash of this block's parent.
- `transactions` (array): Array of transaction objects with `transaction` and `meta` fields.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getBlock",
  "params": [
    378967388,
    {
      "commitment": "finalized",
      "encoding": "json",
      "transactionDetails": "full",
      "maxSupportedTransactionVersion": 0,
      "rewards": false
    }
  ]
}
```
