# 04 - Code & JavaScript

## When to Use the Code Node

Use the Code node when:
- Complex transformations that would require many visual nodes
- Custom algorithms or business logic
- Working with external JavaScript libraries
- Performance-critical processing of large datasets

## Two Modes

### Run Once for All Items
```javascript
// Receives all items as $input.all()
const items = $input.all();
return items.map(item => ({
  json: {
    ...item.json,
    processed: true
  }
}));
```

### Run Once for Each Item
```javascript
// Receives current item as $input.item
const data = $input.item.json;
return {
  json: {
    ...data,
    doubled: data.value * 2
  }
};
```

## Available Variables

| Variable | Description |
|----------|-------------|
| `$input` | Current input data |
| `$json` | Shorthand for current item's json |
| `$items()` | Get items from a specific node |
| `$node` | Reference other nodes |
| `$now` | Current date/time |
| `$workflow` | Workflow metadata |

## Best Practices

1. Prefer expressions for simple field references
2. Use Code node for multi-step logic
3. Always return an array of `{ json: {...} }` objects
4. Handle edge cases (empty arrays, null values)

## Key Files

- Code Node examples (Customer Data Processor, Sales Calculator, etc.)
- `ChatGPT or any LLM to Write JavaScript` workflows

## Exercise

Write a Code node that:
1. Takes an array of numbers
2. Filters values > 50
3. Calculates the average of remaining values
4. Returns a single item with the result

## Next

[05 - AI & LLMs](../05-ai-llms/) — adding intelligence to your workflows.
