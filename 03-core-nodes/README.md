# 03 - Core Nodes

## Essential Nodes You Must Know

### Flow Control
| Node | Purpose |
|------|---------|
| **IF** | Binary condition (true/false path) |
| **Switch** | Multi-way routing based on rules |
| **Merge** | Combine data from multiple branches |
| **Wait** | Pause execution (useful for rate limits, approvals) |
| **Split In Batches** | Process large lists in chunks |

### Data Manipulation
| Node | Purpose |
|------|---------|
| **Set** | Add, modify, or remove fields |
| **Edit Fields** | Visual field editor (newer alternative to Set) |
| **Aggregate** | Combine multiple items into one |
| **Item Lists** | Convert between single items and lists |
| **Remove Duplicates** | Deduplicate based on fields |

### Utilities
| Node | Purpose |
|------|---------|
| **No Operation** | Placeholder / debugging |
| **Sticky Note** | Documentation inside the canvas |
| **Execute Workflow** | Call another workflow (sub-workflows) |

## Mental Model: Branching

```
          ┌─ IF (true)  → Action A
Trigger ──┤
          └─ IF (false) → Action B
```

The IF node creates two output paths. Downstream nodes only receive items from their connected path.

## Key Concepts

- **Continue On Fail**: A node setting that lets the workflow continue even if the node errors
- **Always Output Data**: Forces a node to output even when it would normally produce nothing
- **Pairing Mode**: How multi-input nodes match items

## Practice Workflows

Look for files related to:
- Data transformations
- Conditional routing
- Merging branches

## Next

[04 - Code & JavaScript](../04-code-and-javascript/) — when visual nodes aren't enough.
