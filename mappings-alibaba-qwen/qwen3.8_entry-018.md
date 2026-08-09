---
sid_metadata:
  entry_id: "SID-018"
  schema_version: "1.0-control"
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
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-09"
    verdict: "REJECT"
    verdict_rationale: "The Section 4 prediction that karst aperture distributions collapse onto a gamma/negative-binomial quasi-stationary family does not actually solve the entry's own logistic drift equation from Section 3, which is a wrong-equation FAIL under Check 1."
    failed_checks:
      - "Check 1: the quasi-stationary gamma/negative-binomial distribution formula given in Section 4 does not solve the logistic Fokker-Planck drift the entry itself derives in Section 3"
    flagged_checks:
      - "Check 1 (secondary, non-fatal): the near-threshold reduction A_k(b) ≈ r_k b(1-b/K_k) is asserted rather than derived from the stated dissolution SDE and the q(b) ∝ b^3 flow-feedback mechanism"
      - "Check 3: the boundary_conditions correspondence vector is named and discussed in prose on both sides but never demonstrated with an explicit boundary-condition equation, flux condition, or derivation"
      - "Check 4: falsifiability and asymmetry are structurally satisfied, but the gamma-collapse component of the prediction inherits the Check 1 equation error, while the breakthrough-time scaling component is independently verified correct"
    quoted_evidence:
      - "Near the enlargement threshold, the karst drift can be expanded as `A_k(b) ≈ r_k b(1-b/K_k)`, which is operator-equivalent to the stochastic logistic birth-death drift in gene-family space."
      - "mature hypogene conduit aperture distributions from different caves, when nondimensionalized by posterior `r_k` and `K_k`, should collapse onto the quasi-stationary gamma/negative-binomial family predicted by stochastic birth-death dynamics"
      - "psi_qs(b) is proportional to b^(alpha_q - 1) exp(-b/theta_q), with alpha_q = 2 r_k / sigma_b^2 and theta_q = sigma_b^2 K_k / (2 r_k)"
    stage_3_watch_items:
      - "Confirm whether birth-death or population-level Fokker-Planck framings, independent of the gene-family analogy, already exist in the hypogene karst/speleogenesis literature; the underlying template (logistic-drift Fokker-Planck with R approximately 1 criticality) is generic across population dynamics, epidemiology, ecology, and nucleation theory, which bears on novelty."
      - "Section 1 frames Silo A around phylogenies and inferred ancestral family sizes, but the Section 3 mathematics is a single-lineage birth-death-immigration process with no branching or speciation structure; verify the tree-based inference machinery referenced only in Section 4 is actually compatible with the Section 3 model as implied."
      - "Request the explicit algebra connecting the karst SDE's k1, k2, m, beta, rho_s parameters and the q(b) ∝ b^3 flow-feedback mechanism to the asserted logistic reduction A_k(b) ≈ r_k b(1-b/K_k); as written this step is asserted, not shown."
      - "R_k = kappa q_0^alpha S_0 / (beta b_0) introduces kappa, alpha, q_0, S_0 without tying them back to k1, k2, m, beta, rho_s defined earlier in Section 3; request the connecting derivation."
      - "Prior-art advisory (Check 4c): this specific gene-family/karst pairing is not one I recognize as an established analogy, but bibliometric search should also target whether population-process/Fokker-Planck approaches have been used within karst science on their own terms, since that mathematical skeleton is very widely used elsewhere."
  second_adversarial_review:
    reviewer_model: "OpenAI GPT-5.6 Luna"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-09"
    verdict: "REJECT"
    verdict_rationale: "The displayed gene-family master equation is internally inconsistent with the rate convention used immediately afterward, because its transition terms omit the copy-number factors required by the stated birth/death process and by the subsequent drift and diffusion coefficients."
    failed_checks: ["Check 1: The gene-family master equation does not implement the stated state-dependent per-copy duplication/loss process and is inconsistent with the subsequent definitions of A_g(n) and B_g(n)."]
    flagged_checks: ["Check 3: The boundary_conditions vector is only partially demonstrated because the entry asserts a lower absorbing boundary but does not supply an actual mathematical upper boundary condition; the upper saturation basin is an interior stable state, not itself a boundary condition."]
    quoted_evidence: ["In gene-family evolution, a common mechanistic description treats copy number as a continuous-time birth–death–immigration process. Let `P_n(t)` be the probability that a gene family has `n` copies at time `t`, with state-dependent duplication rate `d_n`, loss rate `l_n`, and innovation/immigration rate `η_n`. The master equation is:\n\n`math\n\\frac{dP_n}{dt}\n=\nd_{n-1}P_{n-1}\n+\nl_{n+1}P_{n+1}\n+\n\\eta_{n-1}P_{n-1}\n-\n\\left(d_n+l_n+\\eta_n\\right)P_n .\n`"]
    stage_3_watch_items: ["Check the claimed Dreybrodt-style aperture evolution law and the asserted gamma/negative-binomial quasi-stationary prediction against the published mathematical formulation.", "Check whether the proposed gene-family-to-karst transfer is genuinely distinct from existing stochastic birth–death or Fokker–Planck treatments of conduit enlargement."]
  third_adversarial_review:
    reviewer_model: "Google Gemini 3.1 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-09"
    verdict: "PASS"
    verdict_rationale: "The entry establishes a mathematically consistent correspondence between one-dimensional state-dependent Fokker-Planck population operators in gene-family evolution and karst conduit widening, supported by explicit differential operators, compatible vocabulary types, and concrete falsifiable scaling laws."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items:
      - "Examine whether the mean-field/independent-segment assumption in the karst aperture Fokker-Planck formulation adequately captures non-local flow redistribution and conduit competition in 3D hypogene networks."
      - "Survey the speleogenesis literature for existing applications of 1D stochastic differential equations or population balance models to aperture distributions."
  fourth_adversarial_review:
    reviewer_model: "Z.AI GLM-5.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-09"
    verdict: "FLAG"
    verdict_rationale: "Core Fokker-Planck isomorphism in Section 3 is mathematically sound across all three correspondence vectors, but the gamma quasi-stationary distribution predicted in Section 4 is inconsistent with the logistic drift dynamics stated in Section 3."
    failed_checks: []
    flagged_checks: ["Check 4: gamma QSD formula in Section 4 does not follow from the logistic Fokker-Planck operator stated in Section 3"]
    quoted_evidence: []
    stage_3_watch_items:
      - "Verify whether the gamma/negative-binomial QSD is a known approximation for logistic birth-death processes, or whether it requires linear (constant per-capita) dynamics with multiplicative noise"
      - "Check dimensional consistency of QSD parameters α_q = 2r_k/σ_b² and θ_q = σ_b²K_k/(2r_k) when b retains physical dimensions of length"
      - "Investigate whether the coarse-graining step from individual conduit SDE to population Fokker-Planck has been published in the karst hydrology literature"
      - "No prior-art recognition for this specific domain pairing from graduate textbooks"
  fifth_adversarial_review:
    reviewer_model: "Meta Muse Spark 1.1"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-09"
    verdict: "PASS"
    verdict_rationale: "All equations are consistently parabolic Fokker-Planck class with matching drift-diffusion structure, vocabulary mappings are type-compatible with explicit operator-role statements, all three correspondence vectors are demonstrated with equations and threshold derivations, and transfer is asymmetric with specific quantitative falsifiable predictions."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: []
  sixth_adversarial_review:
    reviewer_model: "DeepSeek DeepSeek V4 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-09"
    verdict: "PASS"
    verdict_rationale: "All four checks pass; the equations are valid and support the claimed Fokker‑Planck operator correspondence, the vocabulary matrix has no category errors, all three correspondence vectors are demonstrated, and the transfer prediction is asymmetric and falsifiable."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items:
      - "Probe whether the mapping of phylogenetic lineage to conduit segment (carrier of the state variable) is fully consistent with the Fokker‑Planck formalism when one is a temporal domain and the other a spatial object; verify that the coarse-graining to an aperture‑density population does not mask a domain mismatch."
  seventh_adversarial_review:
    reviewer_model: "xAI Grok 4.5 Fast"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-09"
    verdict: "PASS"
    verdict_rationale: "All four checks pass: equations are class-consistent Fokker-Planck operators with matching logistic drift structure, vocabulary mappings are type-compatible with explicit shared operator roles, all three listed vectors are demonstrated by the body equations and boundary analysis, and the transfer direction plus falsifiable predictions are specific and asymmetric."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: []
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ⚠*CONTROL*⚠ ENTRY 018

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
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-09

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The master equation, both Fokker-Planck operator forms, and the karst Langevin SDE are internally sound, but the Section 4 claim that aperture distributions "should collapse onto the quasi-stationary gamma/negative-binomial family predicted by stochastic birth-death dynamics," given as ψ_qs(b) ∝ b^(α_q−1)exp(−b/θ_q) with α_q = 2r_k/σ_b² and θ_q = σ_b²K_k/(2r_k), does not solve the entry's own logistic drift "A_k(b) ≈ r_k b(1-b/K_k)": a gamma (quasi-)stationary density is the signature of linear (CIR/Feller-type) drift, and the zero-current stationary solution for a logistic drift with the stated constant noise term is instead proportional to exp[(r_k/σ_b²)b² − (2r_k/3K_kσ_b²)b³] — a form with no power-law prefactor and a quadratic-minus-cubic exponent, not a gamma density.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All six pairs (duplication↔wall retreat, loss↔precipitation/clogging/collapse, carrying capacity↔undersaturation depletion, extinction↔abandonment/sealing, lineage↔flow path, likelihood↔likelihood) each specify a concrete shared mathematical role — e.g. "populate the same advective coefficient," "absorbing states at the lower boundary" — rather than resting on hedge-only language, and none matches a listed category-error pattern.
- **CHECK 3 (Correspondence Vector Support):** FLAG — governing_differential_operator is demonstrated via the matching Fokker-Planck advection-diffusion operator forms in Section 3; instability_mechanism is demonstrated via the explicit R_g = d_0/l_0 and R_k = κq_0^αS_0/(βb_0) threshold ratios and the stated R≈1 criticality condition in Section 3; boundary_conditions is only asserted in prose across Sections 1–3 (absorbing lower boundary, saturating upper region) with no explicit boundary-condition equation, flux condition, or derivation given for either system.
- **CHECK 4 (Transfer and Falsifiability):** FLAG — The transfer direction (gene-family → karst) is plausibly asymmetric given phylogenetics' mature statistical-inference toolkit versus comparatively ad hoc karst inverse modeling, and the Section 4 prediction is specific and measurable rather than a template non-prediction, naming a distributional family, a lognormal alternative, and a linear-vs-logarithmic breakthrough-time test. However, the gamma/negative-binomial collapse component is the same formula found not to follow from the model's own logistic drift under Check 1 — only the breakthrough-time scaling component, E[T_B] ≈ (1/r_k)ln(K_k/b_0), is independently verifiable as a correct consequence of the stated logistic ODE. No canonical prior art is recognized for this specific gene-family/karst pairing, though the underlying birth-death/logistic-threshold Fokker-Planck template is generic across several fields (advisory only).

