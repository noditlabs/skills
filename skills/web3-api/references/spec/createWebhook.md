# createWebhook

> Create a webhook subscription for EVM-compatible blockchain events. Provide subscription details and a webhook URL to receive event notifications. Returns a Subscription ID for managing the webhook.

- **Category**: Webhook API
- **Official Docs**: https://developer.nodit.io/reference/createWebhook

## Supported Chains
- Arbitrum (mainnet, sepolia)
- Base (mainnet, sepolia)
- BNB (mainnet)
- Ethereum (mainnet, sepolia, hoodi)
- Giwa (sepolia)
- Kaia (mainnet, kairos)
- Optimism (mainnet, sepolia)
- Polygon (mainnet, amoy)

## Endpoint
`POST /{chain}/{network}/webhooks`

## Parameters / Request Body

### Path Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `chain` | string | Yes | Target chain. Enum: `arbitrum`, `base`, `bnb`, `ethereum`, `giwa`, `kaia`, `optimism`, `polygon` |
| `network` | string | Yes | Target network. Enum: `mainnet`, `testnet`, `sepolia`, `hoodi`, `amoy` (varies by chain) |

### Request Body (application/json)

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `eventType` | string | Yes | Event type. Enum: `ADDRESS_ACTIVITY`, `MINED_TRANSACTION`, `SUCCESSFUL_TRANSACTION`, `FAILED_TRANSACTION`, `TOKEN_TRANSFER`, `BELOW_THRESHOLD_BALANCE`, `BLOCK_PERIOD`, `BLOCK_LIST_CALLER`, `ALLOW_LIST_CALLER`, `LOG` |
| `description` | string | No | Description of the webhook |
| `notification` | object | Yes | Notification configuration |
| `notification.webhookUrl` | string | Yes | Publicly accessible URL to receive notifications |
| `isInstant` | boolean | No | Enable instant webhook (default: `false`) |
| `condition` | object | Yes | Event subscription conditions (varies by eventType) |

#### Condition: ADDRESS_ACTIVITY
| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `addresses` | string[] | Yes | List of addresses to monitor for activity (as sender or receiver) |

#### Condition: MINED_TRANSACTION
| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `addresses` | string[] | Yes | Sender addresses to monitor for mined transactions |

#### Condition: SUCCESSFUL_TRANSACTION
| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `addresses` | string[] | Yes | Sender addresses to monitor for successful transactions |

#### Condition: FAILED_TRANSACTION
| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `addresses` | string[] | Yes | Sender addresses to monitor for failed transactions |

#### Condition: TOKEN_TRANSFER
| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `tokens` | object[] | Yes | Token objects to monitor |
| `tokens[].contractAddress` | string | Yes | ERC20/ERC721/ERC1155 contract address |
| `tokens[].tokenId` | string | No | Specific token ID (for ERC721/ERC1155) |

#### Condition: BELOW_THRESHOLD_BALANCE
| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `address` | string | Yes | Address to monitor balance |
| `belowThresholdBalance` | string | Yes | Balance threshold in wei. Alerts when balance drops below this value. Checked every 1 minute. |

#### Condition: BLOCK_PERIOD
| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `period` | integer | Yes | Block period interval. Set to `1` for every block. |

#### Condition: BLOCK_LIST_CALLER
| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `address` | string | Yes | Target address to monitor |
| `blockListCallers` | string[] | Yes | Blocked addresses to alert on when they transfer to target |

#### Condition: ALLOW_LIST_CALLER
| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `address` | string | Yes | Target address to monitor |
| `allowListCallers` | string[] | Yes | Allowed addresses to alert on when they transfer to target |

#### Condition: LOG
| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `address` | string | Yes | Contract address to monitor |
| `topics` | string[] | Yes | Event log topics array (1-4 items). `topics[0]` is the Keccak256 hash of the event signature. `topics[1-3]` are indexed parameters. |

## Response

### 201 Created

| Field | Type | Description |
|-------|------|-------------|
| `subscriptionId` | string | Unique identifier for the webhook |
| `description` | string | Webhook description |
| `protocol` | string | Subscribed chain (e.g., ETHEREUM) |
| `network` | string | Subscribed network (e.g., MAINNET) |
| `eventType` | string | Subscribed event type |
| `notification` | object | Contains `webhookUrl` |
| `signingKey` | string | Signing key for verifying notification authenticity |
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
