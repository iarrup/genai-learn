# 6-Month GenAI Europe Job Preparation Plan — v3

**Target role:** GenAI Developer / Architect (Europe-first)
**Current role:** GenAI Architect, American Express
**Daily commitment:** 2 hours/day
**Cadence:** Mon–Thu learn · Fri revise · Sat–Sun project · Every 6th week = full revision week

---

## How this document is organized

This plan runs **three parallel streams** instead of sequential phases. The streams progress through their own arcs simultaneously, so by Week 4 you've already touched theory, applied work, and coding tools — instead of waiting until Week 12 for applied content.

The three streams:

- **🏗️ BUILDER** — GenAI theory: transformers from scratch, fine-tuning, alignment, recent papers and frontier work
- **🛠️ USER** — Applied GenAI: prompt engineering → context engineering → RAG → agentic → MCP → production
- **⌨️ CODING** — Daily algorithmic practice (deep-ml.com, with a phase-by-phase daily category schedule in its own section below) + intentional rotation through AI coding tools (Claude Code, Cursor, Copilot)

Plus two non-negotiable career tracks running every week:

- **LinkedIn rebuilding** — detailed onboarding starting from a 15-year dormant profile
- **Job search re-entry** — board navigation, ATS reality, application logistics, interview process

Treat the weekly schedule as a structure to fight against, not obey. Life will happen. The non-negotiable is the **weekend project** plus the **weekly LinkedIn cadence** (defined later). Everything else is movable.

---

## Daily / weekly rhythm

Each weekday = 2 hours, structured as:
- **15–20 min:** ⌨️ Coding warmup — 1 deep-ml problem from the daily category schedule (see *Daily deep-ml schedule* section below)
- **90–100 min:** Stream content (Builder or User, alternating)

Stream alternation:
| Day | Stream | Why |
|---|---|---|
| Mon | 🏗️ Builder | Fresh brain for theory-heavy material |
| Tue | 🛠️ User | Applied work, more flexible cognitively |
| Wed | 🏗️ Builder | Build on Monday's foundation |
| Thu | 🛠️ User | Build on Tuesday's foundation |
| Fri | Revision | Both streams' content from the week |
| Sat | Project | Phase's primary project (alternates streams across phases) |
| Sun | Paper + LinkedIn + flex | Reading + content writing + project iteration |

Coding tool rotation — covered in dedicated section below — runs through the weekend project work, not as a separate study block.

---

## Phase overview (24 weeks + 2 buffer)

| Weeks | 🏗️ Builder | 🛠️ User | ⌨️ Coding tool focus | Weekend project |
|---|---|---|---|---|
| 1–5 | Backprop → makemore → attention | Prompt eng → context eng → tool use | Claude Code (your current setup) | nano-GPT (builder track) |
| 6 | **Revision week** | | | |
| 7–11 | GPT-2 repro → modern arch (Llama, Mistral, MoE) | RAG fundamentals → advanced retrieval → eval | Cursor onboarding | Production RAG (user track) |
| 12 | **Revision week** | | | |
| 13–17 | Pretraining → instruction tuning → RLHF/DPO | Agentic systems → multi-agent → MCP | GitHub Copilot in your IDE | Agentic system w/ MCP (user track) |
| 18 | **Revision week** | | | |
| 19–23 | PEFT/LoRA → reasoning models → frontier papers | Production patterns → evals → observability | Hybrid stack (which suits you) | EU AI Act compliance agent (user track) + interview prep |
| 24 | **Final revision + heavy applications** | | | |
| 25–26 | Buffer / active interviews | | | |

---

# ⌨️ Daily deep-ml schedule

This section maps each weekday to a **category + topic** to filter problems by on https://www.deep-ml.com/problems. I deliberately do **not** give you specific problem names or IDs — the problem set grows weekly (it's community-maintained at https://github.com/Open-Deep-ML/DML-OpenProblem), and a hardcoded list would rot quickly and could send you to broken links.

## How to use this each morning (3 min)

1. Open https://www.deep-ml.com/problems
2. Filter by **Category** = the one assigned for today (below)
3. Filter by **Difficulty** = the one assigned for today's phase (below)
4. Pick the next problem you haven't solved yet that touches the day's **topic keyword** (e.g., "softmax", "attention", "gradient descent"). If no topic match exists in your current filter, pick any unsolved problem in that category at that difficulty.
5. Time-box to 20 minutes. If you can't crack it, read the solution, *then re-implement from scratch on a blank file*. The re-implementation is where learning happens, not the first attempt.

## Use Collections for structured progression

deep-ml has curated **Collections** at https://www.deep-ml.com/collections — topic-grouped problem sequences (neural networks, linear algebra, optimization, and more). Complete a collection end-to-end where it matches your phase. Earning the badge is a nice forcing function. The day-by-day mapping below tells you which collection or category to focus on.

## Daily category mapping

The pattern follows your Builder (Mon/Wed) and User (Tue/Thu) streams — Builder days reinforce theory you're studying, User days reinforce applied work.

### Phase 1 (Weeks 1–5) — difficulty: **beginner**

| Day | Category | Topic keywords to favor | Why this day |
|---|---|---|---|
| Mon | Linear Algebra | matrix multiplication, dot product, transpose, eigenvalues | Reinforces math under Karpathy's micrograd & MLP work |
| Tue | Machine Learning | linear regression, logistic regression, gradient descent, MSE | Reinforces the ML primitives under prompt eng / embeddings work |
| Wed | Linear Algebra OR Machine Learning | activation functions, sigmoid, ReLU, softmax, cross-entropy | Reinforces forward/backward in MLPs |
| Thu | Machine Learning OR NLP (beginner) | k-NN, k-means, cosine similarity, TF-IDF, tokenization | Reinforces retrieval & embedding intuitions |

**Recommended collections:** *Linear Algebra* collection through Phase 1, plus the *Machine Learning fundamentals* collection if it exists in your view of the site.

### Phase 2 (Weeks 7–11) — difficulty: **beginner → intermediate**

By now beginner problems should feel mechanical. Promote yourself to intermediate when 3 consecutive beginner problems in a category take under 10 minutes each.

| Day | Category | Topic keywords to favor | Why this day |
|---|---|---|---|
| Mon | Deep Learning | self-attention, scaled dot-product, multi-head, positional encoding, layer norm | Direct reinforcement of Karpathy video 7 (attention) & video 9 (GPT-2 repro) |
| Tue | NLP | embeddings, cosine similarity, BM25, retrieval, vector search | Reinforces RAG retrieval pipeline work |
| Wed | Deep Learning | tokenization, BPE, byte-pair encoding, embedding layer | Reinforces Karpathy video 8 (tokenizer) |
| Thu | NLP | re-ranking, query expansion, chunking, evaluation metrics (recall, precision, MRR, NDCG) | Reinforces advanced RAG & eval work |

**Recommended collections:** any *Neural Networks* or *Transformer* collection visible on the Collections page. Aim to complete one full collection during Phase 2.

### Phase 3 (Weeks 13–17) — difficulty: **intermediate**

| Day | Category | Topic keywords to favor | Why this day |
|---|---|---|---|
| Mon | Deep Learning | RLHF, DPO, KL divergence, reward modeling, policy gradient | Reinforces InstructGPT & DPO reading |
| Tue | NLP OR Machine Learning | tool use, sequence-to-sequence, attention, beam search, sampling (top-k, top-p, temperature) | Reinforces LangGraph & agent tool work |
| Wed | Deep Learning | LoRA, low-rank decomposition, SVD, PEFT, fine-tuning math | Reinforces LoRA paper & PEFT setup |
| Thu | NLP | trajectory evaluation, memory, embedding retrieval, semantic search | Reinforces multi-agent memory layer work |

**Recommended collections:** *Optimization* collection if it exists; any collection covering attention mechanisms or RLHF. Complete a second full collection during Phase 3.

### Phase 4 (Weeks 19–23) — difficulty: **advanced + transformer-specific**

| Day | Category | Topic keywords to favor | Why this day |
|---|---|---|---|
| Mon | Deep Learning (advanced) | multimodal, CLIP, contrastive loss, vision-language, FlashAttention, KV cache | Reinforces frontier paper reading |
| Tue | NLP (advanced) | RAG eval (RAGAS metrics), guardrails, hallucination detection, prompt injection | Reinforces production patterns work |
| Wed | Deep Learning (advanced) | implement scaled dot-product attention from scratch, implement multi-head attention, implement KV cache, implement beam search, implement top-p sampling | This is **interview prep day** — these are the implementations that come up most |
| Thu | Mixed (any category, advanced) | pick problems that simulate interview conditions; whatever the next unsolved advanced problem is | Mental endurance training for actual interview loops |