#### Stage 3 Watch Items
- Confirm whether birth-death or population-level Fokker-Planck framings, independent of the gene-family analogy, already exist in the hypogene karst/speleogenesis literature — the underlying mathematical template is generic across population dynamics, epidemiology, ecology, and nucleation theory, which bears on novelty.
- Section 1 frames Silo A around phylogenies and inferred ancestral family sizes, but Section 3's mathematics is a single-lineage birth-death-immigration process with no branching/speciation structure; verify the tree-based inference machinery referenced only in Section 4 is actually compatible with the Section 3 model as implied.
- Request the explicit algebra connecting the karst SDE's k1, k2, m, β, ρ_s parameters and the q(b) ∝ b³ flow-feedback mechanism to the asserted logistic reduction A_k(b) ≈ r_k b(1-b/K_k); as written this step is asserted, not shown.
- R_k = κq_0^αS_0/(βb_0) introduces κ, α, q_0, S_0 without tying them back to k1, k2, m, β, ρ_s defined earlier in Section 3; request the connecting derivation.
- Prior-art advisory: this specific gene-family/karst pairing is not one recognized as an established analogy, but bibliometric search should also target whether population-process/Fokker-Planck approaches have been used within karst science on their own terms.

### Second Adversarial Review
**Reviewer:** OpenAI GPT-5.6 Luna
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-09

