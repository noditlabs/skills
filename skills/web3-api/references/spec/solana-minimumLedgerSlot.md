# solana-minimumLedgerSlot

> Returns the lowest slot that the node has information about in its ledger

- **Category**: Node API - Solana (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/solana-minimumLedgerSlot

## Supported Chains
solana (mainnet, devnet)

## Method
`minimumLedgerSlot`

## Parameters
None.

## Returns
An integer (uint64): The minimum ledger slot number.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "minimumLedgerSlot"
}
```
