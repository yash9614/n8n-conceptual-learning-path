# n8n Conceptual Learning Path

> A structured, concept-first approach to mastering n8n — the open-source workflow automation platform.

This repository reorganizes a large collection of n8n workflows, templates, and instructional materials into a clear learning path. The focus is on **understanding concepts** (how data flows, why nodes behave the way they do, mental models for agents vs. workflows) rather than just importing JSON files.

## Why This Structure?

Most n8n resources dump hundreds of templates. That's useful once you understand the platform, but overwhelming when you're learning. Here we progress from fundamentals → data handling → AI capabilities → advanced patterns.

## Learning Path

| Module | Focus | Key Concepts |
|--------|-------|--------------|
| [00 - Getting Started](./00-getting-started/) | Setup & first workflow | Editor, execution, self-hosting |
| [01 - Fundamentals](./01-fundamentals/) | Workflows, nodes, triggers | Trigger → Action model, item vs. list |
| [02 - Data & Expressions](./02-data-expressions/) | How n8n handles data | JSON structure, expressions, item pairing |
| [03 - Core Nodes](./03-core-nodes/) | Essential building blocks | IF, Switch, Set, Merge, Wait, etc. |
| [04 - Code & JavaScript](./04-code-and-javascript/) | Custom logic | Code node, `$json`, `$items`, functions |
| [05 - AI & LLMs](./05-ai-llms/) | Adding intelligence | LLM chains, prompts, basic AI nodes |
| [06 - Agents & RAG](./06-agents-rag/) | Autonomous systems | Tools, memory, vector stores, multi-agent |
| [07 - Integrations](./07-integrations/) | Connecting the world | HTTP Request, credentials, webhooks |
| [08 - Advanced Patterns](./08-advanced/) | Production techniques | Error handling, sub-workflows, queues |
| [09 - Templates Gallery](./09-templates/) | Real-world examples | Curated, categorized workflows |

## Quick Start

1. **Set up n8n** (see [00-getting-started](./00-getting-started/))
2. Follow modules in order, or jump to topics you need
3. Import workflows from each module's `workflows/` folder
4. Read the module README *before* opening the workflow — the concepts matter more than the nodes

## How to Use the Workflows

Every JSON file can be imported into n8n:
1. Open n8n → Workflows → Import from File
2. Select the `.json` file
3. Configure credentials as needed
4. Activate and test

**Pro tip**: Open the workflow, then look at the sticky notes and node names. Many original files contain explanatory comments.

## Resources

- [Official n8n Docs](https://docs.n8n.io)
- [n8n Community](https://community.n8n.io)
- [Templates in this repo](./09-templates/)
- Cheatsheets and PDFs in `/resources`

## Contributing

This is a learning-oriented reorganization. Feel free to improve READMEs, add better examples, or categorize templates more finely.

---

*Structured for conceptual learning. Original materials collected from various n8n courses and community sources.*
