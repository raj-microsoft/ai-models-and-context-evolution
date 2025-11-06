# AI Context Evolution Workshop: The Journey to MCP

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Azure OpenAI](https://img.shields.io/badge/Azure-OpenAI-orange.svg)](https://azure.microsoft.com/en-us/products/ai-services/openai-service)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Workshop](https://img.shields.io/badge/Type-Workshop-green.svg)](https://github.com/raj-microsoft/ai-models-and-context-evolution)

## 📖 Overview

This workshop demonstrates the evolution of providing context to AI models, from basic chat to function calling, and how we arrived at the need for the Model Context Protocol (MCP). This is a **foundational learning experience** that prepares you for the next step: diving deep into MCP itself.

Whether you're a developer, architect, or AI enthusiast, this hands-on workshop will guide you through the practical challenges and solutions in AI context management, giving you the knowledge foundation to understand why MCP is revolutionary.

## 🎯 Workshop Objectives

Understand the evolution of AI context provision and why MCP emerged:

1. **Traditional AI**: Limited to training data  
2. **Function Calling**: Manual, predefined functions  
3. **Modern Tools**: Better orchestration, multiple calls  
4. **The MCP Solution**: Dynamic, discoverable, standardized context

## 🏗️ Workshop Architecture

This workshop progressively builds your understanding through four key evolution stages:

```
┌─────────────────────────────────────────────────────────────────┐
│                    AI CONTEXT EVOLUTION                         │
└─────────────────────────────────────────────────────────────────┘

Stage 1: Static Context                Stage 2: Dynamic Context
┌──────────────────────┐              ┌──────────────────────┐
│  System Prompts      │              │  Multi-turn Chat     │
│  • Limited           │    →         │  • Conversational    │
│  • Pre-defined       │              │  • Context Building  │
│  • No Updates        │              │  • Memory            │
└──────────────────────┘              └──────────────────────┘
         ↓                                      ↓
Stage 3: Function Calling               Stage 4: Advanced RAG
┌──────────────────────┐              ┌──────────────────────┐
│  Tool Integration    │              │  Vector Search       │
│  • Real-time Data    │    →         │  • Document Intel    │
│  • API Calls         │              │  • Semantic Search   │
│  • Parallel Tools    │              │  • Knowledge Bases   │
└──────────────────────┘              └──────────────────────┘
         ↓
┌─────────────────────────────────────────────────────────────────┐
│              🚀 Ready for Model Context Protocol                │
│  Unified, Standardized, Dynamic Context for Modern AI           │
└─────────────────────────────────────────────────────────────────┘
```

### Learning Modalities

- **📄 HTTP Examples**: Quick, interactive API calls via REST Client
- **📓 Jupyter Notebooks**: Deep dives with code explanations and experiments
- **🎯 Progressive Complexity**: Each stage builds on previous knowledge

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
ai-models-and-context-evolution/
├── http-examples/                  # REST Client examples showing progression
│   ├── 01_static_context_via_system_prompts.http
│   ├── 02_dynamic_context_multi_turn_conversation.http
│   ├── 03_legacy_function_calling_deprecated.http
│   ├── 04_modern_tools_current_best_practice.http
│   ├── 05_parallel_multiple_tool_execution.http
│   ├── 06_complete_tool_calling_workflow.http
│   ├── 07_assistants_api_with_document_search.http
│   └── 08_complete_rag_workflow_with_embeddings.http
├── notebooks/                      # Jupyter notebooks for deep exploration
│   ├── 01_context_methods_and_prompting.ipynb
│   ├── 02_function_calling_legacy_format.ipynb
│   ├── 03_function_calling_modern_tools.ipynb
│   ├── 04_parallel_multiple_tool_execution.ipynb
│   ├── 05_assistants_api_with_vector_stores.ipynb
│   ├── 06_complete_rag_pipeline_deep_dive.ipynb
│   └── sample_knowledge_base_document.txt
├── assets/
│   └── conference_session_data_sample.json
├── .env                            # Environment variables (create this!)
├── requirements.txt
└── README.md
```

## ⚡ Quick Start (5 Minutes)

Already familiar with Azure OpenAI? Get started immediately:

```bash
# 1. Clone the repository
git clone https://github.com/raj-microsoft/ai-models-and-context-evolution.git
cd ai-models-and-context-evolution

# 2. Create .env file with your credentials
cat > .env << EOF
AZURE_OPENAI_ENDPOINT=https://your-resource.openai.azure.com/
AZURE_OPENAI_API_KEY=your-api-key-here
AZURE_OPENAI_GPT4O_DEPLOYMENT_NAME=gpt-4o
AZURE_OPENAI_GPT4O_API_VERSION=2025-01-01-preview
AZURE_OPENAI_EMBEDDINGS_DEPLOYMENT_NAME=text-embedding-3-large
AZURE_OPENAI_EMBEDDINGS_API_VERSION=2023-05-15
EOF

# 3. Install dependencies
pip install -r requirements.txt

# 4. Start exploring!
# Open http-examples/01_static_context_via_system_prompts.http in VS Code
```

## 🚀 Getting Started (Detailed)

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

- Start with `notebooks/01_context_methods_and_prompting.ipynb`
- Follow the sequence to build understanding step-by-step

## 📚 Learning Path

### Phase 1: Understanding Context Evolution

- `01_static_context_via_system_prompts.http`
- `02_dynamic_context_multi_turn_conversation.http`
- `notebooks/01_context_methods_and_prompting.ipynb`

### Phase 2: Function Calling Evolution

- `03_legacy_function_calling_deprecated.http`
- `04_modern_tools_current_best_practice.http`
- `05_parallel_multiple_tool_execution.http`
- `06_complete_tool_calling_workflow.http`

### Phase 3: Deep Dive Notebooks

- `notebooks/02_function_calling_legacy_format.ipynb`
- `notebooks/03_function_calling_modern_tools.ipynb`
- `notebooks/04_parallel_multiple_tool_execution.ipynb`

### Phase 4: Document Intelligence & RAG

- `07_assistants_api_with_document_search.http`
- `notebooks/05_assistants_api_with_vector_stores.ipynb`
- `08_complete_rag_workflow_with_embeddings.http`
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

### Essential Requirements
- **Azure OpenAI Service**: Active subscription with GPT-4o and `text-embedding-3-large` deployments
- **Python**: Version 3.8 or higher
- **VS Code**: With the [REST Client extension](https://marketplace.visualstudio.com/items?itemName=humao.rest-client)
- **Jupyter**: For running notebooks (installed via `requirements.txt`)

### Azure OpenAI Deployments Needed
1. **GPT-4o Model**: For chat completions and tool calling
2. **text-embedding-3-large**: For embeddings and vector search
3. **API Version**: `2025-01-01-preview` or later recommended

### Operating System
- Windows, macOS, or Linux supported
- Terminal/Command Prompt access for running Python commands

## 📞 Quick Test Checklist

- `01_static_context_via_system_prompts.http`: Static prompt limitations
- `02_dynamic_context_multi_turn_conversation.http`: Dynamic progression
- `04_modern_tools_current_best_practice.http`: Function calling capabilities
- `07_assistants_api_with_document_search.http`: Assistants + Vector Store
- `08_complete_rag_workflow_with_embeddings.http`: Full RAG workflow

## 🎯 What Makes This Workshop Special

This isn't just another AI tutorial—it's a comprehensive journey through the evolution of AI context management:

### 🔍 Deep Understanding
- **The Why**: Understand the fundamental problems each approach solves
- **The How**: Hands-on implementation of every pattern
- **The Evolution**: See how solutions evolved to address limitations
- **The Future**: Connect past challenges to MCP's revolutionary solutions

### 💪 Practical Skills
- **Production-Ready**: Learn patterns used in real-world applications
- **Best Practices**: Avoid common pitfalls and anti-patterns
- **Performance**: Understand cost, latency, and scalability implications
- **Tool Mastery**: Work with Azure OpenAI's full capabilities

### 🎓 Progressive Learning
- **Beginner Friendly**: Start from basics, no prior AI experience needed
- **Advanced Topics**: Progress to sophisticated RAG and tool patterns
- **Hands-on**: Every concept includes working code examples
- **Self-Paced**: Learn at your own speed with clear checkpoints

### 🌉 Bridge to MCP
This workshop uniquely positions you to understand **why MCP matters** by first experiencing the challenges it solves. You'll appreciate MCP's innovations because you've faced the limitations of traditional approaches firsthand.

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

## 🚧 Troubleshooting

### Common Issues and Solutions

#### Issue: Environment Variables Not Loading
**Solution**: 
- Ensure `.env` file is in the root directory
- Check that variable names match exactly as shown in setup
- Restart VS Code after creating/modifying `.env`

#### Issue: REST Client Not Finding Variables
**Solution**: 
- Verify `.vscode/settings.json` exists with correct configuration
- Ensure REST Client extension is installed and enabled
- Check that variable references use correct syntax: `{{$dotenv VARIABLE_NAME}}`

#### Issue: Azure OpenAI API Errors
**Solution**: 
- Verify your API key is valid and not expired
- Check that deployments exist in your Azure OpenAI resource
- Ensure API version is compatible (use `2025-01-01-preview` or later)
- Verify your Azure subscription has sufficient quota

#### Issue: Notebooks Not Running
**Solution**: 
- Run `pip install -r requirements.txt` to ensure all dependencies are installed
- Select correct Python kernel in Jupyter
- Restart kernel and clear outputs if experiencing issues

#### Issue: Embedding or Vector Search Failures
**Solution**: 
- Verify embeddings deployment name matches your Azure resource
- Check that you're using a compatible embeddings model
- Ensure sufficient quota for embedding operations

### Getting Help
- Check [Azure OpenAI Documentation](https://learn.microsoft.com/en-us/azure/ai-services/openai/)
- Review [OpenAI API Reference](https://platform.openai.com/docs/api-reference)
- Open an issue in this repository for workshop-specific problems

## 🗺️ Roadmap: Upcoming Features

We're continuously improving this workshop! Here are the planned enhancements:

### 🎯 Short-term Goals (Next Release)

- **Interactive Demos**: Web-based interactive examples to complement HTTP files
- **Video Tutorials**: Step-by-step video walkthroughs for each phase
- **Docker Support**: Containerized environment for consistent setup across platforms
- **Additional Notebooks**: 
  - Streaming responses and real-time interactions
  - Token optimization and cost management strategies
  - Error handling and retry logic patterns

### 🚀 Medium-term Goals (Upcoming Months)

- **Multi-language Support**: Examples in JavaScript/TypeScript, C#, and Java
- **Cloud Deployment Examples**: 
  - Deploy functions to Azure Functions
  - Host RAG solutions on Azure App Service
  - Use Azure Container Apps for scalable deployments
- **Advanced RAG Techniques**:
  - Hybrid search (keyword + semantic)
  - Re-ranking strategies
  - Query expansion and optimization
- **Monitoring and Observability**: Integration with Azure Monitor and Application Insights
- **Comparative Analysis**: Side-by-side comparison of different context approaches with metrics

### 🌟 Long-term Vision (Future)

- **MCP Integration Deep Dive**: Advanced workshop connecting this content directly to MCP patterns
- **Real-world Case Studies**: Production examples from various industries
- **Performance Benchmarking**: Automated testing framework for comparing approaches
- **AI Agent Patterns**: Multi-agent systems and orchestration patterns
- **Security Best Practices**: Deep dive into securing AI applications
- **Edge Computing Examples**: Running models at the edge with reduced context

### 💡 Community Requested Features

Have an idea for this workshop? We welcome contributions! Please:
1. Open an issue describing your suggestion
2. Tag it with `enhancement` label
3. Discuss with the community
4. Submit a PR if you'd like to implement it

## 🤝 Contributing

We welcome contributions to improve this workshop! Here's how you can help:

### Ways to Contribute

1. **Report Issues**: Found a bug or unclear documentation? Open an issue!
2. **Improve Documentation**: Fix typos, clarify explanations, add examples
3. **Add Examples**: Create new notebooks or HTTP examples
4. **Share Feedback**: Tell us what worked and what didn't in your learning journey
5. **Translate Content**: Help make this workshop accessible in other languages

### Contribution Guidelines

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Make your changes with clear, descriptive commits
4. Test your changes thoroughly
5. Update documentation as needed
6. Submit a pull request with a clear description

### Code of Conduct

We're committed to providing a welcoming and inclusive experience for everyone. Please:
- Be respectful and constructive
- Focus on what's best for the community
- Show empathy towards others
- Accept constructive criticism gracefully

## 📚 Additional Resources

### Official Documentation
- [Azure OpenAI Service](https://learn.microsoft.com/en-us/azure/ai-services/openai/)
- [OpenAI API Documentation](https://platform.openai.com/docs)
- [Model Context Protocol (MCP)](https://github.com/microsoft/mcp-for-beginners)

### Related Learning Paths
- [Azure AI Fundamentals](https://learn.microsoft.com/en-us/training/paths/get-started-with-artificial-intelligence-on-azure/)
- [Develop AI solutions with Azure OpenAI](https://learn.microsoft.com/en-us/training/paths/develop-ai-solutions-azure-openai/)

### Community and Support
- [Azure OpenAI Discussion Forum](https://github.com/Azure/azure-openai/discussions)
- [OpenAI Developer Community](https://community.openai.com/)

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Thanks to the Azure OpenAI team for providing the platform
- Inspired by the evolution of AI context management patterns
- Built to prepare developers for the Model Context Protocol revolution
- Community contributors who helped improve this workshop

## 🔗 Continue Your Journey

**Ready to see how MCP revolutionizes everything you've learned here?**

👉 **[Microsoft MCP for Beginners](https://github.com/microsoft/mcp-for-beginners)**

This next step will show you how MCP addresses every limitation and challenge you've experienced in this workshop, providing a unified, standardized approach to AI context and tool integration.

---

Ready to understand how we went from limited AI to unlimited possibilities? **Let's dive in!** 🚀