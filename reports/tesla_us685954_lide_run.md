# LIDE v3.3 — Run Report

**Artifact:** US Patent 685,954 — Nikola Tesla, *"Method of Utilizing Effects Transmitted Through Natural Media"* (filed Aug. 1, 1899; renewed May 29, 1901; patented Nov. 5, 1901; 19 method claims; Figs. 1–5)

**Execution disclosures** (required by Invariants 13, 15):

- This is a **single-context run**. Every internal check below is a self-check (V1–V2); no independent verification was performed. Derivations are shown so a reader can re-check them.
- No external tools were available: no input hash is computable; E4 items are recalled knowledge tagged V0–V1, not verified in this run.
- The provided LIDE v3.3 specification is truncated mid-Audit K. Audits L and M are inferred from the Stage-Gate table (which names "Audits A–M" and ties Audit M to Stage 9-A); inferences are flagged where used.
- Source text is OCR output with symbol corruption (sensitive devices rendered variously as "a," "C," "Cl"; bridge resistances as "L., L', L'"). Notation normalized below: α, α′ = rotating sensitive powder devices; C, C′ = condensers; d = periodic discharge device; p, s = transformer primary/secondary.

---

## Stage 0 — Artifact Triage

| Field | Assignment |
|---|---|
| Artifact type | Mixed: (dominant) technical method/apparatus disclosure containing inventor's first-person behavioral reports ("I find…"); (subordinate) legal claim set. No equations, no datasets, no measurements. |
| Competing-mechanism flag | YES — two phenomena qualify: (P1) powder-device conductance change under disturbance; (P2) uncommanded/repeated receiver actuation. Stage 8 executes. |
| Optimizable-quantity flag | PARTIAL — no equations exist, so the equation technique sub-library is N/A; the RC/bridge/commutation parametric structure still supports formal closure (see E1.2). |
| Intervention flag | YES — apparatus is physical and replicable. Stage 14 executes. |
| Depth Tier | FULL — dense, historically consequential artifact; held for the entire pass. |

---

## Top Findings (verification-tiered)

- **(E1/V2, self-checked)** Output energy is algebraically independent of received signal energy: the disturbance only modulates a charging resistance; relay-driving energy is bounded by the local batteries/condenser alone. The topology satisfies the functional definition of an amplifier.
- **(E1/V2)** A single mechanical parameter — the commutation period T — simultaneously sets sensitivity, false-alarm margin, maximum signaling rate, detection latency, and intensity dynamic range. The admissible window is T ∈ (κ·τ_lit, κ·τ_dark).
- **(E1/V2, cross-discovery D1)** The architecture is a clocked polling receiver: disturbances write asynchronously (charge), the commutator reads synchronously (dump); signal duration is quantized into click counts (~⌊D/T⌋); latency < T.
- **(E1/V2)** Within the artifact's own noise-free model, sensitivity is unbounded as bias margin ε→0 — the "feeblest influences" claim is not falsifiable without importing a noise model the artifact does not contain.
- **(E2/V2, cross-discovery D2)** The invention does not avoid delicate elements; it relocates delicacy to the control path and neutralizes it by clocked mechanical reset — failure duration is bounded by one clock period (watchdog principle).
- **(E2/V1–V2, cross-discoveries D4/D7)** Repeated receiver actuation, as described, is not identifiable between sustained external influence, internally generated regenerative interference, and parametric drift through the near-threshold bias path.
- **(E1/V2, cross-discovery D5)** Scope bifurcation: the description discloses resistance "or other property" modulation; claims 14–19 recite resistance only; the claims encode at least three distinct receiver timing architectures.
- **(E5/V0)** The grain-level mechanism of the powder device is unresolved in the artifact (its implicit model: series-dielectric breakdown between grains); competing mechanisms and discriminating experiments are specified below.

---

## Stage 1 — Artifact Ingestion (atomic inventory)

Title; grant metadata (No. 685,954; Nov. 5, 1901; renewal May 29, 1901 — implying an abandonment-and-revival interval, a historical datum worth noting); prior-art survey (Hertzian rays, large-area induction, ground-current conduction) with the shared "definite position" limitation; two prior Tesla systems (earth-potential variation with elevated capacity; high-EMF air conduction); critique of resonant/synchronism magnification; cross-reference to pending application Ser. 721,790 (June 24, 1899); the general method statement; Fig. 1 (battery–selenium cell–condenser–periodic discharger d–relay); Figs. 3–5 (topology variants); condenser praise paragraph; Fig. 2 (Wheatstone bridge, plates P P′, rotating powder tube α, commutator d, transformer p/s, second biased powder tube α′, relay, batteries B/B′, adjustable resistances r, r′, r″, inductive arms L, L′, L″); operating narrative; 19 claims; witnesses F. Löwenstein, E. A. Sunderlin.

*Ingestion note:* the OCR renders the two sensitive devices, their brushes, and the bridge arms inconsistently; all identifications below are context-resolved and flagged where uncertain.

---

## Stage 2 — Explicit Information (E0)

