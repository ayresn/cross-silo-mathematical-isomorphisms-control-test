---
sid_metadata:
  entry_id: "SID-018"
  schema_version: "1.0-production"
  maturity_stage: "adversarial-flagged"
provenance:
  company: "Alibaba"
  model_family: "Qwen"
  model_version: "3.8 Max"
  generation_timestamp: "2026-07-28"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "gene-family-evolution"
  domain_b: "hypogene-karst-conduit-enlargement"
  structural_family: "state-dependent-population-fokker-planck-operators"
  triple_correspondence_vectors:
    - "governing_differential_operator"
    - "boundary_conditions"
    - "instability_mechanism"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language / incompatible_ontologies / historically_isolated_communities"
prior_discovery_metrics:
  # NOTE: All scores below are model-generated self-assessments produced at generation time.
  # They reflect the generating model's internal pattern-matching confidence, not externally
  # validated measurements. They should be used as triage-ranking signals for human reviewers
  # deciding which entries to prioritize for Stage 2 bibliometric validation — not as evidence
  # that the isomorphism is real or novel.
  structural_isomorphism_score: 7.9
  vocabulary_divergence_score: 9.1
  expected_methodological_transfer_score: 8.4
  community_separation_score: 8.8
  representation_mismatch_score: 9.3
  expected_transfer_effort: "high"
  novelty_prior:
    estimate: 8.2
    uncertainty: "±0.9"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "constitutive_law_mismatch_between_biochemical_selection_and_mineral_dissolution"
  bibliometric_validation: "pending"
  first_adversarial_review:
    reviewer_model: "Anthropic Claude Sonnet 5"
    review_timestamp: "2026-07-30"
    verdict: "FLAG"
    verdict_rationale: "Checks 1, 3, 4, 5, and 6 pass, but Check 2 finds that Section 3's karst population diffusion coefficient `B_k(b)` is introduced as state-dependent via an unjustified coarse-graining step over explicitly heterogeneous conduits, then silently replaced by the constant single-conduit noise term `σ_b` in Section 4's quasi-stationary-distribution formulas."
    failed_checks: []
    flagged_checks:
      - "Check 2: `B_k(b)` is asserted as a function of aperture in Section 3's population Fokker-Planck equation via an undemonstrated coarse-graining step over stated heterogeneous conduits, then treated as the constant `σ_b` (from the single-conduit Langevin equation) in Section 4's `α_q = 2r_k/σ_b²` formula, with no derivation connecting the two."
    stage_3_watch_items:
      - "Verify whether collapsing a heterogeneous population of single-conduit Langevin equations into one clean population-level Fokker-Planck equation with state-dependent B_k(b) requires a mean-field/homogeneous-parameter assumption the entry never states."
      - "Check the quasi-stationary formulas (α_q = 2r_k/σ_b², θ_q = σ_b²K_k/(2r_k)) in Section 4 against established stochastic-logistic/birth-death quasi-stationary-distribution results; internal reading cannot confirm the coefficients are rigorously derived rather than heuristically borrowed."
      - "Confirm whether the gene-family immigration/innovation rate η is zero at n=0; if η_0 > 0, the 'absorbing extinction boundary' claim supporting the boundary_conditions correspondence vector needs qualification."
      - "The 'Dosage-balance carrying capacity ↔ Undersaturation depletion / flow-competition limit' vocabulary pair (Section 2) is defended only as producing the same saturating mathematical term, not a shared constitutive mechanism — consistent with the entry's own medium constitutive_equivalence_confidence, but confirm the entry does not overreach into mechanistic equivalence elsewhere."
      - "Search karst conduit-network literature for prior use of birth-death, population-dynamics, or competitive-selection framing (e.g., master-conduit selection models); conceptually adjacent even though it would not match the specific gene-family-evolution pairing claimed and would not by itself trigger a Check 5 rejection."
      - "Confirm whether the exponent α in R_k = κq_0^α S_0/(βb_0) is actually derivable from the stated cubic flow law (q ∝ b³) and dissolution reaction order m, since the entry never states this relationship explicitly."
  second_adversarial_review:
    reviewer_model: "OpenAI GPT-5.4 Thinking-Mini"
    review_timestamp: "2026-07-30"
    verdict: "FLAG"
    verdict_rationale: "The entry is internally coherent overall, but Section 3 does not mathematically demonstrate the boundary-conditions correspondence claimed in the YAML, so the triple correspondence is only partially supported."
    failed_checks: []
    flagged_checks:
      - "Check 4: boundary-conditions vector is only gestured at in prose, not demonstrated with an explicit boundary-condition formulation"
    stage_3_watch_items:
      - "Verify that Section 3 includes explicit boundary conditions for both systems, not only references to absorbing or saturation boundaries."
      - "Confirm that the karst threshold and first-passage claims are derived tightly enough for bibliometric review."
  third_adversarial_review:
    reviewer_model: "Google Gemini 3.1 Pro"
    review_timestamp: "2026-07-30"
    verdict: "REJECT"
    verdict_rationale: "The entry contains a fatal mathematical contradiction where the proposed quasi-stationary gamma distribution is mathematically impossible to derive from the specified additive-noise Langevin equation."
    failed_checks: 
      - "Check 2: Incompatible stochastic operators between Equation 3 and Equation 6"
    flagged_checks: 
      - "Check 6: Implausible structural_isomorphism_score given fundamental noise mismatch"
    stage_3_watch_items: []
  fourth_adversarial_review:
    reviewer_model: "Z.AI GLM-5.2"
    review_timestamp: "2026-07-30"
    verdict: "FLAG"
    verdict_rationale: "Core Fokker–Planck structural parallelism is valid, but the Section 4 quasi-stationary gamma distribution is mathematically inconsistent with the stated logistic drift, undermining the entry's falsifiable prediction."
    failed_checks: []
    flagged_checks: ["Check 5: Falsifiable prediction relies on a gamma quasi-stationary distribution that does not follow from the stated logistic drift A_k(b) ≈ r_k b(1-b/K_k); the gamma form requires linear drift A(b)=r(1-b/K) with multiplicative noise, not logistic drift"]
    stage_3_watch_items:
      - "Verify whether the quasi-stationary distribution for logistic drift A(b)=rb(1-b/K) with standard diffusion coefficients actually yields a gamma form; preliminary analysis suggests it does not for any power-law B(b)"
      - "Check whether the logistic drift approximation A_k(b) ≈ r_k b(1-b/K_k) is derivable from the Dreybrodt dissolution law coupled to cubic-law flow, or merely asserted"
      - "Verify dimensional consistency of R_k = κq_0^α S_0 / (βb_0) as a dimensionless threshold parameter"
      - "Assess whether methodological transfer is genuinely asymmetric — could reactive-transport forward-modeling tools from karst inform gene-family spatial dynamics?"
      - "Confirm no prior work connects birth-death population processes to karst conduit enlargement"
  fifth_adversarial_review:
    reviewer_model: "Meta Muse Spark 1.1"
    review_timestamp: "2026-07-30"
    verdict: "FLAG"
    verdict_rationale: "Partial body support for boundary_conditions vector; otherwise internally consistent Fokker-Planck isomorphism with valid equations and type-compatible vocabulary."
    failed_checks: []
    flagged_checks: ["Check 4: boundary_conditions vector only qualitatively described without explicit boundary-condition equation/operator"]
    stage_3_watch_items: ["Probe explicit mathematical form of absorbing lower boundary at n=0 / b=0 and saturating upper boundary K in both Fokker-Planck operators", "Verify that logistic-like drift A_k(b) ≈ r_k b(1-b/K_k) closure derives from Dreybrodt + cubic law rather than imposed analogy", "Validate falsifiable prediction of gamma/negative-binomial collapse vs lithology-specific lognormal in empirical aperture datasets"]
  sixth_adversarial_review:
    reviewer_model: "DeepSeek DeepSeek"
    review_timestamp: "2026-07-30"
    verdict: "PASS"
    verdict_rationale: "All six checks passed without failure or flag; the entry is internally consistent, equations are valid and correctly attributed, vocabulary matrix is coherent, triple-correspondence vectors are fully supported, the analogy is not a textbook cliché, and scores align with the content."
    failed_checks: []
    flagged_checks: []
    stage_3_watch_items: []
  seventh_adversarial_review:
    reviewer_model: "xAI Grok"
    review_timestamp: "2026-07-30"
    verdict: "PASS"
    verdict_rationale: "All six checks pass with full internal consistency between YAML claims, vocabulary mappings, equations, and body text; no category errors, unsupported vectors, or textbook-level analogies detectable from the entry alone."
    failed_checks: []
    flagged_checks: []
    stage_3_watch_items: ["Confirm that the Dreybrodt-style aperture law plus cubic-flow coarse-graining truly yields a logistic-like drift A_k(b) under the parameter regimes typical of hypogene settings.", "Verify whether the quasi-stationary gamma/negative-binomial form and logarithmic breakthrough-time scaling are genuine predictions of the gene-family birth-death process under the stated boundary conditions."]
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 018

