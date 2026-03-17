# luniverse-eth_gettransactionbyblocknumberandindex

> eth_getTransactionByBlockNumberAndIndex

- **Category**: Node API - Luniverse (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/luniverse-eth_gettransactionbyblocknumberandindex

## Supported Chains

Luniverse (mainnet)

## Method

`eth_getTransactionByBlockNumberAndIndex`

## Parameters

Array of parameters:

1. **Block Number or Tag** (`string` (optional)): . - : hexadecimal string (ex. "0x1") - : enum (ex. "latest", "earliest", "pending") - `earliest`: chain oldest . - `finalized`: finalized , status . (PoS) chain , finalized . - `safe`: network . ' ' network (reorgs) . - `latest`: chain , finalized (reorgs) . latest status . - `pending`: , transaction . transaction status confirmation .
2. **Transaction Index** (`string` (optional)): transaction index transaction . transaction index hexadecimal string .

## Returns

An object containing:
- `blockHash` (string): transaction block hash. confirmation transaction null
- `blockNumber` (string): transaction block number (hexadecimal). confirmation null
- `from` (string): transaction sender address
- `gas` (string): transaction gas limit (hexadecimal)
- `gasPrice` (string): (hexadecimal, wei )
- `maxPriorityFeePerGas` (string): fee (EIP-1559, hexadecimal)
- `maxFeePerGas` (string): fee (EIP-1559, hexadecimal)
- `hash` (string): transaction hash
- `input` (string): transaction input data (hexadecimal)
- `nonce` (string): sender transaction count (hexadecimal)

## Example Request

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_getTransactionByBlockNumberAndIndex",
  "params": [
    "0x1076B5A",
    "0x0"
  ]
}
```