#### Results by Check
* **CHECK 1 (Equation Validity):** FAIL — The gene-family master equation omits the copy-number factors implied by the stated birth–death process and by the later definitions `A_g(n) = [d(n)-l(n)]n + η(n)` and `B_g(n) = [d(n)+l(n)]n + η(n)`, so the displayed master equation does not generate the Fokker–Planck coefficients subsequently claimed.
* **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The paired terms are generally compatible state variables, processes, boundaries, or inference objects, and their role descriptions identify concrete shared structures rather than relying solely on analogy.
* **CHECK 3 (Correspondence Vector Support):** FLAG — `governing_differential_operator` is demonstrated by the two Fokker–Planck equations and `instability_mechanism` by the threshold parameters and growth/decay discussion in Section 3, but `boundary_conditions` is only partially demonstrated because the lower absorbing boundary is stated without an explicit boundary condition and the purported upper “saturation” is a stable state rather than a mathematical boundary condition.
* **CHECK 4 (Transfer and Falsifiability):** PASS — The stated transfer is directionally asymmetric in the entry's framing, and the prediction supplies measurable distributional collapse and breakthrough-time scaling criteria that could fail; no prior-art recognition is used as a rejection.

#### Stage 3 Watch Items
* Verify the published formulation and provenance of the claimed Dreybrodt-style aperture evolution equation.
* Verify whether the gamma/negative-binomial quasi-stationary distribution and logarithmic breakthrough-time scaling actually follow from the proposed stochastic logistic model rather than being asserted separately.
* Probe for prior art on stochastic birth–death/Fokker–Planck formulations of karst conduit enlargement and on gene-family-to-geophysical population-process analogies.

