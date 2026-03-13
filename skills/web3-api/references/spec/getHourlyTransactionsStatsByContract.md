# getHourlyTransactionsStatsByContract

> Retrieves hourly transaction count for a specific contract within a specified range.

- **Category**: Data API
- **Official Docs**: https://developer.nodit.io/reference/getHourlyTransactionsStatsByContract

## Supported Chains
- ethereum, luniverse
- **Networks**: mainnet only

## Endpoint
`POST /{chain}/{network}/stats/getHourlyTransactionsStatsByContract`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| chain | string | Yes | Target chain (ethereum, luniverse) |
| network | string | Yes | Target network (mainnet) |

## Request Body

| Name | Type | Required | Description |
|------|------|----------|-------------|
| contractAddress | string | Yes | Contract address (0x + 40 hex characters) |
| startDateTime | string | Yes | Start hour (YYYY-MM-DD-HH format). Max range: 2400 hours |
| endDateTime | string | Yes | End hour (YYYY-MM-DD-HH format). Max range: 2400 hours |

## Response

| Field | Type | Description |
|-------|------|-------------|
| count | integer | Total count (if withCount=true) |
| items | array | List of data points |
| items[].date | string | Date/time in YYYY-MM-DD-HH format |
| items[].count | integer | Count for the period |
