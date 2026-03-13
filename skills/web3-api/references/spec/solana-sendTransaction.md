# solana-sendTransaction

> Submits a signed transaction to the cluster for processing

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-sendTransaction

## Supported Chains
solana (mainnet, devnet)

## Method
`sendTransaction`

## Parameters
- **Signed transaction hash** (string, required): Fully-signed Transaction, as encoded string.
- **Configuration Object** (object, optional):
  - `encoding` (string, enum: `base58`, `base64`, default: `base58`): Encoding used for the transaction data.
  - `skipPreflight` (boolean, default: false): When true, skip the preflight transaction checks.
  - `preflightCommitment` (string, enum: `processed`, `confirmed`, `finalized`, default: `finalized`): Commitment level for preflight.
  - `maxRetries` (integer): Maximum number of times for the RPC node to retry sending the transaction.
  - `minContextSlot` (string): The minimum slot that the request can be evaluated at.

## Returns
A string: First Transaction Signature embedded in the transaction, as base-58 encoded string (transaction id).

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "sendTransaction",
  "params": [
    "4hXTCkRzt9WyecNzV1XPgCDfGAZzQKNxLXgynz5QDuWWPSAZBZSHptvWRL3BjCvzUXRdKvHL2b7yGrRQcWyaqsaBCncVG7BFggS8w9snUts67BSh3EqKpXLUm5UMHfD7ZBe9GhARjbNQMLJ1QD3Spr6oMTBU6EhdB4RD8CP2xUxr2u3d6fos36PD98XS6oX8TQjLpsMwncs5DAMiD4nNnR8NBfyghGCWvCVifVwvA8B8TJxE1aiyiv2L429BCWfyzAme5sZW8rDb14NeCQHhZbtNqfXhcp2tAnaAT"
  ]
}
```
