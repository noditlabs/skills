# getDailyTransactionsStats

> Retrieves daily transaction count within a specified range.

- **Category**: Data API
- **Official Docs**: https://developer.nodit.io/reference/getDailyTransactionsStats

## Supported Chains
- ethereum, luniverse
- **Networks**: mainnet only

## Endpoint
`POST /{chain}/{network}/stats/getDailyTransactionsStats`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| chain | string | Yes | Target chain (ethereum, luniverse) |
| network | string | Yes | Target network (mainnet) |

## Request Body

| Name | Type | Required | Description |
|------|------|----------|-------------|
| startDate | string | Yes | Start dai (YYYY-MM-DD format). Max range: 100 days |
| endDate | string | Yes | End dai (YYYY-MM-DD format). Max range: 100 days |

## Response

| Field | Type | Description |
|-------|------|-------------|
| count | integer | Total count (if withCount=true) |
| items | array | List of data points |
| items[].date | string | Date/time in YYYY-MM-DD format |
| items[].count | integer | Count for the period |