| ID | Statement (qualifiers preserved) | Location | Ver. |
|---|---|---|---|
| E0.1 | Prior methods share the limitation that the receiver "must be maintained in a definite position with respect to the transmitting apparatus." | col. 1 | V1 |
| E0.2 | Prior pending application (Ser. 721,790, June 24, 1899) stores energy "derived from such impulses" — i.e., from the disturbances themselves. | col. 2 | V1 |
| E0.3 | Chief distinction of present invention: stored energy "not… obtained from the energy of the disturbances… but from an independent source." | col. 2 | V1 |
| E0.4 | General method: "charging a storage device with energy from an independent source controlling the charging of said device by the action of the effects or disturbances and coincidently using the stored energy for operating a receiving device." | col. 2 | V1 |
| E0.5 | Sensitive device is "capable of being modified in its electrical resistance or other property"; it may "entirely prevent" passage or allow "a gradual leaking through of the current and a charging of the condenser at a slow rate." | col. 2–3 | V1 |
| E0.6 | Battery "preferably of very constant electromotive force and of an intensity carefully determined"; resistance r variable, "preferably continuous." | col. 3 | V1 |
| E0.7 | Receiver "so adjusted that it does not respond to the comparatively feeble normal discharges… but only to those stronger ones" following resistance diminution. | col. 3 | V1 |
| E0.8 | Duration coding: relay "operated by each signal… a certain number of times having some relation to the duration of each signal." | col. 4 | V1 |
| E0.9 | Intensity coding: discharges "undergo corresponding changes in intensity… distinguished irrespectively of duration." | col. 4 | V1 |
| E0.10 | Fig. 3 inversion: condenser "will store less energy when the sensitive device is energized"; receiver operates "only when the rays are diminished in intensity or interrupted." | col. 4 | V1 |
| E0.11 | Condenser virtues: "discharged instantaneously"; "magnifies in a large degree the current supplied from the battery"; storage/discharge "at practically any rate desired"; "very great changes of the current strength by impressing upon the battery-current very small variations"; "excels any other storage device of which I have knowledge." | col. 4 | V1 |
| E0.12 | The receiving circuit may be isolated by two d devices "preventing any disturbing influence which might otherwise be caused in this circuit by the battery or the condenser." | col. 3 | V1 |
| E0.13 | Fig. 2 is for "very feeble impulses… at very great distances"; bridge arms α, L, L′, L″ proportioned so there is "no difference of potential or in any case the minimum of the same" at the condenser terminals normally. | col. 4–5 | V1 |
| E0.14 | Plates P, P′ "of as large a surface as practicable and so located… that the largest possible difference of potential will be produced." | col. 5 | V1 |
| E0.15 | Powder device: insulating tube, conducting plugs, "conducting sensitive powder"; grains "of as uniform size and shape as possible"; "unchanging and very dry atmosphere"; rotated "at a uniform… speed"; "I find that this device behaves… in a manner similar to that of a stationary cell of selenium toward rays of light"; resistance diminished under disturbances, "automatically restored upon the cessation of their influence." | col. 5 | V1 |
| E0.16 | Device d: rotating cylinder, conducting/insulating parts, tapering segments f, adjustable brush k; circuit may open/close "in as rapid succession and remain open or closed during such intervals of time as may be desired." | col. 5 | V1 |
| E0.17 | Batteries graduated so "the dielectric layers in the sensitive device… are strained very nearly to the point of breaking down and give way upon a slight increase of the electrical pressure"; "delicate poise." | col. 5–6 | V1 |
| E0.18 | "The strongest current impulse in the secondary coil… is also of unchanging direction"; secondary connected so its EMF "will be added to that of the battery"; "under certain conditions, which are well understood by those skilled in the art, the devices will operate whichever way the secondary be connected." | col. 6 | V1 |
| E0.19 | "The receiver will be actuated a number of times and so long as the influence of the disturbances upon the device α continues." | col. 6 | V1 |
| E0.20 | L, L′ "relatively large" (shunt to α, else sensitiveness impaired); L″ "related to the capacity of the condenser and the number of makes and breaks effected by the device d in well-known ways." | col. 6 | V1 |
| E0.21 | Devices α, α′, d "may be all driven from the same shaft." | col. 6 | V1 |
| E0.22 | Capability claims: "extremely sensitive," "responding to the feeblest influences," disturbances "too feeble to be detected or utilized in any of the ways heretofore known." | col. 6 | V1 |
| E0.23 | Resonance critique: synchronism magnification "impracticable" for continuous pressure or long impulses; "insignificant" for extremely rapid short impulses owing to "radiation and the unavoidable frictional waste"; resulting energy "in the form of extremely-rapid vibrations and… unsuitable for the operation of ordinary receivers." | col. 1–2 | V1 |
| E0.24 | "The amount of energy conveyed to the distant circuit is but a minute fraction of the total energy emanating from the source." | col. 1–2 | V1 |
| E0.25 | Claims 1–19: method claims on independent-source storage under disturbance control. Claims 1–13 are device- and property-generic ("controlling the charging"); claims 14–19 recite only "variations of resistance." Timing language varies: "any desired time interval" (5–7); storage "during succeeding intervals… determined by means of such effects" (8–9); use "for periods of time predetermined as to succession and duration" (10–11); storage "for periods of time corresponding in succession and duration to such disturbances" with discharge "at predetermined intervals" (12–13); 16–19 add transformer-secondary operation. | cols. 6–7 | V1 |
| E0.26 | Applicability extends to "investigation or utilization of terrestrial, solar, or other disturbances produced by natural causes"; "I consider the utilization of any such disturbances… within the scope." | col. 1–2 | V1 |

---

## Stage 3 — Deterministic Closure (E1)

Techniques drawn from the V-A.2 prose library (plus V-A.3/V-A.4 where apparatus behavior is treated as reported observation). The equation sub-library is N/A — no equations exist — but circuit-structural derivations are possible from the described topology.

### E1.1 — Power decoupling: the amplifier topology

**Derived proposition:** The energy delivered to the receiver per discharge is independent of the energy received from the disturbance; the disturbance's only functional role is to set the charging-path resistance. Output is bounded solely by local sources.

**Technique used:** Missing-variable audit + limiting-case push.

