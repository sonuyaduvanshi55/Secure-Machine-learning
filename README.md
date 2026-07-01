# Strategic Emailer – AI-Powered Cold Email Generator

An AI-powered cold email generator that extracts job requirements from company career pages and generates personalized cold emails using Llama 3.1, LangChain, ChromaDB, Streamlit and RAG.

## Features

- Extracts job descriptions from career page URLs
- Uses LangChain for LLM workflow orchestration
- Stores and retrieves portfolio projects using ChromaDB vector search
- Matches top relevant portfolio links based on job requirements
- Generates personalized cold emails automatically
- Provides a Streamlit-based user interface

## Tech Stack

- Python
- Llama 3.1 via Groq API
- LangChain
- ChromaDB
- Streamlit
- RAG

## Workflow

1. User enters a company career page URL.
2. The system extracts job listings and requirements.
3. Job content is processed using LangChain.
4. Relevant portfolio projects are retrieved from ChromaDB.
5. Llama 3.1 generates a personalized cold email.

## How to Run

```bash
pip install -r requirements.txt
streamlit run app/main.py

