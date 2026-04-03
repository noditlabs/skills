# kaia-kaia_getrewards

> kaia_getRewards

- **Category**: Node API - Kaia (JSON-RPC)

## Supported Chains

Kaia (mainnet, kairos)

## Method

`kaia_getRewards`

## Parameters

Array of parameters:

1. **Block Number** (`string` (optional)): The block number as a hexadecimal string (e.g., `"0x1"`).
2. **Block Tag** (`string` (optional)): A block tag: `"latest"`, `"earliest"`, `"pending"`, `"safe"`, or `"finalized"`.

## Returns

An object containing:
- `minted` (string): KAIA (hexadecimal, peb )
- `totalFee` (string): transaction count (hexadecimal, peb )
- `burntFee` (string): fee (hexadecimal, peb )
- `proposer` (string): (hexadecimal, peb )
- `stakers` (string): (hexadecimal, peb )
- `kif` (string): Kaia Infrastructure Fund (hexadecimal, peb )
- `kef` (string): Kaia Ecosystem Fund (hexadecimal, peb )
- `rewards` (object): address (key=address, value= hexadecimal)

## Example Request

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "kaia_getRewards",
  "params": []
}
```