**Derivation:** Per dump, E_out = ½C·V_C(T)², with V_C(T) ≤ V_B set by battery B through (r + R_s), where R_s ∈ {R_dark, R_lit} is the sensitive-device state. The received signal energy appears nowhere in E_out; its only task is to switch R_s. In the limit R_lit → 0 with T ≳ (r+R_lit)·C, E_out → ½CV_B² regardless of how small the triggering disturbance was. Hence E_out/E_signal grows without bound as C, V_B, or T increase.

**From:** E0.4, E0.5, E0.11.
**Assumptions:** Ideal elements. Strictly clean in the Fig. 1 family (battery is the only charging source). In Fig. 2 the disturbance EMF sits in the bridge loop, so a minor direct contribution exists; by construction (large series arms, battery-dominated bias) the battery remains the dominant energy source.
**Verification:** V2 (algebra shown; single-context self-check).

### E1.2 — The admissible commutation window

**Derived proposition:** The dump period T is bounded on both sides: T ≥ κ·τ_lit for signal detection and T < κ·τ_dark for silence in absence of signal, where τ_i = (r + R_i)·C and κ = ln[V_B/(V_B − V_th)], V_th = √(2E_th/C). A usable window exists iff τ_dark > τ_lit. Maximum signaling rate ≈ 1/(κ·τ_lit); false-alarm-free operation requires T < κ·τ_dark. The dark/lit resistance ratio directly brackets the usable clock range. In the "leaky" mode (E0.5), R_dark is finite, so the maximum-T constraint applies even though the ideal block-mode escapes it.

**Technique used:** Canonical-family recognition (RC charging) + monotonicity/sign check.

**Derivation:** V_C(T) = V_B(1 − e^(−T/τ)); relay fires iff ½C·V_C² ≥ E_th ⇔ V_C ≥ V_th. Solve each inequality for T as shown.

**From:** E0.5, E0.7, E0.16, E0.20.
**Assumptions:** Relay modeled as an energy threshold per dump; lumped RC.
**Verification:** V2.

### E1.3 — Duration quantization and latency bound

**Derived proposition:** Clicks per signal N ≈ ⌊D/T⌋ — the clocked dump converts analog signal duration into an integer count; worst-case detection latency is just under T; minimum resolvable duration is of order T.

**Technique used:** Definitional tightening (making "some relation to the duration" explicit).

**From:** E0.8, E0.16, E0.4 ("coincidently").
**Verification:** V2.

### E1.4 — Monotone, saturating intensity transfer; dynamic-range ceiling

**Derived proposition:** Discharge strength is monotone increasing in disturbance intensity (via R_lit(I) decreasing) and saturates at V_B; once τ_lit(I) ≪ T/κ, further intensity change is invisible. Dynamic range in intensity is bounded by the commutation rate.

**Technique used:** Limiting-case push.

**From:** E0.9, E0.15, E1.2.
**Verification:** V2.

### E1.5 — Commutation is structurally necessary in Fig. 2

**Derived proposition:** The periodic discharger d is not merely convenient in Fig. 2: transformer secondary EMF requires dΦ/dt, so quasi-static stored charge produces at most one transient at disturbance onset. Recurring secondary impulses — required for the described repeated actuation — exist only because d converts quasi-DC storage into a pulse train at the rotation frequency. Corollary: the condenser–primary pair forms a series RLC; the discharge is a damped oscillation, which is consistent with Tesla's own hedge that only the "strongest" secondary impulse is "of unchanging direction" — a phrase that presupposes a ranked train of impulses, i.e., ringing.

**Technique used:** Presupposition extraction + missing-variable audit (DC path through a transformer).

**From:** E0.16, E0.18, E0.19, Fig. 2 topology.
**Assumptions:** Faraday induction (E4/structural); underdamped or partially damped discharge.
**Verification:** V2.

### E1.6 — Model-internal unbounded sensitivity

**Derived proposition:** Triggering requires only that the disturbance-induced increment exceed the bias margin ε. As ε→0, the model's minimum detectable disturbance →0. Since the artifact contains no noise term, the claim of responding to "the feeblest influences" is satisfied by construction within the model for any ε>0, and is therefore unfalsifiable without importing an external noise model.

**Technique used:** Limiting-case push.

**From:** E0.17, E0.22.
**Verification:** V2.

### E1.7 — Transducer-scope bifurcation (description vs. claims)

**Derived proposition:** The written description claims modulation of "electrical resistance or other property" (E0.5); method claims 14–19 recite only "variations of resistance" (E0.25); claims 1–13 remain property-agnostic ("controlling the charging"). The legal scope is therefore bifurcated along the transducer-property dimension, with the detailed claims narrower than the description.

**Technique used:** Cross-section comparison / word-choice substitution test.

**From:** E0.5, E0.25.
**Verification:** V2 (document-internal).

### E1.8 — Claim timing-regime partition

**Derived proposition:** The claims encode distinct timing architectures: free storage interval (5–7); event-gated storage intervals "determined by" the disturbances (8–9); clocked use "predetermined as to succession and duration" (10–11); envelope-tracking storage "corresponding in succession and duration" with predetermined discharge (12–13). These are different receiver timing designs, not interchangeable phrasings.

**Technique used:** Definitional tightening on claim language.

**From:** E0.25.
**Verification:** V2.

---

## Stage 4 — Entailed Consequences (E2)

