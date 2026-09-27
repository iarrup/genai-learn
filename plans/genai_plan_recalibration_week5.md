# GenAI Plan — Recalibration at Week 5

**This resets the plan from where you actually are** after 4 weeks, not where v6 assumed you'd be. It replaces the Cycle 1–2 week tables in v6 going forward; everything from Cycle 3 onward in v6 (nanochat, RAG, agentic, GenAIOps, the LinkedIn and Job Search guides, the paper list) still stands.

---

## Honest scorecard: first 4 weeks

| Track | Planned by end of W4 | You actually did | Verdict |
|---|---|---|---|
| 🏗️ Builder | micrograd, makemore 1–2, activations/BatchNorm started | micrograd, makemore 1, 2, **3 (done)** | **Slightly ahead** |
| 🛠️ User (Context Eng) | CE bootcamp well underway (~L5–6) | CE lectures 1, 2, 3 | **Behind pace** |
| ⌨️ deep-ml | beginner linear algebra + cosine sim | exactly that | **On track** |
| 🛠️⌨️ Tools | Claude Code → to-do app near shipping | to-do in testing + bonus CampusX Agentic-Claude-Code course | **On track + bonus** |
| 📰 Papers | 2 papers (Attention, Karpathy RNN) | 0 | **Gap** |
| 💼 LinkedIn | profile built, first post, ~50 connections | nothing (mental block) | **Gap** |
| 📰 Newsletter | daily skim of The Code | done daily | **On track** ✅ |

**Net:** Your technical core is healthy — arguably ahead on Builder. The two gaps are both **career/consolidation** items, not technical ones. That's the pattern to fix, because those two gaps are exactly what determines whether the technical work turns into a job.

---

## The recalibration logic (what I changed and why)

1. **Builder: don't slow down, but insert the missing consolidation.** You cleared makemore-3, so you go straight to backprop-ninja → attention. But you skipped both papers, and *Attention Is All You Need* is the one paper you should not reach the attention videos without having read. So it's now scheduled *into a weekday block*, not left as optional weekend reading you'll skip again.

2. **Context Engineering: stop treating it as a race.** Three lectures in four weeks tells me the weekend-adjacent pacing wasn't working for CE, OR the lectures are dense. Either way, I'm giving CE the full User track through the next cycle at a realistic ~2 lectures/week instead of pretending you'll catch up. It finishes when it finishes; RAG (Cycle 3) can absorb a one-week slip.

