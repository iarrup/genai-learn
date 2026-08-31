# 6-Month GenAI Europe Job Preparation Plan — v6

**Target role:** GenAI Developer / Architect (Europe-first)
**Current role:** GenAI Architect, American Express
**Daily commitment:** 2.5 hours/day Mon–Thu · Fri review · Sat–Sun projects
**Cadence:** 3 weeks study + 1 review week, repeating (6 cycles) + 2 buffer weeks
**Start date:** Today. Week 1 begins now — no more delay, no catch-up guilt.

---

## What's new in this revision (compression + full course access)

Four adjustments based on where you actually are:

1. **micrograd + makemore-1 (bigram) compressed into Week 1.** You've done both; Week 1 is now a deliberate speed-run that redoes them from blank. The freed Builder time pulls makemore-2, activations/BatchNorm, and backprop-ninja *forward*, so you reach attention (V7), the tokenizer (V8), and nanochat about a week earlier — more slack in the back half.
2. **Entire Prompt Engineering compressed into Week 1.** Also known material; the full CampusX course is re-run fast on Tuesday+Thursday of Week 1, freeing the User track to start Context Engineering (Vizuara) as early as Week 2.
3. **Full CampusX paid access** — you now have the entire catalog, so every reference to a CampusX course (Prompt Engineering, Advanced RAG, LangChain, LangGraph, Docker for ML, etc.) is fully in scope with no "if you own it" hedging.
4. **Vizuara YouTube membership** — you have all member-only content, so the Context Engineering Bootcamp's member lectures (and any other member playlists) are used directly; no need for the separate paid Engineer Plan unless you want the Colabs.

Net effect on the calendar: the *structure* (6 cycles of 3+1, review weeks 4/8/12/16/20/24) is unchanged, but the Builder track runs ~1 week ahead from Cycle 2 onward. Don't compress anything you *haven't* already done — the speed-up is only justified for genuinely-known material.

## What's new in v6 (two changes)

