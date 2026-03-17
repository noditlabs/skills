# arbitrum-eth_createaccesslist

> eth_createAccessList

- **Category**: Node API - Arbitrum (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/arbitrum-eth_createaccesslist

## Supported Chains

Arbitrum (mainnet, sepolia)

## Method

`eth_createAccessList`

## Parameters

Array of parameters:

1. **Call Object** (`object` (optional)): The transaction call object.

   - `from` (string): transaction from address input.
   - `to` (string): transaction to address input.
   - `gas` (string): transaction hex input . contract call 0x0 input .
   - `gasPrice` (string): hex input.
   - `value` (string): transaction value value.
   - `data` (string): execution transaction method signature hashvalue . ABI .
2. **Block Number or Hash or Tag** (`string` (optional)): A block identifier: block number (hex string, e.g. `"0x1"`), block hash (64-char hex, e.g. `"0x39008..."`), or block tag: `"latest"`, `"earliest"`, `"pending"`, `"safe"`, `"finalized"`.

## Returns

An object containing:
- `accessList` (array): creation
- `gasUsed` (string): gas used (hexadecimal)

## Example Request

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_createAccessList",
  "params": [
    {
      "from": null,
      "to": "0xdAC17F958D2ee523a2206206994597C13D831ec7",
      "data": "0x70a0823100000000000000000000000047ac0Fb4F2D84898e4D9E7b4DaB3C24507a6D503"
    },
    "latest"
  ]
}
```
