# College RAG Chatbot

This repository contains a **lightweight Retrieval-Augmented Generation (RAG) system** built from scratch using raw Python and explicit pipeline logic.  
The system is designed to answer **college-related queries** using **real, structured data scraped from official college websites**.

Instead of relying on pre-built RAG frameworks, every stage of the pipeline is implemented transparently to keep the system **understandable, debuggable, and traceable**.

---

## Overview

The chatbot retrieves relevant information from scraped college web pages and uses it as context for response generation. Each answer is grounded in source data, with metadata attached to ensure transparency.

The project includes a **Streamlit-based user interface** that allows users to interact with the system through a simple web app, making the pipeline easy to test and demonstrate.

Key goals of the project:
- Build a **clean, end-to-end RAG pipeline**
- Keep data sources **verifiable and traceable**
- Avoid black-box abstractions
- Focus on practical, real-world usability

---

## System Architecture

The pipeline follows a clear, modular flow:

1. **Web Scraping**
   - Scrapes multiple college website pages and sections
   - Uses BeautifulSoup to extract structured content

2. **Data Preprocessing**
   - Cleans and normalizes scraped text
   - Organizes content into a query-friendly JSON structure
   - Preserves metadata such as source URL and section

3. **Text Embeddings**
   - Encodes content using Sentence-Transformers
   - Converts text into dense semantic vectors

4. **Vector Indexing**
   - Stores embeddings in FAISS
   - Enables fast similarity-based retrieval

5. **Retrieval**
   - Retrieves the most relevant chunks based on user query
   - Includes source metadata for transparency

6. **Generation**
   - Uses LLaMA 3 via the Groq API
   - Generates answers conditioned strictly on retrieved context

7. **User Interface**
   - Streamlit-based UI for interacting with the chatbot
   - Simple input/output flow for testing queries and responses

---

## Built With

- **Python** – custom pipeline orchestration  
- **BeautifulSoup** – web scraping  
- **Sentence-Transformers** – semantic embeddings  
- **FAISS** – vector similarity search  
- **Groq API (LLaMA 3)** – language generation  
- **Streamlit** – web-based user interface  
- **JSON + Regex** – structured data handling and control  

---

## Features

- End-to-end RAG pipeline built without frameworks
- Source-grounded answers with metadata
- Efficient semantic search using FAISS
- Transparent and modular design
- Interactive Streamlit UI
- Easy to extend with new data sources

---

## Skills Applied & Strengthened

- Retrieval-Augmented Generation (RAG) fundamentals  
- End-to-end pipeline design  
- Semantic search with vector databases  
- NLP with sentence embeddings  
- Web scraping and data structuring  
- Source-grounded and explainable response design  

---

## Scope & Notes

- The system is focused on **college-related information**
- Emphasis is on correctness, traceability, and clean logic
- This is a learning-focused and practical implementation, not a benchmark-driven system

---

## License

This project is released under the **MIT License**.  
You are free to use, modify, and distribute the code with proper attribution.
