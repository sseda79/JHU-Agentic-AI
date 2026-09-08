# DualLens Analytics

**Course:** Prompt Engineering Foundations, JHU Agentic AI Certificate Program
**Status:** Coursework project (learning exercise), not a production system

## Overview

DualLens Analytics integrates quantitative financial data with qualitative insight drawn from a company's public AI-initiative documents, giving a combined view of financial performance and AI/innovation readiness.

## What it does

- Selects a target organization and pulls its financial metrics
- Visualizes key financial indicators
- Loads company AI-initiative documents (PDFs) and indexes them in a vector store (ChromaDB) for retrieval-augmented generation (RAG)
- Retrieves relevant passages to answer questions about the company's AI strategy
- Evaluates the RAG pipeline for groundedness and relevance
- Scores and ranks findings, with a written summary and future-scope discussion

## Tech stack

Python, OpenAI (via Great Learning API proxy), LangChain, ChromaDB, prompt engineering, RAG evaluation

## Notebook

See `DualLens_Analytics_Notebook.ipynb` in this folder.
