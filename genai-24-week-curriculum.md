# GenAI Job Prep — 24-Week Curriculum with Daily Plans

**Goal:** Senior GenAI Developer / Architect role in Europe within ~6 months.
**Weekday budget (Mon–Thu):** Builder 45m + User 45m + deep-ml 30m + Tools 30m ≈ 2.5 hrs.
**Friday (~2 hrs):** review + The Code newsletter + weekly paper + LinkedIn post.
**Weekend:** ~2 hrs/day project block + LinkedIn/job-search work.

**Already completed (removed from this plan):**
- Karpathy micrograd + your extended fork (activation-function registry, loss functions)
- CampusX Prompt Engineering course

**Newsletter:** [The Code](https://codenewsletter.ai/) (replaces AlphaSignal) — skim 2 latest issues every Friday.

---

## Track Definitions

| Track | What it is | Daily time |
|---|---|---|
| **Builder** | Transformer internals, LLMs from scratch (Karpathy + Vizuara) | 45 min |
| **User** | Applied GenAI — RAG, agents, LangGraph, MCP, deployment | 45 min |
| **deep-ml** | [deep-ml.com/problems](https://www.deep-ml.com/problems) drills — **non-negotiable fixed block; historically skip-prone; protect it** | 30 min |
| **Tools** | AI coding tools on throwaway projects only — never portfolio repos | 30 min |
| **Newsletter & Papers** | The Code ×2 + 1 paper/week | Friday |

## Tools Track Rotation

| Month | Tool | Throwaway project |
|---|---|---|
| 1 (Wk 1–4) | Claude Code | Study tracker (Streamlit + SQLite) — already underway |
| 2 (Wk 5–8) | OpenAI Codex | Code-explainer CLI |
| 3 (Wk 9–12) | Cursor | Small web dashboard |
| 4 (Wk 13–16) | Claude Code advanced (MCP, skills, hooks, sub-agents) | Toy MCP server |
| 5 (Wk 17–20) | Cross-tool workflows (plan-review-implement, test-first) | Refactor an old toy repo |
| 6 (Wk 21–24) | Consolidation — "how I use AI tools" narrative | Blog post + demo |

GitHub Copilot and Devin excluded (used at work daily).

## Verified Core Resources

- Karpathy nn-zero-to-hero: <https://github.com/karpathy/nn-zero-to-hero>
- "Let's build GPT": <https://www.youtube.com/watch?v=kCc8FmEb1nY>
- "GPT Tokenizer": <https://www.youtube.com/watch?v=zduSFxRajkE> · minbpe: <https://github.com/karpathy/minbpe>
- makemore P1: <https://www.youtube.com/watch?v=PaCmpygFfXo> · P2: <https://youtu.be/TCH_1BHY58I> · P3: <https://youtu.be/P6sfmUTpUmc> · P5: <https://youtu.be/t3YJ5hKiMQ0>
- Vizuara "Building LLMs from scratch" (43 lectures): <https://www.youtube.com/playlist?list=PLPTV0NXA_ZSgsLAr8YCgCwhPIJNNtexWu>
- Vizuara channel: <https://www.youtube.com/@vizuara> · Context Engineering: <https://context-engineering.vizuara.ai/>
- CampusX LangChain: <https://www.youtube.com/playlist?list=PLKnIA16_RmvaTbihpo4MtzVm4XOQa0ER0>
- CampusX LangGraph: <https://www.youtube.com/playlist?list=PLKnIA16_RmvYsvB8qkUQuJmJNuiCUJFPL>
- CampusX 100 Days of DL: <https://www.youtube.com/playlist?list=PLKnIA16_RmvYuZauWaPlRTC54KxSNLtNn>
- CampusX 100 Days of ML: <https://www.youtube.com/playlist?list=PLKnIA16_Rmvbr7zKYQuBfsVkjoLcJgxHH>
- deep-ml: <https://www.deep-ml.com/problems> · The Code: <https://codenewsletter.ai/>

Where a line says "Vizuara lectures 14–17 region", open the playlist and navigate — playlist links are stable; individual video URLs are not.

---

# PHASE 1 — Foundations (Weeks 1–4)

## Week 1 — Transformer architecture & attention

| Day | Builder (45m) | User (45m) | deep-ml (30m) | Tools (30m) |
|---|---|---|---|---|
| Mon | Vizuara Lecture 1 (series intro + architecture) | Hand-draw the full transformer diagram from memory; annotate | 2× linear algebra (matmul, dot product) | Claude Code: derive `CLAUDE.md` from `ideas.md` |
| Tue | "Let's build GPT" first half (fast through backprop — you have micrograd mastery) | Code scaled dot-product attention from scratch in PyTorch | 2× linear algebra | Claude Code: resolve open study-tracker decisions (minute targets, note field, layout) |
| Wed | "Let's build GPT" second half | Extend to multi-head; sinusoidal positional encoding | 2× deep learning | Claude Code: scaffold repo per CLAUDE.md |
| Thu | Vizuara attention lectures (14–17 region) | Causal mask + verify future-token blocking; simple KV cache | 2× deep learning | Claude Code: first schema migration for tracker |
| **Fri** | *Review + The Code ×2 · Paper: [Attention Is All You Need](https://arxiv.org/abs/1706.03762) §1,3,4 · LinkedIn: profile foundation week (see LinkedIn path) + post #1: "I re-implemented self-attention — 3 surprises"* ||||
| **Sat** | **Mini-GPT Day 1:** pick corpus; repo with uv + pyproject.toml (micrograd-fork conventions); data loader, char tokenizer, Transformer block ||||
| **Sun** | **Mini-GPT Day 2:** train; loss curves; sampling; README + architecture diagram; push + pin ||||

## Week 2 — Tokenization & embeddings

| Day | Builder (45m) | User (45m) | deep-ml (30m) | Tools (30m) |
|---|---|---|---|---|
| Mon | "GPT Tokenizer" part 1 | Code along with minbpe | 2× NLP | Claude Code: tracker data layer (sqlite3, no ORM) |
| Tue | "GPT Tokenizer" part 2 | GPT-2 vs LLaMA tokenizer on identical text; Unicode/emoji/code edge cases | 2× NLP (cosine sim, softmax) | Claude Code: pytest for data layer — plan-first prompting |
| Wed | Vizuara tokenization lectures (5–10 region) | makemore P1 code-along: bigram model + t-SNE of embeddings | 2× NLP | Claude Code: logging + log-entry CRUD |
| Thu | makemore P2 first half (1.5x fine) | Cosine similarity on sentence-transformers; nearest neighbours | 2× mixed | Claude Code: streak calculation logic + tests |
| **Fri** | *Review + The Code ×2 · Read: [HF NLP Course Ch.1](https://huggingface.co/learn/nlp-course/chapter1/1) · LinkedIn post: "Why tokenization is the weirdest part of LLMs" · Connections Batch 1 (see LinkedIn path)* ||||
| **Sat** | Swap Mini-GPT char tokenizer for your BPE; compare perplexity; document ||||
| **Sun** | 600-word dev-log (Medium/Substack); push; update pinned repos ||||

## Week 3 — Fine-tuning & PEFT

| Day | Builder (45m) | User (45m) | deep-ml (30m) | Tools (30m) |
|---|---|---|---|---|
| Mon | makemore P3 — **skip activation sections**; BatchNorm, init scales, diagnostic plots | [HF fine-tuning Ch.3](https://huggingface.co/learn/nlp-course/chapter3/1) hands-on | 2× deep learning | Claude Code: tracker Streamlit pages — keep Claude out of the data layer |
| Tue | [LoRA paper](https://arxiv.org/abs/2106.09685) §1–4; re-derive rank decomposition | LoRA via PEFT on a small HF model | 2× deep learning | Claude Code: weekly-summary page |
| Wed | Vizuara fine-tuning lectures (final third of playlist) | Alpaca-format dataset; train with [Unsloth](https://github.com/unslothai/unsloth) | 2× ML | Claude Code: charts on tracker (progress over time) |
| Thu | [Constitutional AI](https://arxiv.org/abs/2212.08073) §1–3; diagram SFT→RLHF→DPO | Vizuara channel: RLHF/alignment lecture | 2× ML | Claude Code: bug-fix session; note failure modes |
| **Fri** | *Review + The Code ×2 · Paper: LoRA (full) · LinkedIn post: "LoRA explained in one diagram" · Connections Batch 2* ||||
| **Sat** | Fine-tune Phi-3 mini / LLaMA 3.1 8B on domain data (500–1000 pairs); loss curves ||||
| **Sun** | Base vs fine-tuned on 20 prompts; push to HF Hub; README results table; LinkedIn share ||||

## Week 4 — Evaluation frameworks

| Day | Builder (45m) | User (45m) | deep-ml (30m) | Tools (30m) |
|---|---|---|---|---|
| Mon | [RAGAS paper](https://arxiv.org/abs/2309.15217) full | [RAGAS](https://docs.ragas.io/) on toy QA set: faithfulness + relevancy | 2× mixed review | Claude Code: tracker polish |
| Tue | [LLM-as-a-Judge](https://arxiv.org/abs/2306.05685) §1–4 | G-Eval-style judge with Claude/GPT-4o; score 50 pairs | 2× mixed | Claude Code: export feature (CSV) |
| Wed | makemore P5 (WaveNet) — architectural intuition | [DeepEval](https://docs.confident-ai.com/) pytest-style tests on your fine-tuned model | 2× mixed | Claude Code: README + screenshots for tracker |
| Thu | Vizuara channel: evaluation/benchmark lecture | [eval-harness](https://github.com/EleutherAI/lm-evaluation-harness) subset run; notes on when benchmarks lie | 2× mixed | Claude Code month wrap-up: 1-page "what worked / what didn't" |
| **Fri** | *Review + The Code ×2 · Paper: LLM-as-a-Judge (full) · LinkedIn post: "3 metrics to evaluate your RAG system" · Connections Batch 3* ||||
| **Sat** | 50-triple eval dataset + RAGAS/DeepEval metrics dashboard notebook ||||
| **Sun** | **Phase 1 retrospective**; README pass; connect with 5 EU GenAI engineers ||||

---

# PHASE 2 — RAG Mastery (Weeks 5–10)

## Week 5 — RAG patterns & context engineering

| Day | Builder (45m) | User (45m) | deep-ml (30m) | Tools (30m) |
|---|---|---|---|---|
| Mon | Vizuara: unfinished lectures / pretraining lectures | CampusX LangChain Vids 1–2; naive RAG on a PDF ([tutorial](https://python.langchain.com/docs/tutorials/rag/)) | 2× NLP | Codex: install + configure; start code-explainer CLI |
| Tue | [Vizuara Context Engineering outline](https://context-engineering.vizuara.ai/): WSCI framework, six context elements | Refactor RAG prompt into structured context template (system prompt "at the right altitude") | 2× NLP | Codex: CLI arg parsing + first explain command |
| Wed | [HyDE paper](https://arxiv.org/abs/2212.10496) | Implement HyDE; RAGAS vs naive | 2× linear algebra | Codex: note plan/execute-mode differences vs Claude Code |
| Thu | CampusX LangChain text-splitter vids (8–10) | Fixed vs parent-child chunking comparison; hybrid search (BM25 + Qdrant, tune alpha) | 2× mixed | Codex: add syntax highlighting to CLI |
| **Fri** | *Review + The Code ×2 · Paper: [Self-RAG](https://arxiv.org/abs/2310.11511) §1–4 · LinkedIn post: "Naive vs HyDE vs hybrid — benchmark" · Connections Batch 4* ||||
| **Sat** | **RAG Benchmark Day 1:** corpus (EU AI Act or 10-Ks); loaders; chunking; embeddings → [Qdrant](https://qdrant.tech/documentation/) ||||
| **Sun** | **Day 2:** naive + HyDE strategies; 50-pair eval set; RAGAS both; commit CSV ||||

## Week 6 — Vector databases

| Day | Builder (45m) | User (45m) | deep-ml (30m) | Tools (30m) |
|---|---|---|---|---|
| Mon | [Vector search explained (Weaviate)](https://weaviate.io/blog/vector-search-explained) — HNSW internals | 10k vectors in Qdrant; HNSW vs brute-force recall/latency | 2× deep learning | Codex: CLI handles multi-file input |
| Tue | Qdrant docs: quantization + payload indexing | Filtered semantic search (metadata + vectors) | 2× deep learning | Codex: tests for CLI |
| Wed | Vendor architecture comparison reading | Migrate corpus to Weaviate/Chroma; latency comparison | 2× ML | Codex: same task you gave Claude Code wk2 — compare |
| Thu | PQ theory | Enable PQ; recall@10 vs memory; 1-page vendor table (interview artifact) | 2× ML | Codex: refine CLI output formatting |
| **Fri** | *Review + The Code ×2 · Paper: [ColBERT](https://arxiv.org/abs/2004.12832) · LinkedIn post: "Choosing a vector DB for production" · 10 EU-peer connections* ||||
| **Sat** | **RAG Benchmark Day 3:** hybrid as strategy 3; full RAGAS table + charts ||||
| **Sun** | **Day 4:** 800-word README (methodology, results, winner) + diagram; publish on Medium ||||

## Week 7 — Re-ranking & query intelligence

| Day | Builder (45m) | User (45m) | deep-ml (30m) | Tools (30m) |
|---|---|---|---|---|
| Mon | [SBERT retrieve & re-rank](https://www.sbert.net/examples/applications/retrieve_rerank/README.html) | Add cross-encoder / Cohere Rerank; RAGAS delta | 2× mixed | Codex: docstring generation feature |
| Tue | CampusX LangChain RAG vids (16–18 region) | [MultiQueryRetriever](https://python.langchain.com/docs/how_to/MultiQueryRetriever/) + step-back prompting | 2× mixed | Codex: complexity-analysis feature |
| Wed | Query routing theory | Route legal vs technical queries to different indexes | 2× NLP | Codex: error handling pass |
| Thu | [Contextual compression docs](https://python.langchain.com/docs/how_to/contextual_compression/) — the Compress step of WSCI | Add compression; token reduction vs quality | 2× NLP | Codex: README + demo GIF for CLI |
| **Fri** | *Review + The Code ×2 · Paper: Self-RAG (full) · LinkedIn post: "The re-ranking layer most RAG systems skip" · Comment on 3 EU posts daily habit starts* ||||
| **Sat** | **RAG Benchmark Day 5:** re-ranker as strategy 4; rerun full eval ||||
| **Sun** | Final polish: excalidraw diagram, lessons-learned, LinkedIn featured section ||||

## Week 8 — Multi-modal RAG

| Day | Builder (45m) | User (45m) | deep-ml (30m) | Tools (30m) |
|---|---|---|---|---|
| Mon | Vizuara vision/multimodal lecture | CLIP cross-modal retrieval | 2× CV | Codex: CLI edge cases |
| Tue | [LLaVA paper](https://arxiv.org/abs/2304.08485) intro + architecture | [Unstructured](https://docs.unstructured.io/) PDF image+text extraction | 2× CV | Codex: publish CLI to a private repo; tag v0.1 |
| Wed | Table-extraction strategies reading | Tables → Markdown → embed → query | 2× NLP | Codex: wrap-up notes begin |
| Thu | [GraphRAG paper](https://arxiv.org/abs/2404.16130) intro + method | Run [GraphRAG repo](https://github.com/microsoft/graphrag) on small corpus; GraphRAG-vs-dense decision notes | 2× mixed | Codex month wrap-up: 1-page "Claude Code vs Codex" |
| **Fri** | *Review + The Code ×2 · Paper: GraphRAG (full) · LinkedIn post: "Multi-modal RAG"* ||||
| **Sat** | **Multi-modal Q&A Day 1:** chart-heavy PDF; extraction → CLIP → LLaVA/GPT-4V ||||
| **Sun** | **Day 2:** eval; README; demo GIF; push + LinkedIn demo ||||

## Week 9 — Guardrails & safety

| Day | Builder (45m) | User (45m) | deep-ml (30m) | Tools (30m) |
|---|---|---|---|---|
| Mon | [NeMo Guardrails docs](https://docs.nvidia.com/nemo/guardrails/latest/index.html): rail types | NeMo quickstart integration | 2× mixed | Cursor: install; start throwaway dashboard; learn Tab |
| Tue | [Presidio docs](https://microsoft.github.io/presidio/) | PII detection + redaction before indexing | 2× mixed | Cursor: Composer mode on dashboard |
| Wed | [Jailbreak taxonomy](https://learnprompting.org/docs/prompt_hacking/jailbreaking) | Red-team your bot: 10 adversarial prompts; input-validation layer | 2× NLP | Cursor: agent mode task |
| Thu | A provider system card (Claude/GPT-4) safety section | Full NeMo integration into RAG pipeline | 2× ML | Cursor: compare inline-edit ergonomics vs Claude Code |
| **Fri** | *Review + The Code ×2 · Paper: Constitutional AI (full) · LinkedIn post: "3 layers of guardrails" · Start upward networking (team leads, 10/wk)* ||||
| **Sat** | Guardrails on RAG Benchmark: PII + topic rail + injection filter; documented pass rate ||||
| **Sun** | 2-page architecture doc; LinkedIn carousel ||||

## Week 10 — Observability

| Day | Builder (45m) | User (45m) | deep-ml (30m) | Tools (30m) |
|---|---|---|---|---|
| Mon | [LangSmith docs](https://docs.smith.langchain.com/) tracing concepts | LangSmith tracing on RAG pipeline; waterfall view | 2× mixed review | Cursor: dashboard chart feature |
| Tue | CampusX LangGraph observability/LangSmith vids | Profile end-to-end; slowest step; token cost logging | 2× mixed | Cursor: dashboard API integration |
| Wed | [Phoenix docs](https://docs.arize.com/phoenix) quickstart | Phoenix instrumentation; embedding visualizations | 2× mixed | Cursor: replicate a wk-2 Claude Code task; 3-way notes |
| Thu | [LangSmith eval tutorial](https://docs.langchain.com/langsmith/evaluate-rag-tutorial) | A/B test two prompts; win rate | 2× mixed | Cursor: dashboard polish |
| **Fri** | *Review + The Code ×2 · Paper: Self-RAG re-read (interview reference) · LinkedIn post: "Observability for LLM apps — 6 weeks of lessons"* ||||
| **Sat** | Full observability dashboard on RAG Benchmark: latency, cost, RAGAS per strategy ||||
| **Sun** | **Phase 2 retrospective**; plan Research Agent scope; 10 EU connections ||||

---

# PHASE 3 — Agentic Systems (Weeks 11–16)

## Week 11 — Agent patterns

| Day | Builder (45m) | User (45m) | deep-ml (30m) | Tools (30m) |
|---|---|---|---|---|
| Mon | [ReAct paper](https://arxiv.org/abs/2210.03629) full | CampusX LangGraph Vids 1–2 | 2× — protect this block; Phase 3 is where it slips | Cursor: continue dashboard |
| Tue | Implement ReAct from scratch, no framework (Wikipedia + calculator) | CampusX LangGraph Vid 3 + tool-calling vids; multi-tool agent (Claude tool use) | 2× | Cursor: agent-mode refactor task |
| Wed | [Reflexion](https://arxiv.org/abs/2303.11366) §1–4 | Self-critique loop + retry-on-error in your ReAct agent | 2× | Cursor: note task-type preferences per tool |
| Thu | LangGraph state/nodes/edges concepts ([docs](https://langchain-ai.github.io/langgraph/)) | CampusX LangGraph Vids 4–6; stateful graph: retrieve → grade → answer/retry | 2× | Cursor: dashboard tests |
| **Fri** | *Review + The Code ×2 · Paper: [Toolformer](https://arxiv.org/abs/2302.04761) · LinkedIn post: "ReAct vs Plan-and-Execute"* ||||
| **Sat** | **Research Agent Day 1:** design (tools, state schema, topology); skeleton graph; arXiv + web search tools ||||
| **Sun** | **Day 2:** planning node (sub-task decomposition); conditional routing; 5-question test ||||

## Week 12 — Multi-agent systems

| Day | Builder (45m) | User (45m) | deep-ml (30m) | Tools (30m) |
|---|---|---|---|---|
| Mon | [LangGraph multi-agent concepts](https://langchain-ai.github.io/langgraph/concepts/multi_agent/) | CampusX LangGraph multi-agent vids; supervisor → specialist sub-agents | 2× | Cursor: dashboard final feature |
| Tue | Message passing vs shared state tradeoffs | Refactor to 3 sub-agents via message passing | 2× | Cursor: month wrap-up notes |
| Wed | CrewAI + AutoGen quickstart reading | Port 2-agent slice to CrewAI; complexity comparison | 2× | Finalize 3-way comparison doc |
| Thu | HITL / interrupt patterns | CampusX HITL vid; human-approval checkpoint before final report | 2× | Draft tool-comparison LinkedIn post |
| **Fri** | *Review + The Code ×2 · Paper: [MemGPT](https://arxiv.org/abs/2310.08560) · LinkedIn post: "LangGraph vs CrewAI"* ||||
| **Sat** | **Research Agent Day 3:** synthesis node; episodic memory; 10-question end-to-end ||||
| **Sun** | **Day 4:** LangSmith tracing; cost/latency per run; README + trace screenshot ||||

## Week 13 — Tool use & MCP

| Day | Builder (45m) | User (45m) | deep-ml (30m) | Tools (30m) |
|---|---|---|---|---|
| Mon | [MCP introduction](https://modelcontextprotocol.io/introduction) — protocol internals: transports, resources vs tools, sampling (you already run MCP on Claude Desktop) | Build an MCP server exposing a tool; connect from Claude Desktop | 2× | CC-advanced: toy MCP server as throwaway (separate repo from User track) |
| Tue | MCP client architecture | CampusX "MCP Client using LangGraph" vid | 2× | CC-advanced: skills exploration |
| Wed | Structured outputs theory | CampusX LangChain Vid 5; Pydantic + instructor schemas in agent reports | 2× | CC-advanced: hooks (auto-run pytest) |
| Thu | [E2B docs](https://e2b.dev/docs) | Sandboxed code-exec tool; [fallbacks](https://python.langchain.com/docs/how_to/fallbacks/) + backoff + recovery | 2× | CC-advanced: sub-agent for docs lookups |
| **Fri** | *Review + The Code ×2 · Paper: Toolformer (full) · LinkedIn post: "MCP — the missing link in LLM tooling"* ||||
| **Sat** | **Research Agent Day 5:** expose agent tools via MCP; test from Claude Desktop; protocol design doc ||||
| **Sun** | **Day 6:** 20-query end-to-end; fix top 3 bugs; demo video on LinkedIn ||||

## Week 14 — Memory in agents

| Day | Builder (45m) | User (45m) | deep-ml (30m) | Tools (30m) |
|---|---|---|---|---|
| Mon | [MemGPT](https://arxiv.org/abs/2310.08560) full read | Short-term + long-term memory in a conversational agent | 2× | CC-advanced: memory-file experiments |
| Tue | [Lilian Weng — Autonomous Agents](https://lilianweng.github.io/posts/2023-06-23-agent/) | CampusX LangGraph memory vids (22–24) | 2× | CC-advanced: custom slash commands |
| Wed | Checkpointer abstraction + time-travel replay theory | SQLite checkpointing (you know sqlite3 from the tracker); resume a paused run | 2× | CC-advanced: workflow automation |
| Thu | Cognitive-architecture design exercise (planning/memory/perception/action sketch) | [Mem0](https://docs.mem0.ai/) cross-session memory in a support bot | 2× | CC-advanced: notes for wrap-up |
| **Fri** | *Review + The Code ×2 · Paper: MemGPT re-read · LinkedIn post: "Memory in AI agents — a taxonomy"* ||||
| **Sat** | **Research Agent Day 7:** long-term memory; verify 3-session recall ||||
| **Sun** | **Day 8:** 3-page architecture design doc (interview ammunition); publish ||||

## Week 15 — Production deployment

| Day | Builder (45m) | User (45m) | deep-ml (30m) | Tools (30m) |
|---|---|---|---|---|
| Mon | [vLLM docs](https://docs.vllm.ai/en/latest/): paged attention, continuous batching | Serve LLaMA 3.1 8B with vLLM; throughput benchmark | 2× | CC-advanced: scaffold Dockerfiles for a throwaway service |
| Tue | Quantization theory (GGUF/AWQ/GPTQ) | CampusX 100-Days-DL quantization vids; 4-bit AWQ comparison | 2× | CC-advanced: evaluate its infra-code quality |
| Wed | FastAPI async/streaming patterns | FastAPI streaming SSE /query endpoint | 2× | CC-advanced: compose file + healthchecks |
| Thu | Semantic caching theory | GPTCache/Redis semantic cache; hit-rate measurement | 2× | CC-advanced: CI basics with Claude Code |
| **Fri** | *Review + The Code ×2 · Paper: [vLLM/PagedAttention](https://arxiv.org/abs/2309.06180) · LinkedIn post: "Deploying LLMs in production"* ||||
| **Sat** | **EU-compliant service Day 1:** Dockerized FastAPI on RAG Benchmark; PII layer; usage logging; /query /health /metrics ||||
| **Sun** | **Day 2:** Streamlit or Gradio frontend (reuse tracker patterns) + history; push image to Docker Hub ||||

## Week 16 — EU AI Act & compliance

| Day | Builder (45m) | User (45m) | deep-ml (30m) | Tools (30m) |
|---|---|---|---|---|
| Mon | [EU AI Act](https://artificialintelligenceact.eu/the-act/) Articles 1–10 (risk tiers) | Map every project to a risk tier | 2× | CC-advanced: wrap-up write-up begins |
| Tue | [ICO AI guidance](https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/artificial-intelligence/) | Audit pipeline personal-data flows; retention policies | 2× | CC-advanced: MCP/hooks/skills learnings doc |
| Wed | EU AI Act Articles 8–15 (high-risk requirements) | Transparency layer: model version, sources, confidence per response | 2× | Month wrap-up complete |
| Thu | EU AI Act Articles 11–13 (documentation) | Model card + system card (HF template); compliance checklist | 2× | Plan month-5 cross-tool experiments |
| **Fri** | *Review + The Code ×2 · Paper: [Agent survey](https://arxiv.org/abs/2308.11432) taxonomy · LinkedIn post: "EU AI Act for GenAI architects — 5 things" · Request 2–3 informational calls* ||||
| **Sat** | 2-page compliance design doc for your service ||||
| **Sun** | **Phase 3 retrospective**; polish all READMEs + diagrams; LinkedIn featured update ||||

---

# PHASE 4 — Interview Prep & Launch (Weeks 17–24)

## Week 17 — System design I

| Day | Builder (45m) | User (45m) | deep-ml (30m) | Tools (30m) |
|---|---|---|---|---|
| Mon | [Chip Huyen — LLM systems](https://huyenchip.com/2023/10/18/llm-systems.html) | Timed 45m whiteboard: support RAG chatbot, 100k users | 2× | Cross-tool: plan-review-implement loop on old toy repo |
| Tue | Re-read Chip Huyen; extract a design checklist | Whiteboard: document intelligence for a European bank | 2× | Cross-tool: test-first prompting drill |
| Wed | Failure-mode catalogue for RAG systems | Whiteboard: multi-agent assistant, 1000 concurrent | 2× | Cross-tool: same feature, two tools |
| Thu | Compliance-driven architecture patterns | Whiteboard: EU-healthcare GenAI platform | 2× | Cross-tool: notes |
| **Fri** | *Review + The Code ×2 · Paper: LLaMA 3 (architecture + safety) · LinkedIn: share a practice design diagram · Recruiter connections begin (see LinkedIn path)* ||||
| **Sat** | 2 mock system-design interviews on [Pramp](https://www.pramp.com/) ||||
| **Sun** | Document 3 design solutions as Markdown repo with diagrams; share ||||

## Week 18 — System design II

| Day | Builder (45m) | User (45m) | deep-ml (30m) | Tools (30m) |
|---|---|---|---|---|
| Mon | Kafka intro + LLM pipeline use cases | Whiteboard: event-driven re-indexing via Kafka | 2× | Cross-tool drills continue |
| Tue | Streaming vs batch tradeoffs | Redo weakest week-17 design cold | 2× | Cross-tool drills |
| Wed | Cost modelling for LLM systems | Add cost estimates to two designs | 2× | Cross-tool drills |
| Thu | Review all design docs | Speak each design aloud, timed 10 min each | 2× | Cross-tool drills |
| **Fri** | *Review + The Code ×2 · Paper: weekly pick from The Code research section · LinkedIn post from design notes · Recruiter messages (3-line format)* ||||
| **Sat** | 1 Pramp mock + debrief ||||
| **Sun** | Design-repo polish; 10 recruiter/hiring-manager connections ||||

## Week 19 — ML fundamentals I

| Day | Builder (45m) | User (45m) | deep-ml (30m→**4 problems/day now**) | Tools (30m) |
|---|---|---|---|---|
| Mon | **Optimizers from scratch** (micrograd removed — you're past it): implement SGD + momentum | Keep projects warm: issue triage | 4× statistics | Draft "how I use AI tools" narrative |
| Tue | Implement Adam; plot convergence paths side by side | Small fixes on agent repo | 4× optimizer problems | Narrative draft |
| Wed | CampusX 100-Days-DL optimizer vids (Adam/RMSProp region) | Project maintenance | 4× linear algebra | Narrative draft |
| Thu | CampusX 100-Days-ML probability/statistics vids; Bayes/MLE/MAP notes | Project maintenance | 4× probability | Narrative review |
| **Fri** | *Review + The Code ×2 · Paper: pick from The Code research · LinkedIn: fundamentals-notes post · Hiring-manager DMs (<80 words, one project link)* ||||
| **Sat** | Flashcards: fundamentals batch 1 ||||
| **Sun** | LinkedIn block: 10 connections + informational-call follow-ups ||||

## Week 20 — ML fundamentals II

| Day | Builder (45m) | User (45m) | deep-ml (**4/day**) | Tools (30m) |
|---|---|---|---|---|
| Mon | CampusX 100-Days-DL regularization vids (dropout, L2, early stopping) | Projects warm | 4× regularization | Narrative refinement |
| Tue | Bias-variance, cross-validation refresh | Projects warm | 4× ML | Narrative refinement |
| Wed | Attention complexity, KV-cache math refresh | Projects warm | 4× deep learning | Blog-post outline: "3 months, 3 AI coding tools" |
| Thu | Interview-question self-drill from notes | Projects warm | 4× mixed | Blog-post outline |
| **Fri** | *Review + The Code ×2 · Paper: pick from The Code · LinkedIn post · Recruiter follow-ups* ||||
| **Sat** | Flashcards batch 2; mock Q&A with a friend ||||
| **Sun** | LinkedIn block ||||

## Week 21 — Coding interviews I

| Day | Builder (45m) | User (45m) | deep-ml (30m) | Tools (30m) |
|---|---|---|---|---|
| Mon | Real Python: async/await deep dive | Make FastAPI service fully async; benchmark | 2× + LeetCode: 3 mediums (sliding window) | Write the tool-comparison blog post |
| Tue | Generators + decorators deep dive | Service benchmark write-up | 2× + LC: 3 mediums (two pointers) | Blog post |
| Wed | Python memory model, GIL notes | Projects warm | 2× + LC: 2 graph/BFS | Blog post |
| Thu | Review Python gotchas list | Projects warm | 2× + LC: review + complexity analysis | Blog post final |
| **Fri** | *Review + The Code ×2 · LinkedIn: publish tool-comparison post (this one travels) · Applications: 3 roles* ||||
| **Sat** | Timed coding session: 4 problems in 90 min ||||
| **Sun** | LinkedIn block + applications ||||

## Week 22 — Coding interviews II

| Day | Builder (45m) | User (45m) | deep-ml (30m) | Tools (30m) |
|---|---|---|---|---|
| Mon | deep-ml attention-from-scratch problem (their hardest tier) | Projects warm | 2× + LC: 3 mediums | Demo video for blog post |
| Tue | deep-ml BPE/tokenizer problem | Projects warm | 2× + LC: 3 mediums | Demo video |
| Wed | Whiteboard attention by hand, no IDE | Projects warm | 2× + LC: 2 graph | Post demo |
| Thu | Speed-run: implement softmax/layernorm/attention in 30 min | Projects warm | 2× + LC review | Consolidation notes |
| **Fri** | *Review + The Code ×2 · LinkedIn post · Applications: 3 roles* ||||
| **Sat** | Full mock coding interview (timed, spoken aloud) ||||
| **Sun** | LinkedIn block + applications ||||

## Week 23 — Behavioral & storytelling

| Day | Builder (45m) | User (45m) | deep-ml (30m) | Tools (30m) |
|---|---|---|---|---|
| Mon | Flashcard review: full-concept pass | Write 4 STAR stories (system designed, failure recovered) | 2× maintenance | Interview narrative: AI-tooling philosophy paragraph (hand-coded portfolio + deliberate tool study — your differentiator) |
| Tue | Flashcard review | Write 4 more STAR stories (cross-team influence, scale) | 2× | Narrative rehearsal |
| Wed | Weak-area drill | Record yourself: 3 behavioral answers; watch back; refine | 2× | Narrative rehearsal |
| Thu | Weak-area drill | 2-min verbal pitch per project, no notes | 2× | Final narrative |
| **Fri** | *Review + The Code ×2 · LinkedIn: endorsements + 1 recommendation ask · Applications: 3 roles* ||||
| **Sat** | Mock behavioral round with a friend ||||
| **Sun** | Featured-section final state: benchmark write-up, agent design doc, tool post ||||

## Week 24 — Final mocks & launch

| Day | Builder (45m) | User (45m) | deep-ml (30m) | Tools (30m) |
|---|---|---|---|---|
| Mon | Final flashcards | [Pramp](https://www.pramp.com/) full system-design mock | 2× | Final portfolio-link checks |
| Tue | Final flashcards | [Interviewing.io](https://interviewing.io/) technical mock | 2× | GitHub profile README final |
| Wed | Debrief + gap fixes | Fix identified gaps | 2× | — |
| Thu | Rest / light review | LinkedIn final pass: headline, about, Open to Work (recruiters-only) | 2× | — |
| **Fri** | *Review + The Code ×2 · 10 personalised connections to EU hiring managers · Apply to top 5 roles* ||||
| **Sat** | **Launch:** apply to 5 roles (talent.io, Otta, LinkedIn EU) with personalised notes ||||
| **Sun** | **Celebrate. Six months of consistent work.** ||||

---

# Weekly Paper List

| Week | Paper |
|---|---|
| 1 | Attention Is All You Need — <https://arxiv.org/abs/1706.03762> |
| 2 | HF NLP Course Ch.1 (reading week) |
| 3 | LoRA — <https://arxiv.org/abs/2106.09685> |
| 4 | LLM-as-a-Judge — <https://arxiv.org/abs/2306.05685> |
| 5 | Self-RAG §1–4 — <https://arxiv.org/abs/2310.11511> |
| 6 | ColBERT — <https://arxiv.org/abs/2004.12832> |
| 7 | Self-RAG (full) |
| 8 | GraphRAG — <https://arxiv.org/abs/2404.16130> |
| 9 | Constitutional AI — <https://arxiv.org/abs/2212.08073> |
| 10 | RAGAS — <https://arxiv.org/abs/2309.15217> |
| 11 | Toolformer — <https://arxiv.org/abs/2302.04761> |
| 12 | MemGPT — <https://arxiv.org/abs/2310.08560> |
| 13 | ReAct — <https://arxiv.org/abs/2210.03629> |
| 14 | Reflexion — <https://arxiv.org/abs/2303.11366> |
| 15 | vLLM/PagedAttention — <https://arxiv.org/abs/2309.06180> |
| 16 | Agent survey (Wang et al.) — <https://arxiv.org/abs/2308.11432> |
| 17–24 | LLaMA 3 · HyDE · LLaVA · weekly picks from The Code's research section |

---

# Guided Path — LinkedIn Rebuild (dormant account → credible EU-facing profile)

Sequenced deliberately: foundation first, activity second, outreach third. Use the weekend 2-hour blocks. Daily-plan Fridays above reference these milestones.

## Week 1 — Foundation (before any posting)

1. **Photo:** recent, well-lit headshot, plain background.
2. **Banner:** an architecture diagram from your work, or clean gradient + "GenAI Architect · RAG & Agentic Systems".
3. **Headline:**
   > GenAI Architect @ American Express | RAG & Agentic AI Systems | LangGraph · MCP · Evaluation | Open to Senior GenAI roles in Europe
4. **Industry:** "Software Development" (recruiters filter on it).
5. **About:** front-load the first 3 lines (what you do + scale); middle = architecture philosophy (evaluation-first, guardrails, EU AI Act awareness); end = what you're looking for.
6. **Experience:** Amex entry rewritten as 4–6 verb-first bullets ending in outcomes/scale; tech stack per role.
7. **Skills (in this order):** Generative AI, RAG, LangChain, LangGraph, LLM Evaluation, Python, Agentic AI, MCP, Vector Databases, PyTorch.
8. **Open to Work:** recruiters-only (hidden from Amex). Locations: Germany, Netherlands, UK, France, Ireland, Spain. Titles: GenAI Engineer, AI Architect, ML Engineer (LLM), Senior AI Engineer.

## Weeks 2–5 — First 50 connections (batched, in order)

1. **Batch 1 (wk 2, 10–15):** former colleagues/classmates who know your work — fast accepts, seeds the network.
2. **Batch 2 (wk 3, 10–15):** safe current Amex peers.
3. **Batch 3 (wk 4, 10):** creators you learn from (Nitish/CampusX, Vizuara founders) with a genuine 1-line note.
4. **Batch 4 (wk 5, 10–15):** EU-based GenAI **peers** (not hiring managers yet) — note referencing something they posted.

Rule: every request after Batch 1 gets a personalised 1–2 line note.

## Weeks 2–8 — Posting cadence

- 1–2 posts/week, Tue–Thu morning European time.
- Rotate: project posts (after each weekend project) · paper-in-a-diagram · benchmark tables · tool comparisons.
- Reply to every comment within the first hour. 10 min/day commenting substantively on 3 EU GenAI posts (starts week 7 in the daily plan).

## Weeks 9–16 — Network upward

- 10/week: EU team leads and staff engineers at target companies; note = one line on their company's AI work + one line on your relevant project.
- Follow 10–15 target companies.
- Week 16: request 2–3 informational calls ("20 minutes on what your team looks for" — much higher yield than referral asks).

## Weeks 17–24 — Recruiters & hiring managers

- **Wk 17–18:** technical recruiters at target companies; post-accept message: 3 lines — who you are, one impressive specific (RAG benchmark / agent design doc), what you seek + honest visa status.
- **Wk 19–22:** hiring-manager DMs on open roles: reference the role, one project link, under 80 words.
- **Wk 23–24:** Featured section final (benchmark write-up, design doc, tool post, best LinkedIn post); 2–3 endorsements + 1 recommendation.

## Red flags to avoid

- No "seeking opportunities" in the headline while employed.
- Never 100 connection requests in a day (throttling + optics).
- No AI-generated-looking essays — your differentiator is concrete artifacts.
- Don't leave education/certs empty — add Vizuara bootcamp + CampusX certificates as you complete them.

---

*Plan v4 (daily curriculum). Newsletter: The Code. Removed: micrograd + extensions, activation/loss functions, prompt engineering.*
