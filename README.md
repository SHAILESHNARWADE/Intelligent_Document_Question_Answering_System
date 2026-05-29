# Intelligent Document Question Answering System using RAG and Large Language Models

## Overview

The Intelligent Document Question Answering System is an AI-powered application that enables users to upload PDF documents and ask natural language questions based on the document content.

The system leverages Retrieval-Augmented Generation (RAG), semantic search, vector databases, and Large Language Models (LLMs) to provide accurate and context-aware answers from uploaded documents.

Unlike traditional keyword-based search systems, this solution understands semantic meaning and retrieves the most relevant information before generating responses.

---

## Key Features

* Upload PDF documents through an interactive web interface
* Automatic text extraction from PDF files
* Intelligent text chunking with overlap preservation
* Semantic embedding generation using Sentence Transformers
* Fast similarity search using FAISS Vector Database
* Retrieval-Augmented Generation (RAG) architecture
* Local Large Language Model integration using Ollama
* Context-aware question answering
* Modern Streamlit-based user interface
* Completely local deployment without external API dependency

---

## Problem Statement

Organizations frequently work with large documents such as:

* Research Papers
* Technical Documentation
* Company Reports
* Educational Notes
* Legal Agreements
* Medical Documents

Finding specific information manually is time-consuming and inefficient.

This project addresses the problem by combining semantic retrieval and generative AI to enable intelligent document understanding and instant question answering.

---

## Project Architecture

```text
PDF Upload
    │
    ▼
Text Extraction (PyPDF2)
    │
    ▼
Text Chunking
    │
    ▼
Embedding Generation
(Sentence Transformers)
    │
    ▼
FAISS Vector Database
    │
    ▼
User Question
    │
    ▼
Question Embedding
    │
    ▼
Semantic Similarity Search
    │
    ▼
Relevant Context Retrieval
    │
    ▼
Prompt Engineering
    │
    ▼
Local SLM (Phi-3 Mini)
    │
    ▼
Generated Answer
```

---

## Technologies Used

| Technology            | Purpose                             |
| --------------------- | ----------------------------------- |
| Python                | Core Programming Language           |
| Streamlit             | Web Application Framework           |
| PyPDF2                | PDF Text Extraction                 |
| NumPy                 | Numerical Operations                |
| Sentence Transformers | Embedding Generation                |
| FAISS                 | Vector Database & Similarity Search |
| Requests              | API Communication                   |
| Ollama                | Local LLM Runtime                   |
| Phi-3 Mini            | Small Language Model                |
| RAG                   | Retrieval-Augmented Generation      |

---

## Core Concepts Implemented

### PDF Processing

Extracts readable text from uploaded PDF documents.

### Text Chunking

Large documents are divided into smaller overlapping chunks to preserve context.

### Embeddings

Text chunks are transformed into dense vector representations using Sentence Transformers.

### Vector Database

Embeddings are stored in FAISS for efficient similarity search.

### Semantic Search

Retrieves document sections based on meaning rather than exact keyword matching.

### Retrieval-Augmented Generation (RAG)

Combines retrieved document context with Large Language Models to generate accurate answers.

### Prompt Engineering

Structures retrieved context and user queries into optimized prompts for response generation.

---

## Project Workflow

### Step 1

Upload PDF document.

### Step 2

Extract text using PyPDF2.

### Step 3

Split text into overlapping chunks.

### Step 4

Generate embeddings using Sentence Transformers.

### Step 5

Store embeddings in FAISS vector database.

### Step 6

Convert user question into embedding.

### Step 7

Retrieve top relevant chunks through semantic similarity search.

### Step 8

Construct prompt using retrieved context.

### Step 9

Send prompt to local LLM via Ollama.

### Step 10

Generate and display final answer.

---

## Installation

### Clone Repository

```bash
git clone https://github.com/YOUR_USERNAME/Intelligent-Document-Question-Answering-System-Using-RAG-and-LLMs.git

cd Intelligent-Document-Question-Answering-System-Using-RAG-and-LLMs
```

### Install Required Libraries

```bash
pip install streamlit
pip install PyPDF2
pip install numpy
pip install requests
pip install faiss-cpu
pip install sentence-transformers==3.3.1
pip install huggingface-hub==0.25.2
```

---
### Language Model
Initially experimented with Llama3 for response generation.
Migrated to Phi-3 Mini (SLM) due to its lower computational requirements and better performance on resource-constrained systems.

 

## Install Ollama

Download and install Ollama from:

https://ollama.com

Pull the Phi-3 Mini model:

```bash
ollama pull phi3:mini
```

Run the model:

```bash
ollama run phi3:mini
```

Keep Ollama running while using the application.

---

## Run the Application

```bash
streamlit run Intelligent_Document_Question_Answering_System.py
```

Alternative:

```bash
python -m streamlit run Intelligent_Document_Question_Answering_System.py
```

---

## Example Usage

1. Upload a PDF document.
2. Wait for text extraction and vector database creation.
3. Enter a question related to the document.
4. View retrieved context.
5. Receive an AI-generated answer based on document content.

---

## Project Highlights

* End-to-End RAG Pipeline
* Local LLM Deployment
* Semantic Search Implementation
* Vector Database Integration
* Streamlit Dashboard Development
* Generative AI Application
* Prompt Engineering
* Embedding-Based Retrieval System

---

## Future Enhancements

* Multi-PDF Question Answering
* Chat History Support
* Hybrid Search (Keyword + Semantic)
* PDF Summarization
* Source Citation Tracking
* Multi-Model Support
* Voice-Based Question Answering
* Cloud Deployment

---

## Learning Outcomes

This project demonstrates practical implementation of:

* Generative AI
* Large Language Models (LLMs)
* Retrieval-Augmented Generation (RAG)
* Vector Databases
* Semantic Search
* Embedding Models
* Prompt Engineering
* Local AI Deployment
* Streamlit Application Development

---

## Project Developer

**Shailesh Kalyan Narwade**

### Tagline

**Smarter Search. Faster Insights.**
