# solana-sendTransaction

> sendTransaction

- **Category**: Node API - Solana (JSON-RPC)

## Supported Chains

Solana (mainnet, devnet)

## Method

`sendTransaction`

## Parameters

Array of parameters:

1. **Signed transaction hash** (`string` (required)): Fully-signed Transaction, as encoded string.
2. **Configuration Object** (`object` (optional)): Optional configuration object.

   - `encoding` (string): Encoding used for the transaction data. Values: `base58` (slow, `DEPRECATED`), or `base64`. Enum: `base58`, `base64`. Default: `base58`.
   - `skipPreflight` (boolean): When true, skip the preflight transaction checks. Default: false.
   - `preflightCommitment` (string): block confirmation level. - finalized: cluster majority lockout finalized . cluster finalized recognized status . - confirmed: cluster majority vote . - processed: node . cluster . Enum: `processed`, `confirmed`, `finalized`.
   - `maxRetries` (integer): Maximum number of times for the RPC node to retry sending the transaction to the leader. If this parameter not provided, the RPC node will retry the transaction until it is finalized or until the blockhash expires.
   - `minContextSlot` (string): The minimum slot at which the request can be evaluated.

## Returns

- **result** (`integer`): The minimum ledger slot number

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
