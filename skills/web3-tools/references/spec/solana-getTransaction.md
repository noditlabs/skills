# solana-getTransaction

> getTransaction

- **Category**: Node API - Solana (JSON-RPC)

## Supported Chains

Solana (mainnet, devnet)

## Method

`getTransaction`

## Parameters

Array of parameters:

1. **Transaction signature** (`string` (required)): Transaction signature, as base-58 encoded string
2. **Configuration Object** (`object` (optional)): Optional configuration object.

   - `commitment` (string): block confirmation level. - finalized: cluster majority lockout finalized . cluster finalized recognized status . - confirmed: cluster majority vote . - processed: node . cluster . Enum: `processed`, `confirmed`, `finalized`.
   - `maxSupportedTransactionVersion` (integer): parameter value `0` . `0` Versioned transaction transaction . This parameter determines the maximum transaction version that will be returned in the response. If you request a transaction with a higher version than this value, an error will be returned. If you omit this parameter, only legacy transactions will be returned—any versioned transaction will result in an error. Default: `0`.
   - `transactionDetails` (string): transaction . accounts transaction signature transaction . - Transaction metadata is limited to only: fee, err, pre_balances, post_balances, pre_token_balances, and post_token_balances. Enum: `full`, `accounts`, `signatures`, `none`. Default: `full`.

## Returns

An object containing:
- `blockTime` (integer): Estimated production time, as Unix timestamp (seconds since the Unix epoch) of when the transaction was processed. null if not available
- `meta` (object): 
- `slot` (integer): The slot this transaction was processed in
- `transaction` (object): 
- `version` (any): Transaction version. Undefined if maxSupportedTransactionVersion is not set in request params.

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getTransaction",
  "params": [
    "5Pj5fCupXLUePYn18JkY8SrRaWFiUctuDTRwvUy2ML9yvkENLb1QMYbcBGcBXRrSVDjp7RjUwk9a3rLC6gpvtYpZ",
    {
      "commitment": "confirmed",
      "maxSupportedTransactionVersion": 0,
      "encoding": "json"
    }
  ]
}
```
