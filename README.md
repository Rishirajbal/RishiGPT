# RishiGPT — AI Chatbot with File-RAG, Web Search, Memory & More

## Demo
https://rishigpt.streamlit.app/


**RishiGPT** is a generative AI-powered assistant built using Streamlit, LangChain, and Groq. It delivers real-time, context-aware responses through a combination of web search, Retrieval-Augmented Generation (RAG), and memory—designed for developers, researchers, and anyone looking to chat with documents, URLs, or just get smart assistance.

This app isn't just a chatbot—it’s a modular framework to build and evolve AI-native tools. Whether you're pulling insights from a PDF, parsing a website, or running a live search, RishiGPT handles it all.

---

## Features

### Web Search Agent (via SerpAPI)
Ask real-time questions and get accurate web-based answers using LangChain’s SerpAPI agent integrated with Groq’s blazing-fast LLaMA backend.

### RAG from Custom Files
Upload a PDF, plain text file, or even input a web URL—RishiGPT indexes it, embeds it with HuggingFace models, and lets you query it naturally using ConversationalRetrievalChain.

### Memory-Enabled Conversations
Buffered memory enables conversations with up to 10-message history for seamless context carry-over across turns.

### LLaMA 4 via Groq
Powered by `meta-llama/llama-4-scout-17b-16e-instruct`, hosted on Groq hardware—ensuring ultra-low latency responses with high-quality instruction following.

### Multi-Mode Toggle
Easily switch between modes:
- File-based chat (PDF, Web, Text)
- Web search-enabled chat
- Standard LLM chat

### Modular & Extensible Architecture
Each feature (RAG, agent tools, memory) is modular and independently controllable. This architecture ensures rapid experimentation and scaling.

---

## Tech Stack

| Component       | Technology                   |
|----------------|------------------------------|
| App UI         | Streamlit                    |
| LLM Inference  | Groq (Meta LLaMA 4)          |
| Framework      | LangChain                    |
| Vector Store   | FAISS                        |
| Embeddings     | HuggingFace Transformers     |
| Memory         | ConversationBufferMemory     |
| Web Search     | SerpAPI                      |
| File Loaders   | LangChain Community Loaders  |
| Deployment     | Streamlit Cloud              |

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

Create a `.streamlit/secrets.toml` (used by Streamlit Cloud) or local `.env` file with:

```toml
GROQ_API_KEY = "your_groq_api_key"
SERPAPI_API_KEY = "your_serpapi_api_key"
```

---

## Running the App

```bash
streamlit run app_2.py
```

Then open your browser to `http://localhost:8501` or use the public Streamlit Cloud link if deployed.

---

## Roadmap

The current version focuses on file-RAG, web search, and short-term memory. The upcoming releases will expand RishiGPT into an advanced all-rounder GenAI agent:

* Integrate with **LangGraph** to build more sophisticated workflows, memory control, and branching logic.
* Add **GitHub repo interaction**, including code retrieval, understanding, summarization, and generation.
* Build out **code generation capabilities** for functions, classes, or even entire modules using prompt templates.
* Use **n8n** to connect workflows and trigger external APIs or databases from within the chat.
* Improve **memory management** with chunked or vectorized long-term context tracking.
* Enable **role-based personas**, allowing users to switch between dev mode, student tutor mode, and researcher mode.

This isn’t just a chatbot—it’s the groundwork for a fully autonomous, pluggable software engineering assistant.

---

## Author

**Rishiraj Bal**
Enthusiastic about everything AI
Built for experimentation, learning, and eventually—domination of the LLM application stack.
