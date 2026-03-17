# optimism-eth_getunclebyblockhashandindex

> eth_getUncleByBlockHashAndIndex

- **Category**: Node API - Optimism (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/optimism-eth_getunclebyblockhashandindex

## Supported Chains

Optimism (mainnet, sepolia)

## Method

`eth_getUncleByBlockHashAndIndex`

## Parameters

Array of parameters:

1. **Block Hash** (`string` (optional)): The block hash as a 64-character hexadecimal string.
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
  "method": "eth_getUncleByBlockHashAndIndex",
  "params": [
    "0x59f63e3840e0f4a1659074c1a4021e881a268a52d31958688da1d66bfbf6d2ca",
    "0x0"
  ]
}
```
