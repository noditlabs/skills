# sui-sui_getCheckpoint

> sui_getCheckpoint

- **Category**: Node API - Sui (JSON-RPC)

## Supported Chains

Sui (mainnet, testnet)

## Method

`sui_getCheckpoint`

## Parameters

Array of parameters:

1. **id** (`any` (required)): Checkpoint identifier, can use either checkpoint digest, or checkpoint sequence number as input

## Returns

An object containing:
- `checkpointCommitments` (array): Commitments to checkpoint state
- `digest` (object): 
- `endOfEpochData` (object): 
- `epoch` (string): 
- `epochRollingGasCostSummary` (object): Summary of the charges in a transaction. Storage is charged independently of computation. There are 3 parts to the storage charges: `storage_cost`: it is the charge of storage at the time the transaction is executed. The cost of storage is the number of bytes of the objects being mutated multiplied by a variable storage cost per byte `storage_rebate`: this is the amount a user gets back when manipulating an object. The `storage_rebate` is the `storage_cost` for an object minus fees. `non_refundable_storage_fee`: not all the value of the object storage cost is given back to user and there is a small fraction that is kept by the system. This value tracks that charge. When looking at a gas cost summary the amount charged to the user is `computation_cost + storage_cost - storage_rebate` and that is the amount that is deducted from the gas coins. `non_refundable_storage_fee` is collected from the objects being mutated/deleted and it is tracked by the system in storage funds. Objects deleted, including the older versions of objects mutated, have the storage field on the objects added up to a pool of "potential rebate". This rebate then is reduced by the "nonrefundable rate" such that: `potential_rebate(storage cost of deleted/mutated objects) = storage_rebate + non_refundable_storage_fee`
- `networkTotalTransactions` (string): 
- `previousDigest` (object): A representation of a 32 byte digest
- `sequenceNumber` (string): 
- `timestampMs` (string): 
- `transactions` (array): Transaction digests

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "sui_getCheckpoint",
  "params": [
    "1000"
  ]
}
```
