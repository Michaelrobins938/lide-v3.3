# Contributing to LIDE v3.3

## Philosophy

LIDE is a **specification-driven project**. The single source of truth is `Skill.md` — the complete v3.3 specification containing all 16 invariants, the epistemic taxonomy, the 18-stage pipeline, the artifact-type technique library, and the audit framework. Every contribution flows through that specification.

## Types of contributions

- **Specification changes:** Updates to invariants, taxonomies, stage procedures, or technique libraries → go to `Skill.md`
- **Case studies:** New full-depth artifact runs → go to `reports/`
- **Whitepapers:** Academic manuscripts derived from runs → go to `manuscript/`
- **Documentation:** README, ABOUT, TAGS updates → go to the relevant file
- **Assets:** Cover art, diagrams → go to `assets/`

## Process

### 1. Open an issue first

Before making any change, open an issue describing:
- What you want to change
- Why the change is needed
- Which invariant or specification section it affects

### 2. Make the change

Follow these rules:

- **Specification changes:** Update `Skill.md`. Add a CHANGELOG entry to the top of the file. Every entry must reference a gap number and describe the fix.
- **Report changes:** Reports must follow the output contract defined in `Skill.md`. Every proposition must carry an epistemic class and verification state.
- **Documentation changes:** Update the affected file and cross-reference any changed sections in `README.md`.

### 3. Verify the invariants

Before submitting, confirm that all 16 invariants remain satisfied. In particular:

- [ ] **Invariant 13 (Verification Honesty):** No self-check presented as independent verification.
- [ ] **Invariant 16 (Discovery Before Verification):** Cross-discovery sweep runs before verification stages.
- [ ] **Invariant 3 (Closure Before Gap):** All apparent unknowns have been closure-tested before being labeled missing.

### 4. Commit with a descriptive message

Use conventional commit format:

```
spec: add technique for [artifact type]
report: add [artifact] case study
fix: correct invariant [N] wording in Stage [X]
docs: update README [section]
```

### 5. Submit a pull request

Your PR should:
- Reference the issue it addresses
- Include all relevant changes in a single commit
- Pass the invariant verification checklist above

## What we do not accept

- Pull requests that add plausible inferences without epistemic class labels
- Changes that remove or weaken any of the 16 invariants
- Reports that present hypotheses as discoveries
- Tags not defined in `TAGS.md`

## Questions?

Open an issue and we will respond.

---

_Remember: you do not summarize. You decompress._