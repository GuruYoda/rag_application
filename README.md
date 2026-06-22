# 🛰️ RAG Engineering Copilot

A production-style Retrieval-Augmented Generation system over public 
NASA technical reports. Demonstrates end-to-end RAG engineering: 
ingestion → hybrid retrieval → reranking → generation → evaluation → 
observability.

> Mirrors the architecture I built for engineering-requirement copilots 
> at Mercedes-Benz R&D India — with public data and clean, deployable code.

Complete RAG pipeline

A powerful Retrieval-Augmented Generation (RAG) system built with FastAPI, Inngest, and Qdrant. This project allows you to ingest PDF documents, perform semantic searches, and get intelligent answers via Ollama-powered LLMs.

## 🚀 Features
- **Document Ingestion:** Easily upload and parse PDFs.
- **Async Workflows:** Built with Inngest to handle background jobs reliably.
- **Semantic Search:** Powered by Qdrant vector database.
- **LLM Integration:** Uses Llama 3.1 via Ollama for concise, context-aware answers.
- **Interactive UI:** Built with Streamlit for a seamless user experience.

## 🛠️ Tech Stack
- **Backend:** FastAPI
- **Orchestration:** Inngest
- **Vector DB:** Qdrant
- **Frontend:** Streamlit
- **LLM/Embeddings:** Llama 3.1 & Nomic Embed via Ollama

## 📋 Prerequisites
- Python 3.10+
- [Ollama](https://ollama.com/) running locally with `llama3.1` and `nomic-embed-text` models.
- [Qdrant](https://qdrant.tech/) instance running locally.
- [Inngest](https://www.inngest.com/) dev server.

## 🚀 How to Run
1. **Clone the repository:**
```bash
   git clone https://github.com/GuruYoda/rag_application.git
   cd your-repo-name