## 1. CROSS-SILO SYSTEM DEFINITION
*   **Silo A (Field 1):** Gene-family evolution, specifically stochastic duplication–loss–innovation dynamics of discrete gene-copy-number states evolving along phylogenies, with observed extant copy-number distributions and inferred ancestral family sizes.
*   **Silo B (Field 2):** Hypogene karst conduit enlargement, specifically dissolutional widening of fracture/conduit apertures under rising, confined, chemically aggressive groundwater, with observed aperture/conductance distributions and breakthrough or speleothem-age constraints.
*   **Mathematical Isomorphism:** Both systems are state-dependent population processes in a one-dimensional “size” coordinate—gene-copy number in Silo A and conduit aperture/conductance in Silo B—whose probability density evolves under a nonlinear Fokker–Planck/continuity operator with an absorbing loss boundary, a saturating upper boundary, and a threshold feedback number that separates extinction/sealing from runaway expansion/breakthrough; the triple correspondence is explicitly through the governing differential operator, the boundary conditions, and the instability mechanism.

## 2. DIAGNOSTIC VOCABULARY MATRIX
*   **Gene duplication** ↔ **Dissolutional wall retreat**
    *   *Operator Role:* Both act as positive increments in the size coordinate. In the generator, duplication contributes a birth drift term, while dissolution contributes an aperture-growth drift term. Mathematically, they populate the same advective coefficient in the Fokker–Planck limit.
