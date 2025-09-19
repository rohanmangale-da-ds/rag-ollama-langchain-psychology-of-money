# rag-ollama-langchain-psychology-of-money
Retrieval-Augmented Generation (RAG) pipeline using LangChain, Ollama, Chroma, and embeddings to query The Psychology of Money PDF and generate context-aware answers.

# 📚 RAG with LangChain + Ollama + Chroma

This project implements a **Retrieval-Augmented Generation (RAG)** pipeline using **LangChain, Ollama, and ChromaDB**.  
It loads *The Psychology of Money* PDF, splits the text into chunks, stores them in a vector database, and retrieves relevant context for **question answering**.  

---

## 🚀 Project Overview
- **Goal**: Build an end-to-end RAG system for querying a book/document.  
- **Pipeline**:
  1. **Load PDF** with `PyPDFLoader` from LangChain.  
  2. **Chunk text** using `RecursiveCharacterTextSplitter`.  
  3. **Embed chunks** with `OllamaEmbeddings (nomic-embed-text:v1.5)`.  
  4. **Store vectors** in `ChromaDB`.  
  5. **Retrieve relevant docs** using `MultiQueryRetriever`.  
  6. **Generate answers** with `ChatOllama (gemma3:12b)` based on retrieved context.  

---

## 🛠️ Technologies Used
- **LangChain** – RAG pipeline components (loaders, retrievers, prompt templates).  
- **Ollama** – Local LLMs (`gemma3:12b`) + Embeddings (`nomic-embed-text:v1.5`).  
- **ChromaDB** – Vector database for storing embeddings.  
- **Python** – Core scripting and pipeline orchestration.  

---

## 📂 Project Structure
rag-ollama-langchain/
│-- data/ # PDF file (The Psychology of Money)
│-- chroma_db/ # Persisted Chroma vector database
│-- rag_pipeline.py # Main script (RAG implementation)
│-- requirements.txt # Dependencies
