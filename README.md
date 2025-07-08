# RishiGPT

**RishiGPT** is an AI-native, generative assistant designed to deliver high-quality, context-aware responses through a modular, extensible framework. Built on Streamlit, LangChain, and Groq’s high-performance LLaMA backend, RishiGPT combines web search, Retrieval-Augmented Generation (RAG), and conversation memory to power intelligent workflows for developers, researchers, and anyone working with custom data.

**Live Demo:** [RishiGPT Streamlit App](https://rishigpt.streamlit.app/)

---

## Overview

RishiGPT is not just another chatbot—it’s an adaptable blueprint for building AI-first applications that reason over diverse knowledge sources. Whether extracting insights from a PDF, parsing live websites, embedding GitHub repositories, or running real-time web search, RishiGPT provides a unified pipeline that integrates file loaders, vector stores, embeddings, agent tools, and memory.

---

## Key Features

### 1. Web Search Agent

- Powered by LangChain’s SerpAPI integration and Groq’s LLaMA 4 backend.
- Execute live web searches to deliver timely, accurate responses beyond static context.

### 2. File-Based RAG

- Upload PDFs, text files, or supply live web URLs.
- Embedded using HuggingFace Transformers and indexed in FAISS.
- Query via ConversationalRetrievalChain for source-grounded answers.

### 3. GitHub Repository RAG

- Clone public GitHub repositories on the fly.
- Index repository files, embed using HuggingFace models, and enable semantic code/document Q&A.

### 4. Persistent Memory Embedding

- Use [RishiGPT Embedding Station](https://github.com/Rishirajbal/RishiGPT_Pinecone_PersistantMemory_Feature.git) to store documents and URLs in Pinecone with Cohere embeddings.
- Chat with pre-embedded indexes through a dedicated RAG pipeline.

### 5. Contextual Memory

- Built-in conversation buffer memory with up to 10-message history.
- Maintains conversational context for follow-ups, clarifications, and iterative querying.

### 6. Multi-Mode Toggle

- Switch seamlessly between:
  - File-RAG: PDF, text file, or live URL.
  - Web Search Agent: real-time search using SerpAPI.
  - Direct LLM chat for general questions.

### 7. Modular, Extensible Architecture

- Each module (RAG, agent tools, loaders, memory) is isolated and independently configurable.
- Designed to enable rapid experimentation, easy integration of new vector stores, embedding models, or agent workflows.

---

## Tech Stack

| Component              | Technology                                  |
|------------------------|---------------------------------------------|
| App UI                 | Streamlit                                   |
| LLM Inference          | Groq (Meta LLaMA 4)                         |
| Framework              | LangChain                                   |
| Vector Store           | FAISS, Pinecone (persistent mode)           |
| Embeddings             | HuggingFace Transformers, Cohere            |
| Memory                 | ConversationBufferMemory                    |
| Web Search             | SerpAPI                                     |
| File Loaders           | LangChain Community Loaders, GitLoader      |
| Deployment             | Streamlit Cloud                             |

---

## Installation

```bash
git clone https://github.com/YOUR_USERNAME/RishiGPT
cd RishiGPT

# Optional: create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
````

---

## Environment Variables

Create a `.streamlit/secrets.toml` (for Streamlit Cloud) or a local `.env` file:

```toml
GROQ_API_KEY = "your_groq_api_key"
SERPAPI_API_KEY = "your_serpapi_api_key"
```

---

## Running the App

```bash
streamlit run app_2.py
```

Access the app at `http://localhost:8501` or use your Streamlit Cloud deployment URL.

---

## Related Projects

### [RishiGPT+ (LangGraph Pipeline)](https://github.com/Rishirajbal/RishiGPT_PLUS.git)

RishiGPT+ pushes the boundaries of the current framework using [LangGraph](https://github.com/langchain-ai/langgraph) to introduce dynamic, graph-based orchestration for complex multi-step AI workflows. With LangGraph, future versions of RishiGPT will support advanced capabilities like:

* Multi-branch conversation flow and conditional routing.
* Sophisticated memory graphing and retention logic.
* Automatic tool switching for multi-agent workflows.
* Persistent state tracking across parallel tasks.

### [RishiGPT Persistent Memory (Pinecone)](https://github.com/Rishirajbal/RishiGPT_Pinecone_PersistantMemory_Feature.git)

A dedicated module for persistent storage of user files and URLs. Supports:

* Embedding with Cohere’s `embed-english-light-v3.0` model.
* Storage and retrieval via Pinecone vector database.
* Chat interface for querying existing indexes.
* Enables “embed once, chat forever” workflows.

---

## Roadmap & Vision

RishiGPT’s mission is to evolve into a fully autonomous, memory-aware, multi-agent AI development framework. The next phases will focus on:

* **LangGraph Orchestration:** Enable fine-grained workflow control, branching logic, and stateful multi-agent tasks that adapt based on user input, context, or triggers.
* **RAGAnything:** Expand the Retrieval-Augmented Generation pipeline into a truly *multimodal* knowledge system—supporting not only text, PDFs, and code repositories, but also diverse file types such as:

  * Video transcripts
  * Spreadsheets and tabular datasets
  * Markdown wikis and Notion exports
  * HTML dumps and raw JSON
  * Audio transcription
  * Presentation slide decks
  * Scientific datasets and CSVs
* **Memory-Aware Chat:** Integrate chunked or graph-based long-term vector memory to preserve conversation context over extended sessions or projects.
* **End-to-End Code Generation:** Automatically generate functions, classes, or modules based on contextual prompts and retrieved knowledge.
* **n8n Workflow Connectors:** Trigger external APIs, update databases, or integrate third-party services seamlessly from within a conversation loop.
* **Role Switching:** Deploy specialized agent personas—developer assistant, student tutor, research analyst—each optimized for domain-specific workflows.

Together, these advancements will make RishiGPT a truly *autonomous RAG-anything engine*—capable of intelligently reasoning over any data source, maintaining state, and integrating into real-world pipelines for software engineering, research, and intelligent automation.

---

## Author

**Rishiraj Bal**
Independent developer building generative AI systems with an emphasis on practical LLM applications, advanced RAG pipelines, and full-stack AI deployment.

---

For questions, contributions, or to discuss advanced feature integration, please open an issue or submit a pull request.

```