*   **Gene loss / pseudogenization** ↔ **Precipitation, clogging, or collapse**
    *   *Operator Role:* Both act as negative increments or death-like removal from the active population. They generate the downward drift and contribute to the absorbing boundary at zero size, making extinction/sealing a first-passage event.
*   **Dosage-balance carrying capacity** ↔ **Undersaturation depletion / flow-competition limit**
    *   *Operator Role:* Both impose state-dependent saturation. In gene families, selection against excess copy number creates an effective carrying capacity; in hypogene conduits, solute saturation, limited aggressiveness, and competitive flow redistribution cap aperture growth. Both convert exponential growth into logistic-like nonlinear drift.
*   **Gene-family extinction** ↔ **Conduit abandonment / sealing**
    *   *Operator Role:* Both are absorbing states at the lower boundary. Once a gene family reaches zero copies, it cannot return without immigration; once a conduit segment is sealed or clogged, its conductance vanishes and it exits the active flow network.
*   **Phylogenetic lineage** ↔ **Conduit flow path or segment**
    *   *Operator Role:* Both are the carriers of the state variable through time. A lineage transmits copy number under duplication–loss; a conduit segment transmits aperture under dissolution–clogging. In both cases, the observable present-day distribution is a conditioned sample from a historical stochastic process.
*   **Copy-number likelihood** ↔ **Aperture-population likelihood**
    *   *Operator Role:* Both define inverse problems over latent histories. Gene-family methods compute the likelihood of observed copy numbers given hidden duplication/loss histories; the proposed karst transfer computes the likelihood of observed aperture distributions given hidden dissolution/clogging histories.

## 3. CORE MATHEMATICAL PARALLELISM
In gene-family evolution, a common mechanistic description treats copy number as a continuous-time birth–death–immigration process. Let `P_n(t)` be the probability that a gene family has `n` copies at time `t`, with state-dependent duplication rate `d_n`, loss rate `l_n`, and innovation/immigration rate `η_n`. The master equation is:

```math
\frac{dP_n}{dt}
=
d_{n-1}P_{n-1}
+
l_{n+1}P_{n+1}
+
\eta_{n-1}P_{n-1}
-
\left(d_n+l_n+\eta_n\right)P_n .
```

For large copy number, this discrete process has a diffusion approximation:

```math
\partial_t p(n,t)
=
-\partial_n\!\left[A_g(n)\,p(n,t)\right]
+
\frac{1}{2}\partial_{nn}\!\left[B_g(n)\,p(n,t)\right],
```

where `A_g(n) = [d(n)-l(n)]n + η(n)` is the net drift and `B_g(n) = [d(n)+l(n)]n + η(n)` is the stochastic diffusion coefficient. If duplication advantage declines with copy number, `A_g(n)` becomes logistic-like, producing a stable nonzero quasi-stationary copy-number basin and an absorbing extinction boundary at `n=0`.

In hypogene karst conduit enlargement, the local physical process is usually described by reactive transport plus wall retreat. A Dreybrodt-style dissolution law coupled to cubic-law flow gives an aperture evolution equation of the form:

```math
\frac{db}{dt}
=
\frac{1}{\rho_s}
\left[
k_1\left(c_{\mathrm{eq}}-c\right)
+
k_2\left(c_{\mathrm{eq}}-c\right)^m
\right]
-
\beta b
+
\sigma_b\,\xi(t),
```

where `b` is aperture, `c` is dissolved calcium carbonate or equivalent solute concentration, `c_eq` is equilibrium concentration, `ρ_s` is the molar density of the solid, `β` represents precipitation, clogging, or collapse-like aperture loss, and `ξ(t)` represents heterogeneity-induced fluctuations. Because flow scales approximately as `q(b) ∝ b^3`, the dissolution supply term is strongly state dependent. Coarse-graining many heterogeneous conduit segments into an aperture-density population `ψ(b,t)` yields a Fokker–Planck-type equation:

```math
\partial_t \psi(b,t)
=
-\partial_b\!\left[A_k(b)\,\psi(b,t)\right]
+
\frac{1}{2}\partial_{bb}\!\left[B_k(b)\,\psi(b,t)\right].
```

Near the enlargement threshold, the karst drift can be expanded as `A_k(b) ≈ r_k b(1-b/K_k)`, which is operator-equivalent to the stochastic logistic birth–death drift in gene-family space. The latent topology is therefore the same: a lower absorbing boundary, an upper saturation basin, and a threshold-controlled transition from decay to runaway growth. The corresponding dimensionless threshold parameters are:

```math
\mathcal{R}_g = \frac{d_0}{l_0},
\qquad
\mathcal{R}_k = \frac{\kappa q_0^\alpha S_0}{\beta b_0},
```

