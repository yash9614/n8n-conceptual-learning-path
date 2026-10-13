# 05 - AI & LLMs

## Adding Intelligence to Workflows

n8n has first-class AI support. You can:
- Call any LLM (OpenAI, Anthropic, Google, local models via Ollama)
- Build chains (prompt → LLM → parse → action)
- Create agents that use tools
- Implement RAG (Retrieval-Augmented Generation)

## Basic Pattern: LLM Chain

```
Trigger → Set Prompt → LLM Node → Parse Output → Action
```

The LLM node receives a prompt and returns a completion. You control temperature, model, and system message.

## Key Concepts

### Prompts
- **System message**: Sets the AI's role and constraints
- **User message**: The actual task or question
- **Few-shot examples**: Show the model desired input/output patterns

### Output Parsing
LLMs return text. Use the **Structured Output Parser** or Code node to extract JSON, lists, or specific fields.

### Cost & Latency
- Smaller models are faster and cheaper
- Streaming is available for better UX
- Cache results when possible

## Common Use Cases

- Content generation (emails, posts, summaries)
- Classification and extraction
- Decision making based on unstructured text
- Translation and reformatting

## Key Workflows

- AI Document Summarizer
- AI LinkedIn Post Machine
- Business Ideas AI Agent (basic version)
- Various LLM chain examples

## Next

[06 - Agents & RAG](../06-agents-rag/) — when the AI needs to use tools and access knowledge.
