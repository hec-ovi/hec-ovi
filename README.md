<h1 align="center">Hector Oviedo</h1>

<p align="center"><strong>Applied AI Engineer. Agentic engineering.</strong></p>

<p align="center">
  <a href="https://hec-ovi.dev"><img src="https://img.shields.io/badge/Website-hec--ovi.dev-0969da?style=flat-square" alt="Website"></a>
  <a href="https://elcensuradoweb.com"><img src="https://img.shields.io/badge/Censurado-elcensuradoweb.com-e01842?style=flat-square" alt="Censurado, a live AI news portal"></a>
  <a href="https://linkedin.com/in/hec-ovi"><img src="https://img.shields.io/badge/LinkedIn-hec--ovi-0a66c2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
</p>

I build agentic systems end to end: multi-agent engines, MCP servers and clients, RAG backends with published retrieval evals, and local LLM inference on AMD hardware. Last role: Senior AI Solutions Architect at Ohara, building the tool and MCP integration layer of Modu, an agent that generated full apps, and its multimodal vendor stack (Hedra, HeyGen, Veo 3, Runway, Flux, ElevenLabs, PlayHT). Remote, from Rosario, Argentina.

<p align="center">🏆 <strong>1st place, Anna AI-Native App Hackathon 2026</strong>, with <a href="https://github.com/hec-ovi/gamentic">gamentic</a>: my multi-agent dungeon RPG, ported to run natively on the Anna platform in one week (<a href="https://github.com/hec-ovi/gamentic-anna">port repo</a>).</p>

<p align="center"><a href="https://github.com/hec-ovi/gamentic"><img src="assets/anna-hackathon-2026-first-place.jpeg" alt="First place certificate, Anna Hackathon 2026" width="440"></a></p>

---

<h2 align="center">Agents and agentic loops</h2>

