# Senior Mortgage Underwriting System

**Course:** Advanced Agentic AI, JHU Agentic AI Certificate Program
**Status:** Coursework project (learning exercise), not a production system

## Overview

A multi-agent mortgage underwriting system designed to accelerate and standardize loan decisions while building compliance safeguards in from the start.

## Architecture

**Specialist agents** independently evaluate one dimension of the application:
- Credit Analyst — credit score, payment history, derogatory items
- Income Analyst — income stability and debt-to-income ratio
- Asset Analyst — reserves and asset verification
- Collateral Analyst — property/collateral valuation

**Coordination agents** validate inputs, compute an overall risk score, assemble a decision memo, and route borderline cases to human-in-the-loop review.

## Compliance safeguards

- PII sanitization: SSNs, names, addresses, and phone numbers are redacted before any data reaches the LLM
- Bias-signal detection aligned to Fair Lending Act considerations
- Policy retrieval via RAG (ChromaDB), so agents cite actual underwriting policy rather than relying on model memory
- Deterministic calculator tools for anything that must be computed exactly rather than generated
- Full audit trail via LangGraph state, with human-in-the-loop review for borderline cases

## Testing

Three synthetic test cases (strong, borderline, weak applicant) exercise the full workflow end to end.

## Tech stack

Python, LangGraph (StateGraph), LangChain, OpenAI (via Great Learning API proxy), ChromaDB, multi-agent orchestration

## Notebook

See `Mortgage_Underwriting_Notebook.ipynb` in this folder.
