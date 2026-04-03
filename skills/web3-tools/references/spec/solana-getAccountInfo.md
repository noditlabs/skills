# solana-getAccountInfo

> getAccountInfo

- **Category**: Node API - Solana (JSON-RPC)

## Supported Chains

Solana (mainnet, devnet)

## Method

`getAccountInfo`

## Parameters

Array of parameters:

1. **Pubkey** (`string` (required)): The account public key as a base-58 encoded string.
2. **Configuration Object** (`object` (optional)): Optional configuration object.

   - `commitment` (string): block confirmation level. - finalized: cluster majority lockout finalized . cluster finalized recognized status . - confirmed: cluster majority vote . - processed: node . cluster . Enum: `processed`, `confirmed`, `finalized`.
   - `encoding` (string): data encoding . base58 data 129byte . base64 size base64 encoding data is returned. base64+zstd Zstandard base64 encoding result is returned. jsonParsed program status status data is returned. jsonParsed , base64 encoding (data confirmation ). Enum: `base58`, `base64`, `base64+zstd`, `jsonParsed`.
   - `dataSlice` (object): data . base58, base64, base64+zstd encoding data .
   - `minContextSlot` (string): The minimum slot at which the request can be evaluated.

## Returns

An object containing:
- `context` (object): Solana network status data object.
- `value` (object): 

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
      "encoding": "base58",
      "dataSlice": {
        "offset": 0,
        "length": 100
      },
      "minContextSlot": "1234567890"
    }
  ]
}
```