| Repo | What it is |
|---|---|
| [Censurado](https://elcensuradoweb.com) | Self-hosted AI news portal run end to end by an agent harness, live at [elcensuradoweb.com](https://elcensuradoweb.com). The [brain](https://github.com/hec-ovi/censurado-web-brain) is a stdlib Python CLI toolkit an agent drives through tool calls, with its own skill recipe, a gated editorial walk, and a 24/7 serve loop with a multi-agent fallback chain (Gemini, Codex, Claude, local model). The [backend](https://github.com/hec-ovi/censurado-web-backend) is Go with an append-only publish API, distroless. The [frontend](https://github.com/hec-ovi/censurado-web) is a static generator with content-addressed pages. |
| [gamentic](https://github.com/hec-ovi/gamentic) | The hackathon winner above, fully local: state-machine engine, every character its own agent with bounded memory, 40 validated tools, swappable text/image/voice layers. 850+ tests. |
| [noob-cli](https://github.com/hec-ovi/noob-cli) | Compact Rust agent CLI for local OpenAI-compatible models: Docker isolation, sessions, skills, MCP, plan mode, sub-agents, web search. 673 tests, release binary under 4 MB with 40 runtime crates. |
| [agentickit](https://github.com/hec-ovi/agentickit) | React copilot framework on AG-UI: reads app state, fills forms, confirms destructive actions, calls your tools, `.pilot/` markdown skills. 579 tests, on npm. |
| [open-research](https://github.com/hec-ovi/open-research) | Deep-research pipeline: Planner / Finder / Summarizer / Reviewer / Writer agents, SSE telemetry, durable sessions, PDF and Markdown exports. |
| [rebel-forge](https://github.com/hec-ovi/rebel-forge) | Autonomous social-media agent: 11-tool loop with error recovery, per-platform voice memory, publishes to five networks from one prompt. |

<h2 align="center">MCP, skills and agent tooling</h2>

| Repo | What it is |
|---|---|
| [telegram-bot-skill](https://github.com/hec-ovi/telegram-bot-skill) | Any local CLI coding agent (Claude Code, opencode, Codex, Gemini) as a private Telegram bot. One repo, three surfaces: installable skill, npm toolkit, MCP server over stdio or Streamable HTTP. Zero-dependency Node core, deterministic access tiers, 87 tests. |
| [websearch-skill](https://github.com/hec-ovi/websearch-skill) | Keyless multi-engine web search and page reading for agents: rank fusion, clean Markdown extraction, fetched content fenced as untrusted. PyPI and MCP Registry. |
| [research-skill](https://github.com/hec-ovi/research-skill) | Persistent project-scoped knowledge base for SKILL.md agents: progressive disclosure, contrarian-pass investigation, survives context compaction. |
| [mcp-dashboard](https://github.com/hec-ovi/mcp-dashboard) | Browser-only MCP explorer: discover servers, connect over HTTP or SSE, inspect capabilities, run tools live. |
| [mcp-ollama-studio](https://github.com/hec-ovi/mcp-ollama-studio) | Local-first MCP client studio: ReAct agent, OpenAI-compatible backend, React UI with reasoning rail. |

<h2 align="center">RAG and retrieval</h2>

| Repo | What it is |
|---|---|
| [rag-base](https://github.com/hec-ovi/rag-base) | Hybrid search backend: pgvector + ParadeDB BM25 + LightRAG graph, 4-mode rerank on CPU and AMD GPU sidecars, GLiNER NER. 19 endpoints, 115 integration tests, evals report hit@1 / hit@5 / MRR including the cases where the reranker makes results worse. |
| [rag-suite](https://github.com/hec-ovi/rag-suite) | Four isolated backends (inference, ingestion, RAG, reranker) with dense + BM25 and reranked retrieval. |
| [vanilla-rag-architecture](https://github.com/hec-ovi/vanilla-rag-architecture) | Cross-encoder rerank (top-10 to top-3) with multimodal ingestion, FAISS or Chroma. |

<h2 align="center">Local inference on AMD, no CUDA</h2>

AMD Strix Halo (Ryzen AI Max+ 395, gfx1151, 128 GB unified memory) is the rig on my desk, so it is where I specialize and where every number below was measured. Everything serves OpenAI-compatible endpoints. Running these stacks without CUDA is the harder problem; the same setups move to NVIDIA, other GPUs, or hosted endpoints easily.

| Repo | What it is |
|---|---|
| [vllm-awq4-qwen](https://github.com/hec-ovi/vllm-awq4-qwen) | vLLM + Qwen 3.6-27B AWQ-INT4 + DFlash speculative decoding on Strix Halo (gfx1151, 128 GB UMA). Measured 24.8 t/s single-stream, vision, tool calling, 256K context. |
| [llama-vulkan-strix](https://github.com/hec-ovi/llama-vulkan-strix) | llama.cpp server on Vulkan for gfx1151, GGUF weights pinned to GTT, plus an opt-in ROCm FP4 + MTP stack. Real measured benchmarks. |
| [vllm-qwen](https://github.com/hec-ovi/vllm-qwen) / [llama-qwen](https://github.com/hec-ovi/llama-qwen) | BF16 and Q8_0 OpenAI-compatible servers for the same board, 256K context, TheRock ROCm. |
| [comfyui-strix-docker](https://github.com/hec-ovi/comfyui-strix-docker) | ComfyUI on gfx1151, fixing the silent CPU fallback stock images hit. |

Off the agent path: [xubamp](https://github.com/hec-ovi/xubamp), a from-scratch Winamp-style audio player for Wayland written in Rust; [music](https://github.com/hec-ovi/music), a static no-backend YouTube playlist player with agent bulk-import; and [ai-music-studio](https://github.com/hec-ovi/ai-music-studio), local album generation (LLM plan, ACE-Step tracks, FLUX cover art) on ROCm.

Earlier AI work: [computer-vision](https://github.com/hec-ovi/computer-vision) (2024) benchmarks YOLOv8, EfficientDet, Detectron2, and SAM2 head to head for object detection and segmentation in video, PyTorch on CUDA. [nerex](https://github.com/hec-ovi/nerex) (2024) extracts financial entities and numbers over four engines: regex, spaCy, word2number, BERT.

<h2 align="center">How I work</h2>

Agentic engineering: coding agents (Claude Code, my own noob-cli) write most first drafts; architecture, integration tests, and security review stay with me. Happy to walk through any commit on a call.

Open to remote senior Applied AI roles and specialist contracts: agent systems, MCP integrations, RAG, local inference on ROCm. Reach me through [hec-ovi.dev](https://hec-ovi.dev) or [LinkedIn](https://linkedin.com/in/hec-ovi).
