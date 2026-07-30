![Vivek Patil](https://capsule-render.vercel.app/api?type=waving&height=180&color=0:6C5CE7,100:00D2FF&text=Vivek%20Patil&fontColor=ffffff&fontSize=42&fontAlignY=40&animation=fadeIn)


[![Typing SVG](https://readme-typing-svg.demolab.com/?font=Fira+Code&size=20&pause=1000&color=6C5CE7&center=true&vCenter=true&width=600&lines=AI+agent+infrastructure+%26+MCP+servers;Grounded+RAG+pipelines+with+measurable+retrieval;Self-healing+coding+agents)](https://git.io/typing-svg)

I'm a self-taught engineer building AI agent infrastructure — MCP servers, RAG systems, and multi-agent LangGraph pipelines. I care about the engineering *around* the model call, not the call itself: sandboxed code execution, retrieval quality measured with eval harnesses instead of assumed, end-to-end tracing, and real failure handling. I ship projects fully — backend, frontend, infra, tests, and the docs explaining why they're built the way they are...

---

### 📦 Featured projects

#### 📚 [ContextQuery](https://github.com/Vivekpatil200320/contextquery-backend) — grounded RAG with measurable retrieval

**Problem:** RAG systems hallucinate or bury the LLM in irrelevant context, and you can't trust an answer you can't trace back to a source.

**What it does:** Grounded document Q&A over PDFs and DOCX — every answer cites the exact source chunk it came from, and if the documents don't contain the answer, it says so instead of falling back on the model's training knowledge. That constraint is the whole point.

- **Hybrid retrieval, measured:** BM25 keyword search + semantic vector search fused via Reciprocal Rank Fusion, then reranked by an NVIDIA NIM reranker — **~40% fewer irrelevant chunks** reach the LLM versus naive top-K retrieval.
- **Real eval harness:** scores retrieval precision and answer faithfulness across semantic and hybrid modes; latest run hit **100% retrieval precision on applicable cases at ~2.4s average end-to-end latency** — quality is a number, not a vibe.
- **Observable:** every LLM call and retrieval step is traced in Langfuse, so regressions are visible instead of anecdotal.
- **Built for real documents:** async background ingestion (a 950-page doc chunks into thousands of pieces), batched embeddings (96 per request), and token-by-token SSE streaming.
- **Zero paid API spend** — runs entirely on free-tier infrastructure, with runtime switches for retrieval mode (`semantic` / `hybrid`) and LLM provider (`ollama` / `nvidia`).

**Stack:** FastAPI (Python 3.11) · Next.js 15 · Chroma Cloud · NVIDIA NIM (embed · rerank · LLM) · rank_bm25 · Langfuse · Docker → Render + Vercel

[Frontend repo](https://github.com/Vivekpatil200320/contextquery-frontend) · [Live app](https://contextquery-frontend.vercel.app) · [Live API](https://contextquery-backend.onrender.com/docs) · [Write-up: hybrid RRF retrieval](https://dev.to/vivek_vdev/hybrid-retrieval-rrf-how-i-got-100-retrieval-precision-in-a-production-rag-system-1oga)

<br>

#### 🐋 [CyberRescue](https://github.com/Vivekpatil200320/cyberrescue) — MCP server for Docker triage

**Problem:** Giving an AI agent real hands on a system usually means hand-rolling the client call, input validation, output sanitization, and failure handling for *every* capability you expose.

**What it does:** A locally-hosted MCP (Model Context Protocol) server that gives Claude three real tools to debug Docker containers — stream logs, snapshot live CPU/memory, and run diagnostic commands inside a container — over stdio, with no network ports and no API keys beyond what Claude Desktop already uses.

- **Three tools:** `stream_container_logs` (tail / since / keyword filter, 50KB cap), `inspect_memory_dump` (live `docker stats` + top processes), and `execute_isolated_script` (`docker exec` with validation, a command blocklist, and a hard timeout).
- **A reusable safety pattern** — validate → semaphore-gated daemon call → retry with back-off → sanitized errors → capped output — **cuts per-endpoint integration time from ~2 hours to under 30 minutes**; a new capability is one decorated function.
- **Security designed in, not bolted on:** container-ID regex validation, a command-safety blocklist, a concurrency cap (max 4 daemon calls), exponential back-off retry on read-only calls *only* (`exec` is never retried — it isn't idempotent), and raw Docker errors that never leak to the client, since they can carry host socket paths and usernames.
- **42 passing unit tests** run on every push via GitHub Actions CI; verified **A-Grade Quality on [Glama](https://glama.ai/mcp/servers/Vivekpatil200320/cyberrescue)** and listed on global MCP indexes.

**Stack:** Python 3.12+ · FastMCP · python-on-whales · pytest · GitHub Actions (public demo: FastAPI + Next.js on Vercel)

[![cyberrescue MCP server](https://glama.ai/mcp/servers/Vivekpatil200320/cyberrescue/badges/card.svg)](https://glama.ai/mcp/servers/Vivekpatil200320/cyberrescue)

<br>

**More projects:** &nbsp; [🧑‍🏫 AI Coding Mentor](https://github.com/Vivekpatil200320/ai-coding-mentor) &nbsp;·&nbsp; [🚀 PyCursor](https://github.com/Vivekpatil200320/PyCursor--Self-Healing-Hybrid-Coding-Agent)

---

### 💡 Tech stack

**AI & agent engineering**

![Model Context Protocol](https://img.shields.io/badge/MCP-Protocol-blue?style=for-the-badge&logo=anthropic&logoColor=white)
![FastMCP](https://img.shields.io/badge/FastMCP-Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-Agentic-orange?style=for-the-badge)
![LangChain](https://img.shields.io/badge/LangChain-RAG-1C3C3C?style=for-the-badge)
![NVIDIA NIM](https://img.shields.io/badge/NVIDIA_NIM-Inference-76B900?style=for-the-badge&logo=nvidia&logoColor=white)
![Ollama](https://img.shields.io/badge/Ollama-Local_LLMs-black?style=for-the-badge)
![Google Gemini](https://img.shields.io/badge/Gemini-Cloud_Inference-8E75B2?style=for-the-badge&logo=googlegemini&logoColor=white)
![Chroma](https://img.shields.io/badge/Chroma-Vector_DB-FF6B6B?style=for-the-badge)
![Langfuse](https://img.shields.io/badge/Langfuse-Observability-000000?style=for-the-badge)

**Languages & frameworks**

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![Pydantic](https://img.shields.io/badge/Pydantic-Validation-E92063?style=for-the-badge&logo=pydantic&logoColor=white)
![pytest](https://img.shields.io/badge/pytest-Testing-0A9EDC?style=for-the-badge&logo=pytest&logoColor=white)
![TypeScript](https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white)
![Next JS](https://img.shields.io/badge/Next-black?style=for-the-badge&logo=next.js&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/tailwindcss-%2338B2AC.svg?style=for-the-badge&logo=tailwind-css&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)

**Infrastructure & delivery**

![Docker](https://img.shields.io/badge/Docker-Containerization-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-CI-2088FF?style=for-the-badge&logo=github-actions&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-EC2-232F3E?style=for-the-badge&logo=amazonaws&logoColor=white)
![Vercel](https://img.shields.io/badge/vercel-%23000000.svg?style=for-the-badge&logo=vercel&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white)

---

### 📫 Let's connect

- 🌐 **Portfolio:** [vivek-portfolio-vert.vercel.app](https://vivek-portfolio-vert.vercel.app/)
- 💼 **LinkedIn:** [linkedin.com/in/vivek-vdev](https://linkedin.com/in/vivek-vdev)
- 📧 **Email:** vivekpatil200320@gmail.com
- 🛠️ **Glama Registry:** [glama.ai/mcp/servers/vivekpatil200320/cyberrescue](https://glama.ai/mcp/servers/vivekpatil200320/cyberrescue)
- ✍️ **Hashnode:** [vivekpatil23.hashnode.dev](https://vivekpatil23.hashnode.dev/)
- ✍️ **dev.to:** [dev.to/vivek_vdev](https://dev.to/vivek_vdev)

✨ *"First, solve the problem. Then, write the code."* — John Johnson
