# LIDE v3.3 — Tag Taxonomy

This document defines the structured tag system for the LIDE project. Tags are used to classify artifacts, methods, stages, and publications for discoverability, cross-referencing, and domain mapping.

---

## Tag format

All tags use **kebab-case** lowercase. Tags may be combined with dots to indicate a composite concept (e.g., `epistemic-class-e0`, `verification-v2`).

---

## Domain tags

| Tag | Description | Related stages |
|---|---|---|
| `epistemic-decompression` | Core methodology: extracting what an artifact forces to be true | All |
| `latent-discovery` | Finding hidden structure inside explicit text | Stages 3, 9, 9-A |
| `verification-taxonomy` | V0–V5 state machine for evidence grading | Stages 10, 18 |
| `deterministic-closure` | Algebraic/logical derivation before declaring gaps | Stages 3, 12 |
| `cross-discovery` | Relational synthesis across multiple findings | Stage 9-A |
| `experiment-design` | Discriminating experiments with falsifiers | Stages 13, 14, 16 |
| `mechanism-isolation` | Separating competing explanations via intervention | Stage 8 |
| `artifact-agnostic` | Protocol applies to any artifact type | All |
| `historical-analysis` | Application to historical documents or artifacts | All (with N/A flags) |
| `patent-analysis` | Application to patent disclosures | Stages 0, 7, 8 |

## Method tags

| Tag | Description | Related stages |
|---|---|---|
| `epistemic-classes` | E0–E6 taxonomy of claim types | Stages 2–4, 17 |
| `information-value` | LIV scoring: N × R × Rel × A | Stage 11 |
| `closure-before-gap` | Exhaust derivable routes before labeling missing | Stages 3, 12 |
| `evidence-hygiene` | Every proposition carries class × verification coordinates | All |
| `anti-hallucination` | Invariants preventing plausible-inference-as-fact | All |
| `materiality-gating` | Depth scales to artifact complexity and consequence | Stages 0, 14 |
| `technique-library` | Artifact-type-specific named techniques (V-A) | Stages 3, 9 |
| `parameter-space-sweep` | Monte Carlo sweeps for deterministic bounds | Stage 14 |
| `stage-gate-protocol` | Go/No-Go conditions on every stage | All |
| `audit-framework` | Thirteen-point final epistemic audit | Stage 18 |

## Epistemic class tags

| Tag | Description | Meaning |
|---|---|---|
| `epistemic-class-e0` | Explicit | Directly stated by the artifact |
| `epistemic-class-e1` | Deterministic | Forced by E0; derivation shown |
| `epistemic-class-e2` | Entailed | Follows if stated assumptions hold |
| `epistemic-class-e3` | Structural | Required by mathematical/physical structure |
| `epistemic-class-e4` | Cross-source | Externally supported, with provenance |
| `epistemic-class-e5` | Hypothesis | Plausible, testable, tied to a gap |
| `epistemic-class-e6` | Unknown | Cannot currently be established |

## Verification state tags

| Tag | Description | Tier |
|---|---|---|
| `verification-v0` | Extracted/generated but unchecked | — |
| `verification-v1` | Verified against source | Self-checked |
| `verification-v2` | Mathematically/logically checked, steps shown | Self-checked |
| `verification-v3` | Re-derived via separate path/tool/agent | Independently verified |
| `verification-v4` | Empirically tested against real data | Independently verified |
| `verification-v5` | Independently replicated by a separate party | Independently verified |

## Stage tags

| Tag | Description | Primary output |
|---|---|---|
| `stage-0-triage` | Artifact type, applicability flags, depth tier | Type · flags · tier |
| `stage-1-ingestion` | Atomic artifact representation | Atomic units |
| `stage-2-explicit` | Directly stated information | E0 table |
| `stage-3-closure` | Deterministic derivation with named techniques | E1 table |
| `stage-4-entailed` | Conclusions if assumptions hold | E2 table |
| `stage-5-structural` | Requirements imposed by structure | E3 table |
| `stage-6-crosssource` | External knowledge with provenance | E4 table |
| `stage-7-objective` | Stated and hidden objectives, assumptions | Objective inventory |
| `stage-8-competing` | Competing mechanisms, isolation matrix | Mechanism graph |
| `stage-9-classification` | Recoverable / Conditional / Missing | Classification table |
| `stage-9a-crossdiscover` | Relational sweep across all items | D# cross-discoveries |
| `stage-10-verification` | Closure status and verification state | Verification audit |
| `stage-11-liv` | Latent Information Value scoring | LIV table |
| `stage-12-gaps` | Typed information gaps with closure methods | Gap taxonomy |
| `stage-13-hypotheses` | E5 with prediction and falsifier | Hypothesis table |
| `stage-14-experiments` | Discriminating experiments | Experiment table |
| `stage-15-infogain` | Information gain analysis | IG table |
| `stage-16-observation` | Optimal next observation | Observation spec |
| `stage-17-residual` | Local / residual / fundamental unknowns | E6 separation |
| `stage-18-audit` | Thirteen-point final audit | Audits A–M |

## Artifact-type tags

| Tag | Description | Technique library |
|---|---|---|
| `artifact-type-equation` | Mathematical expressions, equations, proofs | V-A.1 |
| `artifact-type-prose` | Paragraphs, prose claims, narrative | V-A.2 |
| `artifact-type-experiment` | Experimental reports, methods sections | V-A.3 |
| `artifact-type-observation` | Datasets, observations, measurements | V-A.4 |
| `artifact-type-mixed` | Composite artifact with multiple types | V-A.1–4 |

## Status tags

| Tag | Description |
|---|---|
| `status-stable` | Release is stable and document-complete |
| `status-development` | Under active development; API or spec may change |
| `status-deprecated` | Superseded; retained for historical reference |
| `status-na-justified` | Stage does not apply to this artifact (marked N/A — Justified) |

---

## Tag usage guidelines

1. **Always use the most specific tag.** Prefer `stage-9a-crossdiscover` over `latent-discovery`.
2. **Combine domain + method tags** when describing a process step (e.g., `epistemic-decompression` + `closure-before-gap`).
3. **Do not invent tags.** All tags must be defined in this document.
4. **Tag the artifact, not the tool.** Tags describe *what* is being analyzed or *what* method is applied, not *which software* performs the analysis.
5. **Preserve tag stability.** Once published, a tag's definition should not change without a CHANGELOG entry.