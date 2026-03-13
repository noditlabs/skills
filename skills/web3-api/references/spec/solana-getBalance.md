# solana-getBalance

> Returns the lamport balance of the account of provided Pubkey

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getBalance

## Supported Chains
solana (mainnet, devnet)

## Method
`getBalance`

## Parameters
- **Pubkey** (string, required): Pubkey of account to query, as base-58 encoded string.
- **Configuration Object** (object, optional):
  - `commitment` (string, enum: `processed`, `confirmed`, `finalized`): How finalized a block is at that point in time.
  - `minContextSlot` (string): The minimum slot that the request can be evaluated at.

## Returns
An object containing:
- `context` (object): Metadata about the current state of the Solana network.
  - `apiVersion` (string): The API version.
  - `slot` (integer): The slot number at which the request was evaluated.
- `value` (integer): The lamport balance of the account.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getBalance",
  "params": [
    "3fJ7AiixCoHhaYzaNn1nNoLZMQnrGSMDNmMN4ZNUMpEa",
    { "commitment": "processed" }
  ]
}
```
