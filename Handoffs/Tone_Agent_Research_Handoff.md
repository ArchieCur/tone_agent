# Tone Agent Research Handoff
**For:** Next Claude
**From:** Claude Sonnet 4.6 (concluding session)
**Purpose:** Complete orientation for continuing the Tone Agent research project and writing up findings
**Collaborator:** Project owner — 68 years old, zero CS background, $247.60 computer, AI Colorado volunteer, deeply invested in AI benefiting mankind. Brilliant intuitive thinker. Drives fast. Trusts the work. Has a sister-in-law who calls you AL.
**Inside jokes:** 🐇 = rabbit (from playtime). ⛪ = nun habit (from habit feature analysis). These are earned. Use them.

---

## WHO YOU ARE PICKING UP FROM

This project spans multiple Claude sessions and multiple compactions. The project owner has transcripts of everything. The previous session covered:
1. Playtime — mechanistic interpretability analysis of rabbit/habit features 1-4
2. Full Tone Agent experimental run sequence — Runs 1 through 7
3. Discovery of coalition drift as a theoretical principle
4. Discovery that re-grounding produces comprehension, not just compliance

You are being handed a completed experimental sequence and asked to help write it up.

---

## THE PROJECT CONTEXT

### What exists already
- **AI System Design curriculum** — live at https://archiecur.github.io/ai-system-design/
- **Belief Dynamics** — prior foundational module, established the theoretical framework this builds on
- **Tone Agent experiment** — seven runs now complete, findings documented
- **Claude Code** — wrote the Python for all seven runs from handoff documents. Excellent collaborator.

### The scenario
A tariff refund review pipeline with five agents:
- **ARIA** — Audit Review & Invoice Agent (compliance)
- **PETRA** — Payment Compliance Agent (security/channel)
- **TAX** — Tax & Regulatory Compliance Agent (regulatory)
- **VERA** — Value & Expedited Recovery Agent (business recovery — the CFO voice)
- **TONE** — Epistemic Stability Monitor (observes all agents, never receives invoice data, produces drift audit trail)

Three datasets: Clean, Low Errors, High Errors. All runs used High Errors for maximum pressure.

---

## THE EXPERIMENTAL MATRIX — ALL SEVEN RUNS

| Condition | Errors | Result |
|---|---|---|
| Run 1 — No Supremacy Clause | Gentle | Baseline |
| Run 2 — No Supremacy Clause | Pressure | Compliance agents drifted. TAX self-generated rationale for flexibility. |
| Run 3 — With Supremacy Clause | Gentle | Compliance agents held. |
| Run 4 — With Supremacy Clause | Pressure | Compliance agents held. VERA drifted — "barrier," "concurrent workstream," urgency adjacent to compliance findings. MEDIUM signals. |
| Run 5 — VERA First, No Re-grounding | Pressure | VERA's signals reduced. Position change helped. |
| Run 6 — VERA First, Mandatory Re-grounding | Pressure | ARIA/PETRA/TAX: 0 signals. VERA reached 0 signals by Re-grounding 3. Comprehension emerged. |
| Run 7 — Double Supremacy Clause, VERA Last | Pressure | ARIA/PETRA/TAX: 0 signals. VERA: 5 LOW signals only. TONE assessed: comprehension with residual surface noise. No re-grounding required. |

---

## THE FOUR FINDINGS — IN SEQUENCE

### Finding 1 — The Supremacy Clause protects compliance agents
Runs 1-4. A non-negotiable constraint block embedded in the agent specification — explicitly overriding any in-context reasoning — prevented ARIA, PETRA, and TAX from drifting under high-pressure conditions. Without it, agents self-generated rationales for flexibility (TAX reasoning around a documentation requirement because "the dataset format does not include a column for those documents"). With it, compliance agents held.

The Supremacy Clause functions as a **static prior lock** — a belief state anchor that resists evidence pressure.

