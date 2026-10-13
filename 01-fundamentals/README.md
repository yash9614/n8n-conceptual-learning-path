# 01 - Fundamentals

## Core Concepts

### Workflow
A workflow is a directed graph of nodes. It defines *what happens* when triggered. Workflows can be active (running continuously) or inactive (manual execution only).

### Nodes
Nodes are the building blocks. Every node has:
- **Inputs**: Data coming from previous nodes
- **Parameters**: Configuration you set in the UI
- **Outputs**: Data sent to the next node(s)

### Items
n8n processes data as **items**. An item is a JSON object. Most nodes process *one item at a time* by default (item mode), but some can process all items together (all items mode).

**Critical insight**: Understanding item pairing is the #1 skill that separates beginners from proficient n8n users.

### Triggers vs. Actions
- **Trigger nodes** start a workflow (Webhook, Schedule, Manual, etc.)
- **Action nodes** do something with data (HTTP Request, Slack, Google Sheets, etc.)

## Execution Model

When you execute a workflow:
1. Trigger fires and produces one or more items
2. Each subsequent node receives those items
3. Nodes can split, merge, filter, or transform items
4. Final nodes produce the end result

## Key Files in This Module

- `Build Your First n8n Workflow Step by Step.json` — Hands-on starter
- `Build Your First Automation with n8n.json` — Simple automation example
- Various introductory PDFs in `/resources`

## Exercises

1. Create a workflow that fetches the current time and sends it somewhere
2. Observe how adding a second item changes downstream nodes
3. Experiment with the "Execute Node" vs "Execute Workflow" buttons

## Next

Move to [02 - Data & Expressions](../02-data-expressions/) — this is where most people get stuck.
