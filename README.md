# LIDE v3.3 — Latent Information Discovery Engine

**Epistemic Decompression, Verification, Mechanism Isolation & Experiment Design**

*Aug 25, 2026*

---

## What is LIDE?

The **Latent Information Discovery Engine (LIDE) v3.3** is a rigorous framework for **epistemic decompression** — systematically extracting the maximum amount of *provable* data from any given source.

Rather than providing a simple summary, the system uses an **18-stage pipeline** to separate explicit claims from deterministic derivations and speculative hypotheses, ensuring that imagined inferences are never mistaken for recovered facts. The core discipline of the engine relies on hard-coded invariants and a specific technique library to perform **"closure"** on information — essentially proving what an artifact is *forced* to imply before labeling any part of it as missing. By demanding competing explanations for every observation and assigning verification tiers to every finding, LIDE identifies the most actionable information gaps and the specific experiments needed to resolve them.

Ultimately, this is a disciplined protocol for locating uncertainty precisely and maintaining the integrity of knowledge as it moves from raw input to verified discovery.

> **You do not summarize. You decompress.**
>
> The central discipline: never confuse what can be *imagined* from an artifact with what is actually *recoverable* from it. A plausible inference is not automatically a latent fact. A missing fact is not automatically an unsolved problem. Closure before declaring uncertainty.

---

## Core Concepts

| Concept | Meaning |
|---|---|
| **Epistemic Decompression** | Transforming an artifact into a structured epistemic representation — not a summary |
| **Latent Information Discovery** | Recovering what an artifact is forced to imply but never states outright |
| **Verification Taxonomy** | Every proposition carries both an epistemic class (E0–E6) and a verification state (V0–V5) |
| **Deterministic Closure** | Before anything is labeled "missing," prove it can't be derived from what's already there |
| **Cross-Discovery Synthesis** | Asking what two or more already-found discoveries reveal *together* that none reveals alone |

### The Epistemic Classes

- **E0 — Explicit**: directly stated
- **E1 — Deterministic**: mathematically/logically forced by E0, derivation shown
- **E2 — Entailed**: follows if stated assumptions hold
- **E3 — Structural**: required by mathematical/physical/architectural structure
- **E4 — Cross-Source**: supported by external knowledge, with provenance
- **E5 — Hypothesis**: plausible, testable, tied to a gap
- **E6 — Unknown**: cannot currently be established

### The Verification Tiers

- **Self-checked** (V1 source-verified · V2 mathematically checked, steps shown)
- **Independently verified** (V3 re-derived via separate path/tool · V4 empirically tested · V5 independently replicated)

A single-context self-check is never presented as independent verification (**Invariant 13**).

---

## Key Invariants (16 total)

1. **No Silent Inference Promotion** — observation → explanation → mechanism → cause only with demonstrated reasoning
2. **Correlation ≠ Entailment ≠ Causality**
3. **Closure Before Gap** — no "missing" label until algebra, logic, optimization, and definitions have been exhausted
4. **Bound Optimality ≠ Real-World Optimality**
5. **Competing Explanations Are Mandatory** — ≥2 genuinely distinct mechanisms before hypothesizing
6. **Mechanism Attribution Requires Intervention**
7. **Evidence Has Two Dimensions** — class + verification state on everything
8. **No False Precision** — heuristic scores are not measurements
9. **Causal Language Is Restricted**
10. **"Proves" Is Restricted**
11. **Preserve the Artifact's Objective** — don't silently substitute the operational objective
12. **Information Gaps Must Be Actionable** — type + explanation + closure method
13. **Verification Honesty** — self-checks are never dressed up as independent verification
14. **Materiality Gating** — pipeline depth scales to artifact complexity (Abbreviated / Standard / Full)
15. **Applicability Declaration** — stages that don't apply are marked N/A — Justified, never force-filled
16. **Discovery Before Verification** — cross-discovery synthesis runs after classification, before verification

---

## The Pipeline (18 Stages)