3. **Papers: move them out of the weekend.** You skipped both. The weekend paper slot competes with project work and loses. So one paper now moves into a **Wednesday Builder-adjacent 30-min slot** (replacing part of that day's newsletter block), where it's protected. One paper per week, not per weekend, and it rides *with* the Builder topic it supports.

4. **LinkedIn: the mental block is the real problem, so I'm shrinking the first step until it's too small to avoid.** The v6 plan said "build your whole profile in Week 1." That's exactly the kind of big scary task a mental block feeds on. New approach below: a 10-minute-a-day ladder where each rung is trivially small. You are not allowed to "build your LinkedIn profile." You are only allowed to do the one tiny thing that day.

---

## LinkedIn: the un-blocking protocol (replaces the old Week 1–2 LinkedIn plan)

The mental block is normal — a 15-year-dormant account plus "I have to present myself professionally" is genuinely aversive. The fix is not willpower; it's making each step so small that doing it is easier than avoiding it. **10 minutes, one rung per day.** Do not skip ahead even if you feel motivated — the point is to prove to yourself it's painless.

| Day | The ONE thing (10 min max) |
|---|---|
| W5 Mon | Just log in. Recover the password if needed. Close the tab. That's the whole task. |
| W5 Tue | Change your profile photo to a decent recent one. Nothing else. |
| W5 Wed | Write only the headline field. Use: `GenAI Architect @ Amex · RAG · Agentic AI · LangGraph`. Save. Done. |
| W5 Thu | Set the profile to private-while-building (Settings → Visibility). Close tab. |
| W5 weekend | Write the About section — 3 short paragraphs. Steal the template from v6's LinkedIn guide. This is the biggest single rung; it's on the weekend for that reason. |
| W6 Mon | Add your current Amex role: title, dates, 3 bullet points. |
| W6 Tue | Add education + one past role (2 bullets). |
| W6 Wed | Add 10 skills. Pin the top 3 (Generative AI, RAG, LLM). |
| W6 Thu | Turn profile back to public. You now have a real profile. |
| W6 weekend | Send 15 connection requests to current/former Amex colleagues (personalized note; template in v6 guide). |
| W7 onward | Rejoin the normal v6 cadence: 2 posts/week + engagement. Your first post is the "starting a 6-month deep dive" one — but now you have 6 weeks of real progress to point at, which makes it easier to write. |

If even the 10-minute rung feels blocked on a given day: do the *physical* action only (open the app, look at it, close it). Momentum matters more than output here.

---

## Recalibrated Cycle 2 — Weeks 5–8

> 🏗️ Builder: backprop-ninja (V5) → WaveNet (V6, light) → attention (V7) → tokenizer (V8) → open nanochat. **Attention Is All You Need paper is read alongside V7.**
> 🛠️ User: Vizuara Context Engineering, lectures 4 onward, ~2/week — finish the bootcamp by end of cycle.
> ⌨️ deep-ml: intermediate — Deep Learning (activations→attention topics) Mon/Wed, NLP/ML Tue/Thu.
> 🛠️⌨️ Tools: ship the to-do app (W5), then begin Codex → alarm app (W6+).
> 📰 Papers/newsletter: The Code daily; **one paper/week in the Wed slot** (not the weekend).
> 💼 LinkedIn: the un-blocking ladder above.

### Week 5 — backprop-ninja + ship the to-do app
| Day | 🏗️/🛠️ (1 hr) | ⌨️ deep-ml (30) | 🛠️⌨️ Tools (30) | 📰 Papers/news (30) |
|---|---|---|---|---|
| Mon | 🏗️ Karpathy V5 *backprop ninja* — first half | DL: sigmoid forward+backward | Claude Code: finish to-do app — fix the bugs you hit in testing | The Code skim |
| Tue | 🛠️ Vizuara CE Bootcamp L4 | ML: logistic regression | Claude Code: to-do app final polish for release | The Code skim |
| Wed | 🏗️ Karpathy V5 — second half; derive 3 gradients yourself | DL: chain rule 2-layer MLP | Claude Code: to-do reflection note (Claude Code strengths/weaknesses) | 📄 **Karpathy "Unreasonable Effectiveness of RNNs"** (the easier of the two you skipped — start here to rebuild the paper habit) |
| Thu | 🛠️ Vizuara CE Bootcamp L5 | DL: layer norm by hand | To-do app: begin the Play Store deployment (your first — go slow, follow the console steps) | The Code skim |
| Fri | **Review**: re-derive the hardest backprop-ninja gradient from blank; CE L4–5 notes | — | — | — |
| Sat | **To-do app: finish Play submission.** Then Project B (prompt+context library) start. | — | 💼 LinkedIn weekend rung (About section) | — |
| Sun | Project B iteration | — | 💼 LinkedIn: — (rest or overflow) | — |

### Week 6 — attention (V7) + Codex/alarm app begins
| Day | 🏗️/🛠️ (1 hr) | ⌨️ deep-ml (30) | 🛠️⌨️ Tools (30) | 📰 Papers/news (30) |
|---|---|---|---|---|
| Mon | 🏗️ Karpathy V7 *Let's build GPT* — first third (single-head attention) | DL: scaled dot-product attention by hand | **Codex M2 W1**: install; scaffold the alarm app; alarm data model + DataStore | The Code skim |
| Tue | 🛠️ Vizuara CE Bootcamp L6 | DL: attention mask basics | Codex: set-alarm UI; feel the ghost-text/CLI flow | The Code skim |
| Wed | 🏗️ Karpathy V7 — second third (multi-head, residual, layernorm) | DL: multi-head split+concat | Codex: `AlarmManager` scheduling + exact-alarm permissions | 📄 **Attention Is All You Need** — read alongside V7. This is the paper you must not skip; you're literally building the thing it describes. |
| Thu | 🛠️ Vizuara CE Bootcamp L7 | DL: positional encoding (sinusoidal) | Codex: the ringing screen (full-screen intent/notification) | The Code skim |
| Fri | **Review**: re-implement the attention block from blank; map it onto the *Attention* paper's diagram; CE L6–7 notes | — | — | — |
| Sat | Project B v2 | — | 💼 LinkedIn weekend rung (15 colleague connections) | — |
| Sun | Project B + README | — | 💼 LinkedIn: — | — |

### Week 7 — attention finish + tokenizer (V8) + open nanochat
| Day | 🏗️/🛠️ (1 hr) | ⌨️ deep-ml (30) | 🛠️⌨️ Tools (30) | 📰 Papers/news (30) |
|---|---|---|---|---|
| Mon | 🏗️ Karpathy V7 — final third (training loop, scaling); re-implement attention from blank | DL: causal mask | **Codex W2**: the lap/stopwatch feature + lap list (real state practice) | The Code skim |
| Tue | 🛠️ Vizuara CE Bootcamp L8 (or continue toward the end of the playlist) | DL: attention scaling (√d) | Codex: foreground service so the alarm survives backgrounding | The Code skim |
| Wed | 🏗️ Karpathy V8 *Tokenizer* — first half (BPE) | DL: BPE by hand | Codex: Cloud mode for a contained task (e.g. settings screen) | 📄 A recent tokenizer/BPE blog post or the SentencePiece paper abstract (light — you've earned an easy week) |
| Thu | 🛠️ Vizuara CE Bootcamp — finish; write your one-page CE summary doc | DL: multi-head attention impl | Codex: reboot persistence (reschedule alarms after restart) | The Code skim |
| Fri | **Review**: finish V8 (BPE deeply); confirm CE bootcamp complete | — | — | — |
| Sat | Project B v3 — package, README, push (portfolio repo). **Open the nanochat repo, read its README end-to-end.** | — | 💼 LinkedIn: first real post (the "6-month deep dive" post — now backed by real progress) | — |
| Sun | Project B finalize | — | 💼 LinkedIn: 5 substantive comments | — |

### Week 8 — REVIEW WEEK
| Day | Block |
|---|---|
| Mon | Re-watch the V7 attention block. Redo it from blank. Re-read the *Attention* paper's method section now that you've built it — it should read completely differently. |
| Tue | Re-do the 4 hardest deep-ml problems from this cycle. |
| Wed | Write long-form note: *"Context engineering — what the Vizuara bootcamp actually taught me."* 1000 words. |
| Thu | Publish + cross-post to LinkedIn (your 2nd post). **Codex/alarm-app check-in:** reliability pass — does it actually wake you up? |
| Fri | Audit Project B repo. Read the nanochat tokenizer + pretraining code to prep Cycle 3. |
| Sat | 📄 *RAG (original)* — https://arxiv.org/abs/2005.11401 (prep for Cycle 3 RAG). 💼 LinkedIn: reach 50 connections. |
| Sun | Rest. |

---

## From Cycle 3 onward: unchanged from v6

Everything after Week 8 in v6 still applies as written:
- **Cycle 3 (W9–12):** nanochat build (tokenizer→pretraining→inference) + RAG fundamentals (CampusX LangChain v1.0). Codex/alarm app wraps ~W10.
- **Cycle 4 (W13–16):** nanochat SFT+GRPO+serving + Advanced RAG. Cursor → polish + ship both apps to Play.
- **Cycle 5 (W17–20):** alignment/reasoning + agentic (LangGraph 1.0 + MCP). *Your bonus CampusX Agentic-Claude-Code course already gives you a head start here.*
- **Cycle 6 (W21–24):** frontier + GenAIOps/deployment/security.
- Plus the full LinkedIn rebuilding guide and Job Search re-entry guide (now partly front-loaded via the un-blocking ladder above).

The one-week CE slip is absorbed by the fact that you're ahead on Builder and did the Agentic-Claude-Code course early. Net calendar position: **on track.**

---

## Three things to hold onto

1. **Your technical engine works.** Four weeks in, you're ahead on the hardest track (Builder). Don't let the two gaps make you feel behind — you're not.
2. **The gaps are both avoidance-shaped, not capacity-shaped.** Papers and LinkedIn didn't happen because they were easy to defer, not because you ran out of time. The fixes above are structural (protected slots, tiny rungs), not "try harder."
3. **Ship the to-do app this week.** A shipped app on Play — even a tiny one — is a bigger confidence and portfolio unlock than another week of study. Get it over the line, then let that momentum carry into the LinkedIn ladder.