where `S_0` is initial undersaturation capacity and `κ q_0^α S_0` parameterizes the flow-enhanced dissolution gain. In both systems, the critical condition is approximately `R = 1`: below it, loss dominates; above it, positive feedback drives expansion toward the saturated state.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
*   **Preferred Transfer Direction:** Gene Family Evolution → Hypogene Karst Conduit Enlargement
*   **Asymmetric Maturity Rationale:** Gene-family evolution possesses a highly mature inverse toolkit: state-dependent birth–death likelihoods, phylogenetic pruning algorithms, hidden Markov ancestral reconstruction, Bayesian data augmentation, and model-selection frameworks for sparse extant observations. Hypogene karst modeling has strong forward reactive-transport simulators, but inverse inference of deep-time aperture evolution from sparse borehole, cave-mapping, geochemical, and U/Th age data remains comparatively ad hoc, strongly nonunique, and limited by poor temporal sampling.
*   **Target Bottleneck Mitigation:** Recasting conduit aperture populations as state-dependent birth–death–immigration processes should allow hypogene speleologists to import gene-family likelihood machinery. The testable hypothesis is that a phylogenetic-style birth–death hidden Markov model, conditioned on survival/non-sealing and fitted to modern aperture distributions plus sparse age constraints, will produce posterior estimates of dissolution “birth” rate, clogging “death” rate, and effective carrying capacity that reduce equifinality in paleo-discharge and breakthrough-time reconstruction more than current deterministic mean-fit reactive-transport inversion.
*   **Falsifiable Prediction:** If the isomorphism is structurally valid, mature hypogene conduit aperture distributions from different caves, when nondimensionalized by posterior `r_k` and `K_k`, should collapse onto the quasi-stationary gamma/negative-binomial family predicted by stochastic birth–death dynamics:

```math
\psi_{\mathrm{qs}}(b)
\propto
b^{\alpha_q-1}
\exp\!\left(-\frac{b}{\theta_q}\right),
\qquad
\alpha_q = \frac{2r_k}{\sigma_b^2},
\quad
\theta_q = \frac{\sigma_b^2 K_k}{2r_k}.
```

Furthermore, breakthrough ages should obey a first-passage scaling approximately given by:

```math
\mathbb{E}[T_B]
\approx
\frac{1}{r_k}
\ln\!\left(\frac{K_k}{b_0}\right).
```

The candidate is falsified if well-sampled hypogene conduit aperture populations systematically follow lithology-specific lognormal distributions with no collapse under `r_k/K_k` nondimensionalization, or if breakthrough ages scale primarily linearly with path length rather than logarithmically with the inferred saturation ratio `K_k/b_0`.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
*   `"state-dependent gene-family birth-death process" AND "duplication-loss likelihood" AND "quasi-stationary copy-number distribution"`
*   `"hypogene speleogenesis" AND "Dreybrodt dissolution law" AND "conduit breakthrough time"`
*   `"birth-death-immigration Fokker-Planck" AND "gene family size distribution" AND "phylogenetic ancestral reconstruction"`
*   `"hypogene maze cave aperture distribution" AND "reactive transport inverse modeling" AND "U-series speleothem age"`

---

## ADVERSARIAL REVIEWS (Stage 2)

### First Adversarial Review
**Reviewer:** Anthropic Claude Sonnet 5
**Verdict:** FLAG
**Review Date:** 2026-07-30

#### Results by Check
- **CHECK 1 (YAML Metadata Integrity):** PASS — `triple_correspondence_vectors` lists exactly three distinct items, `maturity_stage` is `"candidate"`, and `relationship_type` is `"candidate_structural_isomorphism"`, all as required.
- **CHECK 2 (Equation Validity):** FLAG — Section 3 introduces `B_k(b)` as a state-dependent diffusion coefficient in the karst population equation via an asserted (not derived) coarse-graining step over explicitly "heterogeneous conduit segments," then Section 4 substitutes the constant single-conduit noise term `σ_b` (from `db/dt = ... − βb + σ_bξ(t)`) directly into `α_q = 2r_k/σ_b²` without reconciling the two.
- **CHECK 3 (Vocabulary Matrix Coherence):** PASS — all six Section 2 mappings pair objects of compatible mathematical type (growth term↔growth term, loss term↔loss term, saturation term↔saturation term, absorbing state↔absorbing state, sample-path carrier↔sample-path carrier, likelihood↔likelihood), and each Operator Role names a specific shared structure (e.g., "they populate the same advective coefficient in the Fokker–Planck limit") rather than relying on hedged language alone.
- **CHECK 4 (Triple-Correspondence Body Verification):** PASS — `governing_differential_operator` is demonstrated in Section 3 via the parallel Fokker-Planck forms and the explicit claim that `A_k(b) ≈ r_k b(1-b/K_k)` is "operator-equivalent to the stochastic logistic birth-death drift"; `boundary_conditions` is demonstrated via the stated "lower absorbing boundary, an upper saturation basin" tied to drift sign behavior in both systems; `instability_mechanism` is demonstrated via the explicit `R_g`/`R_k` threshold formulas and the stated "critical condition is approximately R=1." All three vectors have equation-level body support in Section 3, though `boundary_conditions` rests on qualitative drift-sign argument rather than an explicit boundary-value equation.
- **CHECK 5 (Rejection Criteria Face-Check):** PASS — the gene-family-evolution/hypogene-karst pairing is not recognizable as a standard graduate-textbook or widely-cited-review analogy (unlike the explicitly rejected Schrödinger/optics, heat/solutal-diffusion, or Ising/lattice-gas cases); the transfer asymmetry is specifically justified (mature phylogenetic pruning/HMM/Bayesian machinery vs. comparatively ad hoc karst inverse methods) rather than merely asserted; and Section 4's prediction is genuinely falsifiable, naming a specific distributional collapse and a specific logarithmic breakthrough-time scaling with explicit alternative outcomes ("lithology-specific lognormal... with no collapse," scaling "linearly with path length") that would falsify it.
- **CHECK 6 (Score-Content Plausibility):** PASS — `structural_isomorphism_score` (7.9) is consistent with the genuine equation-level derivation in Section 3; `operator_equivalence_confidence` ("high") is not contradicted since no category errors were found in the Section 2 matrix; `representation_mismatch_score` (9.3) is plausible rather than inflated given how disparate molecular gene-family evolution and karst reactive-transport geochemistry are as foundational disciplines.

