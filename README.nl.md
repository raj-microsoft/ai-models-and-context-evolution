# AI Context Evolutie Workshop: De Reis naar MCP

Deze workshop demonstreert de evolutie van het verstrekken van context aan AI-modellen, van eenvoudige chat tot function calling, en hoe we tot de behoefte aan het Model Context Protocol (MCP) zijn gekomen. Dit is een **fundamentele leerervaring** die je voorbereidt op de volgende stap: een diepe duik in MCP zelf.

## 🎯 Workshopdoelstellingen

Begrijp de evolutie van AI-contextvoorziening en waarom MCP is ontstaan:

1. **Traditionele AI**: Beperkt tot trainingsdata  
2. **Function Calling**: Handmatige, vooraf gedefinieerde functies  
3. **Moderne Tools**: Betere orkestratie, meerdere aanroepen  
4. **De MCP-Oplossing**: Dynamische, ontdekbare, gestandaardiseerde context

## 🚀 Wat Volgt? Duik Diep in MCP!

Na het voltooien van deze workshop ben je klaar om het **Model Context Protocol** diepgaand te verkennen. Vervolg je reis met:

**👉 [Microsoft MCP voor Beginners](https://github.com/microsoft/mcp-for-beginners)**

Deze uitgebreide gids leert je hoe je:
- Je eigen MCP-servers kunt bouwen
- MCP kunt integreren met verschillende applicaties
- Praktische MCP-oplossingen kunt implementeren
- De architectuur en protocollen van MCP kunt begrijpen  

## 📁 Projectstructuur

```
ai-models-and-context-evolution/
├── http-examples/                  # REST Client voorbeelden met progressie
│   ├── 01_static_context_via_system_prompts.http
│   ├── 02_dynamic_context_multi_turn_conversation.http
│   ├── 03_legacy_function_calling_deprecated.http
│   ├── 04_modern_tools_current_best_practice.http
│   ├── 05_parallel_multiple_tool_execution.http
│   ├── 06_complete_tool_calling_workflow.http
│   ├── 07_assistants_api_with_document_search.http
│   └── 08_complete_rag_workflow_with_embeddings.http
├── notebooks/                      # Jupyter notebooks voor diepgaande verkenning
│   ├── 01_context_methods_and_prompting.ipynb
│   ├── 02_function_calling_legacy_format.ipynb
│   ├── 03_function_calling_modern_tools.ipynb
│   ├── 04_parallel_multiple_tool_execution.ipynb
│   ├── 05_assistants_api_with_vector_stores.ipynb
│   ├── 06_complete_rag_pipeline_deep_dive.ipynb
│   └── sample_knowledge_base_document.txt
├── assets/
│   └── conference_session_data_sample.json
├── .env                            # Omgevingsvariabelen (maak deze aan!)
├── requirements.txt
└── README.md
```

## 🚀 Aan de Slag

### 1. VS Code Configuratie

Maak het `.vscode/settings.json` bestand voor de REST Client extensie:

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

### 2. Omgevingsvariabelen Instellen

Maak een `.env` bestand met je Azure OpenAI inloggegevens:

```env
# Azure OpenAI Configuratie
AZURE_OPENAI_ENDPOINT=https://your-resource.openai.azure.com/
AZURE_OPENAI_API_KEY=your-api-key-here

# GPT-4o Deployment
AZURE_OPENAI_GPT4O_DEPLOYMENT_NAME=gpt-4o
AZURE_OPENAI_GPT4O_API_VERSION=2025-01-01-preview

# Embeddings Deployment
AZURE_OPENAI_EMBEDDINGS_DEPLOYMENT_NAME=text-embedding-3-large
AZURE_OPENAI_EMBEDDINGS_API_VERSION=2023-05-15
```

### 3. Installeer Afhankelijkheden

```bash
pip install -r requirements.txt
```

### 4. Probeer de HTTP Voorbeelden

- Open een `.http` bestand in `http-examples`
- Klik op **Send Request** in VS Code
- REST Client gebruikt automatisch de `.env` variabelen

### 5. Verken de Notebooks

- Begin met `notebooks/01_context_methods_and_prompting.ipynb`
- Volg de volgorde om stap voor stap begrip op te bouwen

## 📚 Leerpad

### Fase 1: Context Evolutie Begrijpen

- `01_static_context_via_system_prompts.http`
- `02_dynamic_context_multi_turn_conversation.http`
- `notebooks/01_context_methods_and_prompting.ipynb`

### Fase 2: Function Calling Evolutie

- `03_legacy_function_calling_deprecated.http`
- `04_modern_tools_current_best_practice.http`
- `05_parallel_multiple_tool_execution.http`
- `06_complete_tool_calling_workflow.http`

### Fase 3: Diepgaande Notebooks

- `notebooks/02_function_calling_legacy_format.ipynb`
- `notebooks/03_function_calling_modern_tools.ipynb`
- `notebooks/04_parallel_multiple_tool_execution.ipynb`

### Fase 4: Document Intelligentie & RAG

- `07_assistants_api_with_document_search.http`
- `notebooks/05_assistants_api_with_vector_stores.ipynb`
- `08_complete_rag_workflow_with_embeddings.http`
- `notebooks/06_complete_rag_pipeline_deep_dive.ipynb`

### Fase 5: Klaar voor MCP!

Zodra je deze workshop hebt voltooid, begrijp je de uitdagingen en beperkingen van traditionele benaderingen, waardoor je klaar bent om de revolutionaire veranderingen die MCP brengt te waarderen.

**🎯 Volgende Stap**: Ga naar [Microsoft MCP voor Beginners](https://github.com/microsoft/mcp-for-beginners) om te leren hoe MCP deze uitdagingen oplost met:
- Dynamische tool-ontdekking
- Gestandaardiseerde protocollen  
- Cross-applicatie context delen
- Naadloze integratie tussen tools en platforms

## 🎓 Belangrijkste Leerresultaten

Na afloop van deze workshop begrijp je:

- ✅ Het Contextprobleem en de evolutie ervan
- ✅ Statische & Dynamische Context technieken
- ✅ Function Calling Evolutie en beperkingen
- ✅ Prestatie-implicaties van verschillende benaderingen
- ✅ Best Practices voor Tools en RAG
- ✅ Document Intelligentie & Vector Search
- ✅ Waarom MCP is ontstaan als de oplossing

**🚀 Klaar voor MCP?** Na het voltooien van deze workshop heb je de basis om te begrijpen waarom MCP revolutionair is en hoe het de uitdagingen oplost die je hier hebt ervaren.

## 🛠️ Technische Vereisten

- Azure OpenAI met GPT-4o + `text-embedding-3-large`
- VS Code met REST Client extensie
- Python 3.8+
- `.env` bestand met vereiste variabelen
- `requirements.txt` geïnstalleerd

## 📞 Snelle Test Checklist

- `01_static_context_via_system_prompts.http`: Statische prompt beperkingen
- `02_dynamic_context_multi_turn_conversation.http`: Dynamische progressie
- `04_modern_tools_current_best_practice.http`: Function calling mogelijkheden
- `07_assistants_api_with_document_search.http`: Assistants + Vector Store
- `08_complete_rag_workflow_with_embeddings.http`: Volledige RAG workflow

## 🎯 Wat Deze Workshop Speciaal Maakt

Het gaat niet alleen om het aanroepen van tools—het gaat om het begrijpen **waarom** context belangrijk is, **hoe** benaderingen zijn geëvolueerd, en **welke uitdagingen** hebben geleid tot de creatie van MCP.

## 🇳🇱 Nederlandse Context

Deze workshop bevat voorbeelden die specifiek relevant zijn voor Nederland:
- **Steden**: Amsterdam, Rotterdam, Utrecht, Den Haag, Eindhoven
- **Bedrijven**: Nederlandse tech-startups, Schiphol, NS, KPN
- **Weer**: Nederlands klimaat en weerpatronen
- **Reizen**: Treinreizen via NS, vluchten vanaf Schiphol
- **Tijdzones**: Europa/Amsterdam (CET/CEST)

## ❓ Veelgestelde Vragen (FAQ)

### 🔍 Embeddings & Vector Search

**V:** Wat zijn embeddings?  
**A:** Vectorrepresentaties van tekst die semantische betekenis vastleggen.

**V:** Welk model moet ik gebruiken?  
**A:** `text-embedding-3-large` voor de beste resultaten; gebruik `-small` of `ada` voor kostenbesparingen.

### 🏗️ RAG (Retrieval-Augmented Generation)

**V:** Wanneer RAG vs Assistants gebruiken?  
**A:** RAG = controle; Assistants = eenvoud + geheugen.

**V:** Hoe ga je om met grote documenten?  
**A:** Chunking, metadata, hiërarchische samenvattingen.

### 📊 Vector Stores

**V:** Azure AI Search vs aangepaste database?  
**A:** Azure voor productie; aangepast als je gespecialiseerde behoeften hebt.

### 💰 Kostenoptimalisatie

**V:** Embedding-kosten verlagen?  
**A:** Cache, batch, slim chunken, kleinere modellen gebruiken.

### 🔧 Technische Implementatie

**V:** Slechte RAG debuggen?  
**A:** Controleer embeddings, chunking, contextvenster, prompts.

### 🛡️ Beveiliging

**V:** Hoe vectordata beveiligen?  
**A:** RBAC, versleuteling, beheerde identiteiten.

### 🚀 Schalen

**V:** Hoe RAG schalen?  
**A:** Caching, horizontaal schalen, asynchrone updates.

### 🎯 De Juiste Tool Kiezen

| Gebruikssituatie    | Beste Aanpak       | Waarom                        |
|--------------------|--------------------|-------------------------------|
| Real-time data     | Function Calling   | Live API-toegang              |
| Document Q&A       | RAG of Assistants  | Semantisch zoeken             |
| Conversationeel    | Assistants API     | Ingebouwd geheugen            |
| Aangepaste systemen| Function Calling   | Volledige controle            |
| Prototypes         | Assistants API     | Snelle opzet                  |

## 🔗 Vervolg Je Reis

**Klaar om te zien hoe MCP alles revolutioneert wat je hier hebt geleerd?**

👉 **[Microsoft MCP voor Beginners](https://github.com/microsoft/mcp-for-beginners)**

Deze volgende stap laat je zien hoe MCP elke beperking en uitdaging aanpakt die je in deze workshop hebt ervaren, en een uniforme, gestandaardiseerde aanpak biedt voor AI-context en tool-integratie.

---

Klaar om te begrijpen hoe we van beperkte AI naar onbeperkte mogelijkheden zijn gegaan? **Laten we beginnen!** 🚀
