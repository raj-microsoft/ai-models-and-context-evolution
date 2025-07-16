
# AI Context Evolution Workshop: The Journey to MCP

This workshop demonstrates the evolution of providing context to AI models, from basic chat to function calling, s## 📞 Quick Test Checklist

- `01-static-context-via-system-prompts.http`: Static prompt limitations
- `02-dynamic-context-multi-turn-conversation.http`: Dynamic progression
- `04-modern-tools-current-best-practice.http`: Function calling capabilities
- `07-assistants-api-with-document-search.http`: Assistants + Vector Store
- `08-complete-rag-workflow-with-embeddings.http`: Full RAG workflow

## 🎯 What Makes This Workshop Special

It's not just about calling tools—it's about understanding **why** context matters, **how** approaches evolved, and **what challenges** led to the creation of MCP.

## 🔗 Continue Your Journey

**Ready to see how MCP revolutionizes everything you've learned here?**

👉 **[Microsoft MCP for Beginners](https://github.com/microsoft/mcp-for-beginners)**

This next step will show you how MCP addresses every limitation and challenge you've experienced in this workshop, providing a unified, standardized approach to AI context and tool integration.e arrived at the need for the Model Context Protocol (MCP). This is a **foundational learning experience** that prepares you for the next step: diving deep into MCP itself.

## 🎯 Workshop Objectives

Understand the evolution of AI context provision and why MCP emerged:

1. **Traditional AI**: Limited to training data  
2. **Function Calling**: Manual, predefined functions  
3. **Modern Tools**: Better orchestration, multiple calls  
4. **The MCP Solution**: Dynamic, discoverable, standardized context

## 🚀 What's Next? Dive Deep into MCP!

After completing this workshop, you'll be ready to explore the **Model Context Protocol** in depth. Continue your journey with:

**👉 [Microsoft MCP for Beginners](https://github.com/microsoft/mcp-for-beginners)**

This comprehensive guide will teach you how to:
- Build your own MCP servers
- Integrate MCP with various applications
- Implement real-world MCP solutions
- Understand MCP's architecture and protocols  

## 📁 Project Structure

```
ai-context-evolution-workshop/
├── http-examples/                  # REST Client examples showing progression
│   ├── 01-static-context-via-system-prompts.http
│   ├── 02-dynamic-context-multi-turn-conversation.http
│   ├── 03-legacy-function-calling-deprecated.http
│   ├── 04-modern-tools-current-best-practice.http
│   ├── 05-parallel-multiple-tool-execution.http
│   ├── 06-complete-tool-calling-workflow.http
│   ├── 07-assistants-api-with-document-search.http
│   └── 08-complete-rag-workflow-with-embeddings.http
├── notebooks/                      # Jupyter notebooks for deep exploration
│   ├── 01_context_methods_and_prompting.ipynb
│   ├── 02_function_calling_legacy_format.ipynb
│   ├── 03_function_calling_modern_tools.ipynb
│   ├── 04_parallel_multiple_tool_execution.ipynb
│   ├── 05_assistants_api_with_vector_stores.ipynb
│   └── 06_complete_rag_pipeline_deep_dive.ipynb
├── assets/
│   └── conference_session_data_sample.json
├── .vscode/
│   └── settings.json
├── .env                            # Environment variables (create this!)
├── requirements.txt
└── README.md
```

## 🚀 Getting Started

### 1. VS Code Configuration

Create the `.vscode/settings.json` file for REST Client extension:

```json
{
  "rest-client.environmentVariables": {
    "$shared": {
      "endpoint": "{{$dotenv AZURE_OPENAI_ENDPOINT}}",
      "apiKey": "{{$dotenv AZURE_OPENAI_API_KEY}}",
      "gpt4oDeployment": "{{$dotenv AZURE_OPENAI_GPT4O_DEPLOYMENT_NAME}}",
      "apiVersion": "{{$dotenv AZURE_OPENAI_GPT4O_API_VERSION}}",
      "embeddingsDeployment": "{{$dotenv AZURE_OPENAI_EMBEDDINGS_DEPLOYMENT_NAME}}",
      "embeddingsApiVersion": "{{$dotenv AZURE_OPENAI_EMBEDDINGS_API_VERSION}}"
    }
  }
}
```

### 2. Environment Variables Setup

Create a `.env` file with your Azure OpenAI credentials:

```env
# Azure OpenAI Configuration
AZURE_OPENAI_ENDPOINT=https://your-resource.openai.azure.com/
AZURE_OPENAI_API_KEY=your-api-key-here

# GPT-4o Deployment
AZURE_OPENAI_GPT4O_DEPLOYMENT_NAME=gpt-4o
AZURE_OPENAI_GPT4O_API_VERSION=2025-01-01-preview

# Embeddings Deployment
AZURE_OPENAI_EMBEDDINGS_DEPLOYMENT_NAME=text-embedding-3-large
AZURE_OPENAI_EMBEDDINGS_API_VERSION=2023-05-15
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Try the HTTP Examples

- Open any `.http` file in `http-examples`
- Click **Send Request** in VS Code
- REST Client will auto-use `.env` variables

### 5. Explore the Notebooks

- Start with `notebooks/01_basic_context_methods.ipynb`
- Follow the sequence to build understanding step-by-step

## 📚 Learning Path

### Phase 1: Understanding Context Evolution

- `01-static-context-via-system-prompts.http`
- `02-dynamic-context-multi-turn-conversation.http`
- `notebooks/01_context_methods_and_prompting.ipynb`

### Phase 2: Function Calling Evolution

- `03-legacy-function-calling-deprecated.http`
- `04-modern-tools-current-best-practice.http`
- `05-parallel-multiple-tool-execution.http`
- `06-complete-tool-calling-workflow.http`

### Phase 3: Deep Dive Notebooks

- `notebooks/02_function_calling_legacy_format.ipynb`
- `notebooks/03_function_calling_modern_tools.ipynb`
- `notebooks/04_parallel_multiple_tool_execution.ipynb`

### Phase 4: Document Intelligence & RAG

- `07-assistants-api-with-document-search.http`
- `notebooks/05_assistants_api_with_vector_stores.ipynb`
- `08-complete-rag-workflow-with-embeddings.http`
- `notebooks/06_complete_rag_pipeline_deep_dive.ipynb`

### Phase 5: Ready for MCP!

Once you've completed this workshop, you'll understand the challenges and limitations of traditional approaches, making you ready to appreciate the revolutionary changes that MCP brings.

**🎯 Next Step**: Head to [Microsoft MCP for Beginners](https://github.com/microsoft/mcp-for-beginners) to learn how MCP solves these challenges with:
- Dynamic tool discovery
- Standardized protocols  
- Cross-application context sharing
- Seamless integration across tools and platforms

## 🎓 Key Learning Outcomes

By the end of this workshop, you'll understand:

- ✅ The Context Problem and its evolution
- ✅ Static & Dynamic Context techniques
- ✅ Function Calling Evolution and limitations
- ✅ Performance Implications of different approaches
- ✅ Best Practices for Tools and RAG
- ✅ Document Intelligence & Vector Search
- ✅ Why MCP emerged as the solution

**🚀 Ready for MCP?** After completing this workshop, you'll have the foundation to understand why MCP is revolutionary and how it solves the challenges you've experienced here.

## 🛠️ Technical Requirements

- Azure OpenAI with GPT-4o + `text-embedding-3-large`
- VS Code with REST Client extension
- Python 3.8+
- `.env` file with required variables
- `requirements.txt` installed

## 📞 Quick Test Checklist

- `01-basic-chat.http`: See limited capabilities
- `02-system-prompt-context.http`: Static prompt
- `03-multi-turn-context.http`: Dynamic progression
- `05-modern-tools.http`: Function calling
- `08-assistants-vector-store.http`: Assistants + Vector Store
- `09-rag-with-embeddings.http`: Full RAG workflow

## 🎯 What Makes This Workshop Special

It’s not just about calling tools—it’s about **why** context matters and **how** MCP changes everything.

## ❓ Frequently Asked Questions (FAQ)

### 🔍 Embeddings & Vector Search

**Q:** What are embeddings?  
**A:** Vector representations of text capturing semantic meaning.

**Q:** What model should I use?  
**A:** `text-embedding-3-large` for best results; use `-small` or `ada` for cost savings.

### 🏗️ RAG (Retrieval-Augmented Generation)

**Q:** When to use RAG vs Assistants?  
**A:** RAG = control; Assistants = simplicity + memory.

**Q:** How to handle large docs?  
**A:** Chunking, metadata, hierarchical summaries.

### 📊 Vector Stores

**Q:** Azure AI Search vs custom DB?  
**A:** Azure for production; custom if specialized needs.

### 💰 Cost Optimization

**Q:** Reduce embedding cost?  
**A:** Cache, batch, chunk smartly, use smaller models.

### 🔧 Technical Implementation

**Q:** Debug poor RAG?  
**A:** Check embeddings, chunking, context window, prompts.

### 🛡️ Security

**Q:** How to secure vector data?  
**A:** RBAC, encryption, managed identities.

### 🚀 Scaling

**Q:** How to scale RAG?  
**A:** Caching, horizontal scaling, async updates.

### 🎯 Choosing the Right Tool

| Use Case         | Best Approach      | Why                          |
|------------------|--------------------|-------------------------------|
| Real-time data   | Function Calling   | Live API access               |
| Document Q&A     | RAG or Assistants  | Semantic search               |
| Conversational   | Assistants API     | Built-in memory               |
| Custom systems   | Function Calling   | Full control                  |
| Prototypes       | Assistants API     | Quick setup                   |

---

Ready to understand how we went from limited AI to unlimited possibilities? **Let’s dive in!** 🚀
