# 00 - Getting Started with n8n

## What is n8n?

n8n (pronounced "n-eight-n") is a fair-code workflow automation platform. Think of it as a visual programming environment where you connect nodes to automate tasks, integrate services, and build AI-powered agents.

**Key differentiators**:
- **Visual + Code**: Drag-and-drop canvas *plus* full JavaScript when you need it
- **Self-hostable**: Run on your own server (Docker, Kubernetes, etc.)
- **AI-native**: First-class support for LLMs, agents, and RAG
- **1500+ integrations**: Plus the HTTP Request node for anything else

## Mental Model

```
Trigger  →  Process  →  Action
   │           │          │
Webhook    Transform    Slack
Schedule   LLM Call     Database
Manual     Filter       Email
```

Every workflow starts with a **Trigger** (something happens) and ends with one or more **Actions** (something is done). In between, you transform, decide, and enrich data.

## Setup Options

### Option 1: n8n Cloud (fastest)
Go to [n8n.cloud](https://n8n.cloud) and create an account. No setup required.

### Option 2: Docker (recommended for learning)
```bash
docker volume create n8n_data
docker run -it --rm --name n8n -p 5678:5678 -v n8n_data:/home/node/.n8n docker.n8n.io/n8nio/n8n
```
Open http://localhost:5678

### Option 3: npx (Node.js required)
```bash
npx n8n
```

## Your First Workflow

1. Click **+** to create a new workflow
2. Add a **Manual Trigger** node
3. Add a **Set** node and create a field called `message` with value `"Hello n8n!"`
4. Click **Execute Workflow**
5. Observe the output in the right panel

**Concept to internalize**: Data flows from left to right. Each node receives items from the previous node and outputs new items.

## Next Steps

Continue to [01 - Fundamentals](../01-fundamentals/) to understand workflows, nodes, and execution model in depth.
