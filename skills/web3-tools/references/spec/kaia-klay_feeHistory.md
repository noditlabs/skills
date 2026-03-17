# kaia-klay_feehistory

> klay_feeHistory

- **Category**: Node API - Kaia (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/kaia-klay_feehistory

## Supported Chains

Kaia (mainnet, kairos)

## Method

`klay_feeHistory`

## Parameters

Array of parameters:

1. **Block Count** (`integer` (optional)): 
2. **Block Number or Tag** (`string` (optional)): . - : hexadecimal string (ex. "0x1") - : enum (ex. "latest", "earliest", "pending") - `earliest`: chain oldest . - `latest`: chain , finalized (reorgs) . latest status . - `pending`: , transaction . transaction status confirmation .
3. **Reward Percentiles** (`array` (optional)): 

## Returns

An object containing:
- `oldestBlock` (string): oldest block number (hexadecimal)
- `reward` (array): fee array (wei, hexadecimal)
- `baseFeePerGas` (array): fee array (wei, hexadecimal). value
- `gasUsedRatio` (array): array (0~1)

## Example Request

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "klay_feeHistory",
  "params": [
    2,
    "latest",
    [
      0,
      100
    ]
  ]
}
```
