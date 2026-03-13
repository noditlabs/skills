# sui-sui_getProtocolConfig

> Return the protocol config table for the given version number. If none is specified, the node uses the version of the latest epoch it has processed.

- **Category**: Node API - Sui (JSON-RPC) / Read API
- **Official Docs**: https://developer.nodit.io/reference/sui-sui_getProtocolConfig

## Supported Chains
sui

## Method
`sui_getProtocolConfig`

## Parameters
| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `version` | `BigInt_for_uint64` | optional | An optional protocol version specifier. If omitted, the latest protocol config table for the node will be returned. |

## Returns
`ProtocolConfig` - ProtocolConfigResponse

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "sui_getProtocolConfig",
  "params": []
}
```
