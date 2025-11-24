<h1 align="center"> Orbit Chat </h1>
<p align="center"> <strong style="background-color: green;">English</strong> | <a href="./README_zh.md" target="_Self">中文</a> </p>

Orbit Chat is a full-stack AI agent chat platform built using LangGraph, FastAPI, NextJS, and Chroma.
It serves as a template for rapidly building AI-agent chat applications powered by the LangGraph framework, with full RAG (Retrieval-Augmented Generation) support to enhance knowledge-base Q&A for agents.

<img src="./pictures/chat_img.png" width="700"/>
Multi-Agent Demo
<img src="./pictures/chat_multi_agent_img.png" width="700"/>
🚀 Features

AI agent chat application built on the LangGraph framework with customizable agent behavior and orchestration.

Supports custom knowledge-base Q&A using ChromaDB for embedding storage and retrieval.

Built-in support for custom tool invocation for agents.

Python backend using FastAPI, fully asynchronous.

Customizable NextJS frontend for agent chat UI.

Streaming chat output using SSE (Server-Sent Events).

Create and switch between multiple agents.

Multi-agent collaboration supported (math, code, general assistant, etc.).

Chat history stored locally in the browser.

📁 Project Structure
backend   → Backend service code
frontend  → Frontend service code

⚡ Quick Start
🟦 Backend Setup

Rename .env.example to .env and configure:

# Environment variable configuration

# Database configuration
# SQLite URL
DATABASE_URL=sqlite+aiosqlite:///resource/database.db

# MySQL
# DATABASE_URL=mysql+aiomysql://root:root@localhost/ai-chatkit

# Application configuration
DEBUG=True
APP_NAME=Orbit Chat

# OpenAI
OPENAI_BASE_URL=
OPENAI_API_KEY=
DEFAULT_MODEL=gpt-4o-mini

# DashScope
# DASHSCOPE_API_KEY=
# DEFAULT_MODEL=qwen-plus

# DeepSeek
# DEEPSEEK_API_KEY=
# DEFAULT_MODEL=deepseek-chat

# Embeddings
# Using bge-m3 via local Ollama for embeddings (supports Chinese + English)
EMBEDDING_MODEL=bge-m3

# ChromaDB storage path
CHROMA_PATH=resource/chroma_db


Run backend:

# Install UV dependency manager
pip install uv

# Replace ${workdir} with your directory
cd ${workdir}/backend

uv sync --frozen

# Activate virtual environment
source .venv/bin/activate
# On Windows:
# .venv/Scripts/activate

# Run backend server
python app/run_server.py

📚 RAG Deployment

Orbit Chat uses the bge-m3 embedding model through local Ollama.

To enable knowledge-base access, deploy bge-m3 using Ollama:

👉 https://ollama.com/library/bge-m3

🟦 Frontend Setup
cd ${workdir}/frontend

# Install dependencies
pnpm install

# Run development server
pnpm dev


After startup, visit:

👉 http://localhost:3000/

🤖 Built-In Agents

Orbit Chat includes sample agents to demonstrate the LangGraph workflow.

1. OA-ASSISTANT

Shows an office-assistant style agent

Supports: Employee info lookup, employee handbook knowledge-base queries

Code: backend/app/ai/agent/oa_assistant.py

2. MULTI_AGENT

Demonstrates multi-agent collaboration with a supervisor managing:

math_agent → Mathematical calculations

code_agent → Code generation

general_agent → General Q&A

Code: backend/app/ai/agent/multi_agent.py