#### Stage 3 Watch Items
- Verify whether collapsing a heterogeneous population of single-conduit Langevin equations into one clean population-level Fokker-Planck equation with state-dependent `B_k(b)` requires a mean-field/homogeneous-parameter assumption the entry never states.
- Check the quasi-stationary formulas (`α_q = 2r_k/σ_b²`, `θ_q = σ_b²K_k/(2r_k)`) in Section 4 against established stochastic-logistic/birth-death quasi-stationary-distribution results; internal reading alone cannot confirm the coefficients are rigorously derived rather than heuristically borrowed.
- Confirm whether the gene-family immigration/innovation rate `η` is zero at `n=0`; if `η_0 > 0`, the "absorbing extinction boundary" claim supporting the `boundary_conditions` correspondence vector needs qualification.
- The "Dosage-balance carrying capacity ↔ Undersaturation depletion / flow-competition limit" pair (Section 2) is defended only as producing the same saturating mathematical term, not a shared constitutive mechanism — consistent with the entry's own "medium" `constitutive_equivalence_confidence`, but confirm the entry does not overreach into mechanistic equivalence elsewhere.
- Search karst conduit-network literature for prior use of birth-death, population-dynamics, or competitive-selection framing (e.g., master-conduit selection models); conceptually adjacent even though it would not match the specific gene-family-evolution pairing claimed here and would not by itself trigger a Check 5 rejection.
- Confirm whether the exponent `α` in `R_k = κq_0^α S_0/(βb_0)` is actually derivable from the stated cubic flow law (`q ∝ b³`) and dissolution reaction order `m`, since the entry never states this relationship explicitly.

### Second Adversarial Review
**Reviewer:** OpenAI GPT-5.4 Thinking-Mini
**Verdict:** FLAG
**Review Date:** 2026-07-30

#### Results by Check
* **CHECK 1 (YAML Metadata Integrity):** PASS — `triple_correspondence_vectors` lists exactly three distinct items, `maturity_stage` is `"candidate"`, and `relationship_type` is `"candidate_structural_isomorphism"`.
* **CHECK 2 (Equation Validity):** PASS — The Section 3 equations are internally consistent with the stated birth–death/diffusion and dissolution-transport narratives, and no equation is plainly misattributed or type-inconsistent.
* **CHECK 3 (Vocabulary Matrix Coherence):** PASS — The paired terms are compatible mathematical/physical objects, and the operator-role explanations describe shared drift, loss, saturation, or inverse-problem structure rather than a category error.
* **CHECK 4 (Triple-Correspondence Body Verification):** FLAG — The governing differential operator and instability mechanism are developed in Section 3, but the boundary-conditions vector is only gestured at by phrases like “a lower absorbing boundary” and “an upper saturation basin” without an explicit boundary-condition formulation, so that YAML correspondence is only partially demonstrated.
* **CHECK 5 (Rejection Criteria Face-Check):** PASS — The pairing is not a canonical textbook analogy in the sense targeted by the protocol, and Section 4’s transfer direction is presented as asymmetrically favoring gene-family methods over karst inversion.
* **CHECK 6 (Score-Content Plausibility):** PASS — The YAML scores are aggressive but not obviously contradicted by the body text, given the entry’s explicit equations, threshold discussion, and inverse-method framing.

#### Stage 3 Watch Items
* Verify that Section 3 supplies explicit boundary conditions for both silos, not just prose references to absorbing and saturation boundaries.
* Check whether the karst diffusion approximation and threshold scaling are stated precisely enough for Stage 3 bibliometric validation.

### Third Adversarial Review
**Reviewer:** Google Gemini 3.1 Pro
**Verdict:** REJECT
**Review Date:** 2026-07-30