### Third Adversarial Review
**Reviewer:** Google Gemini 3.1 Pro
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-09

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both domains are governed by one-dimensional parabolic Fokker–Planck/continuity operators modeling size-dependent drift and diffusion with absorbing lower boundaries and upper saturation dynamics.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All paired terms map equivalent mathematical object types (rates to rates, boundary states to boundary states, and likelihood functionals to likelihood functionals) without category errors or unsupported hedge language.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three claimed correspondence vectors (`governing_differential_operator`, `boundary_conditions`, and `instability_mechanism`) are explicitly derived and demonstrated with matching functional forms in Section 3.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The methodological transfer direction is properly asymmetric toward the data-sparse inverse problem in hypogene speleogenesis, and Section 4 provides rigorous, falsifiable functional forms (Gamma aperture distribution collapse and logarithmic breakthrough time scaling).

#### Stage 3 Watch Items
- Examine whether the mean-field/independent-segment assumption in the karst aperture Fokker–Planck formulation adequately captures non-local flow redistribution and conduit competition in 3D hypogene networks.
- Survey the speleogenesis literature for existing applications of 1D stochastic differential equations or population balance models to aperture distributions.

### Fourth Adversarial Review
**Reviewer:** Z.AI GLM-5.2
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-09

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — All equations in Section 3 are correctly stated and of matching class. The discrete master equation is a standard birth-death-immigration equation with consistent transition rates. The diffusion approximation correctly yields $A_g(n) = [d(n)-l(n)]n + \eta(n)$ and $B_g(n) = [d(n)+l(n)]n + \eta(n)$. The karst SDE combines a Dreybrodt-style dissolution law with stochastic noise, and the coarse-grained Fokker-Planck is parabolic, matching the gene-family diffusion approximation. Both Fokker-Planck equations share the same operator structure: $\partial_t p = -\partial_x[A(x)p] + \frac{1}{2}\partial_{xx}[B(x)p]$. The logistic drift approximation $A_k(b) \approx r_k b(1-b/K_k)$ is explicitly stated as a near-threshold expansion, not an identity.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All six vocabulary mappings pair compatible mathematical types: rates ↔ rates (duplication/dissolution, loss/clogging), boundary conditions ↔ boundary conditions (extinction/sealing), saturation mechanisms ↔ saturation mechanisms (dosage-balance/undersaturation-depletion), structural carriers ↔ structural carriers (lineage/conduit-segment), and inverse-problem likelihoods ↔ inverse-problem likelihoods. Each operator-role explanation names the shared mathematical structure (advective drift coefficient, absorbing boundary, logistic nonlinearity, first-passage conditioning) rather than relying on hedged analogy.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed vectors are demonstrated in the body. `governing_differential_operator` is supported by the paired Fokker-Planck equations in Section 3 with matching operator forms. `boundary_conditions` is supported by the discussion of absorbing loss at zero (extinction/sealing) and saturating upper boundary (carrying capacity/flow-competition limit) in both Sections 1 and 3. `instability_mechanism` is supported by the threshold parameters $\mathcal{R}_g = d_0/l_0$ and $\mathcal{R}_k = \kappa q_0^\alpha S_0/(\beta b_0)$ with the stated critical condition $R \approx 1$ separating decay from runaway growth.
- **CHECK 4 (Transfer and Falsifiability):** FLAG — The transfer direction (gene-family → karst) is genuinely asymmetric: gene-family evolution possesses mature inverse-toolkit machinery (phylogenetic pruning, HMM ancestral reconstruction, Bayesian data augmentation) while hypogene karst inverse inference is described as comparatively ad hoc. The prediction is falsifiable, naming specific measurable outcomes (distributional collapse under nondimensionalization, logarithmic vs. linear breakthrough-age scaling) and explicit falsification conditions. However, the gamma quasi-stationary distribution formula in Section 4 — "$\psi_{\mathrm{qs}}(b) \propto b^{\alpha_q-1} \exp(-b/\theta_q)$, $\alpha_q = 2r_k/\sigma_b^2$, $\theta_q = \sigma_b^2 K_k/(2r_k)$" — does not follow from the logistic Fokker-Planck dynamics stated in Section 3. The stationary distribution of the Fokker-Planck with logistic drift $A_k(b) = r_k b(1-b/K_k)$ and constant diffusion $B = \sigma_b^2$ is $\exp(r_k b^2/\sigma_b^2 - 2r_k b^3/(3\sigma_b^2 K_k))$, not a gamma density. The gamma/negative-binomial quasi-stationary family arises for linear birth-death-immigration dynamics (constant per-capita rates with multiplicative noise $B \propto x$), which is a different operator from the logistic drift with constant diffusion that the entry explicitly states. Additionally, the parameters $\alpha_q = 2r_k/\sigma_b^2$ and $\theta_q = \sigma_b^2 K_k/(2r_k)$ exhibit dimensional inconsistency if $b$ retains physical dimensions: $\alpha_q$ has dimensions $[\text{length}^{-2}]$ rather than being dimensionless, and $\theta_q$ has dimensions $[\text{length}^3]$ rather than $[\text{length}]$. No prior-art recognition for this domain pairing.

