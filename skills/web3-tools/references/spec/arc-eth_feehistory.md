# arc-eth_feehistory

> eth_feeHistory

- **Category**: Node API - Arc (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/arc-eth_feehistory

## Supported Chains

Arc (testnet)

## Method

`eth_feeHistory`

## Parameters

Array of parameters:

1. **Block Count** (`integer` (optional)): 
2. **Block Number or Tag** (`string` (optional)): . * : hexadecimal string (ex. "0x1") * : enum (ex. "latest", "earliest", "pending") * `earliest`: chain oldest . * `finalized`: finalized , status . (PoS) chain , finalized . * `safe`: network . ' ' network (reorgs) . * `latest`: chain , finalized (reorgs) . latest status . * `pending`: , transaction . transaction status confirmation .
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
  "method": "eth_feeHistory",
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
