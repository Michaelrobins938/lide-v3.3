# About LIDE v3.3

## Mission

**LIDE — the Latent Information Discovery Engine** is a specification-grade epistemic framework for decompressing artifacts into structured, provenance-tagged representations of what they contain, what they force to be true, what they silently assume, and what remains genuinely unknown.

We do not summarize. We **decompress**.

## What this project is

LIDE v3.3 is a **complete, self-contained epistemic protocol** — a 18-stage pipeline with 16 hard-coded invariants, a seven-class epistemic taxonomy (E0–E6), a six-tier verification taxonomy (V0–V5), a latent-information-value scoring system (LIV), and a three-gate architecture (Triage → Cross-Discovery → Verification).

It ships with:

- **`Skill.md`** — the complete specification: invariants, taxonomies, stage-by-stage procedures, artifact-type technique library, output contract, and audit framework
- **`reports/`** — two full-depth case studies (Tesla patent US 685,954 and Empedocles fragments) plus a meta-evaluation
- **`manuscript/`** — a journal-ready whitepaper derived from the Tesla run
- **`assets/`** — cover art for presentation and distribution

## What this project is not

- **Not a summarizer.** LIDE does not compress an artifact into a shorter passage. It expands it into a structured epistemic map.
- **Not an inference engine.** LIDE does not generate new claims. It identifies what is already forced, entailed, or structurally required by the artifact itself.
- **Not a fact-checker.** LIDE does not verify claims against external truth. It grades the *verification state* of each claim and labels every proposition with its epistemic class and evidence path.
- **Not artifact-specific.** The protocol was designed to be artifact-agnostic: patents, scientific papers, poems, mathematical proofs, experimental reports, and philosophical arguments all pass through the same 18-stage machinery, with stages that do not apply marked **N/A — Justified**.

## Core epistemic principles

### 1. The discipline

> Never confuse what can be *imagined* from an artifact with what is actually *recoverable* from it.

Plausible inference is not a latent fact. A missing fact is not an unsolved problem. An observed association is not a mechanism. A mathematical expression that appears to contain an unknown may already contain enough information to solve it.

### 2. Evidence has two dimensions

Every proposition carries:
- **Epistemic class** (E0–E6): *what kind* of claim it is
- **Verification state** (V0–V5): *how strongly* it has been checked

These dimensions are independent. A high epistemic class does not imply high verification, and vice versa.

### 3. Closure before gap

Nothing is labeled "missing" until algebra, logic, optimization, and definitional reconstruction have been exhausted. A problem that has not yet been calculated is not necessarily an information gap.

### 4. Competing explanations are mandatory

Before any hypothesis is generated, at least two genuinely distinct mechanisms must be constructed, along with the intervention that separates them.

### 5. Verification honesty

LIDE typically executes as a single reasoning pass in a single context. A self-check is not an independent verification. This is labeled as such — `E1/V2 (self-checked)` means *here are the steps, re-check them yourself.*

### 6. Discovery before verification

A pipeline that verifies each finding as it is produced never notices that three separately-verified findings were one fact. Stage 9-A — Cross-Discovery Synthesis — runs after classification and before verification, searching for relational structure across all findings.

### 7. Materiality gating

Pipeline depth scales to artifact complexity and the consequence of getting a claim wrong. Running full 18-stage treatment on a two-paragraph abstract is not rigor — it manufactures structure the source does not support.

## The v3.3 signature

Version 3.3 introduced the **DISCOVER → CROSS-DISCOVER → VERIFY** architecture, separating the 18 stages into three structural blocks:

- **DISCOVER (Stages 0–9):** Decompress the artifact — extract explicit information, derive deterministic consequences, identify structural constraints, classify latent items.
- **CROSS-DISCOVER (Stage 9-A):** Synthesize relational findings across all classified items — the sweep that catches what single-item processing misses.
- **VERIFY (Stages 10–18):** Locate uncertainty precisely — verify claims, score information value, identify gaps, generate hypotheses and experiments, perform the final epistemic audit.

## Case studies

| Artifact | Domain | Key finding |
|---|---|---|
| Tesla US 685,954 (1901) | Technical patent | Clocked polling architecture; five-dimensional Pareto frontier; structural unidentifiability of stochastic sensitivity |
| Empedocles, Fragments (c. 5th c. BCE) | Humanistic / philosophical | Elemental proportions as structural constraints; proto-information-theoretic cross-discovery; honest heuristic limits |
| Tesla v3.3 meta-evaluation | Self-assessment | Protocol confirmed working; one weakness identified (artifact-contained vs. analyst-imported models) |

## License

LIDE v3.3 is released under the [MIT License](LICENSE). The specification (`Skill.md`) and all reports may be freely used, modified, and distributed. We ask only that derivative works preserve the epistemic discipline that makes LIDE what it is.