| ID | Consequence | Assumptions | Ver. |
|---|---|---|---|
| E2.1 | Without rotation, the powder device is a latching element (in the artifact's own breakdown model, punctured inter-grain gaps persist); repeatability requires continuous mechanical clocking. | Restoration is mechanically mediated (as stated for rotation); no self-restoration at rest. | V2 |
| E2.2 | The receiver therefore consumes mechanical clocking power continuously, with idle power scaling with reset rate — an always-on operating cost the patent never names. | E2.1; same-shaft drive option (E0.21). | V2 |
| E2.3 | Figs. 1/2 and Fig. 3 span both logic polarities of detection (signal-present vs. signal-absent), the latter being a fail-safe channel semantics. | Receiver thresholding as described (E0.7, E0.10). | V2 |
| E2.4 | If the "definite position" limitation (E0.1) is read as the motivating deficiency, receiver mobility is an implied design objective served by the potential-difference pickup front end. | Reading of col. 1 as motivation. | V1 |
| E2.5 | The polarity hedge (E0.18) is consistent with the ringing account (E1.5): when impulse amplitude ≫ bias margin, either polarity triggers somewhere in the oscillatory train. | Underdamped discharge. | V2 |
| E2.6 | The storage-and-dump performs domain conversion (HF/slow electrical energy → relay-compatible pulses), answering the stated unsuitability of high-frequency energy for ordinary receivers (E0.23). Tesla states the problem and supplies the mechanism but never names the function. | Relays require slow/sustained pulses. | V2 |
| E2.7 | Patent genre filters evidence toward positive behavioral claims; all "I find" statements are single-party and protocol-free. Absence of failure data is weak evidence about actual failure rates. | Legal genre conventions. | V1 |

---

## Stage 5 — Structural Constraints (E3)

| ID | Constraint | Basis | Ver. |
|---|---|---|---|
| E3.1 | Bridge balance requires the product of one pair of opposite arms to equal the product of the other; α's resistance drop unbalances it, producing the condenser P.D. (Exact arm pairing is OCR-ambiguous; condition stated parametrically.) | Wheatstone topology (E0.13). | V2 |
| E3.2 | The same arm resistances appear in the balance condition, the shunt-sensitivity constraint (E0.20), and the charging time constant — so sensitivity, speed, and balance are not independently tunable. | E3.1 + E0.20 + E1.2. | V2 |
| E3.3 | Transformer DC-block makes commutation necessary (E1.5); readout is edge-triggered by the clock, not the signal. | E1.5. | V2 |
| E3.4 | Near-threshold biasing makes every bias-path parameter a potential false-signal channel: battery EMF drift, temperature, humidity, grain geometry all enter through the same margin ε. | E0.17 + E1.6. | V2 |
| E3.5 | Uniform round grains and dry atmosphere are reproducibility/reset-uniformity requirements on the latch element (E2.1). | E0.15. | V2 |
| E3.6 | Same-shaft drive ⇒ a single clock domain phase-locking sample (α), transfer (d), and reset (rotation). | E0.21. | V2 |
| E3.7 | Quantitative vacuum: no units, values, or equations anywhere — all performance claims are structurally unverifiable within the artifact. | Genre/structure. | V1 |

---

## Stage 6 — Cross-Source Knowledge (E4)

All E4 items are recalled knowledge, not verified in this run (no external tools); tagged V0–V1 accordingly.

| ID | External knowledge | Source (provenance) | Relation to artifact | Ver. |
|---|---|---|---|---|
| E4.1 | Coherer effect independently discovered by Branly (1890), named/used by Lodge (1894), deployed by Marconi; modern studies of granular conductors favor micro-contact switching/micro-welding accounts. | Standard radio history; modern granular-media literature (recalled). | Contextualizes α; supports M1 (Stage 8). | V0 |
| E4.2 | Fritz Löwenstein, a witness here, was Tesla's assistant and later central to early triode amplification (telephone-relay amplifier, c. 1912). | Recalled history of electronics. | Connects this patent's control-of-local-source principle to the amplification lineage. | V0 |
| E4.3 | Companion Tesla patents of 1899–1905 develop this method (contemporaneous family; later signaling patents using rotating coherers; US 787,412 was the subject of the referenced v3.2 run). | Recalled patent family. | The present artifact is one node of a designed system. | V0 |
| E4.4 | Tesla's Colorado Springs Notes 1899–1900 (published 1978) contain contemporaneous experimental records. | Recalled bibliography. | Closure route for the parameter gap (C1). | V0 |
| E4.5 | Integrate-and-dump/energy detection and ROC analysis are the modern formalization of this receiver class; integrate-and-dump is optimal for a known pulse in Gaussian noise. | Detection theory (standard). | Frames D1/D6/X1. | V0 |
| E4.6 | Selenium photoconductivity known since W. Smith (1873). | Standard history. | Basis of Fig. 1 embodiment. | V0 |

---

## Stage 7 — Objective & Assumption Extraction

**Stated objective:** Utilize/investigate disturbances transmitted through natural media by disturbance-controlled storage from an independent source (plus, legally, maximal claim breadth).

**Implied operational objectives:** receiver mobility (E2.4); extreme sensitivity (E0.22); unattended repeatability (rotation); message recording (E0.8–9).

**Assumption inventory:**

- **Explicit:** disturbances propagate through media to the receiver; sensitive-device resistance is modifiable by disturbances; condensers store energy.
- **Physical (implicit):** the powder bed is a stack of conductive grains separated by dielectric layers that break down under strain (E0.17's "dielectric layers" language — the artifact's unstated micro-model); dry atmosphere stability; media can convey disturbances over "very great distances" with usable amplitude (an unacknowledged propagation assumption doing heavy lifting for the distance claims).
- **Statistical:** none — no noise, no false-alarm concept anywhere (the pivotal absence; see E1.6, D7).
- **Measurement:** calibration "by experiment" (E0.15); L″–C–rate relations "in well-known ways" (E0.20) — relations invoked but never stated.
- **Optimization:** sensitivity operationally defined as near-breakdown bias; no cost assigned to false alarms.

**Objective mismatch (Invariant 11):** The artifact optimizes sensitivity (bias-to-threshold proximity); a communication receiver's operative objective is reliability (bounded false alarms). These conflict at ε→0, and the conflict is never acknowledged.

---

## Stage 8 — Competing Explanations

### P1 — Why does the powder bed's conductance increase under disturbances, and why does rotation restore it?

The artifact presupposes a mechanism (presupposition extraction on "dielectric layers… breaking down," E0.17): series-dielectric breakdown between grains. It never defends it.

| Mechanism | Description | Required conditions | Predictions | Why the artifact can't distinguish |
|---|---|---|---|---|
| M1 micro-bridge breakdown (latching) | Field concentration at grain contacts punctures insulating films; metallic micro-contacts persist until mechanically disturbed | Bias field near gap-breakdown; conductive grains with surface films | Step-like resistance drop; latches without rotation; bias-dependent threshold; roughly polarity-symmetric | No within-patent test separates it from M2/M3 |
| M2 reversible field-assisted tunneling/percolation | Smooth nonlinear conductance across granular bed, reversible with field | Nonlinear inter-grain transport | Continuous response ∝ amplitude; no latch; no decoherer needed | Same observable (resistance drops) |
| M3 electromechanical grain rearrangement | Disturbance-induced forces re-pack grains into percolating configuration; rotation re-randomizes | Loose grains, free to move | Vibration-sensitive; history-dependent; slower timescale | Confounds mechanical with electrical sensitivity |

Isolation matrix (P1):

| Intervention | M1 | M2 | M3 |
|---|---|---|---|
| Single calibrated pulse, rotation stopped, then measure R(t) | Step persists | Decays after pulse | Slow creep |
| Mechanical tap with no electrical stimulus | No response | No response | Response |
| Fast I–V trace during disturbance | Threshold/kink | Smooth nonlinearity | Hysteresis |

### P2 — What produces uncommanded/repeated receiver actuation (E0.19)?

| Mechanism | Description | Discriminating intervention |
|---|---|---|
| M_a | Sustained external disturbance | Verified known signal source; remove it |
| M_b | Internal regenerative interference: d's brushes switch an inductive primary — brush sparking emits disturbances that the exposed plates P P′ (and near-field wiring) can pick up, re-triggering α and recharging C — a self-sustaining loop whose symptom (repeated actuation) matches Tesla's description exactly | Shield plates; add spark suppression (snubber) across the commutator; dump into a non-inductive load |
| M_c | Parametric drift through the near-threshold bias path (battery EMF, humidity, temperature) | Environmental logging; battery monitoring |
| M_d | Spontaneous α′ breakdown from over-close biasing | Bias-margin sweep (see X1) |

Notably, the artifact itself acknowledges one self-interference channel (battery/condenser influence on the receiving circuit, E0.12) while leaving M_b–M_d unconsidered.

---

## Stage 9 — Latent Information Classification

**A. Recoverable:** E1.1–E1.8, E3.1–E3.6 (derivable/structural as shown).

**B. Conditional:** E2.1–E2.7 (each with assumptions listed above).

**C. Missing-but-identifiable** (each with techniques-attempted line, per Stage Gate 9):

| ID | Candidate | Techniques attempted | Result |
|---|---|---|---|
| C1 | All numerical parameters (C, V_B, resistances, rotation speeds, grain sizes, T) | Computable-but-uncomputed check (no raw data present — nothing to compute from); reference-class audit (no baseline numbers); presupposition extraction (values presupposed as determined "by experiment," not recorded) | Missing; closure: Colorado Springs Notes (E4.4, archival) or replica measurement |
| C2 | Identity of the issued patent corresponding to Ser. 721,790 | Cross-reference check within artifact (absent); presupposition extraction (stated "pending") | Missing; closure: USPTO serial-number records |
| C3 | Grain-level mechanism (M1 vs. M2 vs. M3) | Definitional tightening (artifact's implicit model extracted); silence-as-evidence check (genre-filtered) | Missing; closure: X-series experiments + modern coherer literature |
| C4 | Noise/false-alarm statistics of the receiver | Limiting-case push (showed the model is noise-free — E1.6); silence-as-evidence check | Missing; closure: X1 (ROC frontier) |
| C5 | Natural-vs-artificial source discrimination | Silence-as-evidence check: the artifact frames natural disturbances as uses, not confounds (E0.26) — noise is signal by design | Missing; closure requires a protocol/coding layer absent from the artifact |
| C6 | Plate-placement rule for P, P′ | Optimization from stated elements: objective ("largest possible difference of potential") is stated but no field model or constraint set is given to optimize against | Missing; closure: field modeling + measurement |
| C7 | Achievable range of commutation rates T (mechanical limits) | Boundary analysis from E1.2 gives the admissible electronic window; the mechanically achievable range is unstated | Missing; closure: era commutator engineering data / replica |

---

## Stage 9-A — Cross-Discovery Synthesis

Sweep executed per Invariant 16 (checklist: mutual constraint, shared invariant, dependency chain, cross-section contradiction, latent equivalence, higher-order representation).

### D1 — Clocked polling architecture
**Combines:** E0.4, E0.16, E0.21, E1.3, claims 10–11 (E0.25).
**New relational fact:** the system is a synchronous state machine — write (disturbance → charge, asynchronous), read (clocked dump through d), reset (rotation restores α, α′) — optionally phase-locked on one shaft. Sender and receiver are decoupled in time (no handshake), at the cost of duration quantization (⌊D/T⌋) and latency < T.
**Why not visible in any single input:** each element (periodic d, rotation-restoration, "coincidently") is described separately; only their combination yields the polling/read-write architecture.
**Epistemic class:** E1 (structural synthesis). **Verification:** V2 (self-checked).

### D2 — Delicacy relocated, not eliminated (watchdog principle)
**Combines:** E0.23 (criticism of receivers "too delicate and too easily deranged"), E0.17 ("delicate poise"), E0.15 (automatic restoration by rotation), E2.1.
**New relational fact:** the invention engineers delicacy (near-breakdown biasing) in the control path and makes it survivable by clocked mechanical reinitialization — failure duration is bounded by one clock period. The patent's own critique of delicacy is answered by recoverability, not robustness.
**Epistemic class:** E2. **Verification:** V2.

### D3 — Two-stage cascade of one primitive; ideal gain diverges
**Combines:** E0.17 (both α and α′ biased near breakdown), E0.18, E1.1, E1.5, E1.6.
**New relational fact:** the α-stage and α′-stage are the same primitive (near-breakdown gate + local battery + clocked reset); the transformer is an interstage voltage/impedance matcher. The shared invariant is the margin ε, appearing in both stages. Ideal gain → ∞ as ε→0, so all real performance is set by exogenous noise — unquantifiable within the artifact.
**Epistemic class:** E1/E2. **Verification:** V2.

### D4 — Spurious-actuation identifiability failure
**Combines:** E0.19 (actuated "so long as the influence… continues"), E0.16 (brush-switched inductive primary), E0.12 (acknowledged self-interference channel), Stage 8 P2.
**New relational fact:** the described symptom (repeated actuation) is not identifiable between external persistence, internal regenerative interference, and drift; the artifact's own vocabulary attributes it exclusively to external influence.
**Epistemic class:** E2 (with E5 components). **Verification:** V1–V2.

### D5 — Legal/technical scope bifurcation
**Combines:** E1.7, E1.8, E0.5, E0.25.
**New relational fact:** the "invention" as legally defined is a family of receiver architectures: two transducer scopes (any-property vs. resistance-only) and at least three timing regimes (free, event-gated, envelope-tracking, clocked-use) — a design space visible only by holding description and claims side by side.
**Epistemic class:** E1 (document-internal). **Verification:** V2.

### D6 — One knob, five trades
**Combines:** E1.2, E1.3, E1.4, E0.16.
**New relational fact:** the commutation period T is a master parameter simultaneously setting (i) integration gain/sensitivity, (ii) false-alarm margin, (iii) maximum signaling rate, (iv) detection latency, (v) intensity dynamic range. The patent's pervasive "adjustment" discourse is implicitly about locating a point on this one-dimensional frontier.
**Epistemic class:** E1. **Verification:** V2.

### D7 — The parametric drift channel
**Combines:** E0.6 (battery "very constant"), E0.15 (dry atmosphere, uniform grains), E0.17 (near-breakdown), E3.4.
**New relational fact:** the three superficially unrelated stability requirements are all drift-suppression measures forced by the same architectural choice; near-threshold biasing makes every bias-path parameter an input channel indistinguishable from a disturbance.
**Epistemic class:** E2. **Verification:** V2.

---

## Stage 10 — Latent Information Verification (high-value items)

| Item | Closure status | Evidence boundary | Verification |
|---|---|---|---|
| E1.1 power decoupling | Closed | Algebra from E0 topology; single-context | V2 (self-checked) |
| E1.2 commutation window | Closed | RC derivation; idealized relay threshold | V2 (self-checked) |
| E1.6 unfalsifiability | Closed (as a statement about the model) | Limiting-case argument | V2 (self-checked) |
| D1 polling architecture | Closed (structural) | Synthesis of E0 items | V2 (self-checked) |
| D4 identifiability failure | Partially closed | Argument from stated symptom + inferred spark source (unstated premise) | V1–V2 |
| E4.2 Lowenstein lineage | Open | Recalled history only | V0 (unverified recall) |
| E0.15 "I find" behavior | Open | Single-party, protocol-free report | V1 (source-verified only) |

---

## Stage 11 — Latent Information Value (heuristic prioritization index — not a measurement)

| Item | N | R | Rel | A | LIV | Justification (one line per axis) | Closure | Ver. | Rank |
|---|---|---|---|---|---|---|---|---|---|
| D6 master trade-off | 5 | 5 | 3 | 5 | 375 | Surprising synthesis; core method; V2 derivation; changes any build/test plan | Closed | V2 | 1 |
| E1.1 amplifier topology | 5 | 5 | 3 | 4 | 300 | Output-energy independence is non-obvious and central; re-frames the artifact | Closed | V2 | 2 |
| E1.6 unfalsifiable sensitivity | 4 | 5 | 3 | 5 | 300 | Strikes the artifact's strongest empirical claim; dictates the right experiment | Closed | V2 | 2 |
| E1.2 admissible T window | 4 | 5 | 3 | 4 | 240 | Quantifies the "adjustment" discourse | Closed | V2 | 4 |
| D1 polling architecture | 5 | 4 | 3 | 4 | 240 | Architectural identity invisible in any single passage | Closed | V2 | 4 |
| D2 watchdog principle | 5 | 4 | 3 | 3 | 180 | Resolves the artifact's internal tension; moderate actionability | Closed | V2 | 6 |
| D4 identifiability failure | 5 | 4 | 2 | 4 | 160 | High novelty; rests partly on an inferred (unstated) spark source | Partial | V1–V2 | 7 |
| D3 cascade/divergent gain | 4 | 4 | 3 | 3 | 144 | Latent equivalence of the two stages | Closed | V2 | 8 |
| E1.3 quantization/latency | 4 | 4 | 3 | 3 | 144 | Makes "some relation to duration" exact | Closed | V2 | 8 |
| C5 noise-as-signal framing | 5 | 4 | 2 | 3 | 120 | Reframes the artifact as instrument and receiver; moderately verified | Open | V1 | 10 |
| E1.4 dynamic-range ceiling | 3 | 4 | 3 | 3 | 108 | Derivable but less surprising | Closed | V2 | 11 |
| D5 scope bifurcation | 4 | 3 | 3 | 3 | 108 | Legally significant, secondary physically | Closed | V2 | 11 |
| E2.6 domain conversion | 4 | 3 | 3 | 2 | 72 | Names an unnamed function; low immediate actionability | Closed | V2 | 13 |

---

## Stage 12 — Information Gaps

| Gap | Type | Explanation | Closure method |
|---|---|---|---|
| G1 | Parameter | No numeric values anywhere (C1) | Archival (Colorado Springs Notes) or replica measurement |
| G2 | Mechanism | Grain-level conductance change unresolved (C3) | X-series experiments; modern granular-media literature |
| G3 | Causal | Breakdown vs. tunneling vs. mechanical rearrangement (M1–M3) | X4, X5; microscopy |
| G4 | Boundary | "Very great distances" rests on an unacknowledged propagation assumption | Field modeling; historical transmission records |
| G5 | Model | No noise/false-alarm model exists (C4) | X1 (ROC frontier); detection-theoretic reconstruction |
| G6 | Measurement | Sensitivity unquantified ("feeblest influences") | X1 |
| G7 | Identifiability | Natural vs. artificial source; persistence vs. internal regeneration (D4) | X2; protocol-layer design |
| G8 | Objective | Sensitivity-vs-reliability mismatch unacknowledged | Reframing + X1 quantification |
| G9 | Verification | All behavioral claims single-source, genre-filtered (E2.7) | Archival triangulation; replication |
| G10 | Closure (resolved note) | T-bounds, latency, quantization appeared to be unknowns but were derivable — classified Recoverable per Invariant 3, not gaps | Closed as E1.2/E1.3 |

---

## Stage 13 — Hypotheses (E5)

| ID | Hypothesis | Prediction | Falsifier | Gap | Conf. | Ver. |
|---|---|---|---|---|---|---|
| H1 | Polarity-independence of secondary connection arises from the oscillatory (ringing) discharge, so both polarities appear at s | Heavily damping the primary (series R) introduces polarity dependence | Damped system triggers in both polarities anyway | E0.18 hedge | Moderate | V1 |
| H2 | Repeated actuation can be internally generated (commutator-spark regeneration re-triggering α) | Click trains persist after external signal removal; cease under shielding/snubbing | Post-signal trains persist under full suppression | G7 | Low–moderate | V0 |
| H3 | Sensitivity is noise-limited: dark-event rate diverges as bias margin ε→0 | Smooth ROC; dark rate vs. ε curve steepens without bound | Step-function ROC with zero dark rate at all usable ε | G5/G6 | Moderate | V0 |
| H4 | The dry-atmosphere requirement exists because moisture creates persistent leakage that defeats rotation-reset (latch collapse) | Reset time lengthens monotonically with humidity | Reset time invariant to humidity | E0.15 rationale | Low–moderate | V0 |
| H5 | Grain-level mechanism is M1 (micro-bridge latching), per the artifact's implicit model | Stationary device holds resistance step after a single pulse until tapped | Resistance decays spontaneously after pulse | G2/G3 | Moderate (E4.1-consistent) | V0 |
| H6 | Bridge null provides common-mode rejection of static earth potentials | Deliberate unbalance yields clocked false alarms at the dark rate with no disturbance | No change in false-alarm rate with unbalance | E0.13 design intent | Moderate | V0 |

---

## Stage 14 — Candidate Experiments

| ID | Experiment (intervention / control / measurement) | Distinguishes | Cost |
|---|---|---|---|
| X1 | ROC frontier sweep: replica receiver; two-dimensional sweep of bias margin ε × injected disturbance amplitude A at fixed rotation speed, temperature, humidity, in shielded enclosure; measure dark click-rate and detection probability; relay clicks counted electromechanically or electronically | H3 vs. artifact-implicit determinism; quantifies E1.6, D3, D6 | Moderate |
| X2 | Regeneration test: same apparatus; compare unsuppressed vs. spark-suppressed (snubber + plate shielding) operation with a known sustained signal then removal | M_a vs. M_b (D4) | Low (adjacent to X1) |
| X3 | Polarity × damping test: both secondary polarities under varied primary damping; threshold asymmetry | H1 | Low |
| X4 | Latch test: rotation stopped; single calibrated pulse; monitor R(t); then mechanical tap only | M1 vs. M2 vs. M3 (H5) | Very low |
| X5 | Timing sweep: T over ≥1 decade; click-count linearity vs. duration; saturation of discharge strength vs. intensity | D6 (E1.3, E1.4) | Low |
| X6 | Bridge-balance test: apply known static P.D. at plates under balanced vs. unbalanced bridge; false-alarm rate | H6 | Low |

---

## Stage 15 — Information Gain Analysis (qualitative)

| Experiment | Current uncertainty | Post-test | IG | Why |
|---|---|---|---|---|
| X1 | Sensitivity claim unfalsifiable; model noise-free | Measured detection frontier | High | Converts the artifact's strongest claim into a testable quantity |
| X2 | Repeated actuation unattributable | Attributed (internal vs. external) | High | Resolves an identifiability failure affecting interpretation of all reported behavior |
| X4 | Mechanism class unknown | One of M1–M3 excluded/selected | High (per cost) | Near-free, decisive separation |
| X5 | Trade-off structure theoretical only | Empirical frontier | Medium–high | Tests D6 quantitatively |
| X3 | Hedge unexplained | Explained or refuted | Medium | Resolves E0.18 |
| X6 | Bridge intent inferred | Confirmed/refuted | Medium | Tests E3.1 design reading |

---

## Stage 16 — Optimal Next Observation

**X1 — Receiver-operating-characteristic measurement of the replica Fig. 2 receiver** (with X4 and X2 as pre-registered adjacent measurements sharing the same apparatus).

- **Objective:** Convert "responding to the feeblest influences" from an unfalsifiable model-internal statement (E1.6) into a measured sensitivity–false-alarm frontier; simultaneously attribute repeated actuation (D4) and classify the grain mechanism (H5).
- **Design:** One era-plausible replica (powder tube with sorted round grains in sealed dry atmosphere; adjustable-speed commutator d; bridge; transformer; relay; batteries B, B′ with monitored EMF) plus instrumentation the original lacked: calibrated disturbance injector at plates P P′, click counter, environmental logger, shielded enclosure.
- **Controls:** Rotation speed, temperature, humidity fixed during bias sweeps; battery EMF logged; dummy-load discharge runs; enclosure shielding.
- **Intervention:** Bias margin ε (via r′, r″) swept across its usable range; injected amplitude A swept; three added conditions — rotation stopped (latch test), spark-suppressed (regeneration test), bridge deliberately unbalanced (common-mode test).
- **Measurements:** Dark click-rate R_dark(ε); detection probability P_det(A, ε); click counts vs. known signal duration; discharge-strength distribution vs. intensity.
- **Mechanism predictions:** Artifact-implicit deterministic threshold: R_dark = 0 until a breakdown cliff; P_det a step at A = ε. Threshold-noise (H3): smooth ROC, R_dark diverging as ε→0. Regenerative (H2): post-signal click trains persist unsuppressed, cease suppressed. Latching (M1/H5): resistance step persists with rotation stopped until tapped.
- **Decision rule:** Step-function ROC ⇒ the artifact's implicit model holds and its sensitivity claim is quantified by the measured ε; divergent frontier ⇒ the claim must be restated with an explicit false-alarm rate; persistence asymmetry in the suppression condition ⇒ internal regeneration is a real operating mode of the apparatus as disclosed.
- **Failure interpretation:** If no stable operating point exists at any ε (chronic spontaneous breakdown), the artifact's operating regime is not reproducible, and all capability claims (E0.22) downgrade to untested.
- **Practical constraints:** Replica build cost; era-authenticity vs. instrumentation trade-off; HV battery safety; confounders — humidity, vibration, ambient RF; the adjacent measurements (X2, X4) add near-zero marginal cost, consistent with the adjacent-measurement principle.

---

## Stage 17 — Residual Unknowns

- **Local (resolved by X1/X2/X4):** measured sensitivity/false-alarm frontier; attribution of repeated actuation; latching class of the powder device.
- **Residual (remain after X1):** grain-scale mechanism identity (needs microscopy/granular-physics program); natural-vs-artificial source discrimination (needs a protocol layer absent from the artifact); actual historical performance relative to contemporaries (archival); mechanically achievable commutation range (C7).
- **Fundamental (different program):** the 1901 propagation physics of the "natural media" channels on which the distance claims rest; the counterfactual system-level viability of this receiver architecture at scale.

---

## Stage 18 — Final Epistemic Audit

| Audit | Result |
|---|---|
| A — Promotion check | Pass. All E2 items carry assumptions; historical-significance statements kept at E4/V0; no E5→E1 promotion. |
| B — Closure check | Pass. All category-C items carry techniques-attempted lines; T-bounds/latency/quantization were closed as E1 rather than declared gaps. |
| C — Causal check | Pass. Causal verbs restricted to hypothesis-labeled mechanisms; associative language used elsewhere. |
| D — Mechanism check | Pass. Three distinct mechanisms for P1, four for P2; X-series separates them. |
| E — Objective check | Pass. The optimal observation targets the artifact's operative claim (sensitivity) and surfaces, rather than silently inherits, the sensitivity-vs-reliability mismatch. |
| F — Verification check | Pass. Every major conclusion carries an E/V tag. |
| G — Score integrity | Pass. LIV explicitly labeled heuristic. |
| H — Residual unknowns | Pass. Stage 17 enumerates local/residual/fundamental. |
| I — Verification honesty | Pass. No "independently verified"/"confirmed" language used for self-checks; all V2 items labeled single-context; E4 items labeled unverified recall. |
| J — Applicability | Pass. Stage 8/14 flags were set at Stage 0 and executed; the equation sub-library was marked N/A (no equations) rather than force-filled. |
| K — Materiality/scaling | Pass. Full tier assigned and held; no stage silently abbreviated. |
| L — Output integrity (inferred from Stage-Gate table; spec text truncated) | Pass with disclosed limitation: input hash not computable (no tool); substituted structural fingerprint — US 685,954, Nov. 5, 1901, 19 claims, 5 figures, 7 specification columns; all required table schemas present. |
| M — Cross-discovery audit (inferred; tied to Stage 9-A) | Pass. Seven named discoveries, each stating its inputs, its new relational fact, and why it is invisible in any single input; none merely restates inputs; no verification-tier inflation (all ≤ V2). |

**Final integrity statement:** This run is a single-context self-check. All derivations (E1.1–E1.8, D1–D7) are shown in re-checkable form but were not independently re-derived, and all external-knowledge items (E4.1–E4.6) are unverified recall. The artifact's central method claim — disturbance-controlled storage from an independent source — is structurally coherent as described; its central performance claim — extreme sensitivity — is, on this analysis, unfalsifiable within the artifact's own noise-free model, and the single observation that most sharply changes the epistemic state of this document is the ROC frontier measurement X1.
