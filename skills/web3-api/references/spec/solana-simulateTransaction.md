# solana-simulateTransaction

> Simulate sending a transaction

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-simulateTransaction

## Supported Chains
solana (mainnet, devnet)

## Method
`simulateTransaction`

## Parameters
- **Transaction** (string, required): Transaction, as an encoded string.
- **Configuration Object** (object, optional):
  - `commitment` (string, enum: `processed`, `confirmed`, `finalized`, default: `finalized`): How finalized a block is.
  - `encoding` (string, enum: `base58`, `base64`): Encoding used for the transaction data.
  - `replaceRecentBlockhash` (boolean): If true, replace the transaction recent blockhash with the most recent (conflicts with sigVerify).
  - `sigVerify` (boolean): If true, verify transaction signatures (conflicts with replaceRecentBlockhash).
  - `minContextSlot` (string): The minimum slot that the request can be evaluated at.
  - `innerInstructions` (boolean): If true, the response will include inner instructions.
  - `accounts` (array): Accounts configuration for simulation.

## Returns
An object containing:
- `context` (object): Metadata about the current state of the Solana network.
- `value` (object):
  - `accounts` (array or null): Array of account objects if requested.
  - `err` (object or null): Error if transaction failed.
  - `innerInstructions` (array or null): Inner instructions if requested.
  - `logs` (array of strings or null): Array of log messages.
  - `replacementBlockhash` (object): Replacement blockhash info if replaceRecentBlockhash was true.
  - `returnData` (object or null): Most-recent return data.
  - `unitsConsumed` (integer): Number of compute units consumed.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "simulateTransaction",
  "params": [
    "AQAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAABAAEEjNmKiZGiOtSZ+g0//wH5kEQo3+UzictY+KlLV8hjXcs44M/Xnr+1SlZsqS6cFMQc46yj9PIsxqkycxJmXT+veJjIvefX4nhY9rY+B5qreeqTHu4mG6Xtxr5udn4MN8PnBt324e51j94YQl285GzN2rYa/E2DuQ0n/r35KNihi/zamQ6EeyeeVDvPVgUO2W3Lgt9hT+CfyqHvIa11egFPCgEDAwIBAAkDZAAAAAAAAAA=",
    { "commitment": "confirmed", "encoding": "base64", "replaceRecentBlockhash": true }
  ]
}
```
