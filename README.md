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