1. **Newsletter → The Code** (https://codenewsletter.ai/), replacing AlphaSignal, per your preference. The Papers section explains how to use it well (it leans applied/tooling, so pair it with primary research reading so your paper muscle doesn't atrophy).
2. **Tool track now builds two real Android apps you'll ship to Google Play** — a minimalist to-do list and a minimalist alarm clock with a lap button — instead of throwaway CLIs. Claude Code builds the to-do app (Month 1), Codex builds the alarm app (Month 2), Cursor polishes both and ships them to Play (Month 3). The *AI coding tools* section covers the modern Android stack (Kotlin + Jetpack Compose + Room/DataStore), why this doesn't violate your hand-coding principle, and how to frame the apps honestly in interviews.

Everything below this block is carried over from v5.

## What's new in v5 (carried into v6)

You built v4 but life got in the way and you never started. That's fine — nothing is lost, because the field moved in the meantime and the plan needed a refresh anyway. Here's what changed since v4, and why:

**1. Karpathy shipped nanochat — your Builder track now has a much stronger spine.**
In October 2025 Karpathy released **nanochat** (github.com/karpathy/nanochat), the successor to nanoGPT. Where nanoGPT covered only *pretraining*, nanochat is a **full-stack ChatGPT clone** in ~8,000 lines: tokenizer training, pretraining on FineWeb, supervised fine-tuning, optional RL with GRPO, KV-cache inference, and a web UI — all runnable end to end. It's the capstone of his (still-in-development) LLM101n course, but the repo is usable *today*, exactly like nn-zero-to-hero. This is a gift: it takes your Builder track all the way from backprop to a working, fine-tuned, served model — which maps directly onto the "can you take an LLM from scratch to production" story senior interviews probe. **nanochat is now your flagship Builder project (Project C).**

**2. LangChain and LangGraph both hit v1.0 (October 2025) — the applied stack stabilized.**
The frameworks you're learning in the User track are no longer moving targets. LangChain 1.0 is now the "fast to build" high-level agent layer; LangGraph 1.0 is the "run reliably in production" orchestration layer with **durable state, built-in persistence, and human-in-the-loop as first-class features**. Companies like Uber, LinkedIn, and Klarna run production agents on LangGraph. The v4 plan's LangChain/LangGraph content still applies, but I've re-pointed it at the v1.0 patterns (middleware, the core agent loop, durable checkpointing) rather than the pre-1.0 API.

**3. MCP is now the production standard for tool exposure — not a novelty.**
Model Context Protocol has gone from "interesting" in early 2026 to the default way agents discover and call tools. The architecture pattern — MCP servers exposing tools via JSON-RPC, agents dynamically discovering capabilities instead of hardcoding every API call — is now interview table-stakes for an architect. The plan gives MCP more weight and pairs it with the security reality below.

**4. The security conversation shifted to indirect prompt injection.**
The live production concern in 2026 isn't "user types a jailbreak" — it's **indirect prompt injection**: an agent reads a malicious document/email and gets convinced to do something harmful (e.g., purge a database). The mitigations are now standard architect knowledge: a proxy layer that validates action *impact*, HITL interrupts on high-stakes nodes, and short-lived scoped tokens per session. This is folded into the agentic and GenAIOps cycles.

**5. The industry framing: "work factor," not "wow factor."**
2026 is the year GenAI moved from demos to production value — LLMOps, agentic workflows, and small/specialized models (SLMs) over ever-bigger ones. Your target role (Architect) sits exactly on this shift. The plan leans into deployment, evaluation, observability, and cost — the "work factor" skills — more than v4 did.

Everything else — the five daily blocks, the 3+1 cadence, the deep-ml focus, the CampusX/Vizuara/Karpathy resource priority, the LinkedIn and job-search hand-holding — is carried over from v4 unchanged.

---

## What carried over from v4 (your earlier feedback, still honored)

- **Builder time was tight** → still five clearly-bounded blocks, 1 hr main study with a hard stop.
- **deep-ml was easy to skip** → still its own fixed, protected 30-min slot. Skipping is not an option (it's your weak area, so it gets *more* protection, not less).
- **Prompt eng & context eng had no concrete material** → still mapped to CampusX's paid **Prompt Engineering** course and Vizuara's **LLM Context Engineering Bootcamp** playlist.
- **Devin and Copilot** → still excluded from the tool track (you learn them at work). Tool track is Claude Code → OpenAI Codex → Cursor.
- **Cadence** → still 3 weeks study + 1 review week.
- **Newsletter** → changed to **The Code** (codenewsletter.ai) per your latest preference; reasoning updated in the Papers section.

---

## The five daily blocks

Mon–Thu, total 2.5 hours, split into five fully-protected blocks. No block borrows time from another — if you run over in Builder, you stop and move on. The protection is the point.

| # | Block | Time | Mon | Tue | Wed | Thu |
|---|---|---|---|---|---|---|
| 1 | **Regular prep — Builder OR User** | 1 hr | 🏗️ Builder | 🛠️ User | 🏗️ Builder | 🛠️ User |
| 2 | **deep-ml practice** | 30 min | ✓ | ✓ | ✓ | ✓ |
| 3 | **GenAI coding tools** | 30 min | ✓ | ✓ | ✓ | ✓ |
| 4 | **Papers & latest updates** | 30 min | ✓ | ✓ | ✓ | ✓ |
| 5 | **LinkedIn & job search** | — | — | — | — | — |

Block 5 is **weekend only**, ~2 hours total (a Saturday morning push, or 1 hr Sat + 1 hr Sun). Mon–Thu evenings stay clean.

**Friday:** review the week — no new content. Re-read notes, redo the hardest deep-ml problem of the week from blank, update your tracker. ~1.5 hours is plenty.

**Sat–Sun:** weekend project (hand-coded, plain VS Code, no AI assistant) + the 2 hr LinkedIn/job-search block + paper of the week.

### Suggested order within the day

1. **deep-ml first** (30 min) — the block you tend to skip; do it before willpower runs out
2. **Builder / User** (1 hr) — heaviest cognitive block, fresh focus
3. **Coding tools** (30 min) — lighter, good after main study
4. **Papers / newsletter** (30 min) — light reading, fine at the end

Swap freely if the order doesn't fit your day — but **never skip deep-ml.**

---

## The 3+1 cadence (6 cycles)

| Cycle | Weeks | Theme | Review week |
|---|---|---|---|
| 1 | 1–3 | Foundations speed-run (micrograd/makemore known) + Prompt engineering speed-run | Week 4 |
| 2 | 5–7 | Backprop-ninja, attention, tokenizer + Context engineering (finish) | Week 8 |
| 3 | 9–11 | nanochat full-stack build + RAG fundamentals | Week 12 |
| 4 | 13–15 | Fine-tuning/RL (nanochat SFT+GRPO) + Advanced RAG | Week 16 |
| 5 | 17–19 | Alignment & reasoning models + Agentic systems (LangGraph 1.0 + MCP) | Week 20 |
| 6 | 21–23 | Frontier + GenAIOps / deployment / security | Week 24 |
| Buffer | 25–26 | Active interviews & polish | — |

Review weeks (4, 8, 12, 16, 20, 24) are consolidation, not new learning: re-do the hardest material from blank, write one synthesis note, ship one substantial LinkedIn post.

---

## Resource priority (unchanged) with 2026 content map

1. **CampusX** — YouTube (https://www.youtube.com/@campusx-official) + paid courses (https://learnwith.campusx.in/s/store). **You now have full paid-catalog access**, so every course below is directly usable. Anchor courses:
   - **Prompt Engineering** (paid) — prompt-eng gap
   - **Advanced RAG** (paid) — RAG-mastery cycle
   - **Agentic Coding using Claude Code** (paid/YouTube) — pairs with tool track
   - **Generative AI using LangChain** (YouTube) — check for v1.0-updated content; if the playlist predates Oct 2025, supplement with LangChain's own v1.0 docs
   - **Agentic AI using LangGraph** (YouTube) — same note re: v1.0
   - **Docker for Machine Learning** (paid) — deployment cycle
2. **Vizuara** — YouTube (https://www.youtube.com/@vizuara) + pods (https://pods.vizuara.ai/). **You now have the YouTube membership**, so all member-only content is directly in scope.
   - **Building LLMs from scratch** (free playlist) — Builder track companion
   - **LLM Context Engineering Bootcamp** (member content covered by your YouTube membership) — context-eng gap. Covers Foundations of Context, MCP, multi-agent context (AGENTS.md), RAG-as-context-engineering. The separate paid Engineer Plan (context-engineering.vizuara.ai) is only worth it if you specifically want the downloadable Colabs/exercises; the lectures themselves are in your membership.
3. **Karpathy** — Builder track anchor.
   - **nn-zero-to-hero** (https://github.com/karpathy/nn-zero-to-hero) — micrograd → GPT, weeks 1–9
   - **nanochat** (https://github.com/karpathy/nanochat) — full-stack ChatGPT clone, the Cycle 3–4 spine. Read the repo's README and walkthrough; there's a hosted demo at nanochat.karpathy.ai to see the endpoint.
4. **deep-ml** (https://www.deep-ml.com/) — daily 30-min practice.
5. **External** — arXiv papers, The Code (one newsletter), official docs (LangChain/LangGraph v1.0, MCP spec at modelcontextprotocol.io, the coding tools).

Precedence when topics overlap: CampusX (you own it) → Vizuara → Karpathy for theory → external. Karpathy wins for transformer internals and the full-stack build specifically. For **LangChain/LangGraph, prefer the official v1.0 docs** over any pre-1.0 tutorial, since the API stabilized in October 2025.

---

## Phase overview (24 study weeks + 2 buffer)

| Cycle | Weeks | 🏗️ Builder | 🛠️ User | ⌨️ Coding tools | Weekend project (hand-coded) |
|---|---|---|---|---|---|
| 1 | 1–4 | **Speed-run** micrograd + makemore-1 (W1), then makemore-2, activations, backprop-ninja pulled forward | **Speed-run** Prompt engineering (W1), then Context engineering begins (Vizuara member) | **Month 1: Claude Code → To-Do app** | Project A: micrograd + name generator |
| 2 | 5–8 | Finish backprop-ninja, WaveNet, **attention (V7), tokenizer (V8)**, open nanochat | Finish Context engineering (Vizuara member) | Month 1 → Month 2 start | Project B: prompt+context library |
| 3 | 9–12 | **nanochat** — tokenizer, pretraining, inference (a week ahead) | RAG fundamentals (CampusX LangChain v1.0 — full paid access) | **Month 2: OpenAI Codex → Alarm app** | Project C: nanochat pretrained model |
| 4 | 13–16 | **nanochat** — SFT, GRPO RL, eval, serving | Advanced RAG (CampusX paid) | Month 2 → Month 3 start | Project D: production RAG |
| 5 | 17–20 | Alignment, RLHF, DPO, reasoning models | Agentic AI (LangGraph 1.0 + MCP) | **Month 3: Cursor → polish + ship both to Play** | Project E: agentic system w/ MCP |
| 6 | 21–24 | Fine-tuning/PEFT, SLMs, frontier | GenAIOps, deployment, security | Month 3 wrap | Project F: EU AI Act compliance agent |
| — | 25–26 | Buffer / active interviews | — | — | Interview prep |

Review weeks: **4, 8, 12, 16, 20, 24.**

---

# Week-by-week schedule

Each row is one Mon–Thu day, four blocks across. Weekend rows carry 📄 (paper) + 💼 (LinkedIn/job task) + project work.

Column legend: **🏗️/🛠️** = Builder/User (1 hr) · **⌨️** = deep-ml (30 min) · **🛠️⌨️** = coding tools (30 min) · **📰** = papers/newsletter (30 min).

---

## Cycle 1 — Weeks 1–3 (compressed) + Review Week 4: Foundations speed-run + Prompt engineering

> **You've done micrograd, makemore-1 (bigram), and all of Prompt Engineering before — so Cycle 1 is a deliberate speed-run of known material, and the time saved is reinvested by pulling later Builder content forward.** Net effect: you reach attention (Karpathy V7) and nanochat earlier, giving more slack in the back half.
> 🏗️ Builder: Week 1 redoes micrograd + makemore-1 (bigram) fast; Weeks 2–3 pull makemore-2 (MLP), activations/BatchNorm, backprop-ninja forward from the old Cycle 2.
> 🛠️ User: Week 1 redoes **all of CampusX Prompt Engineering** fast (you have full paid access now); Weeks 2–3 begin **Vizuara Context Engineering** early (full member access now — the member-only lectures are in scope).
> ⌨️ deep-ml: beginner→intermediate — LA + ML (W1), add Deep Learning (W2–3)
> 🛠️⌨️ Tools: **Month 1 = Claude Code → To-Do app**
> 📰 Papers: 1 per weekend

### Week 1 — Speed-run week (redo known material)
| Day | 🏗️/🛠️ (1 hr) | ⌨️ deep-ml (30) | 🛠️⌨️ Tools (30) | 📰 Papers (30) |
|---|---|---|---|---|
| Mon | 🏗️ **micrograd** — redo the whole thing from blank in one sitting (you've done it; this is the speed-run). Reference Karpathy V1 only if a spot is fuzzy. | LA: dot product / matrix mul | Claude Code: read docs (https://docs.claude.com/en/docs/claude-code/overview); confirm install. **Set up the Android/Kotlin/Compose project** for the To-Do app in Android Studio | Subscribe to The Code (https://codenewsletter.ai/). Skim today's issue. Read abstract of *Attention Is All You Need* |
| Tue | 🛠️ **CampusX Prompt Eng — speed-run first half** (foundations, structure, few-shot, role, structured output). You've done it; move fast, take fresh notes only on what you'd forgotten. | ML: linear regression closed form | Claude Code: plan-then-execute loop — have it explain the Compose project structure; read every generated file | The Code + Lilian Weng transformer post (lilianweng.github.io) |
| Wed | 🏗️ **makemore-1 (bigram)** — redo from blank. Reference Karpathy V2 only if needed. By end of today, micrograd + bigram are both re-consolidated. | LA: transpose, eigenvalue intuition | Claude Code: build the task-list Composable; read *Permissions* docs; deny one action to feel the loop | The Code + skim one huggingface.co/papers item |
| Thu | 🛠️ **CampusX Prompt Eng — speed-run second half** (CoT, self-consistency, chaining, decomposition, evaluation, advanced patterns). Finish the course today. | ML: gradient descent by hand | Claude Code: create a `CLAUDE.md` with the app's conventions; build the add-task screen | The Code + finish the Weng piece |
| Fri | **Review** (~1.5 hr): confirm micrograd + bigram both re-run from blank cleanly; consolidate your refreshed prompt-pattern library doc | — | — | — |
| Sat | **Project A start** — fork micrograd from blank, add softmax + cross-entropy. Plain VS Code. | 📄 *Attention Is All You Need* — https://arxiv.org/abs/1706.03762 | 💼 LinkedIn Week 1: recover-or-restart decision + Profile Build Sections 1–4 | — |
| Sun | Project A iteration + draft blog *"What backprop actually computes"* | — | 💼 LinkedIn: finish photo + banner + headline + About | — |

### Week 2 — makemore-2 (MLP) + Context engineering begins
| Day | 🏗️/🛠️ (1 hr) | ⌨️ deep-ml (30) | 🛠️⌨️ Tools (30) | 📰 Papers (30) |
|---|---|---|---|---|
| Mon | 🏗️ Karpathy V3 *makemore part 2* (MLP) — first half (new-ish territory, so normal pace resumes) | LA: matrix-vector mul | Claude Code: planning session for the Room persistence layer — refine before it writes code | The Code + 1 abstract |
| Tue | 🛠️ Vizuara CE Bootcamp L1 *Foundations of Context* (full member access — do the member-only depth) | ML: logistic regression | Claude Code: implement Room storage (entity, DAO, database) for tasks | The Code |
| Wed | 🏗️ Karpathy V3 *makemore part 2* (MLP) — second half; re-implement MLP from blank | LA: norms, distances | Claude Code: wire ViewModel + StateFlow so the list reacts to storage | The Code + Karpathy's "Unreasonable Effectiveness of RNNs" (skim) |
| Thu | 🛠️ Vizuara CE Bootcamp L2 (context layers: Instructional/Knowledge/Tool) | ML: cosine similarity | Claude Code: custom slash commands for repeated Compose/Room boilerplate | The Code |
| Fri | **Review** | — | — | — |
| Sat | **Project A v2** — MLP name generator on your micrograd | 📄 *BERT* — https://arxiv.org/abs/1810.04805 | 💼 LinkedIn Week 2: Experience + Education + Skills + first 50 connections | — |
| Sun | Project A v2 + perplexity comparison writeup | — | 💼 LinkedIn: 5 substantive comments | — |

### Week 3 — Activations/BatchNorm + backprop-ninja + Context engineering
| Day | 🏗️/🛠️ (1 hr) | ⌨️ deep-ml (30) | 🛠️⌨️ Tools (30) | 📰 Papers (30) |
|---|---|---|---|---|
| Mon | 🏗️ Karpathy V4 *makemore part 3* (activations & gradients, BatchNorm) — first half | DL: sigmoid forward+backward | Claude Code: add edit + delete + complete-toggle for tasks | The Code + 1 abstract |
| Tue | 🛠️ Vizuara CE Bootcamp L3 (token budget, context-window optimization) | DL: ReLU + leaky variants | Claude Code: have it write tests for the DAO/ViewModel — review each critically | The Code |
| Wed | 🏗️ Karpathy V4 — second half (BatchNorm forward+backward); then V5 *backprop ninja* — first half | DL: softmax forward+backward | Claude Code: light MCP — connect one simple server (quick detour to see the feature) | The Code + skim huggingface.co/papers |
| Thu | 🛠️ Vizuara CE Bootcamp L4 *MCP intro* — connect this to the MCP you'll use in Cycle 5 | DL: BatchNorm by hand | Claude Code: minimalist UI polish; run the app on your own phone | The Code |
| Fri | **Review** | — | — | — |
| Sat | **Project A v3** — finalize micrograd + name generator README, push to GitHub | 📄 *GPT-2 technical report* (OpenAI cdn) | 💼 First LinkedIn post (*"Starting a 6-month deep dive into LLM internals…"*) | — |
| Sun | Plan Project B (prompt+context library) | — | 💼 LinkedIn: 5 comments + 3 connection requests | — |

### Week 4 — REVIEW WEEK
| Day | Block |
|---|---|
| Mon | Re-do the backprop-ninja gradient derivations from blank (this is the hardest Builder material so far). |
| Tue | Re-do the hardest deep-ml problem from each of the last 3 weeks (4 problems × 20 min). |
| Wed | Write long-form note: *"How prompt engineering actually works — what I'd tell a junior engineer."* 1000 words. |
| Thu | Publish + cross-post to LinkedIn. **Claude Code Month 1 wrap:** 300-word reflection note. |
| Fri | Audit Project A README; freshen GitHub; tracker review. |
| Sat | 📄 *GPT-3 / Few-Shot Learners* — https://arxiv.org/abs/2005.14165. 💼 LinkedIn: 10 comments + 5 new connections. |
| Sun | Rest. |

---

## Cycle 2 — Weeks 5–7 + Review Week 8: Attention, tokenizer, nanochat setup + Context engineering

> **Because Cycle 1 pulled V4/V5 forward, Cycle 2 Builder starts higher up the stack — finishing backprop-ninja, then attention (V7) and the tokenizer (V8), and *beginning nanochat setup a week early*.** This is the payoff from the Week-1 speed-run.
> 🏗️ Builder: finish V5 *backprop ninja*, V6 *WaveNet* (light), V7 *Let's build GPT* (attention), V8 *Tokenizer*, then open the nanochat repo.
> 🛠️ User: continue **Vizuara Context Engineering** (member-only lectures included) through the advanced material — you started it in Week 2, so you finish the bootcamp here.
> ⌨️ deep-ml: intermediate — Deep Learning (attention/tokenizer), NLP
> 🛠️⌨️ Tools: Claude Code wrap = ship the To-Do app (W5), begin **Month 2 — OpenAI Codex → Alarm clock app** (W6+)
> 📰 Papers: 1 per weekend

### Week 5 — finish backprop-ninja + WaveNet + To-Do app ships
| Day | 🏗️/🛠️ (1 hr) | ⌨️ deep-ml (30) | 🛠️⌨️ Tools (30) | 📰 Papers (30) |
|---|---|---|---|---|
| Mon | 🏗️ Karpathy V5 *backprop ninja* — second half; derive 3 gradients yourself before checking | DL: chain rule on 2-layer MLP | Claude Code W5 (project week): finish the To-Do app — make it genuinely usable on your phone, fix real bugs | The Code + 1 abstract |
| Tue | 🛠️ Vizuara CE Bootcamp L5 *Multi-agent context, AGENTS.md* (member content) | DL: layer norm by hand | Claude Code: To-Do reflection note (interaction/strengths/weaknesses/fit) | The Code |
| Wed | 🏗️ Karpathy V6 *WaveNet* (lighter watch — dilated convolutions intuition) | DL: dropout intuition | To-Do app: ship v1 to your phone. **Prep Codex:** read https://developers.openai.com/codex (ChatGPT Plus $20/mo covers CLI) | The Code + skim HF Papers |
| Thu | 🛠️ Vizuara CE Bootcamp L6 (advanced context management; member content) | DL: weight init schemes | Codex: install; hello-world; **scaffold the Alarm clock Android project** | The Code |
| Fri | **Review** | — | — | — |
| Sat | **Project B start** — prompt+context library: composable prompt-pattern functions with context-window awareness | 📄 *Sentence-BERT* — https://arxiv.org/abs/1908.10084 | 💼 LinkedIn: second post (paper-takeaway format) | — |
| Sun | Project B + tests | — | 💼 LinkedIn engagement | — |

### Week 6 — Attention (V7)
| Day | 🏗️/🛠️ (1 hr) | ⌨️ deep-ml (30) | 🛠️⌨️ Tools (30) | 📰 Papers (30) |
|---|---|---|---|---|
| Mon | 🏗️ Karpathy V7 *Let's build GPT* — first third (single-head attention) | DL: scaled dot-product attention by hand | **Codex M2 W1**: ghost-text mechanics (CLI vs IDE vs Cloud); build the alarm data model + DataStore | The Code + 1 abstract |
| Tue | 🛠️ Vizuara CE Bootcamp L7 (RAG-as-context-engineering; member content) | DL: attention mask basics | Codex: build the set-alarm UI; reject/cycle suggestions, spot confident-wrong | The Code |
| Wed | 🏗️ Karpathy V7 — second third (multi-head, residual, layernorm) | DL: multi-head split+concat | Codex: `AlarmManager` scheduling + exact-alarm permission model; use /explain on the generated code | The Code + skim HF Papers |
| Thu | 🛠️ Vizuara CE Bootcamp L8 (context for tool-use / agents; member content) | DL: positional encoding (sinusoidal) | Codex: the ringing screen (full-screen intent / notification); configure auth, read pricing | The Code |
| Fri | **Review** | — | — | — |
| Sat | **Project B v2** — add context-budget guards + auto-chunk-for-budget | 📄 *RAG (original)* — https://arxiv.org/abs/2005.11401 | 💼 LinkedIn: Build Log on Project A (micrograd) | — |
| Sun | Project B + README | — | 💼 LinkedIn engagement | — |

### Week 7 — Attention finish + Tokenizer (V8) + open nanochat
| Day | 🏗️/🛠️ (1 hr) | ⌨️ deep-ml (30) | 🛠️⌨️ Tools (30) | 📰 Papers (30) |
|---|---|---|---|---|
| Mon | 🏗️ Karpathy V7 — final third (training loop, scaling intuition); re-implement the attention block from blank | DL: causal mask | **Codex W2**: the lap/stopwatch feature — start/stop/lap and the lap list (real state practice) | The Code + 1 abstract |
| Tue | 🛠️ Vizuara CE Bootcamp — finish the bootcamp; write your context-engineering summary doc | DL: attention scaling (√d) | Codex: foreground service so the alarm survives the app backgrounding | The Code |
| Wed | 🏗️ Karpathy V8 *Tokenizer* — first half (BPE) | DL: BPE by hand | Codex: try Cloud mode for a contained task (e.g. a settings screen) | The Code + skim HF Papers |
| Thu | 🛠️ RAG warm-up — read the LangChain v1.0 intro docs (langchain.com) to prep Cycle 3; you have full CampusX access for the deep version | DL: multi-head attention impl | Codex: reboot persistence (reschedule alarms after device restart) | The Code |
| Fri | **Review** | — | — | — |
| Sat | **Project B v3** — package, README, push. This is a portfolio repo. | 📄 *Dense Passage Retrieval* — https://arxiv.org/abs/2004.04906 | 💼 LinkedIn: 10 comments + 3 connections | — |
| Sun | Project B finalize + **open the nanochat repo, read its README end-to-end** (Project C prep) | — | 💼 LinkedIn engagement | — |

### Week 8 — REVIEW WEEK
| Day | Block |
|---|---|
| Mon | Re-watch V7 attention block + finish V8 tokenizer (BPE deeply). Redo the attention block from blank. |
| Tue | Re-do 4 hardest deep-ml problems from cycle 2. |
| Wed | Write long-form note: *"Context engineering vs prompt engineering — the actual difference."* 1000 words. |
| Thu | Publish + cross-post. **Codex check-in:** 1 hr on the Alarm app — reliability pass. |
| Fri | Audit Project B; tracker. **Read the nanochat tokenizer + pretraining code** to prep Cycle 3 (you're a week ahead here — use it). |
| Sat | 📄 *HyDE* — https://arxiv.org/abs/2212.10496. 💼 LinkedIn: post your context-eng note. |
| Sun | Rest. |

---

## Cycle 3 — Weeks 9–12: nanochat (build) + RAG fundamentals

> 🏗️ Builder: **nanochat** in earnest — you finished the tokenizer video (V8) and opened the repo in Cycle 2, so dive straight into running tokenizer training + pretraining, and KV-cache inference. You are building a real ChatGPT-clone spine. (Full training runs cost GPU money — see the note below; you can study + run the small stages locally/cheaply and rent an 8×H100 node only if/when you want the full speedrun.)
> 🛠️ User: **CampusX Generative AI using LangChain** + LangChain **v1.0 docs** (langchain.com) — build a naive→hybrid RAG pipeline
> ⌨️ deep-ml: intermediate — Deep Learning (attention/tokenizer/KV-cache), NLP
> 🛠️⌨️ Tools: continue **Codex → Alarm app** (working alarm+lap on your phone by ~W10)
> 📰 Papers: 1 per weekend

> **nanochat cost note:** the famous "$100 / 4 hours on 8×H100" is the *full* speedrun. You do **not** need to spend that to learn from it. Read the code, run the tokenizer and a tiny pretraining run on whatever GPU you can access (even a single consumer GPU or a short cloud rental), and study the SFT/RL/inference stages from the code. If you *do* want a trained model to show, budget one deliberate cloud run — but the learning is in the code, not the credit-card charge.

### Week 9
| Day | 🏗️/🛠️ (1 hr) | ⌨️ deep-ml (30) | 🛠️⌨️ Tools (30) | 📰 Papers (30) |
|---|---|---|---|---|
| Mon | 🏗️ nanochat: run tokenizer training on a small corpus; understand how the Rust tokenizer maps to what you learned in V8 | DL: BPE by hand | **Codex W3**: handle Do Not Disturb + edge cases; make the alarm actually reliable | The Code + 1 abstract |
| Tue | 🛠️ CampusX LangChain v1.0 — intro, models, prompts, LCEL | NLP: token frequencies | Codex: /tests for the alarm scheduling logic — review critically | The Code |
| Wed | 🏗️ nanochat: pretraining loop — read it end to end; understand the FineWeb data path and the Transformer config | DL: multi-head attention impl | Codex: agentic pass to clean up the alarm codebase | The Code + HF Papers |
| Thu | 🛠️ CampusX LangChain — chains, output parsers, structured output | NLP: BM25 basics | Codex: draft reflection note (Android was unfamiliar — note where Codex misled you) | The Code |
| Fri | **Review** | — | — | — |
| Sat | **Project C start (nanochat)** — clone repo, run tokenizer training on a small corpus, read the pretraining loop | 📄 *Llama 3 paper* — https://arxiv.org/abs/2407.21783 | 💼 LinkedIn: Build Log on Project B | — |
| Sun | Project C — understand FineWeb data pipeline; run a tiny pretraining step | — | 💼 LinkedIn engagement | — |

### Week 10
| Day | 🏗️/🛠️ (1 hr) | ⌨️ deep-ml (30) | 🛠️⌨️ Tools (30) | 📰 Papers (30) |
|---|---|---|---|---|
| Mon | 🏗️ nanochat: pretraining internals — how it differs from nanoGPT; the Transformer config | DL: KV cache mechanics | **Codex W4/wrap**: Alarm app must actually wake you up (the real test); final reflection | The Code + 1 abstract |
| Tue | 🛠️ CampusX LangChain — embeddings + vector stores (Chroma, Qdrant, pgvector) | NLP: cosine sim at scale | Codex: README + push the Alarm app repo | The Code |
| Wed | 🏗️ nanochat: KV-cache inference — trace a generation end to end | DL: softmax with temperature | Codex wrap (Alarm app done). **Prep Cursor:** read cursor.com/docs | The Code + HF Papers |
| Thu | 🛠️ CampusX LangChain — hybrid retrieval (BM25 + dense), measure on 50-query set | NLP: TF-IDF | Cursor: install, import settings; open both app repos to plan the polish pass | The Code |
| Fri | **Review** | — | — | — |
| Sat | **Project C** — get a small pretrained nanochat generating text; save checkpoints | 📄 *Self-RAG* — https://arxiv.org/abs/2310.11511 | 💼 LinkedIn: post comparing Claude Code vs Codex (from your two reflection notes) | — |
| Sun | Project C — sample generations, document the run | — | 💼 LinkedIn engagement | — |

### Week 11
| Day | 🏗️/🛠️ (1 hr) | ⌨️ deep-ml (30) | 🛠️⌨️ Tools (30) | 📰 Papers (30) |
|---|---|---|---|---|
| Mon | 🏗️ nanochat: read the SFT (supervised fine-tuning) stage with SmolTalk — preview of Cycle 4 | DL: positional encoding impl | **Cursor M3 W1**: Tab completion (takes days to adjust); start To-Do polish — app icon, dark theme | The Code + 1 abstract |
| Tue | 🛠️ CampusX LangChain — chunking strategies (fixed, recursive, semantic, structure-aware) | NLP: causal mask | Cursor: Cmd+K / Cmd+L to add a settings screen + accessibility labels to the To-Do app | The Code |
| Wed | 🏗️ nanochat: evaluation harness (ARC-Easy, MMLU, GSM8K, HumanEval) — how the report card works | DL: attention scaling (√d) | Cursor: `.cursorrules` with your app conventions; consistent structure across both apps | The Code + HF Papers |
| Thu | 🛠️ Hands-on: 4 embedding models on same 100-doc corpus, tabulate retrieval quality | NLP: hybrid retrieval | Cursor: `@` references to refactor shared patterns across To-Do and Alarm | The Code |
| Fri | **Review** | — | — | — |
| Sat | **Project C polish** — README with loss curves + sample generations + the nanochat report card. Portfolio repo. | 📄 *nanoGPT/nanochat design* — read Karpathy's nanochat README as the "paper" this week | 💼 LinkedIn: Build Log on Project C — *"I trained a small ChatGPT-clone end to end with Karpathy's nanochat. Here's what each stage taught me."* (strong post) | — |
| Sun | Project C finalize | — | 💼 LinkedIn engagement | — |

### Week 12 — REVIEW WEEK
| Day | Block |
|---|---|
| Mon | Re-watch Karpathy V7–8. Re-read the nanochat pretraining + inference code until you can explain every stage. |
| Tue | Re-do 4 hardest deep-ml problems from cycle 3. |
| Wed | Write long-form note: *"From nanoGPT to nanochat — what the full LLM pipeline actually involves."* 1500 words. |
| Thu | Publish + cross-post. Cursor: write the Play listing assets (screenshots, description) for both apps. |
| Fri | Audit Project C; freshen GitHub. |
| Sat | 📄 *Corrective RAG* — https://arxiv.org/abs/2401.15884. 💼 First **soft-outreach DMs** (3–5 EU GenAI engineers). |
| Sun | Rest. |

---

## Cycle 4 — Weeks 13–16: nanochat fine-tuning/RL + Advanced RAG

> 🏗️ Builder: **nanochat SFT + GRPO RL + serving** — the "make it useful" half of the pipeline. Plus modern-architecture reading (Llama, Mistral, MoE, SLMs).
> 🛠️ User: **CampusX Advanced RAG paid course** — HyDE, multi-query, reranking, RAGAS evaluation, agentic RAG
> ⌨️ deep-ml: intermediate — Deep Learning + NLP
> 🛠️⌨️ Tools: continue **Cursor → polish both apps + ship to Play** (submitted by ~W15)
> 📰 Papers: 1 per weekend

### Week 13
| Day | 🏗️/🛠️ (1 hr) | ⌨️ deep-ml (30) | 🛠️⌨️ Tools (30) | 📰 Papers (30) |
|---|---|---|---|---|
| Mon | 🏗️ nanochat SFT — run supervised fine-tuning on the SmolTalk conversations | DL: impl multi-head attention | **Cursor W2**: Composer/Agent mode — coordinated multi-file cleanup across both apps | The Code + 1 abstract |
| Tue | 🛠️ CampusX Advanced RAG — opening modules, chunking deep dive | NLP: BGE/E5 embeddings overview | Cursor: review every multi-file diff before accepting (you own every line you ship) | The Code |
| Wed | 🏗️ nanochat SFT — evaluate before/after; understand what SFT changes | DL: RMSNorm vs LayerNorm | Cursor: ghost-text vs Composer — when each fits, on real polish tasks | The Code + HF Papers |
| Thu | 🛠️ CampusX Advanced RAG — query transformations (HyDE, multi-query, step-back) | NLP: HyDE pseudocode | Cursor: learn the release path — signing, building a `.aab` | The Code |
| Fri | **Review** | — | — | — |
| Sat | **Project D start** — production RAG over a corpus you care about; hybrid retrieval + reranking + RAGAS from the start. Plain VS Code. | 📄 *FlashAttention* — https://arxiv.org/abs/2205.14135 | 💼 LinkedIn: post on Advanced RAG learnings | — |
| Sun | Project D scaffolding | — | 💼 LinkedIn engagement | — |

### Week 14
| Day | 🏗️/🛠️ (1 hr) | ⌨️ deep-ml (30) | 🛠️⌨️ Tools (30) | 📰 Papers (30) |
|---|---|---|---|---|
| Mon | 🏗️ nanochat GRPO — read the RL stage; understand GRPO vs PPO at a high level | DL: policy gradient intuition | **Cursor W3**: set up Play Console (one-time ~$25); prepare the To-Do app for submission | The Code + 1 abstract |
| Tue | 🛠️ CampusX Advanced RAG — reranking (Cohere, BGE-reranker, cross-encoders) | NLP: cross-encoder reranking | Cursor: finalize To-Do app — build signed `.aab`, submit to Play | The Code |
| Wed | 🏗️ nanochat GRPO — run the RL stage if compute allows; else study the reward loop in code | DL: KL divergence | Cursor: prepare the Alarm app for submission — listing, assets | The Code + HF Papers |
| Thu | 🛠️ CampusX Advanced RAG — RAGAS framework (docs.ragas.io); build a 50-question golden set | NLP: context-recall metric | Cursor: finalize Alarm app — build signed `.aab`, submit to Play | The Code |
| Fri | **Review** | — | — | — |
| Sat | **Project D** — implement HyDE + reranking; run RAGAS baseline | 📄 *DPO* — https://arxiv.org/abs/2305.18290 | 💼 LinkedIn: 10 comments + 5 connections | — |
| Sun | Project D + golden set | — | 💼 LinkedIn engagement | — |

### Week 15
| Day | 🏗️/🛠️ (1 hr) | ⌨️ deep-ml (30) | 🛠️⌨️ Tools (30) | 📰 Papers (30) |
|---|---|---|---|---|
| Mon | 🏗️ nanochat serving — the web UI + inference server; you now have an end-to-end system | DL: beam search | **Cursor W4/wrap**: both apps submitted to Play; Cursor reflection note | The Code + 1 abstract |
| Tue | 🛠️ CampusX Advanced RAG — Self-RAG / Corrective RAG / agentic RAG modules | NLP: faithfulness metric | Cursor: READMEs for both app repos; reflect on Agent mode | The Code |
| Wed | 🏗️ Modern architectures — Mistral (sliding-window attn), MoE (Switch), and the SLM trend | DL: MoE routing | Cursor wrap (both apps shipped). **Synthesize 3-tool narrative** from all reflection notes | The Code + HF Papers |
| Thu | 🛠️ CampusX Advanced RAG — finish; write your RAG decision matrix | NLP: NDCG / MRR | Draft the interview answer on tools | The Code |
| Fri | **Review** | — | — | — |
| Sat | **Project D evaluation pass** — real RAGAS numbers in README. Flagship repo. | 📄 *Switch Transformers / MoE* — https://arxiv.org/abs/2101.03961 | 💼 LinkedIn: Build Log on Project D with RAGAS numbers | — |
| Sun | Project D polish | — | 💼 LinkedIn engagement | — |

### Week 16 — REVIEW WEEK
| Day | Block |
|---|---|
| Mon | Re-read the full nanochat pipeline (tokenizer→pretrain→SFT→GRPO→inference→serve). Can you whiteboard it? |
| Tue | Re-do 4 hardest deep-ml problems from cycle 4. |
| Wed | Write long-form note: *"How I evaluate a RAG system"* — with the 3-tool reflection embedded. 1500 words. |
| Thu | Publish + cross-post. |
| Fri | Audit Project D; freshen GitHub. Push nanochat (Project C) final if not done. |
| Sat | 📄 *Reflexion* — https://arxiv.org/abs/2303.11366. 💼 LinkedIn: 10 follow-up DMs. |
| Sun | Rest. |

---

## Cycle 5 — Weeks 17–20: Alignment & reasoning + Agentic systems (LangGraph 1.0 + MCP)

> 🏗️ Builder: InstructGPT (RLHF), DPO, Constitutional AI, and **reasoning models** (DeepSeek R1, test-time compute). You've now *done* RLHF-adjacent work in nanochat, so these papers land concretely.
> 🛠️ User: **CampusX Agentic AI using LangGraph** + LangGraph **v1.0 docs** + **MCP**. Emphasis on the v1.0 production features (durable state, persistence, HITL) and MCP tool exposure. This is your architect differentiator.
> ⌨️ deep-ml: intermediate→advanced — Deep Learning (RLHF/DPO/PEFT), NLP (tools/agents)
> 🛠️⌨️ Tools: **Month 4 freed** — use the 30 min for extra deep-ml (your weak area) or deepening one tool. Recommend extra deep-ml.
> 📰 Papers: 1 per weekend

### Week 17
| Day | 🏗️/🛠️ (1 hr) | ⌨️ deep-ml (30) | 🛠️⌨️ extra deep-ml (30) | 📰 Papers (30) |
|---|---|---|---|---|
| Mon | 🏗️ InstructGPT — methodology; map it onto what nanochat's SFT+RL did | DL: KL divergence | Extra DL — reward modeling | The Code + 1 abstract |
| Tue | 🛠️ CampusX LangGraph v1.0 — state, nodes, edges; the core agent loop | NLP: tool-use schemas | Extra NLP | The Code |
| Wed | 🏗️ RLHF deep dive — PPO vs the GRPO you saw in nanochat | DL: policy gradient | Extra DL | The Code + HF Papers |
| Thu | 🛠️ CampusX LangGraph — basic agents; **durable state + checkpointing (v1.0)** | NLP: beam search | Extra NLP | The Code |
| Fri | **Review** | — | — | — |
| Sat | **Project E start** — agentic system (research assistant / code reviewer / expense categorizer) on LangGraph 1.0 | 📄 *InstructGPT / RLHF* — https://arxiv.org/abs/2203.02155 | 💼 LinkedIn: post on RLHF intuition | — |
| Sun | Project E scaffolding | — | 💼 LinkedIn engagement | — |

### Week 18
| Day | 🏗️/🛠️ (1 hr) | ⌨️ deep-ml (30) | 🛠️⌨️ extra deep-ml (30) | 📰 Papers (30) |
|---|---|---|---|---|
| Mon | 🏗️ DPO — read fully; DPO vs RLHF pros/cons matrix | DL: DPO objective | Extra DL | The Code + 1 abstract |
| Tue | 🛠️ CampusX LangGraph — tool calling; build 5 real tools for Project E | NLP: top-k / top-p sampling | Extra NLP | The Code |
| Wed | 🏗️ Reasoning models — DeepSeek R1 + test-time compute scaling; why RL-for-reasoning matters | DL: reward shaping | Extra DL | The Code + HF Papers |
| Thu | 🛠️ Agent memory — short-term vs long-term; **built-in persistence (v1.0)**; implement both | NLP: vector store as memory | Extra NLP | The Code |
| Fri | **Review** | — | — | — |
| Sat | **Project E** — add tools + memory + durable checkpointing | 📄 *DeepSeek R1* — https://arxiv.org/abs/2501.12948 | 💼 LinkedIn: Build Log on Project E progress | — |
| Sun | Project E + tests | — | 💼 LinkedIn engagement | — |

### Week 19
| Day | 🏗️/🛠️ (1 hr) | ⌨️ deep-ml (30) | 🛠️⌨️ extra deep-ml (30) | 📰 Papers (30) |
|---|---|---|---|---|
| Mon | 🏗️ Constitutional AI — write your own 10-rule constitution for a hypothetical assistant | DL: KL constraint | Extra DL | The Code + 1 abstract |
| Tue | 🛠️ CampusX LangGraph — multi-agent (supervisor, swarm, hierarchical); pick one | NLP: supervisor pattern | Extra NLP | The Code |
| Wed | 🏗️ Reasoning continued — implications for agent design (plan→act→observe→re-plan loops) | DL: harmlessness modeling | Extra DL | The Code + HF Papers |
| Thu | 🛠️ **MCP for real** — build an MCP server exposing Project E's tools via JSON-RPC; connect the agent. Add **HITL interrupt** on any high-stakes node. | NLP: MCP server design | Extra NLP | The Code |
| Fri | **Review** | — | — | — |
| Sat | **Project E polish** — observability (LangSmith), trajectory evals, **indirect-prompt-injection guardrail** (proxy that validates action impact) | 📄 *Constitutional AI* — https://arxiv.org/abs/2212.08073 | 💼 LinkedIn: post — *"I built my first MCP server and added HITL + an injection guardrail. Here's why this is the real agentic-security story in 2026."* | — |
| Sun | Project E final | — | 💼 LinkedIn engagement | — |

### Week 20 — REVIEW WEEK
| Day | Block |
|---|---|
| Mon | Re-read InstructGPT + DPO + R1 notes. Re-explain GRPO (from nanochat) in your own words. |
| Tue | Re-do 4 hardest deep-ml problems from cycle 5. |
| Wed | Write long-form note: *"Production agentic design in 2026 — LangGraph 1.0 durable state, MCP tools, and defending against indirect prompt injection."* 1500 words. This is an architect-level piece. |
| Thu | Publish + cross-post. |
| Fri | Audit Project E; freshen GitHub. **First real applications** — 3 dream EU companies, tailored. |
| Sat | 📄 *Toolformer* — https://arxiv.org/abs/2302.04761. 💼 LinkedIn: 15 DMs + 5 connections. |
| Sun | Rest. |

---

## Cycle 6 — Weeks 21–24: Frontier + GenAIOps / deployment / security

> 🏗️ Builder: LoRA/QLoRA/PEFT, SLMs (why smaller+specialized is winning in 2026), FlashAttention, and 2–4 frontier papers of your choosing from the past 30 days.
> 🛠️ User: **GenAIOps** — deployment (Docker, vLLM/Ollama for local, NVIDIA NIM), observability (LangSmith/Arize Phoenix/W&B), cost optimization, and the 2026 security stack (indirect prompt injection defenses, scoped tokens, proxy validation). CampusX **Docker for ML** for deployment basics.
> ⌨️ deep-ml: advanced — transformer-specific implementations from blank (attention, KV cache, sampling)
> 🛠️⌨️ Tools: none active — extra deep-ml
> 📰 Papers: frontier focus

### Week 21
| Day | 🏗️/🛠️ (1 hr) | ⌨️ deep-ml (30) | 🛠️⌨️ extra (30) | 📰 Papers (30) |
|---|---|---|---|---|
| Mon | 🏗️ LoRA — read; run a LoRA fine-tune (HF PEFT or Unsloth) on a small model | DL: impl scaled dot-product attn from blank | Extra DL — KV cache | The Code + 1 abstract |
| Tue | 🛠️ Deployment — Docker + FastAPI for an LLM app; vLLM vs Ollama for serving | NLP: batching / throughput | Extra NLP — serving | The Code |
| Wed | 🏗️ SLMs — why 2026 favors small+specialized; when to fine-tune vs RAG vs prompt | DL: low-rank decomposition | Extra DL — top-p sampling | The Code + HF Papers |
| Thu | 🛠️ Cost optimization — caching, prompt compression, model routing (LiteLLM, OpenRouter) | NLP: prompt caching | Extra NLP — observability | The Code |
| Fri | **Review** | — | — | — |
| Sat | **Project F start** — EU AI Act compliance agent: takes an ML system description, outputs risk classification (Article 6) + required documentation checklist. Built on LangGraph 1.0 with MCP + HITL. | 📄 *LoRA* — https://arxiv.org/abs/2106.09685 | 💼 LinkedIn: post — *"Three things every ML engineer should know about EU AI Act Article 6"* | — |
| Sun | Project F scaffolding | — | 💼 LinkedIn engagement | — |

### Week 22
| Day | 🏗️/🛠️ (1 hr) | ⌨️ deep-ml (30) | 🛠️⌨️ extra (30) | 📰 Papers (30) |
|---|---|---|---|---|
| Mon | 🏗️ FlashAttention — why it matters for serving cost | DL: impl multi-head attn from blank | Extra DL — flash-attention block diagram | The Code + 1 abstract |
| Tue | 🛠️ Security — OWASP LLM Top 10; **indirect prompt injection** deep dive; scoped-token pattern | NLP: injection patterns | Extra NLP — jailbreak detection | The Code |
| Wed | 🏗️ Reasoning frontier — pick 2 recent papers from huggingface.co/papers (last 30 days) | DL: beam search | Extra DL — temperature sampling | The Code + HF Papers |
| Thu | 🛠️ Observability — instrument Project F end to end (traces, cost, latency) | NLP: eval harness | Extra NLP | The Code |
| Fri | **Review** | — | — | — |
| Sat | **Project F** — implement the risk classifier core + documentation generator | 📄 *FlashAttention* (deeper re-read) — https://arxiv.org/abs/2205.14135 | 💼 LinkedIn: Build Log on Project F | — |
| Sun | Project F | — | 💼 LinkedIn engagement | — |

### Week 23
| Day | 🏗️/🛠️ (1 hr) | ⌨️ deep-ml (30) | 🛠️⌨️ extra (30) | 📰 Papers (30) |
|---|---|---|---|---|
| Mon | 🏗️ Frontier reading — 2 more recent papers | DL: impl KV cache from blank | Extra DL — speculative decoding | The Code + 1 abstract |
| Tue | 🛠️ Interview prep — write 8 STAR-format stories from your Amex work | — | — | The Code |
| Wed | 🏗️ Frontier reading — 2 more | DL: impl layer norm + RMSNorm from blank | Extra DL | The Code + HF Papers |
| Thu | 🛠️ Mock behavioral — record yourself answering 5 questions | — | — | The Code |
| Fri | **Review** | — | — | — |
| Sat | **Project F polish** — final flagship repo | 📄 *Tree of Thoughts* — https://arxiv.org/abs/2305.10601 | 💼 Application sprint — 10 tailored applications | — |
| Sun | Project F final | — | 💼 LinkedIn engagement | — |

### Week 24 — FINAL REVIEW WEEK
| Day | Block |
|---|---|
| Mon | Re-read all 6 cycle notes. Re-reading is how you compress for recall under interview pressure. |
| Tue | Polish all flagship repos. Final READMEs. Demo videos (nanochat's web UI makes a great demo). |
| Wed | LinkedIn final audit — Featured section, recommendations, banner, headline. |
| Thu | CV final audit — quantified impact, project links, EU-friendly format. |
| Fri | Direct-ask outreach to anyone in-network at target companies. |
| Sat | 📄 *Chain of Thought* — https://arxiv.org/abs/2201.11903. 💼 Application sprint — 15 applications. |
| Sun | Reflect. Plan the next 4 weeks of active interviewing. |

### Weeks 25–26 — Buffer / active interviews
You should be in interview loops with 3+ companies. If not, the bottleneck is almost always CV, LinkedIn, or application volume — not technical knowledge.

---

# ⌨️ Daily deep-ml schedule (30 min, Mon–Thu)

> **Why this gets its own protected block:** it was your weak area, and you skipped it when it was bolted onto the start of the main block. A fixed slot — plus treating skipping as not-an-option — is the fix. A weak area needs *more* protection, not less.

## How to use it each weekday (3 min setup, 27 min work)

1. Open https://www.deep-ml.com/problems
2. Filter **Category** = today's (below), **Difficulty** = your current cycle's
3. Pick the next unsolved problem touching the day's topic keyword; if none, any unsolved problem in that category/difficulty
4. Time-box **20 min**. If stuck, read the solution, then re-implement from a blank file in the remaining 7 min — that's where learning happens
5. Log it in `deepml-log.md` (date, problem, time, solved Y/N)

## Collections
Use deep-ml's **Collections** (https://www.deep-ml.com/collections) — topic-grouped sequences. Complete one per cycle where it matches. The badge is a useful forcing function.

## Daily category mapping

| Cycle | Mon | Tue | Wed | Thu | Difficulty |
|---|---|---|---|---|---|
| 1 (W1–4) | Linear Algebra | Machine Learning | Linear Algebra | Machine Learning | Beginner |
| 2 (W5–8) | Deep Learning (activations) | Machine Learning | Deep Learning (norms) | Machine Learning | Beginner→Intermediate |
| 3 (W9–12) | Deep Learning (attention, KV cache) | NLP (BPE, tokenization) | Deep Learning (positional enc, masks) | NLP (BM25, retrieval) | Intermediate |
| 4 (W13–16) | Deep Learning (RMSNorm, MoE) | NLP (embeddings, chunking) | Deep Learning (RL basics) | NLP (reranking, RAGAS) | Intermediate |
| 5 (W17–20) | Deep Learning (KL, reward, DPO) | NLP (tool schemas, agents) | Deep Learning (policy gradient) | NLP (sampling, MCP) | Intermediate→Advanced |
| 6 (W21–24) | Deep Learning (impl attn/KV cache from blank) | NLP (injection, serving) | Deep Learning (impl norms/beam search from blank) | NLP (evals) | Advanced |

## Friday & weekend policy
- **Friday:** no new problem — re-solve the week's hardest from blank. The real test.
- **Sat/Sun:** projects take priority; one bonus problem only if you finish early.

## When you hit a wall
- **Category exhausted at this difficulty** → promote difficulty, or rotate adjacent category
- **Problem taking 60 min** → stop at 20, read solution, re-implement from blank; the *slot* is fixed, the *problem* is negotiable
- **Solved but don't understand it** → read the problem's *learn* tab before moving on

## Two honest metrics (top line of `deepml-log.md` each cycle)
- **Skip count** — weekdays you did the block this cycle. Target 12/12; below 9/12 = red flag, re-protect the slot.
- **Solved-without-help count** — should trend up across cycles. If flat, you're moving difficulty too fast — slow down.

---

# 📰 Papers & latest updates (30 min, Mon–Thu)

## Newsletter — The Code (your pick)

You've chosen **The Code** (https://codenewsletter.ai/) as your single newsletter. It's a strong developer-facing source, published a few times a week, covering model releases, coding-tool and agent-framework updates, notable repos, and applied engineering news.

One honest note, since it changes how you should *use* the 30-min block: The Code leans toward the coding-tool and applied-engineering ecosystem (Cursor / Claude Code / Codex / agent frameworks / new repos) more than toward research papers. That's a fine fit for your architect goal and your Android-app tool track — but it means the newsletter alone won't feed the *research-depth* side that senior interviews also probe. So the daily 30-min structure below deliberately pairs The Code (for currency) with primary research reading (for depth). Don't let The Code become the *only* thing you read in this block, or your paper muscle atrophies.

Read The Code's email itself over coffee — it doesn't need to eat the 30-min block. Use the block for the structured reading below.

## Daily 30-min structure
| Day | Content |
|---|---|
| Mon | One arXiv abstract from the past week (from The Code's links if it surfaced one, otherwise huggingface.co/papers). 20 min read, 10 min note. |
| Tue | A deeper blog post — Lilian Weng (lilianweng.github.io), Sebastian Raschka (magazine.sebastianraschka.com), Anthropic Engineering, or LangChain's blog for v1.0 patterns. |
| Wed | Browse huggingface.co/papers weekly trending; read one paper's abstract+intro+conclusion. Triage skill. |
| Thu | Skim The Code's recent issues for tool/framework/repo updates relevant to your current cycle, then read the code or docs behind one of them. This is where The Code earns its place — it keeps your applied stack current. |

## Weekly paper (Saturday, 45 min)
Full 24-paper list in the *Paper reading list* section. One per weekend.

## Paper-note template (200 words, in a `papers/` folder in your portfolio)
1. **Problem** — in one sentence
2. **Idea** — the mechanism, in your words
3. **Evidence** — what experiments support it
4. **Use** — where you'd reach for it
5. **One open question** — what wasn't answered (the most important line)

---

# AI coding tools — project-based learning curriculum

## Philosophy (updated): hand-code your GenAI learning; use AI tools to ship real apps

The boundary is unchanged in spirit: your **GenAI portfolio and curriculum** — the flagship repos, the weekend projects, deep-ml, **nanochat** — stays hand-coded/hand-run in plain VS Code with no AI assistant. That's how the transformer/RAG/agentic fundamentals become genuinely yours, and it's what your interviewers will probe.

What's changed is the *tool track's projects*. Instead of throwaway CLIs, you'll use the AI coding tools to build **two real Android apps you'll actually use and ship to Google Play**:
- a **minimalist to-do list** (mobile-first personal task tracker)
- a **minimalist Android alarm clock** with a **lap button**

This is a strictly better learning vehicle: real shipping constraints (a Play listing, an app that has to actually work on your own phone every morning) force you to engage the tools far more seriously than a disposable script would. And it's honest about a truth of 2026 engineering — for a *new domain you don't already know* (native Android), AI tools are exactly where they earn their keep.

### Why this doesn't violate the hand-coding principle

Two reasons, and it's worth being explicit so the boundary stays clean:

1. **Different domain from your interview story.** Your GenAI credibility rests on transformers, RAG, and agents — all hand-built. Android/Kotlin is a *separate* skill you're learning partly as a tool-study vehicle and partly for your own use. Using AI to learn a new UI framework doesn't undercut "I built a ChatGPT clone from scratch."
2. **You're the reviewer, not the passenger.** The discipline that matters is understanding every line you ship. Even with the AI generating Compose boilerplate, you read, question, and own the result — the same critical-review muscle you apply at work with Copilot/Devin. If you find yourself shipping code you can't explain, that's the signal to slow down, not to abandon the approach.

**Keep them in separate repos** from your GenAI portfolio: `todo-android/` and `alarm-android/`, each clearly a personal-app project. Pin them if you like — two shipped Play Store apps is a credible signal of end-to-end delivery — but frame them honestly in interviews as "personal apps where I used AI tooling deliberately to learn native Android fast," not as hand-built-from-scratch work. That framing is both accurate and impressive.

## Scope
| Tool | In track? | Why |
|---|---|---|
| Claude Code | ✓ Month 1 (W1–5) | Already set up; CLI + agentic; good first study, and strong at scaffolding a whole project |
| OpenAI Codex | ✓ Month 2 (W6–10) | Terminal + IDE + Cloud; in ChatGPT Plus ($20/mo); rounds out the agent-CLI comparison |
| Cursor | ✓ Month 3 (W11–15) | Full IDE replacement; multi-file Agent mode; best tool for a cross-app polish + ship pass |
| GitHub Copilot | ✗ learn at work | You use it at Amex |
| Devin | ✗ learn at work | You use it at Amex |

## The modern Android stack (what you'll actually learn)

Both apps use Google's current recommended stack, so you learn it once and reuse it:
- **Language:** Kotlin (the only option for new apps; Compose requires it)
- **UI:** Jetpack Compose (declarative UI, Material 3)
- **State:** ViewModel + StateFlow
- **Storage:** Room (database) for the to-do list; DataStore (preferences) for alarm settings
- **IDE:** Android Studio (you've already set it up on Ubuntu via the tar.gz method per your notes — good, that avoids the Snap/Flatpak emulator friction)
- **Ship:** signed **Android App Bundle (.aab)** → Google Play Console

Free official grounding if you want it alongside the AI-tool work: **Android Basics with Compose** (developer.android.com/courses/android-basics-compose/course) and the Compose quick-start (developer.android.com/develop/ui/compose/setup).

## Structure: each tool-month builds toward a shipped app

**Month 1 — Claude Code (W1–5) → the to-do app.**
The to-do list is the right *first* app: it exercises the core stack end to end (Compose UI, a list, add/edit/delete, Room persistence, state) without OS-level complexity. Claude Code's plan-then-execute loop and whole-project scaffolding shine here for a greenfield app in an unfamiliar framework.
- Weeks 1–3 (features): set up the Android project; learn Compose basics through Claude Code (let it scaffold, then read and understand every composable); build the task list, add-task screen, Room storage, state with ViewModel.
- Week 4 (project): make it genuinely usable on your own phone — polish the UI to actually-minimalist, fix the real bugs you hit using it.
- Deliverable: a working to-do app on your phone + 300-word Claude Code reflection note.
- Docs: https://docs.claude.com/en/docs/claude-code/overview

**Month 2 — OpenAI Codex (W6–10) → the alarm clock app.**
The alarm clock is deliberately *harder* and a good second app: it pushes past pure UI into Android system integration — scheduling exact alarms (`AlarmManager`), a foreground service / notification for the ringing alarm, handling the device asleep, and a **lap button** (a stopwatch-style lap list, which is real state-management practice). Codex's spread across CLI, IDE, and Cloud gives you different angles on a more complex build.
- Weeks 1–3 (features): alarm data model + DataStore; the set-alarm UI; `AlarmManager` scheduling and the permission model for exact alarms; the ringing screen; the lap/stopwatch feature with its lap list.
- Week 4 (project): make it reliable enough to actually wake you up (the real test), handle edge cases (reboot persistence, Do Not Disturb).
- Deliverable: a working alarm+lap app on your phone + Codex reflection note.
- Docs: https://developers.openai.com/codex. Cost: included in ChatGPT Plus $20/mo (CLI + IDE + Cloud, rolling 5-hr windows) — confirm current pricing at the docs link.

**Month 3 — Cursor (W11–15) → polish both + ship to Play.**
By now both apps work but aren't launch-ready. This is exactly what Cursor's multi-file Agent/Composer mode is best at: coordinated cleanup across a codebase. Use it to refactor both apps to a consistent structure, add the launch essentials, and get them onto Play.
- Weeks 1–3 (features): use Composer for cross-file refactors; add app icons, a settings screen, dark theme, accessibility labels; write the Play listing assets; learn the release path — signing, building an `.aab`, the Play Console flow (developer account is a one-time ~$25 fee).
- Week 4 (project): ship. Submit both apps to Google Play. Even if review runs into the buffer weeks, the submission is the milestone.
- Deliverable: both apps live (or submitted) on Play + Cursor reflection note + the synthesized 3-tool interview narrative.
- Docs: https://cursor.com/docs

**Month 4 — freed (W17+).** Redirect the 30 min to extra deep-ml (your weak area). If a Play review kicks back a fix, that also lands here.

> **Scope discipline:** "minimalist" is load-bearing. The failure mode is feature-creep turning a 4-week app into a 4-month one and eating your GenAI study time. If an app isn't shippable by the end of its tool-month, cut features, don't extend the timeline — the tool-track is capped at 30 min/day and must never borrow from the main blocks.

## Reflection note template (per tool, ~300 words)
1. Interaction model — how you drive it
2. Strengths — concrete example from the app you built
3. Weaknesses — where it was confidently wrong (especially in an unfamiliar framework — Android is a good stress test for this)
4. Where it fits — what you'd reach for it for, and not

## The interview narrative
By Week 15 you've studied 3 tools deliberately, used Copilot and Devin at work, built your whole *GenAI* portfolio by hand (including nanochat), and shipped two real apps to Play using AI tooling in a domain you didn't previously know. The answer to *"How do you use AI coding tools?"* is now unusually strong:

> *"I draw a deliberate line. My GenAI fundamentals I built by hand in plain VS Code — including a from-scratch ChatGPT clone via Karpathy's nanochat — because I wanted that understanding to be genuinely mine. But for shipping in a domain I didn't already know, I lean on AI tooling hard and on purpose: I built and launched two Android apps to the Play Store — a to-do list and an alarm clock — using Claude Code, Codex, and Cursor, a tool per stage, native Android being new to me. Copilot and Devin I use daily at Amex too. So I can speak to all five from hands-on use, I know where each fits, and I know the difference between code I should own line-by-line and code I can delegate. That judgment — what to build by hand versus what to accelerate — is the actual skill."*

Every sentence is something you'll have genuinely done. Two shipped apps also quietly prove something a lot of senior candidates can't: that you take things all the way to *delivered*, not just *demoed*.

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

Read for the idea, not every equation. 30–45 min each. Note in a `papers/` folder using the 5-line template.

| # | Weekend | Paper | Track | Link |
|---|---|---|---|---|
| 1 | W1 | Attention Is All You Need | Builder | https://arxiv.org/abs/1706.03762 |
| 2 | W2 | BERT | Builder | https://arxiv.org/abs/1810.04805 |
| 3 | W3 | GPT-2 technical report | Builder | OpenAI cdn |
| 4 | W4 | GPT-3 / Few-Shot Learners | Builder | https://arxiv.org/abs/2005.14165 |
| 5 | W5 | Sentence-BERT | User | https://arxiv.org/abs/1908.10084 |
| 6 | W6 | RAG (original) | User | https://arxiv.org/abs/2005.11401 |
| 7 | W7 | Dense Passage Retrieval | User | https://arxiv.org/abs/2004.04906 |
| 8 | W8 | HyDE | User | https://arxiv.org/abs/2212.10496 |
| 9 | W9 | Llama 3 | Builder | https://arxiv.org/abs/2407.21783 |
| 10 | W10 | Self-RAG | User | https://arxiv.org/abs/2310.11511 |
| 11 | W11 | nanochat README + walkthrough (Karpathy) — read as this week's "paper" | Builder | https://github.com/karpathy/nanochat |
| 12 | W12 | Corrective RAG | User | https://arxiv.org/abs/2401.15884 |
| 13 | W13 | FlashAttention | Builder | https://arxiv.org/abs/2205.14135 |
| 14 | W14 | DPO | Builder | https://arxiv.org/abs/2305.18290 |
| 15 | W15 | Switch Transformers / MoE | Builder | https://arxiv.org/abs/2101.03961 |
| 16 | W16 | Reflexion | User | https://arxiv.org/abs/2303.11366 |
| 17 | W17 | InstructGPT / RLHF | Builder | https://arxiv.org/abs/2203.02155 |
| 18 | W18 | DeepSeek R1 (reasoning via RL) | Builder | https://arxiv.org/abs/2501.12948 |
| 19 | W19 | Constitutional AI | Builder | https://arxiv.org/abs/2212.08073 |
| 20 | W20 | Toolformer | User | https://arxiv.org/abs/2302.04761 |
| 21 | W21 | LoRA | Builder | https://arxiv.org/abs/2106.09685 |
| 22 | W22 | FlashAttention (deeper) or a 2026 serving-efficiency paper of your choice | Builder | huggingface.co/papers |
| 23 | W23 | Tree of Thoughts | User | https://arxiv.org/abs/2305.10601 |
| 24 | W24 | Chain of Thought | User | https://arxiv.org/abs/2201.11903 |

**Two "living" additions** (not fixed-date — read when they surface in The Code/HF Papers, likely Cycles 5–6):
- A current **reasoning-model** paper beyond R1 (the space moves monthly — pick the most-discussed one that quarter).
- A current **agentic-systems or MCP** paper — the production-agent literature is growing fast; grab whatever the field is citing when you reach Cycle 5.

The point of the two living slots is to force the habit you'll need on the job: reading *this quarter's* work, not just the canon.

---

# GitHub portfolio targets

By Week 24 your pinned section should be (quality over quantity — a complete small repo beats a half-finished ambitious one):

1. **`micrograd-extended`** — your micrograd build with softmax/cross-entropy extensions and a name generator. Full README.
2. **`prompt-context-toolkit`** (Project B) — composable prompt-pattern functions with context-window awareness; demonstrates the prompt-eng + context-eng skills that were your gaps.
3. **`nanochat-from-scratch`** (Project C) — your run through Karpathy's nanochat: tokenizer → pretraining → SFT → GRPO → inference → web UI, with a README documenting each stage, your loss curves, and the report-card metrics. **This is your headline repo** — it's the "scratch to served model" story that senior interviews probe, and the web UI makes a great demo video.
4. **`production-rag-toolkit`** (Project D) — hybrid retrieval + reranking + RAGAS evals + a golden question set with real numbers.
5. **`agentic-mcp-system`** (Project E) — LangGraph 1.0 multi-agent with MCP-served tools, durable checkpointing, HITL interrupts, an indirect-prompt-injection guardrail, and trajectory evals. This one screams "2026 architect."
6. **`eu-ai-act-compliance-agent`** (Project F) — risk classifier + documentation generator; catnip for EU recruiters.

Plus two **shipped Android apps** — `todo-android/` and `alarm-android/` — built during the tool-literacy track and launched to Google Play. Pin them if you like: two apps that are actually live is a rare, credible signal that you take things all the way to *delivered*. Frame them honestly (personal apps where you used AI tooling to learn native Android fast), and keep the three per-tool reflection notes alongside them as your record of the deliberate tool study.

Every repo: clean README (problem, architecture diagram, demo, eval numbers, design rationale), tests for non-trivial logic, and a "what I learned" section.

---

# Final notes

You lost a few weeks to life. That's genuinely fine — the plan is built in movable blocks precisely so a slow start costs nothing structurally. The only thing that would hurt is treating the delay as a reason to rush or skip the protected blocks. Start Week 1 today, at a normal pace.

Three failure modes to watch over the six months:

1. **Tutorial drift** — watching Karpathy is not the same as learning. The blank-file re-implementation (Thursdays and review weeks) is the actual learning. With nanochat especially: reading the code is necessary but not sufficient — the understanding comes from being able to explain each stage without the repo open.

2. **Stream imbalance** — the three streams compound when balanced. Skip Builder and your interviews go shallow; skip User and your portfolio looks academic; skip deep-ml (the old temptation) and you'll feel it in coding rounds. The fixed slots exist to stop exactly this.

3. **Career-track procrastination** — LinkedIn and applications stay awkward for about six weeks, then compound into recruiter inbound around Month 3. The awkwardness is the tax; pay it early.

Two things v5 added that are worth protecting specifically:
- **nanochat is the spine of Cycles 3–4.** Don't let RAG (which feels more "jobby") crowd it out. The from-scratch-to-served-model story is your single strongest technical differentiator, and almost no candidates have actually done it end to end.
- **The 2026 agentic-security angle** (indirect prompt injection, HITL, scoped tokens, MCP) is what separates an "architect" from a "someone who wired up LangChain." Lean into it in Project E and your Cycle 5 LinkedIn post.

Adjust dates when life happens. Protect the weekend project, the LinkedIn weekly cadence, the Friday review, and — above all — the deep-ml slot. Everything else is movable.

Good luck. See you in Berlin / Amsterdam / London / Paris / Dublin in six months.