#### Results by Check
- **CHECK 1 (YAML Metadata Integrity):** PASS — All required metadata fields are present and properly formatted.
- **CHECK 2 (Equation Validity):** FAIL — The falsifiable prediction in Equation 6 claims a gamma/negative-binomial stationary distribution (`\psi_{\mathrm{qs}}(b) \propto b^{\alpha_q-1} \exp\!\left(-\frac{b}{\theta_q}\right)`), but this is mathematically impossible to derive from the additive noise term (`\sigma_b\,\xi(t)`) in Equation 3 combined with the logistic drift (`A_k(b) \approx r_k b(1-b/K_k)`); an additive-noise logistic Fokker-Planck equation yields an exponentiated-cubic stationary distribution, whereas a gamma distribution strictly requires a multiplicative/demographic noise scaling ($B(b) \propto b$).
- **CHECK 3 (Vocabulary Matrix Coherence):** PASS — The vocabulary pairs map compatible mathematical objects (e.g., absorbing boundary states, saturation parameters, probability distributions) and explicitly define their shared mathematical operator roles.
- **CHECK 4 (Triple-Correspondence Body Verification):** PASS — All three YAML vectors (`governing_differential_operator`, `boundary_conditions`, `instability_mechanism`) are explicitly addressed and mathematically demonstrated in Section 3.
- **CHECK 5 (Rejection Criteria Face-Check):** PASS — The analogy is non-canonical and the methodological transfer from phylogenetics to hydrogeology is genuinely asymmetric and clearly articulated.
- **CHECK 6 (Score-Content Plausibility):** FLAG — The `structural_isomorphism_score` of 7.9 and `operator_equivalence_confidence` of `high` are implausible given the unacknowledged structural mismatch between demographic noise ($B_g(n)$ scales with $n$) in the gene-family operator and additive noise ($B_k(b) = \sigma_b^2$) in the karst operator.

#### Stage 3 Watch Items
None identified.

### Fourth Adversarial Review
**Reviewer:** Z.AI GLM-5.2
**Verdict:** FLAG
**Review Date:** 2026-07-30

#### Results by Check
- **CHECK 1 (YAML Metadata Integrity):** PASS — `triple_correspondence_vectors` lists exactly 3 distinct items (`governing_differential_operator`, `boundary_conditions`, `instability_mechanism`), `maturity_stage` is `"candidate"`, and `relationship_type` is `"candidate_structural_isomorphism"`.
- **CHECK 2 (Equation Validity):** PASS — The Section 3 equations are valid and correctly attributed. The gene-family master equation is a standard continuous-time birth–death–immigration master equation; its Fokker–Planck diffusion approximation has correctly computed drift `A_g(n)=[d(n)-l(n)]n+η(n)` and diffusion `B_g(n)=[d(n)+l(n)]n+η(n)`. The karst SDE couples a Dreybrodt-style dissolution law with cubic-law flow dependence and a stochastic fluctuation term, consistent with the stated physical domain. The population-level Fokker–Planck for aperture density is a standard coarse-graining. The two Fokker–Planck operators together support the claimed structural isomorphism through shared advective–diffusive structure with state-dependent coefficients.
- **CHECK 3 (Vocabulary Matrix Coherence):** PASS — All six vocabulary pairs map objects of compatible mathematical type. Gene duplication ↔ dissolutional wall retreat are both positive-increment processes populating the birth drift term; gene loss ↔ precipitation/clogging are both death-like removal processes; dosage-balance carrying capacity ↔ undersaturation depletion are both state-dependent nonlinear saturation mechanisms; extinction ↔ sealing are both absorbing lower boundaries; phylogenetic lineage ↔ conduit segment are both state-variable carriers; copy-number likelihood ↔ aperture-population likelihood are both inverse-problem formulations. Operator role explanations specify mathematical structure (advective coefficient, first-passage event, logistic nonlinear drift) rather than relying solely on hedged analogy.
- **CHECK 4 (Triple-Correspondence Body Verification):** PASS — All three YAML vectors are supported in Section 3 with mathematical specificity. (1) `governing_differential_operator`: both Fokker–Planck equations are displayed and their structural parallelism is demonstrated. (2) `boundary_conditions`: the absorbing lower boundary at zero and the saturating upper boundary are discussed for both domains, with first-passage framing. (3) `instability_mechanism`: the dimensionless threshold parameters `R_g` and `R_k` are defined, and the critical condition `R=1` separating decay from runaway expansion is stated for both systems.
- **CHECK 5 (Rejection Criteria Face-Check):** FLAG — The domain pairing (gene-family evolution ↔ hypogene karst conduit enlargement) is not a recognizable textbook analogy. The methodological transfer is plausibly asymmetric given the maturity gap in inverse inference tooling. However, the falsifiable prediction contains a mathematical inconsistency. The entry states logistic drift `A_k(b) ≈ r_k b(1-b/K_k)` and then claims the quasi-stationary distribution is gamma: `ψ_qs(b) ∝ b^{α_q-1} exp(-b/θ_q)` with `α_q = 2r_k/σ_b²` and `θ_q = σ_b²K_k/(2r_k)`. For a Fokker–Planck equation with logistic drift `A(b)=rb(1-b/K)`, the stationary solution is `ψ ∝ (1/B) exp(∫ 2A/B db)`, which for any power-law diffusion coefficient `B(b)=σ²b^p` produces a Gaussian-like or super-exponential tail from the `b²` term in the exponent — not the exponential tail of a gamma distribution. The gamma distribution with the stated parameters requires linear drift `A(b)=r(1-b/K)` with multiplicative noise `B(b)=σ²b` (the Feller/CIR process), which lacks the extra factor of `b` present in the logistic form. The prediction is falsifiable in form, but tests for a distributional shape that does not follow from the stated dynamics.
- **CHECK 6 (Score-Content Plausibility):** PASS — The `structural_isomorphism_score: 7.9` is supported by the valid parallel Fokker–Planck construction in Section 3. The `operator_equivalence_confidence: "high"` is defensible at the operator level (both systems share the Fokker–Planck structure with state-dependent drift and diffusion). The `representation_mismatch_score: 9.3` is plausible given the large gap between discrete gene-copy-number states on phylogenetic trees and continuous conduit apertures in 3D geological media. The `constitutive_equivalence_confidence: "medium"` is appropriately cautious, consistent with the stated `primary_failure_risk` of constitutive-law mismatch.