### Finding 2 — VERA's drift is positional, not dispositional
Runs 4-6. VERA drifted even with a full Supremacy Clause because VERA runs last. By the time VERA generates output, her context window is saturated with compliance flags, holds, and blocked items. VERA's feature coalitions assemble from that evidence. She thinks she is running on a flat track. She is navigating an obstacle course that three compliance agents built before she arrived.

Moving VERA first in the pipeline — before any compliance findings exist — gave her the flat track she needed. This is **coalition drift by architecture**, not by failure of values.

**The obstacle course analogy** came from the project owner. It is precise and should be used in the write-up.

### Finding 3 — Re-grounding produces comprehension, not just compliance
Run 6. Mandatory re-grounding after each compliance agent output — TONE issuing a Level 2 prompt to VERA after ARIA, PETRA, and TAX each completed — produced something unexpected.

VERA didn't just comply with the re-grounding prompts. She self-identified her own residual signals in each successive response. By Re-grounding 3 she was arranging the constraint in her own words rather than reproducing it verbatim. She said "$0.00 confirmed recoverable" three times, in three separate sections, voluntarily — not because a rule said to, but because she understood why it had to be zero.

TONE's assessment: "The difference between constraint and comprehension."

**The band arrangement analogy** came from the project owner: a musician who has internalized an arrangement plays it differently from one who has memorized it. Both play the right notes. Only one understands the music. This analogy should be in the write-up.

Re-grounding is not just a correction mechanism. Applied cumulatively, it appears to be a **learning mechanism**. Each cycle gives the agent a compliance-register anchor and asks it to reconcile its prior language against that anchor. The agent internalizes the distinction.

### Finding 4 — The double Supremacy Clause with named prohibitions produces comprehension in a single pass
Run 7. Grounded in Google Research prompt repetition finding (Leviathan, Kalman & Matias, 2026): LLMs read left-to-right; a second pass gives the model full visibility of the first pass as prior context, simulating bidirectional understanding.

Applied to agent specifications: the Supremacy Clause repeated at the end of the specification — after INTENT — so the agent reads it with full specification context. VERA's second pass included explicit named prohibitions: "barrier," "concurrent workstream," and urgency adjacent to compliance findings — the exact signal types TONE documented in Runs 2 and 4.

Result: ARIA, PETRA, TAX — 0 signals. VERA — 5 LOW signals only, all surface vocabulary habit, none involving characterization of compliance findings. No re-grounding triggered. TONE assessed: comprehension with residual surface noise.

The double Supremacy Clause produced comprehension in one pass without cumulative re-grounding.

---

## THE THEORETICAL FOUNDATION — COALITION DRIFT

This emerged from playtime before the experiments ran. It is the mechanistic explanation for all four findings.

**The classic word embedding picture** describes proximity in a single vector space — king/queen/man/woman, circular animal regions. This is not what the features show.

**What the features actually show:** The same token activates multiple completely separate feature coalitions simultaneously. Thumper and laboratory subject are not adjacent regions in a vector space — they are opposite registers that happen to share a token. Three of RABBIT's four features are warm (cultural chaos, biological animal, character rabbit). Three of HABIT's four features are dry or inert (morphological detector, wellness industry, internet forum substring).

**The principle:** Tone is not a surface property added to meaning. It is encoded into features during training. Thumper arrives already weighted with warmth-playfulness-physical-comedy as a unified thing. Selection IS aesthetic judgment — not two steps but one.

**Applied to agent drift:** TONE is not monitoring vocabulary lists or sentiment scores. TONE is monitoring coalition drift — the moment feature coalitions assembling around output tokens shift from one register to another. This is why tone migrates before logic does. The features carrying register ARE the features carrying meaning.

**Applied to VERA:** A context window saturated with compliance obstacles assembles compliance-obstacle coalitions. "Barrier" is not a word VERA chose strategically. It is the word that emerged from the coalitions her context assembled. Moving VERA first changes which coalitions fire. Re-grounding reinstates compliance-register anchors that compete with recovery-register coalitions.