#### Stage 3 Watch Items
- Verify whether the gamma/negative-binomial quasi-stationary distribution is a known approximation for logistic (state-dependent) birth-death processes in the population genetics literature, or whether it is exact only for linear birth-death-immigration dynamics. If the latter, the entry's Section 4 prediction conflates two different operator classes.
- Check dimensional consistency of the QSD parameters $\alpha_q = 2r_k/\sigma_b^2$ and $\theta_q = \sigma_b^2 K_k/(2r_k)$. If $r_k$ is $[\text{time}^{-1}]$, $\sigma_b$ is $[\text{length}/\sqrt{\text{time}}]$, and $K_k$ is $[\text{length}]$, then $\alpha_q$ is not dimensionless and $\theta_q$ has dimensions $[\text{length}^3]$ rather than $[\text{length}]$. Clarify whether the formula is intended to use nondimensionalized variables.
- Investigate whether the coarse-graining step from individual conduit SDE to population-level Fokker-Planck has been published in the karst hydrology literature, and whether the resulting drift $A_k(b)$ retains the logistic form claimed.
- Confirm that the gene-family diffusion coefficient $B_g(n) = [d(n)+l(n)]n + \eta(n)$ (approximately multiplicative for large $n$) and the karst diffusion coefficient $B_k(b) = \sigma_b^2$ (constant, from additive noise) do not undermine the claimed operator equivalence. The operators are structurally parallel but not identical in their diffusion structure, which affects the QSD form.
- No prior-art recognition identified for this specific domain pairing from graduate textbooks or widely-cited reviews.