**Recommended collections:** any *Transformer* or *LLM* collection. Re-do problems from Phases 1–3 that took you longest — if they're now fast, you've leveled up. If not, that's where to spend Friday revision time.

## Friday & weekend deep-ml policy

- **Friday revision:** No new deep-ml problem. Instead, re-solve the *hardest* problem from Mon–Thu of that week, from a blank file. This is the real test.
- **Sat/Sun:** No mandatory deep-ml — weekends are project time. If you finish project work early, do one bonus problem in an area you're weak in.

## What to do when you hit a wall

Three failure modes and the fix for each:

- **"I've completed everything in this category at this difficulty."** Promote to the next difficulty. If already at advanced, rotate to an adjacent category (Linear Algebra ↔ Deep Learning, Machine Learning ↔ NLP).
- **"This problem is taking 90 minutes."** Stop at 20 min. Read the solution. Implement from blank. Move on. The warmup is not the main event — protect the main 90-100 min block.
- **"I solved it but don't really understand why my solution works."** Open the problem's *learn* tab (deep-ml provides background reading per problem). Read it before moving to the next problem.

## Optional: track your streak

deep-ml has a heat-points / streak system. Treat the streak as a *secondary* metric, not the goal. The primary metric is: *can I re-implement this without help?* If yes, the streak number is a fun side effect. If no, the streak is theater.

---

# Week-by-week schedule

Notation:
- 🏗️ = Builder block (Mon, Wed)
- 🛠️ = User block (Tue, Thu)
- 📄 = Paper for that weekend
- 💼 = Career task that week (LinkedIn/jobs — see dedicated sections for what these mean)

Resource shortcuts:
- **Karpathy** = https://github.com/karpathy/nn-zero-to-hero (use this README as the source of truth for video links; navigate the playlist on https://www.youtube.com/@AndrejKarpathy)
- **Vizuara** = https://www.youtube.com/@vizuara — go to *Playlists* tab, find *Building LLMs from scratch*
- **CampusX** = https://www.youtube.com/@campusx-official — go to *Playlists* tab; specific playlists referenced by name. Paid courses at https://learnwith.campusx.in/s/store
- **deep-ml** = https://www.deep-ml.com/

---

## Phase 1 (Weeks 1–6) — Foundations of theory + applied basics

> Daily ⌨️ deep-ml warmup this phase: **beginner** Linear Algebra (Mon/Wed) and Machine Learning / NLP (Tue/Thu). See *Daily deep-ml schedule* section for topic keywords.

### Week 1

| Day | Block |
|---|---|
| 🏗️ Mon | Karpathy video 1: *Spelled-out intro to neural networks and backpropagation: building micrograd* — first half, code along |
| 🛠️ Tue | Prompt engineering fundamentals — Anthropic's guide (https://docs.claude.com/en/docs/build-with-claude/prompt-engineering/overview) and OpenAI's guide. Build 5 prompts for the same task across different patterns |
| 🏗️ Wed | Karpathy video 1 — second half. Finish micrograd implementation |
| 🛠️ Thu | Advanced prompting — chain-of-thought, few-shot, role prompting. Try each on a hard reasoning task and tabulate outputs |
| Fri | Revision: 30 min on backprop notes, 30 min re-doing prompt comparisons, 30 min noting what didn't stick |
| Sat | **Project A start** — fork micrograd from blank, extend with at least one new op (softmax + cross-entropy is good) |
| Sun | 📄 *Attention Is All You Need* — https://arxiv.org/abs/1706.03762 + project iteration + 💼 LinkedIn Week 1 task |

💼 **Week 1 LinkedIn task:** Decide: recover dormant account or start fresh? (Decision tree in LinkedIn section.) Then complete the *Profile Build Sequence* — Sections 1–4. Don't post yet.

### Week 2

| Day | Block |
|---|---|
| 🏗️ Mon | Karpathy video 2: *makemore part 1* (bigram model) |
| 🛠️ Tue | Context engineering — what's actually in the context window? Token counting, context pollution, system vs user vs assistant turn dynamics. Read https://www.anthropic.com/news/contextual-retrieval for the mental model. |
| 🏗️ Wed | Karpathy video 3: *makemore part 2* (MLP) — first half |
| 🛠️ Thu | Context window engineering — write the same task with 3 context strategies: minimal, kitchen-sink, structured-XML. Compare outputs. |
| Fri | Revision |
| Sat | **Project A** — finish micrograd extensions, write README, push to GitHub |
| Sun | 📄 *BERT* — https://arxiv.org/abs/1810.04805 + 💼 LinkedIn Profile Build Sequence Sections 5–7 |

💼 **Week 2 LinkedIn task:** Finish profile (Experience, Education, Skills, Featured). Still no posting. First connections (current colleagues, batchmates) — see *First 50 Connections Strategy* in LinkedIn section.

### Week 3