#### Stage 3 Watch Items
- The quasi-stationary gamma distribution `ψ_qs(b) ∝ b^{α_q-1} exp(-b/θ_q)` with `α_q = 2r_k/σ_b²`, `θ_q = σ_b²K_k/(2r_k)` is mathematically incompatible with the stated logistic drift `A_k(b) ≈ r_k b(1-b/K_k)`. Stage 3 should determine whether a corrected quasi-stationary distribution (e.g., one with Gaussian-like tails from the `b²` term in the logistic exponent) would still yield a falsifiable distributional prediction, or whether the entire prediction needs reformulation.
- The logistic drift approximation `A_k(b) ≈ r_k b(1-b/K_k)` is asserted ("can be expanded as") but not derived from the Dreybrodt dissolution law and cubic-law flow coupling. Stage 3 should verify whether this functional form is a valid local approximation or a post-hoc imposition to force parallelism with the gene-family drift.
- The dimensional consistency of `R_k = κq_0^α S_0 / (βb_0)` should be verified — the lumped parameter `κ` must carry specific dimensions for this ratio to be dimensionless, and these are not specified.
- The first-passage time formula `E[T_B] ≈ (1/r_k) ln(K_k/b_0)` is the exponential-growth-phase approximation, valid only when `b_0 ≪ K_k` and breakthrough occurs before significant saturation. Stage 3 should assess whether this regime is physically realistic for hypogene karst systems.
- The asymmetry claim should be probed: while gene-family inverse-inference tooling is clearly more mature, reactive-transport forward-modeling capability from the karst side could plausibly transfer to spatial gene-family dynamics (e.g., along chromosome position), which would weaken the asymmetry criterion.
- Bibliometric verification should confirm no prior work has connected birth–death population processes to fracture/conduit aperture evolution.

### Fifth Adversarial Review
**Reviewer:** Meta Muse Spark 1.1
**Verdict:** FLAG
**Review Date:** 2026-07-30

#### Results by Check
- **CHECK 1 (YAML Metadata Integrity):** PASS — triple_correspondence_vectors lists exactly 3 distinct items ["governing_differential_operator", "boundary_conditions", "instability_mechanism"], maturity_stage is "candidate", relationship_type is "candidate_structural_isomorphism".
- **CHECK 2 (Equation Validity):** PASS — Gene-family master equation and Fokker-Planck approximation correctly model birth-death-innovation, karst aperture SDE with Dreybrodt law correctly models reactive dissolution plus loss, and both yield operator-equivalent Fokker-Planck forms supporting the claimed isomorphism.
- **CHECK 3 (Vocabulary Matrix Coherence):** PASS — All six pairings map compatible mathematical types (positive-drift operators, negative-drift operators, scalar saturation parameters, absorbing states, trajectory carriers, likelihood functionals) with Operator Role explanations specifying shared advective/diffusive/boundary roles.
- **CHECK 4 (Triple-Correspondence Body Verification):** FLAG — governing_differential_operator is fully supported by dual Fokker-Planck equations in Section 3, instability_mechanism is supported by threshold equations "R_g = d0/l0" and "R_k = κ q0^α S0 / β b0" and critical condition "R = 1", but boundary_conditions is only qualitatively gestured at as "absorbing extinction boundary at n=0" and "lower absorbing boundary, an upper saturation basin" without explicit mathematical boundary condition formulation.
- **CHECK 5 (Rejection Criteria Face-Check):** PASS — Gene-family evolution ↔ hypogene karst pairing is not a canonical textbook analogy, transfer Gene Family Evolution → Karst is genuinely asymmetric per inverse toolkit maturity rationale, and falsifiable prediction specifies measurable gamma collapse "ψ_qs(b) ∝ b^{α_q-1} exp(-b/θ_q)" vs lognormal and logarithmic vs linear breakthrough scaling "E[T_B] ≈ (1/r_k) ln(K_k/b0)".
- **CHECK 6 (Score-Content Plausibility):** PASS — Scores (structural_isomorphism_score 7.9, representation_mismatch_score 9.3, operator_equivalence_confidence high) are plausible given demonstrated dual Fokker-Planck operators and highly disparate foundational objects.

