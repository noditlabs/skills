# sui-unsafe_requestWithdrawStake

> Creates an unsigned transaction to withdraw stake from a validator's staking pool.

- **Category**: Node API - Sui (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/sui-unsafe_requestWithdrawStake

## Supported Chains
sui (mainnet)

## Method
`unsafe_requestWithdrawStake`

## Parameters
Array of 4 items:

1. **signer** (`string`, required): The transaction signer's Sui address.

2. **staked_sui** (`string`, required): The StakedSui object ID representing the stake to withdraw.

3. **gas** (`string` | `null`, optional): The gas object ID to use for payment. If `null`, the system selects automatically.

4. **gas_budget** (`string`, required): The gas budget for the transaction in MIST.

## Returns
- **TransactionBytes** (`object`): The unsigned transaction bytes.
  - `txBytes` (`string`): Base64-encoded BCS serialized transaction data.
  - `gas` (`array`): Array of gas object references used.
  - `inputObjects` (`array`): Array of input object metadata.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "unsafe_requestWithdrawStake",
  "params": [
    "0xd4e2b8f9b0c3a5e7f1d6a8c2e4b0f3d5a7c9e1b3",
    "0xa1b2c3d4e5f6a7b8c9d0e1f2a3b4c5d6e7f8a9b0",
    null,
    "10000000"
  ]
}
```
