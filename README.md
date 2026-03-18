# Financial Document Intelligence Chatbot (RAG)

A document-grounded chatbot that allows users to query financial reports using natural language. Built using Retrieval-Augmented Generation (RAG), the system ensures accurate and explainable answers strictly based on the uploaded documents.

---

## Overview

Financial documents such as annual reports contain valuable insights but are often lengthy and complex. Extracting key information like revenue, net sales, or operating income requires significant time and effort.

This project provides a conversational interface that:
- Retrieves relevant information from financial documents
- Generates accurate answers grounded in the document
- Supports follow-up and comparison queries

---

## Features

- Document-grounded responses (no hallucinations)
- Semantic search using vector embeddings
- Multi-turn conversational support
- Year-wise and region-wise comparisons
- Works with real financial PDF documents
- Interactive web interface using Gradio
- Fully open-source (no paid APIs required)

---

## Tech Stack

**Programming**
- Python
- Google Colab

**LLM & NLP**
- Hugging Face Transformers
- Mistral-7B-Instruct (4-bit quantized)

**RAG Framework**
- LlamaIndex

**Embeddings**
- all-MiniLM-L6-v2

**UI**
- Gradio

---

## System Architecture

1. Upload financial PDF documents  
2. Split documents into smaller chunks  
3. Convert chunks into vector embeddings  
4. Store embeddings in a vector index  
5. Convert user query into embedding  
6. Retrieve top-k relevant chunks  
7. Generate answer using LLM based on retrieved context  

---

## Example Queries

- What is the total net sales for 2024?  
- Compare net sales for 2024, 2023, and 2022  
- Which region contributed the most revenue?  
- What is the operating income trend?  

---

## Installation

```bash
git clone https://github.com/your-username/financial-rag-chatbot.git
cd financial-rag-chatbot
pip install -r requirements.txt
