# sui-suix_getDynamicFieldObject

> suix_getDynamicFieldObject

- **Category**: Node API - Sui (JSON-RPC)

## Supported Chains

Sui (mainnet, testnet)

## Method

`suix_getDynamicFieldObject`

## Parameters

Array of parameters:

1. **parent_object_id** (`any` (required)): The ID of the queried parent object
2. **name** (`any` (required)): The Name of the dynamic field

## Returns

An object containing:
- `data` (object): 
- `error` (any): 

## Example Request

```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "suix_getDynamicFieldObject",
  "params": [
    "0x3ddea0f8c3da994d9ead562ce76e36fdef6a382da344930c73d1298b0e9644b8",
    {
      "type": "0x0000000000000000000000000000000000000000000000000000000000000009::test::TestField",
      "value": "some_value"
    }
  ]
}
```
