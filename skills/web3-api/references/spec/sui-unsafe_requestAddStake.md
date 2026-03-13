# sui-unsafe_requestAddStake

> Creates an unsigned transaction to add stake to a validator's staking pool.

- **Category**: Node API - Sui (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/sui-unsafe_requestAddStake

## Supported Chains
sui (mainnet)

## Method
`unsafe_requestAddStake`

## Parameters
Array of 5 items:

1. **signer** (`string`, required): The transaction signer's Sui address.

2. **coins** (`array` of `string`, required): Array of SUI coin object IDs to stake.

3. **amount** (`string` | `null`, optional): The amount of SUI to stake in MIST. If `null`, the entire coin value is staked.

4. **validator** (`string`, required): The validator's Sui address to stake with.

5. **gas** (`string` | `null`, optional): The gas object ID to use for payment. If `null`, the system selects automatically.

6. **gas_budget** (`string`, required): The gas budget for the transaction in MIST.

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
  "method": "unsafe_requestAddStake",
  "params": [
    "0xd4e2b8f9b0c3a5e7f1d6a8c2e4b0f3d5a7c9e1b3",
    [
      "0xa1b2c3d4e5f6a7b8c9d0e1f2a3b4c5d6e7f8a9b0"
    ],
    "1000000000000",
    "0x44b1b319e23495995fc837dafd28fc6af8b645edddff15bb556f882e3a7f1573",
    null,
    "10000000"
  ]
}
```
