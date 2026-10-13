# 06 - Agents & RAG

## From Chains to Agents

| Type | Behavior | Best For |
|------|----------|----------|
| **LLM Chain** | Fixed sequence of steps | Predictable tasks |
| **Agent** | Decides which tools to use | Open-ended tasks |
| **RAG** | Retrieves relevant context first | Knowledge-grounded answers |
| **Multi-Agent** | Specialized agents collaborate | Complex workflows |

## Agent Mental Model

```
User Request
     │
     ▼
┌─────────────┐
│   Agent     │ ← Has tools, memory, system prompt
│  (LLM +     │
│   Tools)    │
└─────────────┘
     │
     ├─ Tool: Search Web
     ├─ Tool: Query Database
     ├─ Tool: Send Email
     └─ Tool: Calculate
```

The agent loops: think → choose tool → observe result → think again → until done.

## RAG Pattern

1. **Ingest**: Chunk documents → embed → store in vector DB
2. **Retrieve**: User query → embed → similarity search → top-k chunks
3. **Generate**: Prompt = system + retrieved context + user question → LLM

## Key Components in n8n

- **AI Agent** node (with tool calling)
- **Vector Store** nodes (Pinecone, Supabase, Qdrant, etc.)
- **Memory** nodes (short-term and long-term)
- **Embeddings** nodes
- **Tool** nodes (custom tools the agent can call)

## Important Files

- AI Agent from Scratch
- RAG Agent examples
- WhatsApp + Supabase memory agents
- Multi-agent systems
- Vectorise from Drive to Pinecone

## Best Practices

1. Start with a simple chain, graduate to agent only when needed
2. Give agents clear tool descriptions
3. Limit tool count (too many confuses the model)
4. Add memory for multi-turn conversations
5. Always include a "final answer" instruction

## Next

[07 - Integrations](../07-integrations/) — connecting to real services.
