---
sid_metadata:
  entry_id: "SID-018"
  schema_version: "1.0-production"
  maturity_stage: "candidate"
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