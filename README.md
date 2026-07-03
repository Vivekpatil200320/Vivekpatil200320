# 💫 About Me

Hi there 👋, I'm **Vivek Patil** — **Founder & Operations Manager at VDev Automations** | **AI Agent Infrastructure Engineer** 🚀

I build production-ready AI agent infrastructure: MCP servers that give LLMs real diagnostic hands, grounded RAG pipelines with measurable retrieval quality, and self-healing coding agents that run fully on-device. From full-stack web platforms to context-aware telemetry bridges that fix AI "sandbox blindness," I build tools that let intelligent agents interact safely with real-world infrastructure.

---

### 🌱 Current Focus

* **VDev Automations:** Custom business workflows, speed-to-lead engines, and enterprise outreach systems.
* **AI Agent Infrastructure:** MCP servers, hybrid-retrieval RAG backends, and LangGraph agent loops — shipped, deployed, and observable.
* **DSA Practice:** Working through the NeetCode 75 roadmap in Python, 3–4 problems a week.

---

### 📦 Featured Projects

#### ⚓ [CyberRescue](https://github.com/vivekpatil200320/cyberrescue)
*A secure MCP host telemetry gateway — gives Claude eyes and hands inside broken Docker containers.*
* Exposes container log streaming, live memory/CPU probing, and isolated diagnostic execution to any MCP client, with input validation, command blocklists, retry with back-off, and sanitized errors built in.
* Cuts per-endpoint agent integration time from ~2 hours to under 30 minutes — new diagnostic capabilities are a single decorated function.
* **Status:** Verified **A-Grade Quality** on Glama, CI-tested on every push, listed on global MCP indexes.

[![cyberrescue MCP server](https://glama.ai/mcp/servers/Vivekpatil200320/cyberrescue/badges/card.svg)](https://glama.ai/mcp/servers/Vivekpatil200320/cyberrescue)

#### 📚 [ContextQuery](https://github.com/vivekpatil200320/contextquery-backend)
*Grounded document Q&A with hybrid retrieval — every answer traceable to the exact source passage.*
* Hybrid BM25 + semantic search (fused via Reciprocal Rank Fusion) with NVIDIA NIM reranking cuts irrelevant context injection by ~40% versus naive top-K retrieval.
* FastAPI + Chroma Cloud + NVIDIA NIM (embed/rerank/LLM), traced end-to-end in Langfuse, with a repeatable eval harness. [Next.js 15 frontend](https://github.com/vivekpatil200320/contextquery-frontend) · [Live demo](https://contextquery-frontend.vercel.app)

#### 🚀 [PyCursor](https://github.com/Vivekpatil200320/PyCursor--Self-Healing-Hybrid-Coding-Agent)
*A self-healing Python coding agent — writes, executes, and fixes its own code.*
* LangGraph state machine feeds runtime stack traces back into the LLM until the code executes cleanly: 90% self-healing success rate on Python stack traces.
* Runs fully on-device via Ollama (Qwen2.5-Coder 7B) by default, with a one-toggle switch to Gemini cloud inference.

#### 🧠 [leetcode-solutions](https://github.com/vivekpatil200320/leetcode-solutions)
*DSA practice in Python, structured around the NeetCode 75 roadmap — 3–4 problems a week, each with complexity notes and intuition.*

---

### 💡 Tech Stack

#### 🤖 AI & Agent Engineering
![Model Context Protocol](https://img.shields.io/badge/MCP-Protocol-blue?style=for-the-badge&logo=anthropic&logoColor=white)
![FastMCP](https://img.shields.io/badge/FastMCP-Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-Agentic-orange?style=for-the-badge)
![LangChain](https://img.shields.io/badge/LangChain-RAG-1C3C3C?style=for-the-badge)
![NVIDIA NIM](https://img.shields.io/badge/NVIDIA_NIM-Inference-76B900?style=for-the-badge&logo=nvidia&logoColor=white)
![Ollama](https://img.shields.io/badge/Ollama-Local_LLMs-black?style=for-the-badge)
![Chroma](https://img.shields.io/badge/Chroma-Vector_DB-FF6B6B?style=for-the-badge)
![Langfuse](https://img.shields.io/badge/Langfuse-Observability-000000?style=for-the-badge)

#### 🌐 Languages & Frameworks
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![TypeScript](https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white)
![Next JS](https://img.shields.io/badge/Next-black?style=for-the-badge&logo=next.js&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/tailwindcss-%2338B2AC.svg?style=for-the-badge&logo=tailwind-css&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)

#### 🗄️ Infrastructure & Delivery
![Docker](https://img.shields.io/badge/Docker-Containerization-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-CI-2088FF?style=for-the-badge&logo=github-actions&logoColor=white)
![Vercel](https://img.shields.io/badge/vercel-%23000000.svg?style=for-the-badge&logo=vercel&logoColor=white)
![Render](https://img.shields.io/badge/Render-Deploy-46E3B7?style=for-the-badge&logo=render&logoColor=white)

---

### 📫 Let's Connect!
* 💼 **LinkedIn:** [linkedin.com/in/vivekpatil23](https://linkedin.com/in/vivek-vdev)
* 📧 **Email:** vivekpatil200320@gmail.com
* 🛠️ **Glama Registry Profile:** [glama.ai/mcp/servers/vivekpatil200320/cyberrescue](https://glama.ai/mcp/servers/vivekpatil200320/cyberrescue)

✨ *"First, solve the problem. Then, write the code."* — John Johnson