| Day | Block |
|---|---|
| 🏗️ Mon | Karpathy video 3 — second half. Implement MLP from blank afterward |
| 🛠️ Tue | Tool use / function calling fundamentals. Anthropic tool-use guide + OpenAI's. Build a calculator + weather tool with a simple agent loop |
| 🏗️ Wed | Karpathy video 4: *makemore part 3* (activations, gradients, BatchNorm) — first half |
| 🛠️ Thu | Structured outputs — JSON mode, schema-guided generation, Pydantic with instructor library |
| Fri | Revision |
| Sat | **Project A v2** — bigram + MLP name generator from scratch using your micrograd. Compare perplexities. |
| Sun | 📄 *GPT-2 technical report* (https://cdn.openai.com/better-language-models/language_models_are_unsupervised_multitask_learners.pdf) + 💼 First LinkedIn post |

💼 **Week 3 LinkedIn task:** Your first post. Template provided in LinkedIn section. Keep it short, vulnerable, concrete.

### Week 4

| Day | Block |
|---|---|
| 🏗️ Mon | Karpathy video 4 — second half (BatchNorm forward + backward) |
| 🛠️ Tue | Embeddings deep dive — what they encode, how to choose models. Run 4 embedding models (OpenAI, Cohere, BGE, E5) on the same 100-doc corpus. Tabulate retrieval quality. |
| 🏗️ Wed | Karpathy video 5: *makemore part 4* (becoming a backprop ninja) — first half |
| 🛠️ Thu | Vector stores — Chroma vs Qdrant vs pgvector. Build same index in 2. |
| Fri | Revision |
| Sat | **Project A v3** — MLP improvements + write a blog draft "What I learned reproducing makemore from scratch" |
| Sun | 📄 *GPT-3 / Few-Shot Learners* — https://arxiv.org/abs/2005.14165 + 💼 LinkedIn engagement (10 substantive comments) |

💼 **Week 4 LinkedIn task:** Comment substantively on 10 posts in your feed. No posting this week — let Week 3 post breathe.

### Week 5

| Day | Block |
|---|---|
| 🏗️ Mon | Karpathy video 5 — second half. Derive at least 3 gradients yourself before checking |
| 🛠️ Tue | RAG fundamentals — naive retrieval pipeline end-to-end with LangChain. CampusX LangChain playlist videos 1–2 |
| 🏗️ Wed | Karpathy video 6: *makemore part 5* (WaveNet) |
| 🛠️ Thu | Chunking strategies — fixed, recursive, semantic, structure-aware. Test 3 chunkers on the same corpus. |
| Fri | Revision |
| Sat | **Project A v4** — start nano-GPT scaffold (will continue Week 6 onward as Project B) |
| Sun | 📄 *Sentence-BERT* — https://arxiv.org/abs/1908.10084 + 💼 second LinkedIn post |

💼 **Week 5 LinkedIn task:** Second post. Use the *Build Log* template (LinkedIn section). Aim to reach 50 connections by end of week.

### Week 6 — Phase 1 Revision Week

| Day | Block |
|---|---|
| Mon | Re-watch the BatchNorm and manual-backprop segments — these come up in interviews |
| Tue | Re-do Project A end-to-end on a blank file. Time-box 90 min. |
| Wed | Write your full blog post draft — *"What backprop actually computes"* |
| Thu | Publish blog post (Medium/Substack/personal site) and cross-post on LinkedIn |
| Fri | 💼 **Job research kickoff** — read the *Job Search Re-entry Guide* below + start the company tracker spreadsheet |
| Sat | Networking — message 5 EU-based GenAI engineers (template in LinkedIn section). Update CV with Phase 1 work. |
| Sun | Rest or extend Project A |

---

## Phase 2 (Weeks 7–12) — GPT-2, modern architectures, RAG mastery

> Daily ⌨️ deep-ml warmup this phase: **beginner → intermediate** Deep Learning (Mon/Wed, attention & tokenizer topics) and NLP (Tue/Thu, retrieval & re-ranking topics). See *Daily deep-ml schedule* section.

⌨️ **Coding tool focus this phase:** Onboard onto **Cursor** (https://cursor.com). Use it for at least one weekend project. Document what works, what doesn't.

### Week 7

| Day | Block |
|---|---|
| 🏗️ Mon | Karpathy video 7: *Let's build GPT from scratch* — first third (single-head attention) |
| 🛠️ Tue | RAG with reranking. Cohere rerank + BGE-reranker. CampusX LangChain — embeddings + reranking videos |
| 🏗️ Wed | Karpathy video 7 — second third (multi-head, residuals, layernorm) |
| 🛠️ Thu | Hybrid retrieval (BM25 + dense) — implement and measure on 50-query eval set |
| Fri | Revision |
| Sat | **Project B start** — nano-GPT trained on a custom corpus you care about. Use Cursor as your IDE for the entire build. |
| Sun | 📄 *RAG (original)* — https://arxiv.org/abs/2005.11401 + 💼 LinkedIn post |

💼 **Week 7 LinkedIn task:** Post about your blog. Format: "Spent 6 weeks reproducing X. Here are 3 things I didn't expect." Aim 75 connections.

### Week 8

| Day | Block |
|---|---|
| 🏗️ Mon | Karpathy video 7 — final third (training loop, scaling intuition) |
| 🛠️ Tue | Query transformations — HyDE, multi-query, step-back prompting. Implement HyDE on Project B |
| 🏗️ Wed | Karpathy video 8: *Let's build the GPT Tokenizer* — first half |
| 🛠️ Thu | RAG evaluation — RAGAS framework (https://docs.ragas.io). Build 50-question golden set for a small corpus |
| Fri | Revision |
| Sat | **Project B** — train nano-GPT to convergence, sample text, write README with loss curves |
| Sun | 📄 *Dense Passage Retrieval* — https://arxiv.org/abs/2004.04906 + 💼 LinkedIn engagement |

💼 **Week 8 LinkedIn task:** Comment on 10 posts. Follow 30 EU GenAI practitioners (list in LinkedIn section).

### Week 9

| Day | Block |
|---|---|
| 🏗️ Mon | Karpathy video 8 — second half (BPE deeply) |
| 🛠️ Tue | Self-RAG and Corrective RAG. Read papers, implement one |
| 🏗️ Wed | Karpathy video 9: *Let's reproduce GPT-2 (124M)* — first quarter |
| 🛠️ Thu | Continue advanced RAG implementation. RAGAS scoring. |
| Fri | Revision |
| Sat | **Project C start** — production RAG system over a corpus of your choosing. Hybrid retrieval + reranking + RAGAS evals built in from the start. Use Cursor. |
| Sun | 📄 *HyDE* — https://arxiv.org/abs/2212.10496 + 💼 LinkedIn post |

💼 **Week 9 LinkedIn task:** Build Log post about Project B (nano-GPT). Include a sample generation. Aim 100 connections.

### Week 10

| Day | Block |
|---|---|
| 🏗️ Mon | Karpathy video 9 — second quarter (mostly watch, this is a 4-hr video) |
| 🛠️ Tue | Modern architectures — read Llama 3 paper or Mistral architecture writeups. Compare to vanilla GPT-2. |
| 🏗️ Wed | Karpathy video 9 — third quarter |
| 🛠️ Thu | Graph RAG — Microsoft's GraphRAG approach, https://github.com/microsoft/graphrag |
| Fri | Revision |
| Sat | **Project C** — add RAGAS golden set, run baseline numbers |
| Sun | 📄 *Llama 3 paper* — https://arxiv.org/abs/2407.21783 + 💼 LinkedIn engagement |

💼 **Week 10 LinkedIn task:** Comment on 15 posts. Send first soft outreach DMs (3–5; template in LinkedIn section).

### Week 11

| Day | Block |
|---|---|
| 🏗️ Mon | Karpathy video 9 — final quarter |
| 🛠️ Tue | RAG observability — LangSmith setup, tracing, dataset creation |
| 🏗️ Wed | Mixture of Experts — read the Switch Transformers paper, understand routing |
| 🛠️ Thu | Multimodal RAG (images + text) using CLIP-based retrieval |
| Fri | Revision |
| Sat | **Project C** — final polish, all RAGAS metrics in README, demo video. This becomes Flagship Repo #1 |
| Sun | 📄 *Self-RAG* — https://arxiv.org/abs/2310.11511 + 💼 LinkedIn post |

💼 **Week 11 LinkedIn task:** Build Log post about Project C with the RAGAS numbers. This is your strongest content yet.

### Week 12 — Phase 2 Revision Week

| Day | Block |
|---|---|
| Mon | Re-watch GPT-2 reproduction, attention block, tokenizer |
| Tue | Re-do nano-GPT from scratch in 2 hours. If you can't, that's the gap to close. |
| Wed | Write *"How I evaluate a RAG system"* blog post |
| Thu | Publish + cross-post |
| Fri | 💼 **Job research deepening** — start filling the company tracker (instructions in Job Search section). Identify your top 20 EU targets. |
| Sat | Networking — 10 outreach DMs. Audit the 5 papers you've read so far — if any paper notes are weak, redo them. |
| Sun | Rest |

---

## Phase 3 (Weeks 13–18) — Alignment, agentic systems, MCP

> Daily ⌨️ deep-ml warmup this phase: **intermediate** Deep Learning (Mon/Wed, RLHF/DPO/LoRA topics) and NLP / ML (Tue/Thu, sampling/tool-use/memory topics). See *Daily deep-ml schedule* section.

⌨️ **Coding tool focus:** Add **GitHub Copilot** to your IDE (https://github.com/features/copilot). Run it alongside Cursor for one project to compare. Many EU enterprises standardize on Copilot, so familiarity matters.

### Week 13

| Day | Block |
|---|---|
| 🏗️ Mon | Pretraining → instruction tuning. Read InstructGPT paper intro and methodology |
| 🛠️ Tue | LangGraph fundamentals. CampusX LangGraph playlist videos 1–2 |
| 🏗️ Wed | RLHF deep dive — read the InstructGPT paper fully + watch any Karpathy/HuggingFace explainer |
| 🛠️ Thu | LangGraph state, nodes, edges. Build a 3-node graph from blank: planner → executor → reflector |
| Fri | Revision |
| Sat | **Project D start** — agentic system. Pick a real problem you'd use: research assistant, code review bot, expense categorizer. |
| Sun | 📄 *InstructGPT / RLHF* — https://arxiv.org/abs/2203.02155 + 💼 LinkedIn post |

💼 **Week 13 LinkedIn task:** Post a takeaway from Phase 2. Format: *"Three things I changed about my RAG eval after reading RAGAS"*. Aim 150 connections.

### Week 14

| Day | Block |
|---|---|
| 🏗️ Mon | DPO vs RLHF intuition — read DPO paper, compare to PPO-based RLHF |
| 🛠️ Tue | Tool calling in LangGraph. CampusX LangGraph tool videos. Build 5 real tools. |
| 🏗️ Wed | Constitutional AI — read paper. Understand the alignment philosophy |
| 🛠️ Thu | Memory in agents — short-term (within thread) vs long-term (across threads). Implement both. |
| Fri | Revision |
| Sat | **Project D** — add tools and memory layer |
| Sun | 📄 *DPO* — https://arxiv.org/abs/2305.18290 + 💼 LinkedIn engagement |

💼 **Week 14 LinkedIn task:** Comment on 15 posts. First *informational* recruiter DM if you've spotted any (template in Job Search section).

### Week 15

| Day | Block |
|---|---|
| 🏗️ Mon | LoRA paper — https://arxiv.org/abs/2106.09685. Understand low-rank intuition |
| 🛠️ Tue | Multi-agent patterns — supervisor, swarm, hierarchical. Pick one for Project D |
| 🏗️ Wed | QLoRA + Unsloth (https://github.com/unslothai/unsloth) — set up environment |
| 🛠️ Thu | Human-in-the-loop interrupts in LangGraph. Persistence with checkpointers. |
| Fri | Revision |
| Sat | **Project D** — convert to multi-agent if it makes sense |
| Sun | 📄 *Constitutional AI* — https://arxiv.org/abs/2212.08073 + 💼 LinkedIn post |

💼 **Week 15 LinkedIn task:** Build Log post about agentic Project D. Mention you're working with LangGraph.

### Week 16

| Day | Block |
|---|---|
| 🏗️ Mon | Run a LoRA fine-tune on a small model with HuggingFace PEFT or Unsloth |
| 🛠️ Tue | **MCP (Model Context Protocol) intro** — https://modelcontextprotocol.io. Read the spec. |
| 🏗️ Wed | Continue fine-tune. Save adapter, evaluate before/after |
| 🛠️ Thu | Build your first MCP server. Connect to Claude Desktop. Expose 2–3 tools from your filesystem or APIs |
| Fri | Revision |
| Sat | **Project D** — convert tools to be MCP-served if possible. This is interview-grade differentiation. |
| Sun | 📄 *Reflexion* — https://arxiv.org/abs/2303.11366 + 💼 LinkedIn post |

💼 **Week 16 LinkedIn task:** Post about MCP. *"I built my first MCP server this weekend. Here's what I learned about why this protocol matters."* This is hot, recent, and demonstrates currency.

### Week 17

| Day | Block |
|---|---|
| 🏗️ Mon | Reasoning models — read about o-series approach, DeepSeek R1 paper |
| 🛠️ Tue | Agent observability — LangSmith setup for Project D, trajectory evals, cost tracking |
| 🏗️ Wed | Test-time compute scaling — read https://arxiv.org/abs/2408.03314 (Scaling LLM Test-Time Compute) |
| 🛠️ Thu | Guardrails — input/output validation, prompt injection defenses, OWASP LLM Top 10 |
| Fri | Revision |
| Sat | **Project D** — final polish with observability, evals, guardrails. This becomes Flagship Repo #2. |
| Sun | 📄 *DeepSeek R1* (https://arxiv.org/abs/2501.12948) or *Scaling Test-Time Compute* + 💼 LinkedIn post |

💼 **Week 17 LinkedIn task:** Build Log post about Project D's final form. Include observability screenshot.

### Week 18 — Phase 3 Revision Week

| Day | Block |
|---|---|
| Mon | Re-watch hardest LangGraph segments. Re-read MCP spec. |
| Tue | Mock interview alone: "Design an agentic system for X." Whiteboard. Record yourself. |
| Wed | Write comparison piece: *Devin vs Claude Code vs Cursor vs custom agents — what production agent design patterns actually look like.* You're already studying Devin per your notes; this is gold for senior-architect positioning. |
| Thu | Publish piece + 💼 update CV with all Phase 3 work |
| Fri | 💼 **First real applications.** 3 dream EU companies. Tailored. (Application logistics in Job Search section.) |
| Sat | Networking — 15 outreach DMs |
| Sun | Rest |

---

## Phase 4 (Weeks 19–24) — Frontier topics, applications, interview prep

> Daily ⌨️ deep-ml warmup this phase: **advanced** Deep Learning (Mon/Wed, multimodal & transformer-from-scratch implementations) and NLP / mixed advanced (Tue/Thu, RAG eval & interview-condition problems). Wednesdays this phase are interview-prep day — implement attention/KV cache/sampling from scratch. See *Daily deep-ml schedule* section.

⌨️ **Coding tool focus:** Settle into the hybrid stack you'll use for application work. Most senior engineers end up with Cursor or Claude Code as primary + Copilot for company-mandated environments. Have an opinion ready for interviews — you'll be asked.

### Week 19

| Day | Block |
|---|---|
| 🏗️ Mon | Multimodal models — read https://arxiv.org/abs/2103.00020 (CLIP) and a recent VLM paper (e.g., Llava or Qwen-VL) |
| 🛠️ Tue | Production patterns — caching, prompt compression, model routing (LiteLLM, OpenRouter) |
| 🏗️ Wed | FlashAttention — https://arxiv.org/abs/2205.14135. Understand why it matters |
| 🛠️ Thu | Cost optimization patterns. Build a cost dashboard for any of your projects. |
| Fri | Revision |
| Sat | **Project E start** — EU AI Act compliance agent. Takes an ML system description and outputs risk classification + required documentation checklist. |
| Sun | 📄 *FlashAttention* + 💼 LinkedIn post |

💼 **Week 19 LinkedIn task:** Post about EU AI Act. *"Started building a tool that classifies ML systems by AI Act risk tier. Three things every ML engineer should know about Article 6."* This single post gets EU recruiter attention.

### Week 20

| Day | Block |
|---|---|
| 🏗️ Mon | EU AI Act technical reading — official summary at https://artificialintelligenceact.eu/. Focus: risk categories, GPAI obligations, technical documentation. |
| 🛠️ Tue | System design practice 1: "Design a customer support agent for a fintech with 10M users" |
| 🏗️ Wed | EU AI Act practical — what does a compliant RAG/agent system look like? |
| 🛠️ Thu | System design 2: "Design an LLM-powered code review system for 5000 engineers" |
| Fri | Revision |
| Sat | **Project E** — implement core AI Act risk classifier |
| Sun | 📄 *Tree of Thoughts* — https://arxiv.org/abs/2305.10601 + 💼 LinkedIn engagement |

💼 **Week 20 LinkedIn task:** Apply to 5 EU companies (Job Search section has the playbook). Comment on 15 posts.

### Week 21

| Day | Block |
|---|---|
| 🏗️ Mon | Implement multi-head attention from scratch in PyTorch. Time yourself. |
| 🛠️ Tue | System design 3: "Design a multi-tenant RAG SaaS with strong tenant isolation" |
| 🏗️ Wed | Implement KV cache + beam search + temperature sampling. These come up. |
| 🛠️ Thu | Coding interview prep — deep-ml.com hard problems on transformers |
| Fri | Revision: speed-run all of the above in 90 minutes |
| Sat | **Project E** — final polish. This becomes Flagship Repo #3. |
| Sun | 📄 *Chain of Thought* — https://arxiv.org/abs/2201.11903 + 💼 Apply to 5 more companies |

💼 **Week 21 LinkedIn task:** Build Log on Project E (AI Act compliance agent). Tag the topic prominently — `#EUAIAct`.

### Week 22

| Day | Block |
|---|---|
| 🏗️ Mon | Frontier reading: pick 2 recent papers from https://huggingface.co/papers (last 30 days) and read them |
| 🛠️ Tue | Behavioral prep — write 8 STAR-format stories from your Amex work (template in Job Search section) |
| 🏗️ Wed | Frontier reading continued: 2 more papers |
| 🛠️ Thu | Mock behavioral interviews — record yourself answering 5 behavioral Qs |
| Fri | Revision |
| Sat | 💼 Heavy applications — 10 tailored applications |
| Sun | 📄 *Mixture of Experts / Switch Transformers* — https://arxiv.org/abs/2101.03961 + 💼 LinkedIn post |

💼 **Week 22 LinkedIn task:** Post about something specific in your portfolio. *"I built X because I wanted to understand Y. Here's what I learned."*

### Week 23

| Day | Block |
|---|---|
| Mon | Mock interview 1 (technical, friend or Pramp/Interviewing.io) |
| Tue | Mock interview 2 (system design) |
| Wed | Mock interview 3 (behavioral + culture fit) |
| Thu | Debrief — every weak answer gets a better-version written down |
| Fri | 💼 Salary research — Levels.fyi, Glassdoor for EU specifically. (Compensation guidance in Job Search section.) |
| Sat | 💼 Application sprint — 10 more applications |
| Sun | Rest |

### Week 24 — Final revision week

| Day | Block |
|---|---|
| Mon | Re-read all your phase notes |
| Tue | 💼 Polish all 3 flagship repos. Final READMEs. Demo videos. |
| Wed | 💼 LinkedIn final audit — featured section, recommendations, banner, headline |
| Thu | 💼 CV final audit — quantified impact, links to projects, EU-friendly format |
| Fri | 💼 Direct ask outreach to anyone in your network at target companies |
| Sat | 💼 Application sprint — 15 applications |
| Sun | Reflect. Plan next 4 weeks of active interviewing. |

---

# Coding tools rotation guide

You're going to be asked in interviews: *"Tell me about how you use AI coding tools."* The wrong answer is "I use ChatGPT sometimes." The right answer demonstrates intentional evaluation across the major tools.

### Phase 1 — Claude Code (your existing setup)

You already have this configured (Ubuntu 25.04, `uv`-managed environments per your notes). For Phase 1, build everything in Claude Code. Specifically practice:
- Long planning sessions before coding (let Claude propose architecture, debate with it)
- The `uv run python` idiom you've already established for the bash-shell issue
- Using Claude Code in agentic mode for non-trivial refactors
- Writing custom slash commands for repeated tasks

### Phase 2 — Cursor onboarding

Install Cursor (https://cursor.com). It's a fork of VS Code with AI built in. Key things to learn:
- Tab completion (it's much more aggressive than Copilot's, takes getting used to)
- Cmd+K inline edits
- Cmd+L chat panel
- The Composer / Agent mode for multi-file changes
- `.cursorrules` file for project-specific instructions

Build at least one weekend project entirely in Cursor (Project C is a good candidate).

### Phase 3 — GitHub Copilot in IDE

Most EU enterprises (banks, telcos, insurers) have standardized on Copilot because of Microsoft's enterprise contracts. You'll be expected to be fluent. Install in VS Code or your preferred IDE.
- Inline ghost-text completion
- `/explain`, `/fix`, `/tests` chat commands
- Workspace-aware chat (Copilot Workspace if available)
- Repository indexing

Run Copilot in parallel with Cursor for one project — same task, two tools — and write up the difference.

### Phase 4 — Hybrid stack + interview narrative

By Week 19 you should have a clear opinion. The narrative for interviews:

> *"For deep agentic work where I'm pairing with the AI for hours on a complex problem, I prefer Claude Code — the long-context planning and the file-system access make it a real engineering partner. For routine in-IDE work I use Cursor; the tab completion is the best I've used. I've also used Copilot extensively because most enterprise Java/Python codebases I've worked in have it standardized — the workspace indexing makes it strong for exploring unfamiliar code. Devin I've evaluated as a case study in autonomous engineering — it's strong for migration and well-scoped tickets, weaker for ambiguous design work. Honestly, the meta-skill isn't picking the tool — it's knowing what to delegate and what to do yourself."*

Have something true and specific to say in each sentence. That's the bar.

### Daily ⌨️ algorithmic practice

deep-ml.com problem each weekday before the main block. Progression:

- Phase 1: Linear Algebra + ML easy/medium (foundational)
- Phase 2: ML medium + Deep Learning easy
- Phase 3: Deep Learning medium
- Phase 4: Deep Learning hard + transformer-specific implementations

Track your streak. The combination of "I've done 100 ML implementation problems" + "I've reproduced GPT-2" is a much stronger signal than either alone.

---

# LinkedIn rebuilding guide (15-year dormant account)

This is the section you said you needed most hand-holding on. I'm going to be very specific. Do these in order.

## Step 0 — Recover or restart?

Decision tree:
1. **Try password recovery** at https://www.linkedin.com/uas/request-password-reset using any email address you might have used 15 years ago. If that works → log in and keep the account.
2. **If you can log in but the profile is empty/stale** — keep it. LinkedIn mildly favors older accounts. Wipe everything outdated and rebuild.
3. **If you can't recover it** — start fresh. Don't waste a week on this. Account age is a marginal factor; profile quality is the real signal.
4. **If you find the account but it has wrong info you can't change** — start fresh and ignore the old one.

Pick one path, spend at most 30 minutes on this decision, and move on.

## Step 1 — Settings to flip first (before the world sees you)

Set your profile to **private/hidden** while you build. Settings → Visibility → *Profile viewing options* → switch to private mode temporarily. Also Settings → Visibility → *Profile photo visibility* → *Your network* (you'll change to *Public* later).

This means recruiters won't index a half-built profile. Don't skip — a half-built profile that gets indexed early sets a weak first impression.

## Step 2 — Profile build sequence

Do these sections in this order. Don't skip ahead.

### 2.1 — Profile photo (Week 1)

The single most important visual. Spec:
- **400×400 minimum**, square
- **Head and shoulders**, not full body
- **Face takes ~60% of the frame**
- **Neutral or blurred background** (not a beach, not a wedding)
- **Good lighting** (window light, no harsh shadows)
- **Closed-mouth smile or neutral pleasant expression** — not a wide grin, not stone-faced
- **Solid color shirt** if possible, dark blue or charcoal works well
- **Recent** — within 2 years of how you actually look

A well-lit iPhone selfie taken by a friend in front of a plain wall, processed lightly in any photo app, beats a 5-year-old photo from a wedding. If you have access to ChatGPT/Gemini for background blur, use it; or pay $20 for a half-hour with a local photographer.

### 2.2 — Banner image (Week 1)

1584×396 px. Options ranked from best to worst:
- **Best:** A clean architecture diagram you actually drew (RAG pipeline, agent topology). Subtle, technical, says "I think in systems."
- **Good:** A solid color or subtle gradient with your name + tagline on the right side ("Building RAG and Agentic AI Systems")
- **OK:** Solid dark color with no text
- **Avoid:** Generic stock images (city skylines, mountains, bridges), motivational quotes, your company's logo, AI-generated abstract art

Tools: Canva (free, has LinkedIn banner templates), or just a 1584×396 PNG in any image editor.

### 2.3 — Name + Headline (Week 1)

- **Name:** Your real name, no credentials, no emojis
- **Headline (220 chars):** Most important field. Format:

  `[Current Role] | [Specific tech] | [What you're building / writing about]`

  Examples for you:
  - `GenAI Architect at American Express | RAG · Agentic Systems · LangGraph · MCP | Writing about LLM internals`
  - `GenAI Architect at American Express | Building production RAG and Agentic AI | Reproducing GPT-2 from scratch`

  Pick one and live with it. Recruiters search keywords, so include the specific tech terms a recruiter would type.

### 2.4 — About section (Week 1)

3–4 short paragraphs. Template:

> **Para 1 — what you do today (specific):**
> "I'm a GenAI Architect at American Express, where I design and ship retrieval-augmented and agentic systems used by [scale-of-impact, vague enough to be safe]. My day-to-day is split between architecture for new GenAI products and coaching engineering teams on production patterns for LLM applications."
>
> **Para 2 — your technical depth:**
> "I'm currently going deep on transformer internals (reproducing GPT-2 from scratch via Karpathy's nn-zero-to-hero), advanced RAG patterns, and the LangGraph/MCP stack for agentic systems. I read 1–2 GenAI papers a week and document what I learn here."
>
> **Para 3 — what you're exploring:**
> "Recent rabbit holes: the practical implications of the EU AI Act for production ML systems, multi-agent design patterns, and the design philosophy behind autonomous engineering tools like Devin and Claude Code."
>
> **Para 4 — soft signal of openness (only if your manager is aware, otherwise skip):**
> "Open to conversations about senior GenAI architect / engineer roles in Europe."

If your manager doesn't know you're looking, skip Para 4. Recruiters will still find you via the keywords in Para 1–3.

### 2.5 — Experience (Week 2)

Current role first. Format for each position:
- **Title** (your actual title)
- **Company**
- **Dates**
- **Location** (city, country)
- **3–5 bullet points** of what you built, with metrics where possible

Bullet template: *Verb + What + Quantified impact*. Example:
- "Designed and shipped a RAG-based [system type] reducing [metric] by [%] for [user count] users"
- "Led architecture review for [N] GenAI initiatives across [business unit]"
- "Mentored [N] engineers on production LLM patterns including evaluation, observability, and cost optimization"

Don't write essays in your experience section. Bullets, scannable, specific.

For older roles (5+ years ago), 2 short bullets each is enough. Recent role gets the volume.

### 2.6 — Education (Week 2)

Just the facts. Degree, institution, years. Don't pad with coursework or activities unless very recent.

### 2.7 — Skills (Week 2)

10–15 specific technical skills. Order matters — top 3 are pinned. For you:

Top 3 (pin these): **Generative AI · Retrieval-Augmented Generation (RAG) · Large Language Models (LLM)**

Next tier: LangChain, LangGraph, Python, Agentic AI, Prompt Engineering, Vector Databases, Fine-Tuning, PyTorch, MLOps, System Design, AWS

Avoid: "Leadership", "Teamwork", "Communication" — these are noise. Keep technical.

### 2.8 — Featured (Week 6 onward)

This is the section that pins 1–3 things to the top of your profile. As you ship, add:
- Your blog post on backprop (Week 6)
- Your top GitHub repo (Week 11)
- Your blog post on RAG eval (Week 12)
- Replace older items with newer/better ones over time

Always have something here by Week 6.

### 2.9 — Recommendations (Week 12 onward)

Ask 2–3 people you've worked with at Amex for short recommendations. Make it easy for them: send a draft they can edit. Template:

> *"Hi [Name], I'm doing some career housekeeping and wondered if you'd be open to writing a short LinkedIn recommendation. To save you time, here's a draft you can edit or rewrite — totally fine to change all of it. No rush. Thanks!"*
>
> Draft: "[Your name] and I worked together on [project/team] for [time]. [One specific technical strength]. [One specific human strength]. [Outcome you delivered together]."

Two solid recommendations beat ten generic ones.

## Step 3 — Make profile public (end of Week 2)

Once Steps 1–2 are done:
- Settings → Visibility → Profile viewing → switch back to public
- Settings → Visibility → Profile photo → Public
- Settings → Communications → review notification preferences (turn off most marketing)

## Step 4 — First 50 connections (Weeks 1–4)

Order matters. Send connection requests in this order:

1. **Current Amex colleagues** (50% of your first batch). Easy yes. Builds your "social proof" mutual connection count.
2. **Past colleagues from previous companies**.
3. **University batchmates** — search your alma mater, find classmates.
4. **People you've met at conferences/meetups** — even if it was years ago, "hi, we met at [event]" is fine.
5. **Friends who happen to be in tech**.

For *all* connection requests, **always include a personalized note**. Default LinkedIn message is "I'd like to add you to my professional network." Don't use it. Template:

> "Hi [name], reconnecting after a while. Looking forward to seeing what you're building these days."

Or for a closer colleague:

> "Hi [name], been meaning to reconnect. Hope you're doing well at [their company]."

Aim for 50 connections by end of Week 2, 200 by end of Week 4. After ~200, LinkedIn's algorithm starts working *for* you.

**Don't connect with strangers, recruiters you haven't spoken to, or people far outside your domain.** This dilutes your network signal.

## Step 5 — Follow (don't connect with) influencers and target companies

Connecting is mutual. Following is one-way and doesn't require approval. Follow:

**People (no DMs needed):**
- Andrej Karpathy
- Yann LeCun
- Andrew Ng
- Sebastian Raschka
- Lilian Weng
- Jerry Liu (LlamaIndex)
- Harrison Chase (LangChain)
- Logan Kilpatrick
- Dario Amodei (Anthropic)
- Leaders at your EU target companies (search company → People → senior titles)

**Companies (follow, see their job posts):**
Mistral, Hugging Face, Aleph Alpha, DeepL, ElevenLabs, Stability AI, Synthesia, Black Forest Labs, Anthropic, OpenAI, Google DeepMind, Microsoft AI, Cohere, Spotify, Booking.com, Adyen, Klarna, Revolut, Bolt, Trade Republic, Personio, Celonis.

## Step 6 — First post (Week 3)

Most people freeze here. Don't overthink. Template for your first post:

> *Starting a 6-month deep dive into LLM internals.*
>
> *I've spent the last few years building RAG and agentic systems at work, but I've felt the foundation under that work could be stronger. So I'm going through Karpathy's nn-zero-to-hero series end-to-end, reproducing GPT-2 from scratch.*
>
> *Plan is to document the journey here — what's clicking, what isn't, and the projects I ship along the way.*
>
> *Anyone else working through it? Curious which segment surprised you most.*

That's it. ~80 words. Vulnerable (admits a gap), specific (Karpathy, GPT-2), invites engagement (question at the end). No emojis, no hashtag spam, no "🚀🚀🚀".

Post on a Tuesday or Wednesday morning EU time (so it's also late afternoon US, maximizing reach).

## Step 7 — Posting cadence (Week 5+)

**Two posts per week.** One on Tuesday, one on Friday. Use one of these formats:

### Format A: Build Log

> *Just finished [project]. Here's what I learned.*
>
> *[Bullet 1 — specific technical insight]*
> *[Bullet 2 — surprise or counterintuitive finding]*
> *[Bullet 3 — what you'd do differently]*
>
> *Repo: [github link]*
>
> *[Question to invite comments]*

### Format B: Paper takeaway

> *Read [paper] this weekend. [One sentence why it matters.]*
>
> *Three things that stuck:*
> *1. [Insight]*
> *2. [Insight]*
> *3. [Insight]*
>
> *[A practical implication for working engineers]*
>
> *[Question]*

### Format C: Observation / take

> *[A specific observation from your work or reading. ~3 sentences.]*
>
> *[Why it matters / a counterintuitive consequence. ~3 sentences.]*
>
> *[What you'd watch for. ~2 sentences.]*
>
> *[Question.]*

Avoid:
- "Excited to share I completed a course!"
- "AGI is coming faster than you think 🚀"
- Generic motivation
- Reposting other people's threads

Hashtags: 2–3 max, in a single line at the bottom. Use `#GenerativeAI #LLM #RAG` — what EU GenAI people actually search.

## Step 8 — Engagement (every weekday, 10 min)

This is where the algorithm rewards you and where real conversations happen.

Spend 10 minutes daily commenting on 5 posts in your feed. Comment substantively:

**Bad:** "Great post! 🔥"
**Better:** "The point about chunking strategy resonates — we saw similar with hybrid retrieval where semantic chunking actually hurt recall on technical documentation."
**Best:** [Same as Better, plus a follow-up question that invites the original poster to share more]

Bias toward commenting on EU GenAI practitioners' posts — recruiters from those circles see the comments.

## Step 9 — DM templates (Month 3+)

**Never DM cold to ask for a job.** Ever. It's the fastest way to get muted.

**Soft outreach DM (after seeing their post or work):**

> *Hi [name], I came across your [post / work] on [specific topic] — your point about [specific thing] resonated. I'm working on similar problems at Amex and would love to hear how your team approached [specific question]. No agenda, genuinely curious.*

**Informational chat DM (after a few interactions):**

> *Hi [name], thanks for [recent comment / post]. I'm exploring senior GenAI roles in Europe over the next few months and would love a 20-minute chat to hear about [their company / their team]. Happy to work around your schedule. Either way, appreciate the work you share here.*

**After they say yes:** prepare 5 specific questions about their stack, team structure, and current challenges. Don't pitch yourself. Listen. The pitch happens organically when they ask "so what are you working on?" — and they will.

**After the call:** send a thank-you note within 24 hours, with one specific takeaway from the conversation. This is what gets you remembered.

## Step 10 — "Open to Work" badge — when?

LinkedIn lets you turn on a green "Open to Work" frame on your photo. Two settings:
- **Visible to all** — green frame, recruiters know
- **Visible only to recruiters** — quiet, no green frame

Decision:
- If your Amex manager knows → turn on **visible to all** at Week 18
- If they don't → turn on **visible only to recruiters** at Week 12, **visible to all** only after you've signed a new offer

## Step 11 — Things to never do

- Send the default "I'd like to add you to my professional network" connection message
- Post anything controversial in your first 6 months (politics, AGI doom, hot takes on competing companies)
- Engage with engagement-bait posts ("Like if you agree")
- Pay for LinkedIn Premium until Month 4 — it's worth it once you're actively interviewing for InMail credits
- Ghost recruiters who reach out, even for irrelevant roles — a polite "thanks, this isn't quite the fit, but I'd be interested in [X]" keeps the door open
- Lie about anything (titles, dates, scope). LinkedIn lying is reputation suicide in tech circles

## LinkedIn weekly cadence checklist

Pin this to your fridge:

- [ ] Mon: 10 min engagement (5 substantive comments)
- [ ] Tue: First post of the week
- [ ] Wed: 10 min engagement
- [ ] Thu: 10 min engagement
- [ ] Fri: Second post of the week
- [ ] Sat: 30 min — review who viewed your profile, accept good connection requests, send 2–3 new connection requests with personalized notes
- [ ] Sun: 30 min — write next week's posts in draft

Total time: ~2 hours per week. Treat it as a non-optional career investment.

---

# Job search re-entry guide (20-year gap)

The job market has changed dramatically since you last searched. Here's the modern playbook.

## Step 1 — Mental model: how senior tech hiring works in 2026

Three sources of senior role discovery, in order of yield:
1. **Inbound from recruiters** (best, but requires a strong LinkedIn — that's why Step 1 of LinkedIn rebuilding matters so much)
2. **Referrals** from your network (second-best yield, hardest to engineer)
3. **Cold applications** through job boards (lowest yield per application but highest volume — needed for breadth)

For your 6-month timeline, plan for *all three*, weighted approximately:
- 30% effort: making yourself inbound-discoverable (LinkedIn, blog posts, GitHub)
- 30% effort: networking that produces referrals (DMs, coffee chats, conference attendance)
- 40% effort: tailored cold applications

The mistake most people make is going 100% cold applications and burning out. Your network and LinkedIn presence do the slow compounding work.

## Step 2 — Where to actually look

### Primary boards

- **LinkedIn Jobs** (https://www.linkedin.com/jobs) — table stakes; 60% of EU senior tech roles flow through here. Set up keyword alerts for "GenAI Architect", "LLM Engineer", "AI Engineer", "Machine Learning Engineer GenAI", filter by Europe.
- **Welcome to the Jungle** (https://www.welcometothejungle.com/) — strong for France, Germany, Netherlands, Spain. Better UX than LinkedIn.
- **Otta** (now part of Welcome to the Jungle) — modern UX, good for tech-first companies
- **Wellfound** (https://wellfound.com/) — formerly AngelList, startup-heavy, smaller European presence but worth checking
- **HackerNews "Who's Hiring"** monthly thread — search for "EU" or specific cities. AI startups disproportionately represented.
- **YC Job Board** (https://www.workatastartup.com/) — filter by location

### GenAI-specific boards

- **AI Jobs** (https://aijobs.net/) — focused on AI/ML roles
- **Mercor** (https://mercor.com/) — AI talent marketplace, can get matched
- **Cohere/Mistral/Hugging Face career pages directly** — top targets, apply on company site

### Country-specific (when you've narrowed down)

- **Germany:** StepStone, Xing (LinkedIn equivalent — *do* set up an Xing profile if targeting Germany)
- **Netherlands:** Techleap.nl jobs
- **UK:** Otta, Hired.com
- **Ireland:** Irishjobs.ie, IDA Ireland talent portal

## Step 3 — Build the application tracker (Week 6)

A single spreadsheet that runs your entire search. Columns:

| Company | Role | Location | Source | Date applied | Stage | Recruiter contact | Salary band | Notes | Next action |

Tabs:
- **Active applications**
- **Companies to research** (target list)
- **Networking pipeline** (people you've DMed, with status)
- **Interview prep** (per company: what their stack is, who you talked to, what to mention)

A simple Google Sheet works. Don't overengineer.

By Week 12, fill the *Companies to research* tab with 30–50 EU companies. By Week 18, that list should be triaged into:
- **Tier 1 — Dream** (5–10 companies) — heavy tailoring, network entry
- **Tier 2 — Strong fit** (15–20 companies) — solid tailoring
- **Tier 3 — Volume** (15–20 companies) — lighter tailoring, recent JD match

## Step 4 — CV / Resume in 2026

CV (EU term) = Resume (US term). Both used.

**Format requirements (very different from 20 years ago):**

- **One page** if possible (two only if you have 15+ years and the second page genuinely matters)
- **Single column** — ATS systems mangle multi-column layouts
- **No tables** — same reason
- **No photo** in the EU (despite older German/French tradition; modern EU companies don't expect it; UK/Netherlands explicitly avoid)
- **No date of birth, marital status, nationality** unless visa-relevant
- **Plain fonts** — Inter, Calibri, Helvetica. No Comic Sans (yes, this needs saying)
- **PDF format**, named `FirstName_LastName_CV.pdf`

**Sections in order:**
1. **Header:** Name (size 18–22), location (city, country), email, phone (with country code), LinkedIn URL, GitHub URL
2. **Summary** (2–3 lines): "GenAI Architect with X years of experience designing and shipping production RAG and agentic systems. Specialist in [specific tech]. Currently building [thing]."
3. **Experience** (most space): Reverse chronological. For each: Title · Company · Location · Dates. 3–5 bullets. Each bullet: *verb + what + impact*.
4. **Projects** (1–3 lines per project): Your flagship GitHub repos. *"nano-GPT reproduction (PyTorch) — Karpathy-style GPT-2 implementation trained on custom corpus. Repo: [link]."*
5. **Skills** (one line, comma-separated): the 10–15 from your LinkedIn skills
6. **Education** (1–2 lines)
7. **(Optional) Publications/Talks/Open source**

**The "achievement bullet" formula:**

`[Action verb] + [Specific thing] + [Quantified impact OR scale OR scope]`

Examples for you:
- "Architected production RAG pipeline serving [N] queries/day with hybrid retrieval and re-ranking, reducing answer-quality complaints by [X]%"
- "Led design of multi-agent customer-facing system across [N] business workflows, with full observability and human-in-the-loop guardrails"
- "Mentored [N] engineers on LLM evaluation patterns including RAGAS, trajectory evals, and cost-aware model routing"

If you can't quantify, scope: "across 5 product teams", "for the credit risk org", etc.

## Step 5 — ATS reality

Most companies use Greenhouse, Lever, Ashby, or Workday. The CV gets parsed mechanically before any human sees it. Implications:

- **Keywords matter.** If the JD says "LangGraph", make sure "LangGraph" appears verbatim in your CV. Don't keyword-stuff (it backfires when humans review), but cover the essential terms.
- **Headers matter.** Use standard section names: "Experience", "Education", "Skills". Not "Where I've Worked" or other creative variants.
- **No images, icons, or text-in-text-boxes** in the CV — they don't parse.
- **Submit PDF unless they specifically ask for .docx**.

When you hit *"upload your resume to autofill"* in an application, the more standard your CV layout, the cleaner the autofill. Saves time.

## Step 6 — Cover letters

Still expected for ~50% of EU applications, especially Germany, France, the Nordics. UK and Netherlands often skip them.

**3-paragraph structure:**

1. **Why this company specifically** (1–2 sentences). Not "I admire your innovation" — say something concrete from their blog/talks/products. *"Your engineering blog post on multi-tenant RAG isolation last month touched on exactly the architectural problem I've been working on at Amex."*
2. **Why you** (3–4 sentences). One specific past achievement that maps to their JD + one piece of evidence (project, blog post, repo).
3. **What you'd do in your first 90 days** (2–3 sentences). Shows initiative. *"I'd want to spend the first month understanding [specific thing about their product], then propose [specific contribution]."*

Keep it under 250 words. The cover letter's job is to get the human reviewer to actually open your CV, not to be the CV.

## Step 7 — The interview process — what to expect

Typical senior GenAI Architect/Engineer loop in EU:

| Stage | Length | What it covers | How to prep |
|---|---|---|---|
| 1. Recruiter screen | 30 min | Visa, salary, motivation, basic role fit | Have a clear "why I'm leaving / why I'm looking" story; know your salary band |
| 2. Hiring manager call | 45–60 min | Past projects, technical depth surface, team fit | Two strong project stories from Amex; questions about their team |
| 3. Technical interview | 60–90 min | Coding (often LLM-flavored) + ML/LLM theory | Phase 4 prep covers this |
| 4. System design | 60–90 min | Design a GenAI system end-to-end | Phase 4 weeks 20–21 |
| 5. Take-home or pair-prog | Varies | Often skipped at senior level; sometimes a 4-hour design exercise | Decline politely if take-home is >4hrs unpaid; pair-prog is fine |
| 6. Behavioral / values | 30–60 min | STAR-format stories, culture fit | 8 STAR stories prepared (Phase 4 week 22) |
| 7. Cross-functional / VP | 30–60 min | Strategic thinking, leadership signal | Be ready to discuss the broader GenAI landscape with opinions |

Total wall-clock time per company: 3–8 weeks from first call to offer. Plan accordingly — start dream companies early.

## Step 8 — Compensation in EU (this surprises people)

Senior GenAI total comp in major EU cities for someone at your experience level:

| City | Base (EUR/GBP) | Equity | Total comp typical range |
|---|---|---|---|
| London | £100K–£170K | Often <£20K/year | £100K–£200K |
| Amsterdam | €90K–€150K | Modest | €90K–€170K |
| Berlin | €85K–€140K | Modest | €85K–€160K |
| Paris | €85K–€140K | Modest | €85K–€160K |
| Zurich | CHF 130K–200K | Modest | CHF 130K–220K |
| Dublin | €100K–€170K | Modest | €100K–€190K |

Frontier AI labs (DeepMind, Anthropic London, OpenAI London) pay materially more — often US-comparable for senior hires. Mistral and other EU AI-natives are catching up.

**Reality check:** EU senior comp is often 30–50% lower than US for equivalent roles. But:
- Healthcare typically not a personal expense
- Vacation: 25–30 days standard (vs 15 in US)
- Income tax higher; social security charges higher
- Cost of living varies enormously (Berlin much cheaper than London)
- Equity component much smaller; less upside but also less risk

**Sources for current data:**
- Levels.fyi (https://www.levels.fyi/) — has decent EU data, filter by country
- Glassdoor (https://www.glassdoor.com) — patchy but useful
- LinkedIn Salary insights
- Reddit r/cscareerquestionsEU
- Talk to people — your DMs in Phase 3 should explicitly ask about comp ranges

## Step 9 — Salary negotiation 101

Three things to internalize:

**1. Don't volunteer your current comp.** When recruiter asks, deflect: *"I'd rather focus on what makes sense for the role and market. What's the band you're working with?"* If forced (some EU recruiters are blunter), share a range that includes your actual + 30%.

**2. Always counter the first offer.** It's expected. 10–15% upside is normal. Counter on:
- Base salary first
- Sign-on bonus (often the easiest variable to flex)
- Equity (harder to move at established companies)
- Vacation days
- Relocation budget
- Visa support / lawyer fees covered

**3. Get everything in writing** before resigning from Amex. Always.

## Step 10 — Visa logistics (research now, refresh quarterly)

Main paths from India for senior tech (confirm current thresholds at application time — they update yearly):

- **🇩🇪 Germany Blue Card** — most accessible. Salary threshold around €48K (lower for "shortage occupation" IT roles). 4-year path to permanent residence. Processing 1–3 months.
- **🇳🇱 Netherlands Highly Skilled Migrant** — employer must be on the recognized sponsors list. Threshold ~€5,600/month for under-30s, higher above. Fast processing (often 2–4 weeks).
- **🇮🇪 Ireland Critical Skills Permit** — €38K threshold for relevant roles. Direct path. Processing 4–8 weeks.
- **🇫🇷 France Talent Passport** — multiple sub-categories including salaried employee. Threshold around €43K.
- **🇬🇧 UK Skilled Worker** — post-Brexit, sponsoring company required. Threshold currently £38,700 for most roles. Global Talent visa is endorsement-based and avoids employer dependency but requires specific endorsement.

**Practical implications for your search:**
- **Always confirm the company sponsors visas before investing in interview prep** — ask the recruiter on the screen call
- Companies that frequently sponsor: large tech, AI-natives (Mistral, Cohere, Anthropic, Hugging Face), most consultancies, large fintechs
- Companies that often don't: small startups under 50 people unless they have an established sponsor program

## Step 11 — Notice periods (will surprise you)

In EU, notice periods are commonly **1–3 months** for senior roles, sometimes longer. This affects:
- Your start date negotiation
- The other side's patience (they're used to it)
- When to actually resign from Amex (don't until the offer is signed and visa is at least filed)

Plan: assume 60–90 days from offer signed to first day in EU. Visa adds another 4–12 weeks depending on country.

## Step 12 — Reference checks

EU reference checks tend to be more thorough than India/US norms. Have 3 references warmed up before you need them:
- Current or recent manager (carefully — only after offer stage)
- A peer or report
- A senior cross-functional partner

Tell them you might list them, and brief them on the role you're applying for. References get called.

## Step 13 — When you receive an offer

Don't accept on the call. Standard playbook:

1. *"Thank you, this is really exciting. Let me think it through and get back to you in [2–3 days]."*
2. Read the full written offer carefully (base, bonus, equity vesting, sign-on, benefits, notice, non-compete, IP)
3. Negotiate in writing or on a follow-up call (Step 9 above)
4. Sign once everything is locked
5. Communicate timeline to your other active processes — many will accelerate when they hear you have a deadline
6. *Then* resign from Amex

## Step 14 — Common pitfalls

- **Applying too early** — under-built profile + half-finished projects = wasted apps
- **Volume without targeting** — 200 apps in a week, all generic, all rejected
- **Ghost recruiters** — always reply, even to "no thanks"; the industry is small
- **Lying about visa status** — gets discovered at offer stage, brutal
- **Burning out month 4** — pace yourself; this is a marathon
- **Not negotiating** — you leave 10–20% on the table; recruiters expect counters
- **Accepting the first offer when you have other active processes** — let the others play out for 1–2 weeks if you can

---

# Paper reading list (24 papers, one per weekend)

| # | Paper | Track | Link |
|---|---|---|---|
| 1 | Attention Is All You Need | Builder | https://arxiv.org/abs/1706.03762 |
| 2 | BERT | Builder | https://arxiv.org/abs/1810.04805 |
| 3 | GPT-2 (technical report) | Builder | OpenAI cdn |
| 4 | GPT-3 / Few-Shot Learners | Builder | https://arxiv.org/abs/2005.14165 |
| 5 | Sentence-BERT | User | https://arxiv.org/abs/1908.10084 |
| 6 | RAG (original) | User | https://arxiv.org/abs/2005.11401 |
| 7 | DPR | User | https://arxiv.org/abs/2004.04906 |
| 8 | HyDE | User | https://arxiv.org/abs/2212.10496 |
| 9 | Llama 3 | Builder | https://arxiv.org/abs/2407.21783 |
| 10 | Self-RAG | User | https://arxiv.org/abs/2310.11511 |
| 11 | Corrective RAG | User | https://arxiv.org/abs/2401.15884 |
| 12 | InstructGPT / RLHF | Builder | https://arxiv.org/abs/2203.02155 |
| 13 | DPO | Builder | https://arxiv.org/abs/2305.18290 |
| 14 | Constitutional AI | Builder | https://arxiv.org/abs/2212.08073 |
| 15 | LoRA | Builder | https://arxiv.org/abs/2106.09685 |
| 16 | Reflexion | User | https://arxiv.org/abs/2303.11366 |
| 17 | ReAct | User | https://arxiv.org/abs/2210.03629 |
| 18 | DeepSeek R1 / Test-Time Compute | Builder | https://arxiv.org/abs/2501.12948 |
| 19 | FlashAttention | Builder | https://arxiv.org/abs/2205.14135 |
| 20 | CLIP / multimodal | Builder | https://arxiv.org/abs/2103.00020 |
| 21 | Tree of Thoughts | User | https://arxiv.org/abs/2305.10601 |
| 22 | Chain of Thought | User | https://arxiv.org/abs/2201.11903 |
| 23 | Mixture of Experts / Switch | Builder | https://arxiv.org/abs/2101.03961 |
| 24 | Toolformer | User | https://arxiv.org/abs/2302.04761 |

Note paper notes in a single place (Obsidian, Notion, or a `papers/` folder in your portfolio repo). 200-word summary each: *what problem, what idea, what evidence, what I'd use it for.*

---

# GitHub portfolio targets

By Week 24 your pinned section should be:

1. **`micrograd-extended`** — your micrograd build with extensions, full README
2. **`nano-gpt-from-scratch`** (Project B) — GPT-2-style model, training writeup, sample generations
3. **`production-rag-toolkit`** (Project C) — Hybrid retrieval, reranking, RAGAS evals, golden dataset
4. **`agentic-mcp-system`** (Project D) — LangGraph multi-agent with MCP tools, observability, trajectory evals
5. **`eu-ai-act-compliance-agent`** (Project E) — Risk classifier with documentation generator

Every repo:
- Clean README (problem, architecture diagram, demo, eval numbers, design rationale)
- Tests for non-trivial logic
- A "what I learned" section
- Demo gif or video where applicable

---

# Final notes

Three failure modes to watch for over 6 months:

1. **Tutorial drift** — watching is not learning. The blank-file re-implementation step on Thursdays and Saturdays is the actual learning. Don't skip.

2. **Stream imbalance** — the streams compound when balanced. If you skip Builder for 3 weeks because User feels more "productive," your interview performance suffers. If you skip User, your portfolio looks academic.

3. **Career-track procrastination** — the LinkedIn posts and applications feel awkward at first and stay awkward for ~6 weeks. Do them anyway. The compounding shows up as inbound recruiter messages around Month 3 and is very hard to fake.

Adjust the schedule when life happens. Protect the weekend project block, the LinkedIn weekly cadence, and the Friday revision. Everything else is movable.

Good luck. See you in Berlin / Amsterdam / London / Paris / Dublin in 6 months.
