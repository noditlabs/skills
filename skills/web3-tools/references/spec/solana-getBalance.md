# solana-getBalance

> getBalance

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getBalance

## Supported Chains

Solana (mainnet, devnet)

## Method

`getBalance`

## Parameters

Array of parameters:

1. **Pubkey** (`string` (required)): The account public key as a base-58 encoded string.
2. **Configuration Object** (`object` (optional)): Optional configuration object.

   - `commitment` (string): block confirmation level. - finalized: cluster majority lockout finalized . cluster finalized recognized status . - confirmed: cluster majority vote . - processed: node . cluster . Enum: `processed`, `confirmed`, `finalized`.
   - `minContextSlot` (string): The minimum slot at which the request can be evaluated.

## Returns

An object containing:
- `context` (object): Solana network status data object.
- `value` (integer): balance

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getBalance",
  "params": [
    "3fJ7AiixCoHhaYzaNn1nNoLZMQnrGSMDNmMN4ZNUMpEa",
    {
      "commitment": "processed",
      "minContextSlot": "1234567890"
    }
  ]
}
```
