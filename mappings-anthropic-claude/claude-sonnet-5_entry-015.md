---
sid_metadata:
  entry_id: "SID-015"
  schema_version: "1.0-production"
  maturity_stage: "candidate"
provenance:
  company: "Anthropic"
  model_family: "Claude"
  model_version: "Sonnet 5"
  generation_timestamp: "2026-07-28"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "actuarial-ruin-theory"
  domain_b: "plasma-physics"
  structural_family: "integro-differential-characteristic-equations / complex-root-spectral-theory"
  triple_correspondence_vectors:
    - "governing_differential_operator"
    - "instability_mechanism"
    - "numerical_solution_family"
    - "dimensionless_similarity_parameter"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language / historically_isolated_communities — a discrete jump-claims stochastic process and a continuum electromagnetic kinetic field theory look nothing alike on the surface, which hides the shared complex-analytic root-finding structure underneath"
prior_discovery_metrics:
  # NOTE: All scores below are model-generated self-assessments produced at generation time.
  # They reflect the generating model's internal pattern-matching confidence, not externally
  # validated measurements. They should be used as triage-ranking signals for human reviewers
  # deciding which entries to prioritize for Stage 2 bibliometric validation — not as evidence
  # that the isomorphism is real or novel.
  structural_isomorphism_score: 7.0
  vocabulary_divergence_score: 9.0
  expected_methodological_transfer_score: 6.5
  community_separation_score: 9.5
  representation_mismatch_score: 8.5
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 6.0
    uncertainty: "±1.5"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "low"
  primary_failure_risk: "the load-bearing mechanism (finding an exponential rate by Laplace/Fourier-transforming a linear governing equation) is a broadly-instantiated applied-math motif, not unique to these two fields; the entry only earns its novelty on the narrower claim that Nyquist/Penrose-style root-counting specifically is un-imported into actuarial numerics, not on the general transform trick"
  bibliometric_validation: "pending"
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY 015

## 1. CROSS-SILO SYSTEM DEFINITION
*   **Silo A (Field 1):** Actuarial ruin theory — the classical and generalized Cramér–Lundberg collective risk model, specifically the search for the Lundberg adjustment coefficient (or, for matrix-exponential/phase-type claim severities, the full set of roots of the generalized Lundberg equation) governing the exponential decay rate of the infinite-horizon ruin probability ψ(u).
*   **Silo B (Field 2):** Collisionless kinetic plasma theory — Landau's treatment of the linearized Vlasov–Poisson system, and the plasma dispersion relation whose complex roots ω(k) give the oscillation frequency and growth/damping rate of electrostatic (Langmuir) wave perturbations.
*   **Mathematical Isomorphism:** Both fields collapse a linear integro-differential governing equation to a scalar characteristic equation by inserting an exponential trial solution, equating a linear "streaming" term against the transform of a kernel distribution evaluated at the trial rate (governing_differential_operator); both must resolve cases where that transform isn't safely evaluable on the real axis — an unbounded moment generating function for heavy-tailed claims, or a pole sitting on the velocity-integration contour — via complex-plane analytic continuation (instability_mechanism); and only the mature field has turned this into a routine, closed-form-free procedure for locating and counting *every* relevant root rather than just the dominant one (numerical_solution_family).

## 2. DIAGNOSTIC VOCABULARY MATRIX
*   **Lundberg adjustment coefficient R** (real root of `cR = λ(M_X(R) − 1)`) ↔ **Complex mode frequency ω = ω_r + iγ** (root of the plasma dielectric function ε(k,ω) = 0)
    *   *Operator Role:* Both are roots of a scalar characteristic equation produced by substituting an exponential trial solution into the field's governing linear integro-differential equation. The purely-real ruin exponent is the degenerate, non-oscillatory special case of the general complex "rate" object plasma theory treats as the default.
*   **Claim-size moment generating function M_X(r) = E[e^{rX}]** ↔ **Velocity-space integral ∫ (∂f₀/∂v)/(ω − kv) dv inside ε(k,ω)**
    *   *Operator Role:* Both are transforms of the field's "microscopic" kernel distribution (claim-severity density vs. equilibrium velocity distribution), evaluated at the trial rate to close the characteristic equation — and both can hit an obstruction (unbounded MGF for subexponential claims; a pole sitting directly on the integration path at the wave's phase velocity) that blocks a naive real-axis evaluation.
*   **Net profit / safety loading θ = (c − λμ)/(λμ) > 0** ↔ **Marginal-stability sign condition (e.g. the Penrose criterion)**
    *   *Operator Role:* Each is a single dimensionless comparison deciding whether the relevant root sits in the physically meaningful regime at all — θ>0 is exactly the condition for Lundberg's equation to admit a genuine positive real R; the plasma threshold is exactly the condition for the dispersion relation's root to cross into growing (unstable) territory.
