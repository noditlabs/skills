# solana-simulateTransaction

> simulateTransaction

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-simulateTransaction

## Supported Chains

Solana (mainnet, devnet)

## Method

`simulateTransaction`

## Parameters

Array of parameters:

1. **Transaction** (`string` (required)): The encoded transaction data.
2. **Configuration Object** (`object` (optional)): Optional configuration object.

   - `commitment` (string): block confirmation level. - finalized: cluster majority lockout finalized . cluster finalized recognized status . - confirmed: cluster majority vote . - processed: node . cluster . Enum: `processed`, `confirmed`, `finalized`.
   - `encoding` (string): Encoding used for the transaction data. Values: `base58` (slow, `DEPRECATED`), or `base64`. Enum: `base58`, `base64`.
   - `replaceRecentBlockhash` (boolean): If true the transaction recent blockhash will be replaced with the most recent blockhash (conflicts with `sigVerify`)
   - `sigVerify` (boolean): If true the transaction signatures will be verified (conflicts with replaceRecentBlockhash)
   - `minContextSlot` (string): The minimum slot at which the request can be evaluated.
   - `innerInstructions` (boolean): If true the response will include inner instructions. These inner instructions will be jsonParsed where possible, otherwise json.
   - `accounts` (array): 

## Returns

An object containing:
- `context` (object): Solana network status data object.
- `value` (object): 

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "simulateTransaction",
  "params": [
    "AQAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAABAAEEjNmKiZGiOtSZ+g0//wH5kEQo3+UzictY+KlLV8hjXcs44M/Xnr+1SlZsqS6cFMQc46yj9PIsxqkycxJmXT+veJjIvefX4nhY9rY+B5qreeqTHu4mG6Xtxr5udn4MN8PnBt324e51j94YQl285GzN2rYa/E2DuQ0n/r35KNihi/zamQ6EeyeeVDvPVgUO2W3Lgt9hT+CfyqHvIa11egFPCgEDAwIBAAkDZAAAAAAAAAA=",
    {
      "commitment": "confirmed",
      "encoding": "base64",
      "replaceRecentBlockhash": true
    }
  ]
}
```
