# sui-suix_getCommitteeInfo

> Return the committee information for the asked `epoch`.

- **Category**: Node API - Sui (JSON-RPC) / Governance Read API
- **Official Docs**: https://developer.nodit.io/reference/sui-suix_getCommitteeInfo

## Supported Chains
sui

## Method
`suix_getCommitteeInfo`

## Parameters
| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `epoch` | `BigInt_for_uint64` | optional | The epoch of interest. If None, default to the latest epoch |

## Returns
`CommitteeInfo` - SuiCommittee

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "suix_getCommitteeInfo",
  "params": []
}
```
