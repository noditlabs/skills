# aptos-createWebhook

> Create a webhook subscription for Aptos blockchain events. Provide subscription details and a webhook URL to receive event notifications. Returns a Subscription ID for managing the webhook.

- **Category**: Webhook API
- **Official Docs**: https://developer.nodit.io/reference/aptos-createWebhook

## Supported Chains
- Aptos (mainnet, testnet)

## Endpoint
`POST /aptos/{network}/webhooks`

## Parameters / Request Body

### Path Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `network` | string | Yes | Target network. Enum: `mainnet`, `testnet` |

### Request Body (application/json)

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `eventType` | string | Yes | Event type to subscribe to. Enum: `EVENT`, `TRANSACTION` |
| `description` | string | No | Description of the webhook |
| `notification` | object | Yes | Notification configuration |
| `notification.webhookUrl` | string | Yes | Publicly accessible URL to receive webhook notifications |
| `isInstant` | boolean | No | Enable instant webhook (default: `false`). When `true`, messages are sent immediately upon event detection regardless of block finality. When `false`, messages are sent only after the block is finalized. |
| `condition` | object | Yes | Event subscription conditions (varies by eventType) |

#### Condition: EVENT

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `eventType` | string | Yes | Event type to monitor in `module_address::module_name::event_name` format |
| `eventAccountAddress` | string | Yes | Address that emits the event. Use `0x0` for Module Events. |
| `eventData` | json | No | Event data filtering conditions. JSON object, max 3 levels of nesting. |

#### Condition: TRANSACTION

Supports three condition sets:

**Function condition set:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `payloadFunction` | string | Yes | Function to monitor in `module_address::module_name::function_name` format |

**Event condition set:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `eventType` | string | Yes | Event type in `module_address::module_name::event_name` format |
| `eventAccountAddress` | string | Yes | Address that emits the event |
| `eventData` | json | No | Event data filtering conditions |

**Function and event condition set:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `payloadFunction` | string | Yes | Function to monitor |
| `eventType` | string | Yes | Event type to monitor |
| `eventAccountAddress` | string | Yes | Address that emits the event |
| `eventData` | json | No | Event data filtering conditions |

## Response

### 201 Created

| Field | Type | Description |
|-------|------|-------------|
| `subscriptionId` | string | Unique identifier for the webhook |
| `description` | string | Webhook description |
| `protocol` | string | Subscribed chain (e.g., `aptos`) |
| `network` | string | Subscribed network (e.g., `mainnet`) |
| `eventType` | string | Subscribed event type |
| `notification` | object | Notification info containing `webhookUrl` |
| `signingKey` | string | Signing key for verifying webhook notification authenticity |
| `isInstant` | boolean | Whether instant webhook is enabled |
| `condition` | object | Subscription conditions |
| `createdAt` | string | Creation timestamp (ISO 8601) |

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | INVALID_PARAMETER | Bad request |
| 401 | AUTHENTICATION_FAILED | Unauthorized |
| 403 | PERMISSION_DENIED | Forbidden |
| 404 | RESOURCE_NOT_FOUND | Not found |
| 429 | TOO_MANY_REQUESTS | Rate limited |