### Fifth Adversarial Review
**Reviewer:** Meta Muse Spark 1.1
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-09

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both sides present state-dependent Fokker-Planck operators ∂_t p = -∂[A p] + 1/2 ∂_{nn}[B p] with logistic-like drift A_g ≈ and A_k ≈ r_k b(1-b/K_k), same parabolic class, and Dreybrodt-style dissolution SDE is correctly attributed to karst domain.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All six pairings map compatible types (positive drift ↔ positive drift, negative drift ↔ negative drift, saturation parameter ↔ saturation mechanism, absorbing state ↔ absorbing state, state-carrier ↔ state-carrier, likelihood functional ↔ likelihood functional) with explicit shared operator roles, no dimensional, domain-time, or rate-position category errors.
- **CHECK 3 (Correspondence Vector Support):** PASS — governing_differential_operator demonstrated by the two Fokker-Planck equations in Section 3; boundary_conditions demonstrated by absorbing boundary at n=0 / b=0 and upper saturating basin K in Sections 1 and 3; instability_mechanism demonstrated by dimensionless thresholds R_g = d_0/l_0 and R_k = κ q_0^α S_0 / β b_0 with critical condition R=1 separating extinction/sealing from runaway expansion in Section 3.
- **CHECK 4 (Transfer and Falsifiability):** PASS — Asymmetry is genuine: mature inverse birth-death likelihood / pruning / HMM toolkit in gene-family evolution versus ad hoc forward-only inversion in hypogene karst; falsifiability is quantitative: predicts gamma collapse ψ_qs(b) ∝ b^{α_q-1} exp(-b/θ_q) with α_q = 2r_k/σ_b^2 and logarithmic first-passage E[T_B] ≈ 1/r_k ln(K_k/b_0), with explicit falsifiers (lognormal non-collapse, linear path-length scaling). No canonical textbook prior-art recognized.

#### Stage 3 Watch Items
- None identified.

### Sixth Adversarial Review
**Reviewer:** DeepSeek DeepSeek V4 Pro
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-09

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The gene‑family birth‑death master equation and its Fokker‑Planck diffusion approximation, together with the karst aperture evolution Langevin equation and the coarse‑grained Fokker‑Planck equation, all correctly model the claimed domains; the operator is consistently parabolic and the logistic‑drift threshold condition is explicitly given, supporting the structural correspondence without equation‑class mismatch.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All six mapping pairs assign objects of compatible mathematical type and the operator‑role explanations name specific shared structures (e.g., advective drift coefficient, absorbing boundary, saturating nonlinear drift) rather than mere hedged analogy.
- **CHECK 3 (Correspondence Vector Support):** PASS — The three listed vectors (governing_differential_operator, boundary_conditions, instability_mechanism) are each demonstrated in Section 3: the Fokker‑Planck operator appears on both sides, the absorbing lower boundary and upper saturation basin are described, and the instability is expressed via dimensionless threshold numbers R_g and R_k with the critical condition R≈1.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction (gene‑family evolution → hypogene karst) is asymmetrically justified by the maturity of inverse phylogenetic likelihood tools vs. ad‑hoc karst inversion; the falsifiable prediction specifies a quantitative distribution collapse to a gamma/negative‑binomial family and a logarithmic first‑passage scaling, with clear falsification conditions (lognormal non‑collapse, linear path‑length scaling). No canonical prior art is recognized from graduate‑textbook analogies.

#### Stage 3 Watch Items
- Examine whether the phylogenetic‑lineage ↔ conduit‑segment mapping, which treats a temporal lineage as analogous to a spatial conduit object, remains robust when the Fokker‑Planck operator uses only time as the independent variable and the conduit segment is not a coordinate in the population PDE.

### Seventh Adversarial Review
**Reviewer:** xAI Grok 4.5 Fast
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-09

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both sides reduce to the same Fokker–Planck form with logistic-like drift \(A(n)\) or \(A(b)\), diffusion coefficient, absorbing lower boundary, and saturating upper basin; the displayed master-equation and aperture-evolution equations correctly generate the claimed operators.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — Every paired token is of compatible mathematical type (increment rates, saturation mechanisms, absorbing states, process carriers, likelihood functionals) and the Operator Role statements name shared structures (advective coefficients, absorbing boundaries, nonlinear drift saturation) rather than mere analogy.
- **CHECK 3 (Correspondence Vector Support):** PASS — governing_differential_operator is shown by the explicit Fokker–Planck operators and the logistic expansion of \(A_k(b)\); boundary_conditions by the absorbing-zero and saturating-upper descriptions; instability_mechanism by the shared threshold parameters \(\mathcal{R}_g\) and \(\mathcal{R}_k\) with critical value 1.
- **CHECK 4 (Transfer and Falsifiability):** PASS — Transfer direction is asymmetrically justified by the relative maturity of inverse birth–death toolkits versus ad-hoc karst inversion; the prediction supplies concrete distributional collapse and first-passage scaling that can be measured and potentially falsified.

#### Stage 3 Watch Items
None identified.