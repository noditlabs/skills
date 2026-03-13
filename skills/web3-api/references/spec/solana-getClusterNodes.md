# solana-getClusterNodes

> Returns information about all the nodes participating in the cluster

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-getClusterNodes

## Supported Chains
solana (mainnet, devnet)

## Method
`getClusterNodes`

## Parameters
None.

## Returns
An array of objects, each containing:
- `featureSet` (integer): The unique identifier of the node's feature set.
- `gossip` (string): Gossip network address for the node.
- `pubkey` (string): Node public key, as base-58 encoded string.
- `rpc` (string): JSON RPC network address for the node, or null.
- `shredVersion` (integer): The shred version the node has been configured to use.
- `tpu` (string): TPU network address for the node.
- `version` (string): The software version of the node, or null.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "getClusterNodes"
}
```
