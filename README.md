<h1 align="center">Hector Oviedo</h1>

<h3 align="center">Applied AI Engineer</h3>

<p align="center"><em>Agentic engineering</em></p>

<p align="center">
  <a href="https://linkedin.com/in/hec-ovi"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linkedin/linkedin-original.svg" height="24" alt="LinkedIn"></a>&nbsp;&nbsp;
  <a href="https://x.com/hec_ovi"><picture><source media="(prefers-color-scheme: dark)" srcset="https://cdn.simpleicons.org/x/white"><img src="https://cdn.simpleicons.org/x/black" height="24" alt="X"></picture></a>&nbsp;&nbsp;
  <a href="https://reddit.com/user/hec-ovi"><img src="https://cdn.simpleicons.org/reddit/FF4500" height="24" alt="Reddit"></a>
</p>

<p align="center">
  <a href="https://hec-ovi.dev"><img src="https://img.shields.io/badge/Website-hec--ovi.dev-0969da?style=flat-square" alt="Website"></a>
</p>

Generalist AI engineer: I implement AI anywhere, from agentic enhancement of an existing product, to computer vision, TTS/STT, or any generative AI, to a full system built from scratch, cloud or fully local.

<h2 align="center">Looking for funding</h2>

<a href="https://elcensuradoweb.com"><img src="https://img.shields.io/badge/Censurado-cf222e?style=flat-square" alt="Censurado"></a> Self-publishing AI news portal, live at [elcensuradoweb.com](https://elcensuradoweb.com): an agentic workflow of up to 14 editorial steps that researches, drafts, evaluates, fact-checks, illustrates, and publishes every story on its own.

<a href="https://github.com/hec-ovi/noob-cli"><img src="https://img.shields.io/badge/noob--cli-bc4c00?style=flat-square" alt="noob-cli"></a> Compact Rust agent CLI for local models: Docker isolation, skills, MCP, sub-agents, and live context-budget accounting in a release binary under 4 MB.

<a href="https://github.com/hec-ovi/gamentic"><img src="https://img.shields.io/badge/gamentic-8250df?style=flat-square" alt="gamentic"></a> Winner of the Anna AI-Native App Hackathon 2026 ([Anna port](https://github.com/hec-ovi/gamentic-anna)): fully local AI dungeon RPG, a multi-agent engine (a narrator plus every NPC as its own agent with its own behavior, context, and memory) over a persistent SQLite world state that only changes through 40 validated tools.

<p align="center"><a href="https://github.com/hec-ovi/gamentic"><img src="assets/anna-hackathon-2026-first-place.jpeg" alt="First place certificate, Anna Hackathon 2026" width="440"></a></p>

---

<h2 align="center">Agents and agentic loops</h2>

Systems where agents run loops with real responsibilities: tools, state, memory, recovery.

| Project Repo Link | What it is |
|---|---|
| [**Censurado**](https://elcensuradoweb.com) | Self-hosted AI news portal run end to end by an agentic workflow loop, live at [elcensuradoweb.com](https://elcensuradoweb.com). Synthetic authors with their own editorial bias and source lists, stories fact-checked against real sources behind a gated editorial review, an append-only publish API so nothing rewrites history, and a 24/7 serve loop that falls back across agents (Gemini, Codex, Claude, local model) when one fails. <a href="https://github.com/hec-ovi/censurado-web-brain"><img src="https://img.shields.io/badge/brain-8250df?style=flat-square" alt="brain"></a> <a href="https://github.com/hec-ovi/censurado-web-backend"><img src="https://img.shields.io/badge/backend-1a7f37?style=flat-square" alt="backend"></a> <a href="https://github.com/hec-ovi/censurado-web"><img src="https://img.shields.io/badge/frontend-0969da?style=flat-square" alt="frontend"></a> |
| [gamentic](https://github.com/hec-ovi/gamentic) | The hackathon winner above, fully local. The world is an explicit state machine: everything the model changes goes through one of 40 validated tools writing to SQLite, so long adventures stay consistent. Every character is its own agent with bounded context and memory, and the text, image, and voice layers (llama.cpp, ComfyUI FLUX.2, Maya1) swap for any OpenAI-compatible or hosted vendor without touching the engine. 850+ tests. |
| [noob-cli](https://github.com/hec-ovi/noob-cli) | Compact Rust agent CLI for local OpenAI-compatible models: Docker isolation, sessions, skills, MCP, plan mode, sub-agents, web search, and live context-budget accounting with compaction receipts. 673 tests, release binary under 4 MB. |
| [open-research](https://github.com/hec-ovi/open-research) | Deep-research pipeline: Planner / Finder / Summarizer / Reviewer / Writer agents, SSE telemetry, durable sessions, PDF and Markdown exports. |
| [rebel-forge](https://github.com/hec-ovi/rebel-forge) | Autonomous social-media agent: 11-tool loop with error recovery, per-platform voice memory, publishes to five networks from one prompt. |

<h2 align="center">Skills, tools, agentic toolkits & MCPs</h2>

Installable infrastructure for other agents: skills, toolkits, MCP servers and clients. Published on PyPI, npm, and the MCP Registry.

| Project Repo Link | What it is |
|---|---|
| [telegram-bot-skill](https://github.com/hec-ovi/telegram-bot-skill) | Any local CLI coding agent (Claude Code, opencode, Codex, Gemini) as a private Telegram bot. One repo, three surfaces: installable skill, npm toolkit, MCP server over stdio or Streamable HTTP. Zero-dependency Node core, deterministic access tiers so strangers wait at a gate, 87 tests. |
| [agentickit](https://github.com/hec-ovi/agentickit) | React copilot framework on AG-UI: reads app state, fills forms, calls your tools, confirms destructive actions with the user before running them, `.pilot/` markdown skills. 579 tests, on npm. |
| [websearch-skill](https://github.com/hec-ovi/websearch-skill) | Keyless multi-engine web search and page reading for agents: rank fusion, clean Markdown extraction, and fetched content fenced as untrusted so a page cannot inject instructions into the agent. PyPI and MCP Registry. |
| [research-skill](https://github.com/hec-ovi/research-skill) | Persistent project-scoped knowledge base for SKILL.md agents: progressive disclosure, contrarian-pass investigation, survives context compaction. |

<h2 align="center">RAG, CAG and agentic accuracy</h2>

Two decisions carry most of an agent's accuracy: what the model is allowed to write, and what enters its context. At Ohara I removed hallucinated API code from Modu's generated apps by replacing free-written integrations with deterministic template injection: the model fills validated interfaces instead of improvising them. On the context side, when the knowledge fits the window, CAG (cache-augmented generation: preload it once into the KV cache and answer from it, no retriever in the loop) beats RAG; RAG earns its place when the corpus outgrows the context. The same constraint-first design runs through the repos above: state-machine grounding in gamentic, source-checked publishing in Censurado, context budgets in noob-cli.

| Project Repo Link | What it is |
|---|---|
| [rag-base](https://github.com/hec-ovi/rag-base) | Hybrid search backend: pgvector + ParadeDB BM25 + LightRAG graph, 4-mode rerank on CPU and GPU sidecars, GLiNER NER. 19 endpoints, 115 integration tests, and an eval harness reporting hit@1 / hit@5 / MRR, including the configurations where the reranker makes results worse. |
| [rag-suite](https://github.com/hec-ovi/rag-suite) | RAG platform split into four isolated backends (inference, ingestion, RAG, reranker) with dense + BM25 hybrid retrieval and reranking. FastAPI + Qdrant, Docker Compose. |

<h2 align="center">Generative AI</h2>

| Project Repo Link | What it is |
|---|---|
| [ai-music-studio](https://github.com/hec-ovi/ai-music-studio) | Local AI album generation: an LLM plans the album, ACE-Step 1.5 generates the tracks, FLUX renders the cover art. SSE-streamed FastAPI backend, React frontend, MP3/MP4 and YouTube-ready exports. |
| [comfyui-strix-docker](https://github.com/hec-ovi/comfyui-strix-docker) | ComfyUI image generation packaged for AMD gfx1151, fixing the silent CPU fallback stock images hit. |

<h2 align="center">Shipped in production at Ohara</h2>

Ohara's Modu was a vibe-coding agent platform, same shape as Lovable: you asked it for an app ("a Facebook clone with NFTs", "a Mario-style game") and it built and deployed it. I joined to write its instruction sets, about 30 of them covering Three.js, Phaser, web3, and the generative vendors below (what Agent Skills are today, before they had a name), and ended up owning the tooling layer the agent ran on. The template-injection fix described above came out of this work. Everything here ran in production:

| Piece | What it was |
|---|---|
| **Video generation** | Hedra, HeyGen, Luma, Veo 3, Runway behind one middleware. Generated apps called video through a single validated interface, and vendors swapped without touching the generated code. |
| **Image generation** | GPT-Image and Flux, same middleware pattern. |
| **Voice and audio** | ElevenLabs and PlayHT for speech, Lyria 2 for music. |
| **Sprite-sheet toolkit** | One run turned a prompt into 16 game-ready sprite assets, so Modu's 2D games got coherent art instead of mismatched one-off images. |
| **Image to 3D** | Text to image to a GLB model that dropped straight into Three.js scenes, so generated games could use real 3D assets. |
| **Multiplayer layer** | Real-time multiplayer for generated apps: SpacetimeDB over WebSocket. I maintained it and rebuilt it every time an upstream change broke it. |
| **Web3 tooling** | Flaunch and Thirdweb integrations, plus a blockchain tool that took an AI-generated Solidity contract through compile, sign, and deploy, and handed the contract address back to the app. |
| **Platform devops** | The template images and shell scripts behind everything: they configured the VMs, spun up databases, created the git repo for each generated app, and pushed it to the cloud automatically. The CLI tools Modu called were mine to maintain. |

<h2 align="center">Local inference, on the hardware you have</h2>

AMD Strix Halo (Ryzen AI Max+ 395, gfx1151, 128 GB unified memory) is the box on my desk, so every number below was measured there. The practice is hardware-agnostic: CUDA, ROCm, Vulkan, or CPU, tuned per board and shipped as Docker with measured benchmarks. Everything serves OpenAI-compatible endpoints.

| Project Repo Link | What it is |
|---|---|
| [vllm-awq4-qwen](https://github.com/hec-ovi/vllm-awq4-qwen) | vLLM + Qwen 3.6-27B AWQ-INT4 + DFlash speculative decoding. Measured 24.8 t/s single-stream, vision, tool calling, 256K context. Matches a DGX Spark at a third of the cost. |
| [llama-vulkan-strix](https://github.com/hec-ovi/llama-vulkan-strix) | llama.cpp server on Vulkan, GGUF weights pinned to GTT, plus an opt-in ROCm FP4 + MTP stack. Real measured benchmarks. |
| [vllm-qwen](https://github.com/hec-ovi/vllm-qwen) / [llama-qwen](https://github.com/hec-ovi/llama-qwen) | BF16 and Q8_0 OpenAI-compatible servers for the same board, 256K context, TheRock ROCm. |

Off the agent path: [xubamp](https://github.com/hec-ovi/xubamp), a classic Winamp 2.9x player rebuilt from scratch in Rust as a native Wayland client (no toolkit, PipeWire audio, classic .wsz skins, 1.5 MB deb), and [music](https://github.com/hec-ovi/music), a static no-backend YouTube playlist player with agent bulk-import.

<h2 align="center">Early AI work</h2>

Where the AI arc started. [computer-vision](https://github.com/hec-ovi/computer-vision) (2024) is my project for the computer-vision module of the Applied AI degree at IU: YOLOv8, EfficientDet, Detectron2, and SAM2 benchmarked head to head for object detection and segmentation in video, PyTorch on CUDA, with a React viewer for the results ([computer-vision-frontend](https://github.com/hec-ovi/computer-vision-frontend)). It is one of three university modules I scored 100% on, each with its own repo: [healthhub](https://github.com/hec-ovi/healthhub) for object-oriented Python, a habit-tracking app (Flask backend, Node frontend, MongoDB, Docker), and [snakeless](https://github.com/hec-ovi/snakeless) for cloud programming, a Terraform-automated serverless stack on AWS: DynamoDB, two Lambda functions, and a static frontend served from S3 through CloudFront.

Further back: the early AI implementations I did at ADGS (Doha, 2018-2024), NLP before GPT was a product. Sentiment analysis, financial entity and number extraction compared across four engines (regex, spaCy, word2number, BERT), and tool calling implemented by hand, back when no model API offered it and LangChain did not exist. ADGS is also where I built a cybersecurity telemetry layer at the application frontend: vanilla JS that captured per-key timing, pressure, gyroscope, and location, and streamed it to a biometric-verification backend that decided whether you were really you.

<h2 align="center">Experience</h2>

Applying AI since 2023, on an AI track that started with pre-GPT NLP at ADGS, on top of 23+ years of production software: games, real-time apps, and frontend platforms. Open to remote applied-AI roles and specialist contracts: agent systems, MCP integrations, RAG, generative pipelines, local inference. Reach me through [hec-ovi.dev](https://hec-ovi.dev) or [LinkedIn](https://linkedin.com/in/hec-ovi).
