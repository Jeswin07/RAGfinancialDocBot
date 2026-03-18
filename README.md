Financial Document Intelligence Chatbot (RAG)

A document-grounded chatbot that enables users to query financial reports using natural language. Built using Retrieval-Augmented Generation (RAG), the system ensures accurate and explainable answers strictly based on the uploaded documents.

Overview

Financial documents such as annual reports contain valuable insights but are often difficult to analyze due to their size and complexity. This project provides a conversational interface that allows users to extract key financial information efficiently.

The chatbot retrieves relevant document sections using semantic search and generates responses using a local Large Language Model.

Features

Document-grounded responses (no hallucinations)

Semantic search using vector embeddings

Multi-turn conversational support

Year-wise and region-wise comparisons

Works with real financial PDF documents

Interactive web interface using Gradio

Fully open-source and API-free setup

Tech Stack

Programming

Python

Google Colab

LLM & NLP

Hugging Face Transformers

Mistral-7B-Instruct (4-bit quantized)

RAG Framework

LlamaIndex

Embeddings

all-MiniLM-L6-v2

UI

Gradio

System Architecture

Upload financial PDF documents

Split documents into smaller chunks

Convert chunks into vector embeddings

Store embeddings in a vector index

Convert user query into embedding

Retrieve top-k relevant chunks

Generate answer using LLM based on retrieved context

Example Queries

What is the total net sales for 2024?

Compare net sales for 2024, 2023, and 2022

Which region contributed the most revenue?

What is the operating income trend?

Installation
git clone https://github.com/your-username/financial-rag-chatbot.git
cd financial-rag-chatbot
pip install -r requirements.txt
Usage
python app.py

Then open the Gradio link in your browser.

Project Structure
financial-rag-chatbot/
│
├── data/                # Input PDFs
├── models/              # Model configs (optional)
├── app.py               # Main application
├── rag_pipeline.py      # Retrieval + generation logic
├── requirements.txt
└── README.md
Results

Accurate extraction of financial metrics

Reliable comparison across years and regions

Reduced hallucination due to document grounding

Smooth interaction through chatbot UI

Limitations

Requires GPU for optimal performance

Slower response time due to local LLM inference

Performance depends on document quality

Indexing time increases with large documents

Future Improvements

API integration for faster inference

Multi-document cross-analysis

Persistent vector database (FAISS or Chroma)

Cloud deployment (AWS, GCP, Hugging Face Spaces)

Author

Jeswin K Reji
Aspiring Data Scientist
