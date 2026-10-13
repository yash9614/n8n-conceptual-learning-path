# 07 - Integrations & APIs

## Connecting to the Outside World

n8n's power comes from its integrations. You have three main approaches:

### 1. Native Nodes
Pre-built nodes for popular services (Slack, Google Sheets, Notion, etc.).
- Handle authentication automatically
- Provide helpful UI for parameters
- Best for common operations

### 2. HTTP Request Node
The universal connector. Use it for any REST API.
```
Method: GET/POST/PUT/DELETE
URL: https://api.example.com/endpoint
Authentication: Header Auth / OAuth2 / API Key
Body: JSON or Form
```

### 3. Webhooks
Both inbound (trigger workflows) and outbound (send data to external systems).

## Credentials

Credentials are stored securely and referenced by nodes. Never hardcode API keys in workflows.

**Types**:
- API Key
- OAuth2
- Basic Auth
- Header Auth
- Custom

## Common Patterns

- **Polling vs Webhooks**: Prefer webhooks when available (real-time, efficient)
- **Rate limiting**: Use Wait nodes or Split In Batches
- **Pagination**: Loop with HTTP Request + IF until no more pages
- **Error handling**: Use "Continue On Fail" + error workflows

## Key Topics

- Google APIs setup
- Webhooks in n8n
- Deep Dive into APIs
- Community Nodes

## Next

[08 - Advanced Patterns](../08-advanced/) — production-ready techniques.
