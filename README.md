# RishiGPT — AI Chatbot with File-RAG + Web Search + Memory

**RishiGPT** is a GenAI-powered assistant built using **Streamlit**, **LangChain**, and **Groq**, designed to provide smart, conversational interactions — enhanced with **Web Search**, **PDF/Text/Web RAG**, and **context-aware memory**.

> It's like ChatGPT with a memory, a library card, and Google access — but running on your terms.

---

## Features

**Web Search Agent (SerpAPI)**  
Ask real-time questions and get live web answers, using a LangChain agent backed by Groq + SerpAPI.

**RAG from Your Files**  
Upload your own PDF, `.txt`, or fetch from a URL — RishiGPT will embed, index, and chat over it with precise context.

**Memory-enabled Conversations**  
Persistent buffer memory retains your past queries for up to 10 messages — making chats natural and context-aware.

**LLaMA 4 via Groq**  
Superfast inference using Meta's `llama-4-scout-17b-16e-instruct`, thanks to blazing Groq hardware.

**Multi-mode Toggle**  
Easily switch between:
- Personalised file chat
- Web Search
- Normal conversation

**Modular & Extensible**  
Built with clear separation of RAG, agent, and base chat for easy customization and feature expansion.

---

## Tech Stack

| Component | Stack |
|----------|-------|
| App UI | Streamlit |
| LLM | Groq (LLaMA 4) |
| Framework | LangChain |
| Vector DB | FAISS |
| Embeddings | HuggingFace Transformers |
| Memory | ConversationBufferMemory |
| Search Agent | SerpAPI |
| Deployment | Streamlit Cloud |

---

## Installation

```bash
git clone https://github.com/YOUR_USERNAME/rishigpt
cd rishigpt

# (Optional) create virtualenv
python -m venv venv
source venv/bin/activate  # On Windows use venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
