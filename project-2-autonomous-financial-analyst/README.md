# Autonomous Financial Research Analyst

**Course:** Designing and Building Agentic Systems, JHU Agentic AI Certificate Program
**Status:** Coursework project (learning exercise), not a production system

## Overview

A financial research agent that progresses from a simple reactive LLM to a fully autonomous, tool-using agent, then extends it with retrieval-augmented generation (RAG) over private analyst reports.

## Part 1: Agent Charter and Tools

- Compares a traditional reactive LLM prompt against a goal-oriented agent charter
- Implements four tools: stock price lookup, stock price history, financial news search, and sentiment analysis
- Builds the agent as a LangGraph state graph, with constraints and error handling for tool failures
- Tests three configurations: traditional LLM, basic goal-oriented agent, and full autonomous agent

## Part 2: RAG and Investment Intelligence

- Loads private analyst PDF reports, chunks them, and embeds them into a ChromaDB vector store
- Adds a `query_private_database` tool so the agent can pull from private research alongside public data
- Produces a multi-company ranking and investment recommendation (Buy/Hold/Sell) across MSFT, GOOGL, NVDA, AMZN, and IBM, citing sources and flagging data gaps

## Tech stack

Python, LangGraph, LangChain, OpenAI (via Great Learning API proxy), ChromaDB, Tavily (news search), sentiment analysis, RAG

## Notebook

See `Autonomous_Financial_Analyst_Notebook.ipynb` in this folder.
