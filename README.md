<h1 align="center">🚀 Orbit Chat</h1>
<p align="center">
  <strong style="background-color: green; padding: 3px 8px; color: white; border-radius: 4px;">English</strong>
</p>

<p align="center">
Orbit Chat is a full-stack AI agent chat platform built using <strong>LangGraph</strong>, <strong>FastAPI</strong>, <strong>NextJS</strong>, and <strong>ChromaDB</strong>.<br>
A production-ready template for building AI-agent chat apps with full <strong>RAG (Retrieval-Augmented Generation)</strong> support.
</p>

---

## 🌌 Preview

<p align="center">
  <img src="./pictures/chat_img.png" width="700"/>
</p>

<p align="center">
  <strong>Multi-Agent Demo</strong>
</p>

<p align="center">
  <img src="./pictures/chat_multi_agent_img.png" width="700"/>
</p>

---

## ✨ Features

- 🤖 **AI agent chat system** built with LangGraph (customizable agent behavior)
- 🧠 **Knowledge-base Q&A** using ChromaDB
- 🛠️ **Custom tool invocation** support
- ⚡ **Async FastAPI backend**
- 🎨 **NextJS frontend with modern UI**
- 📡 **Streaming responses** via SSE
- 👤 **Create & switch between multiple agents**
- 👥 **Multi-agent collaboration** (math, code, general assistant)
- 💾 **Local browser chat history**
- 🧩 **Template ready** for extending with your own agents & tools

---

## 📁 Project Structure

```
backend   → FastAPI backend (AI, RAG, LangGraph workflows)
frontend  → NextJS frontend (chat UI + agent management)
```

---

## ⚡ Quick Start

# 🟦 Backend Setup

### 1️⃣ Configure Environment Variables  
Rename `.env.example` → `.env` and update:

```env
# Database configuration
DATABASE_URL=sqlite+aiosqlite:///resource/database.db
# For MySQL:
# DATABASE_URL=mysql+aiomysql://root:root@localhost/ai-chatkit

# App configuration
DEBUG=True
APP_NAME=Orbit Chat

# OpenAI Keys
OPENAI_BASE_URL=
OPENAI_API_KEY=
DEFAULT_MODEL=gpt-4o-mini

# Embeddings (using bge-m3 via Ollama)
EMBEDDING_MODEL=bge-m3

# Chroma Storage
CHROMA_PATH=resource/chroma_db
```

### 2️⃣ Run Backend

```bash
pip install uv
cd ${workdir}/backend
uv sync --frozen

# Activate env
source .venv/bin/activate
# Windows:
# .venv/Scripts/activate

# Start server
python app/run_server.py
```

---

## 📚 RAG Deployment

Orbit Chat uses **bge-m3 embeddings** from local **Ollama**.

Install the model:

👉 https://ollama.com/library/bge-m3

---

# 🟦 Frontend Setup

```bash
cd ${workdir}/frontend
pnpm install
pnpm dev
```

Then open:

👉 http://localhost:3000/

---

## 🤖 Built-In Agents

### 1️⃣ **OA-ASSISTANT**
- Office assistant with employee info lookup
- Uses knowledge-base queries  
**Code:** `backend/app/ai/agent/oa_assistant.py`

### 2️⃣ **MULTI_AGENT**
Multi-agent system with supervisor managing:
- `math_agent`
- `code_agent`
- `general_agent`  
**Code:** `backend/app/ai/agent/multi_agent.py`

---

## ⭐ Summary

Orbit Chat is a complete, extensible starter kit for:
- Building AI chat systems
- Using LangGraph for agent orchestration
- Adding RAG, tools, and multiple agents
- Deploying full-stack LLM applications

---
