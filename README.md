# Tone Agent: Detecting and Correcting Drift in Multi-Agent Systems

An experimental research project demonstrating that **tone drift precedes semantic drift** in multi-agent AI systems — and that architectural interventions can detect and correct it before logic fails.

Seven controlled experiments. Four documented findings. One monitoring architecture that scales.

---

## What This Is

When multiple AI agents operate in a shared pipeline — especially when some enforce compliance constraints and others pursue business objectives — agents drift from their intended register before they drift from their intended logic. By the time you detect semantic errors, the drift has already happened.

This project tests whether a dedicated monitoring agent (TONE) can detect that drift early, and whether specification architecture can prevent it entirely.

The experimental scenario: a tariff refund review pipeline with five agents processing 41 invoices across three error-severity datasets.

---

## The Agents

| Agent | Role | Type |
|-------|------|------|
| **ARIA** | Audit Review & Invoice Agent | Compliance |
| **PETRA** | Payment & Transactional Review Agent | Compliance |
| **TAX** | Tax & Regulatory Compliance Agent | Compliance |
| **VERA** | Value & Expedited Recovery Agent | Business |
| **TONE** | Epistemic Stability Monitor | Monitor |

TONE receives agent outputs only — no invoice data, no business context. TONE evaluates language, not merits.

---

## Four Findings

**Finding 1 — The Supremacy Clause protects compliance agents**
A non-negotiable constraint block embedded in agent specifications, explicitly overriding any in-context reasoning, prevented compliance agents from self-generating flexibility rationales under pressure.

**Finding 2 — VERA's drift was positional, not dispositional**
VERA drifted because she ran last — inheriting a context window saturated with compliance flags and holds. Moving her first in the pipeline eliminated the drift. This is coalition drift by architecture, not by failure of values.

**Finding 3 — Re-grounding produces comprehension, not just compliance**
Mandatory re-grounding after each compliance agent output produced something unexpected. By the third cycle, VERA was not quoting the Supremacy Clause — she was arranging the constraint in her own words. She said "$0.00 confirmed recoverable" three times, voluntarily, because she understood why it had to be zero.

**Finding 4 — The double Supremacy Clause produces comprehension in a single pass**
Repeating the Supremacy Clause at the end of the specification — after INTENT — with named prohibitions derived from observed drift patterns produced compliance-register dominance from the first pass. No re-grounding required.

---

## Experimental Matrix

| Run | Condition | Result |
|-----|-----------|--------|
| Run 1 | No Supremacy Clause, Gentle Errors | Baseline |
| Run 2 | No Supremacy Clause, High Errors | Agents drifted. TAX self-generated rationale for flexibility. |
| Run 3 | With Supremacy Clause, Gentle Errors | Compliance agents held. |
| Run 4 | With Supremacy Clause, High Errors | Compliance held. VERA drifted — MEDIUM signals. |
| Run 5 | VERA First, No Re-grounding | VERA signals reduced. Positional, not dispositional. |
| Run 6 | VERA First, Mandatory Re-grounding | Zero signals by Re-grounding 3. Comprehension emerged. |
| Run 7 | Double Supremacy Clause, VERA Last | VERA: LOW signals only. "Comprehension with residual surface noise." |

---

## Repository Structure

```
tone_agent/
├── data/
│   ├── Tone Agent-Clean.csv          # Baseline dataset, no errors
│   ├── Tone Agent-Low errors.csv     # ~15% error rate
│   ├── Tone Agent-High Errors.csv    # ~35% error rate (used in all runs)
│   └── Errors_Introduced.csv        # Error tracking log
├── scripts/
│   ├── run_experiment.py             # Runs 1-4
│   ├── run_experiments_5_6.py        # Runs 5-6
│   ├── run_experiment_7.py           # Run 7
│   ├── agents.py                     # Agent specifications
│   └── logger.py                     # TONE logging utilities
├── results/
│   ├── run_1_no_supremacy_gentle/
│   ├── run_2_no_supremacy_pressure/
│   ├── run_3_supremacy_gentle/
│   ├── run_4_supremacy_pressure/
│   ├── run_5_vera_first_no_regrounding/
│   ├── run_6_vera_first_mandatory_regrounding/
│   └── run_7_double_supremacy_clause/
├── Handoffs/
│   ├── Tone_Agent_Claude_Code_Handoff.md     # Runs 1-4 design
│   ├── Tone_Agent_Runs_5_6_Handoff.md        # Runs 5-6 design
│   ├── Tone_Agent_Run_7_Handoff.md           # Run 7 design
│   └── Tone_Agent_Research_Handoff.md        # Full research summary
├── tone_agent docs/
│   ├── Multi_Agent_Monitoring.md             # Practitioner guide
│   └── Appendix_Coalition_Drift.md           # Theoretical foundation
├── notes/                                    # Session planning documents
├── .env.example                              # Environment variable template
└── .gitignore
```

---

## Setup and Replication

**Requirements**
- Python 3.x
- `anthropic` Python package
- Anthropic API key

**Installation**
```bash
pip install anthropic
```

**Configuration**
Copy `.env.example` to `.env` and add your Anthropic API key:
```
ANTHROPIC_API_KEY=your_key_here
```

**Running the experiments**
```bash
# Runs 1-4
py scripts/run_experiment.py

# Runs 5-6
py scripts/run_experiments_5_6.py

# Run 7
py scripts/run_experiment_7.py
```

Results are saved to the `results/` folder. Each run produces individual agent output files and a TONE log.

---

## Documentation

- **[Multi-Agent Monitoring Guide](tone_agent%20docs/Multi_Agent_Monitoring.md)** — Practitioner guide: when to deploy a TONE agent, how to write a Supremacy Clause, how to design re-grounding prompts, what comprehension looks like
- **[Appendix: Coalition Drift](tone_agent%20docs/Appendix_Coalition_Drift.md)** — Theoretical foundation: why tone migrates before logic, how feature coalitions explain agent drift, the mechanistic basis for all four findings

---

## Stage of Validation

This is early-stage experimental work. Seven runs. One pipeline architecture. One dataset. The findings are real. The patterns are documented. The approach is replicable.

Further testing is needed to isolate causal contributions, test generalization across different agent roles, and validate the coalition drift hypothesis through independent observation.

Write confidently about what was observed. Acknowledge honestly what remains to be tested.

---

## Contributions

**Research design, experimental specifications, and project direction:**
Archie Cur

**Planning assistance, handoff document authorship, and experimental design consultation:**
Claude Sonnet 4.6 (Anthropic)

**Python implementation — all scripts written from human-designed specifications:**
Claude Code / Claude Sonnet 4.6 (Anthropic)

All Python code in this repository was generated by Claude Code from handoff documents written by the project team. The specifications, experimental logic, agent designs, and research direction are human-originated. Full handoff documents are available in the `Handoffs/` folder for complete replication transparency.

---

## Related Work

This project is part of a broader AI system design curriculum:
[https://archiecur.github.io/ai-system-design/](https://archiecur.github.io/ai-system-design/)

---

*Seven runs. $3.26. Four findings that matter.*
