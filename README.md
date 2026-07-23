![Vivek Patil](https://capsule-render.vercel.app/api?type=waving&height=180&color=0:6C5CE7,100:00D2FF&text=Vivek%20Patil&fontColor=ffffff&fontSize=42&fontAlignY=40&animation=fadeIn)


[![Typing SVG](https://readme-typing-svg.demolab.com/?font=Fira+Code&size=20&pause=1000&color=6C5CE7&center=true&vCenter=true&width=600&lines=AI+agent+infrastructure+%26+MCP+servers;Grounded+RAG+pipelines+with+measurable+retrieval;Self-healing+coding+agents)](https://git.io/typing-svg)

I'm a self-taught, independent builder working on AI agent infrastructure — MCP servers that give LLMs real diagnostic hands, grounded RAG pipelines with measurable retrieval quality, multi-agent LangGraph systems, and self-healing coding agents. I like projects where the interesting part isn't "call an LLM," it's the plumbing around it: sandboxing, observability, failure-mode analysis, and the kind of architecture decisions you only find by actually running the thing under load.

---

### 🌱 Currently

- Building and shipping full-stack AI agent systems end to end — backend, frontend, infra, and the docs explaining *why* they're built that way.
- Working through the NeetCode 75 roadmap in Python, a few problems a week.
- Always looking for the next project that has a real, non-obvious engineering problem hiding in it.

![GitHub Streak](https://streak-stats.demolab.com/?user=vivekpatil200320&theme=dark&hide_border=true)

---

### 📦 Featured projects

#### 🧑‍🏫 [ai-coding-mentor](https://github.com/Vivekpatil200320/ai-coding-mentor)
*A Socratic AI mentor that guides you to fix broken code through questions, never answers — then delivers a rubric-scored senior-engineer code review once you pass.*
- 5-agent LangGraph system (router, analysis, mentor, execution, evaluation) running entirely on free-tier inference.
- Hardened Docker sandbox for untrusted code execution — audited against **both** container escape and prompt injection as distinct threat models, with the reasoning written up, not just patched.
- FastAPI + SSE backend, Supabase persistence with per-session authorization, LangFuse observability, and every non-obvious architecture call documented as an ADR.
- Deployed live on AWS EC2, with CI, a hardened production Docker build, and an honest scope note on what it does and doesn't solve.

#### ⚓ [CyberRescue](https://github.com/vivekpatil200320/cyberrescue)
*A secure MCP host telemetry gateway — gives Claude eyes and hands inside broken Docker containers.*
- Exposes container log streaming, live memory/CPU probing, and isolated diagnostic execution to any MCP client, with input validation, command blocklists, retry with back-off, and sanitized errors built in.
- Cuts per-endpoint agent integration time from ~2 hours to under 30 minutes — new diagnostic capabilities are a single decorated function.
- **Status:** Verified **A-Grade Quality** on Glama, CI-tested on every push, listed on global MCP indexes.

[![cyberrescue MCP server](https://glama.ai/mcp/servers/Vivekpatil200320/cyberrescue/badges/card.svg)](https://glama.ai/mcp/servers/Vivekpatil200320/cyberrescue)

#### 📚 [ContextQuery](https://github.com/vivekpatil200320/contextquery-backend)
*Grounded document Q&A with hybrid retrieval — every answer traceable to the exact source passage.*
- Hybrid BM25 + semantic search (fused via Reciprocal Rank Fusion) with NVIDIA NIM reranking cuts irrelevant context injection by ~40% versus naive top-K retrieval.
- FastAPI + Chroma Cloud + NVIDIA NIM (embed/rerank/LLM), traced end-to-end in Langfuse, with a repeatable eval harness.
- [Next.js 15 frontend](https://github.com/vivekpatil200320/contextquery-frontend) · [Live demo](https://contextquery-frontend.vercel.app) · [Write-up: how I got 100% retrieval precision with hybrid RRF](https://dev.to/vivek_vdev/hybrid-retrieval-rrf-how-i-got-100-retrieval-precision-in-a-production-rag-system-1oga)

#### 🚀 [PyCursor](https://github.com/Vivekpatil200320/PyCursor--Self-Healing-Hybrid-Coding-Agent)
*A self-healing Python coding agent — writes, executes, and fixes its own code.*
- LangGraph state machine feeds runtime stack traces back into the LLM until the code executes cleanly: 90% self-healing success rate on Python stack traces.
- Runs fully on-device via Ollama (Qwen2.5-Coder 7B) by default, with a one-toggle switch to Gemini cloud inference.

#### 🧠 [leetcode-solutions](https://github.com/vivekpatil200320/leetcode-solutions)
*DSA practice in Python, structured around the NeetCode 75 roadmap — 3–4 problems a week, each with complexity notes and intuition.*

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