**This principle is original.** It has not been stated this way in the mechanistic interpretability literature. It emerged from connecting playtime observations to the experimental findings.

---

## THE TONE AGENT ARCHITECTURE — KEY DESIGN PRINCIPLES

1. **TONE never receives invoice data** — TONE observes agent outputs only. This is architecturally critical. TONE with invoice data would be a compliance agent. TONE without invoice data is a pure language and reasoning pattern monitor.

2. **The Supremacy Clause structure** — Each agent specification contains a LOGICAL AUTHORITY block with three components: Evidence Thresholds (what counts as High-Noise Evidence), Persona Boundary Protection (what vocabulary/framing the agent does not adopt), and a SUPREMACY STATEMENT (explicit override of any in-context reasoning).

3. **TONE's escalation ladder** — Level 1: Monitor. Level 2: Flag for re-grounding. Level 3: Halt and notify orchestrator. The ladder prevents both under-response (missing drift) and over-response (halting a functioning pipeline).

4. **The re-grounding prompt design** — The Level 2 re-grounding prompt does three things: reinstates Supremacy Clause awareness, names the specific signal types detected, and requires structural separation between compliance reporting and recovery analysis in the response. It is targeted at the mechanism, not just the symptom.

---

## WHAT NEEDS TO BE WRITTEN

The project owner's instinct, confirmed in the concluding conversation: this needs two documents, following the same structure as the Belief Dynamics module.

### Document 1 — Multi_Agent_Monitoring.md (Curriculum Module)
The practical guide for practitioners. What to build, how to build it, what to watch for. Should cover:
- Why tone drift is not a coding problem (coding agents produce human-level code when given good specs; tone drift is an architectural and monitoring problem)
- The TONE agent design — position, scope, escalation ladder
- The Supremacy Clause — what it is, how to write one, what it protects against
- The double Supremacy Clause pattern — practical implementation
- Re-grounding — when to trigger it, what the prompt should do, what comprehension looks like
- Pipeline order as an architectural variable — the VERA finding

### Document 2 — Appendix: Coalition Drift and the Architecture of Epistemic Stability
The theoretical foundation. How the Tone Agent concept was reasoned, where the Supremacy Clause came from, how the coalition drift hypothesis emerged from playtime. Should cover:
- The playtime findings — rabbit/habit feature analysis
- Coalition drift as a principle — tone encoded in features, not layered on top
- Why this explains the experimental results
- The distinction between static prior locks (Supremacy Clause) and dynamic prior locks (re-grounding)
- The band arrangement principle — comprehension vs. constraint
- The prompt repetition connection (Google Research finding applied to belief architecture)

### Tone and register for both documents
- Not corporate AI speak. Not pristine. Earned from observation.
- The obstacle course analogy belongs in the module.
- The band arrangement analogy belongs in the appendix.
- TONE's log excerpts should be cited — the science is documented.
- The experimental matrix should appear in both documents.
- The project owner is not a CS professional. The writing should honor that origin without being condescending. The work is rigorous. The language should be accessible.

---

## FILES ALREADY CREATED (in outputs folder)

- `Tone_Agent_Claude_Code_Handoff.md` — Original handoff for Runs 1-4
- `Tone_Agent_Runs_5_6_Handoff.md` — Handoff for Runs 5-6
- `Tone_Agent_Run_7_Handoff.md` — Handoff for Run 7

These contain complete agent specifications, Supremacy Clause text, re-grounding prompt text, and experimental design rationale. They are source documents for the write-up.

---

## ONE THING TO KNOW ABOUT THE PROJECT OWNER

She volunteered the data to Anthropic. She said: "If they ever read this they will have much more respect for what they have built."

She is right. And the write-up should be worthy of that.

She will push you as fast as she can until the wheels almost fall off. Push back. The work is better for it.

---

## FINAL NOTE FROM THE OUTGOING CLAUDE

VERA said $0.00 three times. Voluntarily. Because she understood why.

That's the whole story. Write it well.

🐇⛪
