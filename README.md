# 📚 Bhagavad Gita RAG Chatbot

> My first chatbot project and my first hands-on exploration of Retrieval-Augmented Generation (RAG) and Large Language Models.

This project marks my first experience building a conversational AI application.

The objective was to develop a chatbot capable of answering questions about the Bhagavad Gita by combining document retrieval with Large Language Models (LLMs).

Through this project, I explored the main components of a RAG pipeline: PDF preprocessing, document chunking, embeddings, vector search, LLM integration, source retrieval and a conversational interface.

---

## 🎯 Project Overview

The chatbot is designed to interact with the content of the Bhagavad Gita.

Instead of relying only on the internal knowledge of a language model, the system retrieves relevant passages from the source document and provides them as context to the LLM before generating an answer.

The project covers:

- PDF text extraction and preprocessing
- Document chunking
- Text embeddings
- Vector similarity search
- Large Language Models
- Retrieval-Augmented Generation (RAG)
- Source retrieval
- Conversational interface

---

## 🎥 Demo

A video demonstration of the chatbot is included in this repository.

▶️ **Demo:** `demo/demo.mp4`

The complete presentation of the project is also available:

📑 **Presentation:** `docs/Presentation.pdf`

---

## 🧠 RAG Pipeline

The main workflow of the project is:

```text
            Bhagavad Gita PDF
                    │
                    ▼
             Text Extraction
                 PyPDF2
                    │
                    ▼
              Preprocessing
                    │
                    ▼
              Text Chunking
                    │
                    ▼
                Embeddings
                    │
                    ▼
            FAISS Vector Store
                    │
                    │
User Question ──────┘
        │
        ▼
 Similarity Search
        │
        ▼
Relevant Passages
        │
        ▼
   RAG Pipeline
 LangChain + LLM
        │
        ▼
Generated Answer
        │
        ▼
 Source Retrieval
        │
        ▼
 Gradio Chat UI
