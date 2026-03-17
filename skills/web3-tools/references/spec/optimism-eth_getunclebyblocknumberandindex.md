# optimism-eth_getunclebyblocknumberandindex

> eth_getUncleByBlockNumberAndIndex

- **Category**: Node API - Optimism (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/optimism-eth_getunclebyblocknumberandindex

## Supported Chains

Optimism (mainnet, sepolia)

## Method

`eth_getUncleByBlockNumberAndIndex`

## Parameters

Array of parameters:

1. **Block Number or Tag** (`string` (optional)): . - : hexadecimal string (ex. "0x1") - : enum (ex. "latest", "earliest", "pending") - `earliest`: chain oldest . - `finalized`: finalized , status . (PoS) chain , finalized . - `safe`: network . ' ' network (reorgs) . - `latest`: chain , finalized (reorgs) . latest status . - `pending`: , transaction . transaction status confirmation .
2. **Transaction Index** (`string` (optional)): transaction index transaction . transaction index hexadecimal string .

## Returns

An object containing:
- `baseFeePerGas` (string): fee (EIP-1559, hexadecimal wei)
- `difficulty` (string): (hexadecimal)
- `extraData` (string): data (hexadecimal)
- `gasLimit` (string): (hexadecimal)
- `gasUsed` (string): (hexadecimal)
- `hash` (string): block hash
- `logsBloom` (string): event Bloom filter (2048 , hexadecimal)
- `miner` (string): address
- `mixHash` (string): mix hash
- `nonce` (string): nonce (hexadecimal)

## Example Request

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_getUncleByBlockNumberAndIndex",
  "params": [
    "0x5BAD54",
    "0x0"
  ]
}
```