*   **Wiener–Hopf factorization of the risk/queueing process** ↔ **Landau contour deformation + Nyquist/Penrose winding-number diagram**
    *   *Operator Role:* Both are complex-analytic machinery for transforms that can't be trusted on the real axis alone. The actuarial/queueing side, by its own literature's admission, mostly stops at existence-and-rough-count arguments (Rouché's theorem for polynomial cases); the plasma side has a mature, numerically robust, closed-form-free procedure already re-derived and exported to at least three unrelated fields when they hit the same root-counting problem.

## 3. CORE MATHEMATICAL PARALLELISM
Ruin theory models an insurer's surplus as the jump process

```math
U(t) = u + ct - \sum_{i=1}^{N(t)} X_i
```

where u is initial capital, c the premium rate, N(t) a Poisson(λ) claim-arrival process, and X_i i.i.d. claim severities. Under the net profit condition c > λE[X], the ruin probability ψ(u) = P(inf_{t≥0} U(t) < 0) satisfies Lundberg's inequality ψ(u) ≤ e^{−Ru}, where the adjustment coefficient R is the unique positive root of

```math
\lambda + cR = \lambda M_X(R), \qquad M_X(r) = \mathbb{E}\!\left[e^{rX}\right]
```

found by seeking an exponential-form solution to the underlying renewal/integro-differential ruin equation. For matrix-exponential (PH(n)) severities this generalizes to a higher-order characteristic equation with several roots, some non-real, whose sub-dominant terms are already known in the literature to sharpen the single-exponential approximation at moderate u — but which actuarial numerics locates, when at all, by scalar root search rather than any systematic complex-plane scan.

Plasma theory models small perturbations of a collisionless electron plasma via the linearized Vlasov–Poisson system: writing f = f₀(v) + f₁(x,v,t) and Fourier–Laplace transforming in space and time reduces the dynamics to requiring the dielectric function vanish,

```math
\varepsilon(k,\omega) = 1 + \frac{4\pi e^2}{m_e k}\int_{L}\frac{\partial f_0/\partial v}{\omega - kv}\,dv = 0,
```

with contour L deformed below the pole at v = ω/k — the Landau prescription — whenever the naive real-axis integral isn't analytic where the physically relevant root lives. The complex root ω = ω_r + iγ gives the wave frequency and its damping (γ<0) or growth (γ>0) rate. Both equations are the same *kind* of object — a kernel transform, evaluated at a trial rate, set against a linear term — but where Lundberg's equation is typically asked only "does the dominant real root exist," the dispersion relation is routinely asked "how many roots exist, and where, across the whole half-plane," and plasma physics answers that harder question with dedicated machinery (Section 4).

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
*   **Preferred Transfer Direction:** Kinetic plasma theory (Landau/Nyquist spectral root-finding) → actuarial ruin theory (generalized/matrix-exponential Lundberg-equation root-finding).
*   **Asymmetric Maturity Rationale:** Missing an unstable root is a first-order physical error in plasma physics, so the field built a numerically robust, closed-form-free pipeline — Landau's contour prescription, then the Nyquist/Penrose winding-number criterion, which counts every root with γ>0 via a contour integral without ever solving ε=0 explicitly. This pipeline works for arbitrary, even numerically-tabulated f₀, and has already been re-derived in at least three unrelated fields (solar-wind turbulence, QCD quark–gluon plasma, neutrino "fast-flavor" oscillations) when they hit the same root-counting problem — direct evidence the machinery is portable, not plasma-specific folklore. Actuarial ruin theory has no comparable tool: multiple, sometimes-complex roots of the generalized Lundberg equation are already documented for PH(n) claim models, and the neighboring queueing-theory literature explicitly flags complex root/pole location for the analogous Wiener–Hopf problem as difficult in general — but the standard response on both sides is a scalar dominant-root search, not a winding-number scan.
*   **Target Bottleneck Mitigation:** Hypothesis — reformulating the generalized Lundberg equation for matrix-exponential/Coxian claim-severity models as a plasma-style dispersion function D(r), and scanning it with a Nyquist/Penrose-style contour integral instead of scalar Newton iteration, would reliably enumerate every root of D(r)=0 in a target half-plane — including complex sub-dominant roots already known to exist in PH(n) models — without requiring D to be a low-degree polynomial.
*   **Falsifiable Prediction:** For a benchmark family of matrix-exponential/Coxian ruin models with a known exact ψ(u), a multi-exponential approximation built from every root a Nyquist-style scan locates should show measurably lower relative error at moderate (non-asymptotic) u than the standard single-root approximation — and, distinctly, the winding number should be able to *certify* whether a conventional Newton search actually found every relevant root, which the scalar approach cannot self-verify. Both halves are directly checkable against models with published closed-form solutions.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
*   `"adjustment coefficient" AND "Lundberg equation" AND "multiple roots"`
*   `"Landau damping" AND "Nyquist criterion" AND "dispersion relation"`