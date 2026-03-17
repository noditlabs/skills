# solana-getBlock

> getBlock

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getBlock

## Supported Chains

Solana (mainnet, devnet)

## Method

`getBlock`

## Parameters

Array of parameters:

1. **Slot number** (`any` (required)): 
2. **Configuration Object** (`object` (optional)): Optional configuration object.

   - `commitment` (string): block confirmation level. - finalized: cluster majority lockout finalized . cluster finalized recognized status . - confirmed: cluster majority vote . - processed: node . cluster . Enum: `processed`, `confirmed`, `finalized`.
   - `encoding` (string): transaction encoding . Parsed Responses . - `jsonParsed` attempts to use program-specific instruction parsers to return more human-readable and explicit data in the transaction.message.instructions list. - If `jsonParsed` is requested but a parser cannot be found, the instruction falls back to regular JSON encoding (accounts, data, and programIdIndex fields). Enum: `json`, `jsonParsed`, `base58`, `base64`.
   - `transactionDetails` (string): transaction . accounts transaction signature transaction . - Transaction metadata is limited to only: fee, err, pre_balances, post_balances, pre_token_balances, and post_token_balances. Enum: `full`, `accounts`, `signatures`, `none`. Default: `full`.
   - `maxSupportedTransactionVersion` (integer): parameter value `0` . `0` Versioned transaction transaction . This parameter determines the maximum transaction version that will be returned in the response. If you request a transaction with a higher version than this value, an error will be returned. If you omit this parameter, only legacy transactions will be returned—any versioned transaction will result in an error. Default: `0`.
   - `rewards` (boolean): Whether to populate the rewards array. If parameter not provided, the default includes rewards. Default: `True`.

## Returns

An object containing:
- `blockHeight` (integer): The number of blocks beneath this block.
- `blockTime` (integer): Estimated production time, as Unix timestamp (seconds since the Unix epoch). null if not available.
- `blockhash` (string): The blockhash of the block, as base-58 encoded string
- `parentSlot` (integer): The slot index of the parent block.
- `previousBlockhash` (string): The blockhash of this block's parent, as base-58 encoded string; if the parent block is not available due to ledger cleanup, this field will return "11111111111111111111111111111111"
- `transactions` (array): 

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
