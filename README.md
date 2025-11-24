<h1 align="center"> ORBITCHAT </h1>
<p align="center">
  <strong style="background-color: green;">English</strong>
  |
  <a href="./README_zh.md" target="_Self">中文</a>
</p>

OrbitChat is a full-stack AI agent chat tool built using components such as LangGraph, FastAPI, NextJS, and Chroma.

This project serves as a template to help you quickly build AI agent chat applications using the LangGraph framework, and supports RAG (Retrieval-Augmented Generation) to enhance knowledge-base Q&A capabilities.

<img src="./pictures/chat_img.png" width="700"/>  

Multi-agent:

<img src="./pictures/chat_multi_agent_img.png" width="700"/>


## Features

1. AI agent chat application built on the LangGraph framework, supporting custom behavior logic orchestration for agents.  
2. Supports custom knowledge-base Q&A capabilities for agents using ChromaDB.  
3. Supports custom tool invocation for agents.  
4. Python backend API implemented using FastAPI, supporting full asynchronous calls.  
5. NextJS frontend for agent interactions.  
6. Supports chat streaming output (SSE).  
7. Supports multiple custom agents.  
8. Supports multi-agent collaboration.  
9. Chat history is saved in the local browser cache.


## Structure

- `backend`: Backend service code  
- `frontend`: Frontend service code  


## Quick Start

### Backend Service

Rename `.env.example` → `.env`

```properties
# Database configuration
DATABASE_URL=sqlite+aiosqlite:///resource/database.db

# Application configuration
DEBUG=True
APP_NAME=OrbitChat

# OpenAI
OPENAI_BASE_URL=
OPENAI_API_KEY=
DEFAULT_MODEL=gpt-4o-mini

# Embeddings
EMBEDDING_MODEL=bge-m3
CHROMA_PATH=resource/chroma_db