#### Stage 3 Watch Items
- Request explicit mathematical form of absorbing lower boundary (p=0 flux, zero) and saturating upper boundary (reflecting, logistic cap) in both Fokker-Planck operators to fully satisfy boundary_conditions vector.
- Verify that logistic-like cap K_k and drift A_k(b) ≈ r_k b(1-b/K_k) emerges from Dreybrodt + q(b) ∝ b^3 closure rather than being imposed to mirror gene-family logistic.
- Validate falsifiable prediction against empirical aperture datasets for gamma/negative-binomial collapse under r_k/K_k nondimensionalization.

### Sixth Adversarial Review
**Reviewer:** DeepSeek DeepSeek
**Verdict:** PASS
**Review Date:** 2026-07-30

#### Results by Check
- **CHECK 1 (YAML Metadata Integrity):** PASS — `triple_correspondence_vectors` contains exactly three distinct items, `maturity_stage` is `"candidate"`, and `relationship_type` is `"candidate_structural_isomorphism"`.
- **CHECK 2 (Equation Validity):** PASS — All equations correctly model the stated domains; the gene‑family master equation and diffusion approximation are standard, the hypogene aperture SDE and resulting Fokker‑Planck are physically plausible, and together they support the claimed logistic‑drift/absorbing‑boundary isomorphism.
- **CHECK 3 (Vocabulary Matrix Coherence):** PASS — All six mapping pairs pair objects of compatible mathematical type (rates, saturation limits, absorbing boundaries, trajectories, likelihoods) and the operator‑role explanations specify shared mathematical structure without reliance on vague analogy.
- **CHECK 4 (Triple-Correspondence Body Verification):** PASS — Section 3 explicitly derives or discusses the governing Fokker‑Planck operator, the absorbing lower boundary, and the threshold instability via dimensionless parameters \( \mathcal{R}_g \) and \( \mathcal{R}_k \), fully covering all three YAML vectors.
- **CHECK 5 (Rejection Criteria Face-Check):** PASS — The gene‑family/hypogene‑karst pairing is not a canonical textbook analogy; methodological transfer is clearly asymmetric (gene‑family’s mature inverse toolkit → karst’s limited inverse methods); the falsifiable prediction specifies collapse to a gamma/negative‑binomial distribution and logarithmic breakthrough‑age scaling, with concrete conditions for falsification.
- **CHECK 6 (Score-Content Plausibility):** PASS — All prior‑discovery‑metrics scores are consistent with the body content; no score contradicts the demonstrated mathematical parallelism or the clearly divergent vocabularies and communities.

#### Stage 3 Watch Items
None identified.

### Seventh Adversarial Review
**Reviewer:** xAI Grok
**Verdict:** PASS
**Review Date:** 2026-07-30

#### Results by Check
- **CHECK 1 (YAML Metadata Integrity):** PASS — triple_correspondence_vectors contains exactly three distinct items, maturity_stage is "candidate", and relationship_type is "candidate_structural_isomorphism".
- **CHECK 2 (Equation Validity):** PASS — The master equation, its Fokker–Planck diffusion approximation, the aperture evolution ODE, and the corresponding Fokker–Planck equation for ψ(b,t) are internally consistent with the claimed state-dependent population processes and support the shared nonlinear drift-plus-diffusion structure.
- **CHECK 3 (Vocabulary Matrix Coherence):** PASS — All six paired tokens are objects of compatible mathematical type (increment processes, saturation mechanisms, absorbing states, carriers, likelihood functionals) and the Operator Role explanations specify shared structure in the generator/advective coefficients rather than mere analogy.
- **CHECK 4 (Triple-Correspondence Body Verification):** PASS — All three YAML vectors (governing_differential_operator, boundary_conditions, instability_mechanism) are demonstrated with explicit equations and threshold analysis in Section 3.
- **CHECK 5 (Rejection Criteria Face-Check):** PASS — The gene-family ↔ hypogene-karst pairing is not a canonical textbook or review-article analogy; the claimed transfer direction is asymmetrically justified by inverse-method maturity; and the prediction supplies concrete, measurable distributional and scaling signatures that can falsify the claim.
- **CHECK 6 (Score-Content Plausibility):** PASS — The reported structural_isomorphism_score (7.9), operator_equivalence_confidence ("high"), and representation_mismatch_score (9.3) are consistent with the matching Fokker–Planck operators, category-correct vocabulary, and distant ontologies shown in the body.

#### Stage 3 Watch Items
- Confirm that the Dreybrodt-style aperture law plus cubic-flow coarse-graining truly yields a logistic-like drift A_k(b) under the parameter regimes typical of hypogene settings.
- Verify whether the quasi-stationary gamma/negative-binomial form and logarithmic breakthrough-time scaling are genuine predictions of the gene-family birth-death process under the stated boundary conditions.