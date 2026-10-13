# 08 - Advanced Patterns

## Production Techniques

### Error Handling
- **Error Trigger** node: Catches errors from other workflows
- **Continue On Fail**: Per-node setting
- **Retry on Fail**: Automatic retries with backoff
- **Error Workflow**: Dedicated workflow for logging and alerting

### Sub-workflows
Use the **Execute Workflow** node to:
- Reuse logic across workflows
- Keep main workflows readable
- Separate concerns (validation, enrichment, notification)

### Queues & Scaling
- For high volume: Use external queues (Redis, RabbitMQ) + worker patterns
- Split In Batches for controlled processing
- Wait nodes for rate-limit compliance

### Human-in-the-Loop
- Wait node with webhook resume
- Approval flows via Slack/Email + webhook callback
- Form triggers for manual input

### Observability
- Execution data retention settings
- Logging to external systems
- Cost tracking for AI workflows

## Architecture Patterns

```
Main Workflow
  ├── Validation Sub-workflow
  ├── Enrichment Sub-workflow
  ├── Action Sub-workflow
  └── Error Handler Workflow
```

## Key Concepts from Materials

- Workflows, Automations, AI Agents — differences
- Community Nodes
- Understanding Three Ways to Run n8n

## Next

[09 - Templates Gallery](../09-templates/) — explore real-world implementations.
