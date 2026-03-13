# aptos-updateWebhook

> Update an existing Aptos webhook's subscription conditions, activate or deactivate it, or change its notification URL and description.

- **Category**: Webhook API
- **Official Docs**: https://developer.nodit.io/reference/aptos-updateWebhook

## Supported Chains
- Aptos (mainnet, testnet)

## Endpoint
`PATCH /aptos/{network}/webhooks/{subscriptionId}`

## Parameters / Request Body

### Path Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `network` | string | Yes | Target network. Enum: `mainnet`, `testnet` |
| `subscriptionId` | string | Yes | The subscription ID of the webhook to update |

### Request Body (application/json)

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `notification` | object | No | Notification configuration |
| `notification.webhookUrl` | string | No | New publicly accessible webhook URL |
| `description` | string | No | Updated description |
| `isActive` | boolean | No | Set `true` to activate, `false` to deactivate. Deactivated webhooks stop receiving notifications but are not deleted. |
| `condition` | object | No | Updated subscription conditions |

#### Condition: EVENT

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `eventType` | string | Yes | Event type in `module_address::module_name::event_name` format |
| `eventAccountAddress` | string | Yes | Address that emits the event. Use `0x0` for Module Events. |
| `eventData` | json | No | Event data filtering conditions |

#### Condition: TRANSACTION

Supports three condition sets:

**Function condition set:**
| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `payloadFunction` | string | Yes | Function in `module_address::module_name::function_name` format |

**Event condition set:**
| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `eventType` | string | Yes | Event type to monitor |
| `eventAccountAddress` | string | Yes | Address that emits the event |
| `eventData` | json | No | Event data filtering |

**Function and event condition set:**
| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `payloadFunction` | string | Yes | Function to monitor |
| `eventType` | string | Yes | Event type to monitor |
| `eventAccountAddress` | string | Yes | Address that emits the event |
| `eventData` | json | No | Event data filtering |

## Response

### 200 Successful Response

| Field | Type | Description |
|-------|------|-------------|
| `result` | boolean | `true` on success, `false` on failure |

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | INVALID_PARAMETER | Bad request |
| 401 | AUTHENTICATION_FAILED | Unauthorized |
| 403 | PERMISSION_DENIED | Forbidden |
| 404 | RESOURCE_NOT_FOUND | Not found |
| 429 | TOO_MANY_REQUESTS | Rate limited |
