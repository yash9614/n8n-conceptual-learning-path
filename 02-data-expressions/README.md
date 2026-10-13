# 02 - Data & Expressions

## How n8n Handles Data

n8n is fundamentally a **JSON processor**. Every node outputs an array of items, where each item is a JSON object.

```json
[
  { "json": { "name": "Alice", "score": 95 } },
  { "json": { "name": "Bob", "score": 87 } }
]
```

### Expressions

Expressions let you reference data dynamically using `{{ }}` syntax:

```javascript
{{ $json.name }}           // Current item's name
{{ $json["full name"] }}   // Keys with spaces
{{ $itemIndex }}           // Current item's index (0-based)
{{ $now }}                 // Current timestamp
```

### Common Expression Patterns

| Goal | Expression |
|------|------------|
| Previous node's data | `{{ $json.field }}` |
| Specific node | `{{ $node["Node Name"].json.field }}` |
| All items from a node | `{{ $items("Node Name") }}` |
| Conditional | `{{ $json.score > 90 ? "Pass" : "Fail" }}` |

## Item Pairing

When nodes have multiple inputs, n8n pairs items intelligently:
- By default, items are paired by index
- You can control pairing mode in node settings

**This is the most important concept in n8n.** Misunderstanding pairing causes 80% of "why is my data wrong?" bugs.

## Key Workflows

- `What is JSON and How it Works in n8n.json`
- `Hands-On JSON Practice - Interactive Data Types Template.json`
- `Mastering Expressions Interactive Template and Exercises.json`
- `Referencing JSON Data - Connecting Nodes with Expressions.json`

## Practice

1. Import the expressions template
2. Modify expressions and observe the output
3. Create a workflow that transforms an array of objects using expressions only (no Code node)

## Next

[03 - Core Nodes](../03-core-nodes/) — learn the essential nodes that power almost every workflow.