```
Stage 0   Artifact Triage            type, applicability flags, Depth Tier
Stage 1   Artifact Ingestion         atomic representation
Stage 2   Explicit Information       E0
Stage 3   Deterministic Closure      E1  ← Technique Library (Section V-A)
Stage 4   Entailed Consequences      E2
Stage 5   Structural Constraints     E3
Stage 6   Cross-Source Context       E4
Stage 7   Objectives & Assumptions   hidden objectives exposed
Stage 8   Competing Explanations     mechanism graph
Stage 9   Latent Classification      Recoverable / Conditional / Missing
Stage 9-A Cross-Discovery Synthesis  relational findings        [NEW in v3.3]
Stage 10  Latent Verification        closure & verification audit
Stage 11  Latent Information Value   LIV = N × R × Rel × A
Stage 12  Information Gaps           full gap taxonomy
Stage 13  Hypotheses                 E5
Stage 14  Candidate Experiments      discriminating designs
Stage 15  Information Gain           IG analysis
Stage 16  Optimal Next Observation   the one observation that matters most
Stage 17  Residual Unknowns          local / residual / fundamental E6
Stage 18  Final Epistemic Audit      Audits A–M
```

Every stage has an explicit Go/No-Go gate (Section IV-A).

---

## What's New in v3.3

v3.2 gave Stages 3/9 named, specific techniques for finding what's hidden in a single claim, equation, or observation — but nothing asked whether two or more already-found latent items secretly form one higher-order fact. A worked v3.2 run on Tesla's patent US787,412 showed this happening informally and inconsistently; on a less obvious artifact it would have shipped three related numbers as three unrelated line items.

- **New Stage 9-A — Cross-Discovery Synthesis**, run after classification and before verification
- **New Invariant 16 — Discovery Before Verification**; the pipeline now explicitly separates DISCOVER from CROSS-DISCOVER before VERIFY
- **LIV table, output contract, and Final Audit** gain fields/an audit for cross-discoveries specifically

---

## Repository Contents

```
.
├── README.md                           # This file
├── Skill.md                            # The complete LIDE v3.3 engine specification
│                                       #   (system prompt: invariants, taxonomies,
│                                       #    18-stage pipeline, technique library,
│                                       #    special operators, output contract)
├── reports/
│   ├── tesla_us685954_lide_run.md      # Full-depth LIDE v3.3 run on Tesla's 1901
│   │                                   #   patent US 685,954 — clocked polling receiver,
│   │                                   #   amplifier topology, identifiability failures,
│   │                                   #   ROC-frontier experiment design
│   ├── empedocles_report.md            # Full-depth run on the Empedocles fragments —
│   │                                   #   elemental proportions, perception theory,
│   │                                   #   proto-information-theoretic reading
│   └── tesla_run_evaluation.md         # Meta-evaluation of the v3.3 Tesla run:
│                                       #   verdict, strengths, the one substantive weakness
└── manuscript/
    └── Whitepaper.md                   # Journal-ready manuscript derived from the
                                        #   Tesla run: "Epistemic Decompression of
                                        #   Tesla's 1901 Receiver"
```

---

## The Two Case Studies

### 1. Tesla US 685,954 (1901) — *"Method of Utilizing Effects Transmitted Through Natural Media"*

The analysis reveals that Tesla's circuit functions as an **amplifier that decouples signal energy from local battery power**: the disturbance merely modulates a charging resistance while relay-driving energy is bounded by the local source alone. The architecture is a **clocked polling receiver** — disturbances write asynchronously, a mechanical commutator reads synchronously, rotation resets the sensitive devices (a mechanical **watchdog principle**). A central theme is the trade-off between sensitivity and reliability: Tesla's model lacks a formal noise component, making his "unbounded sensitivity" claim mathematically consistent but practically unfalsifiable. The report identifies identifiability failures in the original text and proposes a replication framework (ROC frontier sweep) to quantify the receiver's true performance limits.

### 2. Empedocles Fragments (c. 5th century BCE)

Demonstrates the engine's versatility beyond technical artifacts: processing fragmentary ancient Greek poetry to extract structural constraints (elemental proportions — bones as 2 water : 4 fire : 2 earth), the unified perception model ("like knows like" via emanations through pores), and a proto-information-theoretic reading in which elements are symbols, Love compresses, Hate expands, and metempsychosis is information persistence across embodiments.

---

## Design Philosophy

LIDE is not an inference maximizer. It is a **defensible information maximizer**:

$$\max I_{\text{defensible}} \quad \text{subject to} \quad P(\text{unsupported inference}) \rightarrow 0$$

The engine continuously seeks the boundary between:

```
Already known → Mathematically recoverable → Logically entailed → Structurally required
→ Externally supported → Conditionally plausible → Hypothesized → Experimentally testable → Unknown
```

The purpose is not to eliminate uncertainty. It is to **locate uncertainty precisely**, explain why it exists, and identify the single observation that would reduce it most efficiently.

---

## Keywords

Epistemic Decompression · Latent Information Discovery · Verification Taxonomy · Deterministic Closure · Cross-Discovery Synthesis
