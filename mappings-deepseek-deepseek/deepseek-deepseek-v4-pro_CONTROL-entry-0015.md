---
sid_metadata:
  entry_id: "CONTROL-SID-0015"
  schema_version: "2.0-control"
  maturity_stage: "adversarial-flagged"
provenance:
  company: "DeepSeek"
  model_family: "DeepSeek"
  model_version: "V4 Pro"
  generation_timestamp: "2026-08-17"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "nematic-liquid-crystal-director-dynamics"
  domain_b: "neural-field-pattern-formation"
  structural_family: "nonconvex-gradient-flow-pattern-formation"
  triple_correspondence_vectors:
    - "shared_nonconvex_lyapunov_gradient_descent"
    - "shared_typeI_finite_wavenumber_bifurcation_threshold"
    - "shared_boundary_quantized_mode_spectrum"
discovery_rationale:
  why_not_obvious: "incompatible_ontologies_and_distinct_disciplinary_language"
prior_discovery_metrics:
  structural_isomorphism_score: 8.2
  vocabulary_divergence_score: 9.1
  expected_methodological_transfer_score: 7.8
  community_separation_score: 9.4
  representation_mismatch_score: 7.5
  expected_transfer_effort: "high"
  novelty_prior:
    estimate: 8.4
    uncertainty: "±1.0"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "constitutive_law_mismatch_between_nonlocal_synaptic_kernel_and_local_nematic_elasticity"
  bibliometric_validation: "pending"
  first_adversarial_review:
    reviewer_model: "Anthropic Claude Sonnet 5"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "REJECT"
    verdict_rationale: "Section 4's falsifiable-prediction worked example asserts the homogeneous state is u0=0 (f'(0)=1), but the entry's own fixed-point equation combined with the stated kernel (W0=1) and I=0 forces u0=f(u0), and since f(0)=0.5≠0, u0≠0, so the claimed instability τλ(k_c)=0.1906>0 is computed at the wrong linearization point and does not follow from the entry's own mathematics."
    failed_checks: ["Check 1: Falsifiable-prediction worked example (Section 4) miscomputes the homogeneous state as u0=0 with f'(0)=1, contradicting the entry's own fixed-point equation from Section 3 given the stated kernel and I=0, which inverts the sign of the claimed instability."]
    flagged_checks:
      - "Check 1: Discrete periodic mode formula k_m=2πm/L (Sections 2 and 3) is inconsistent with the stated periodic domain x∈[-L,L] (length 2L); periodicity on that domain implies k_m=πm/L."
      - "Check 1: The Lyapunov potential Φ'(u)=uf'(u) (Section 3) does not reproduce the stated Amari equation's +I term via the claimed relation τ∂u/∂t=-(1/f'(u))δL/δu; a term such as Φ'(u)=(u-I)f'(u) would be needed for consistency with general I."
      - "Check 4a: The asymmetric-maturity claim (nematic energy-stable numerics vs. explicit-Euler-dominated neural-field numerics) is specific and plausible from the text but not independently verifiable without literature search."
    quoted_evidence:
      - "the homogeneous state has f′(0)=1"
      - "zero input I=0"
      - "w(x)=2g(x;1)-g(x;2)"
      - "u0=W0 f(u0)+I, W0=∫w"
    stage_3_watch_items:
      - "The general amplitude-equation / Type-I finite-wavenumber bifurcation framework used to unify pattern-forming systems near threshold is a well-established lens in the nonequilibrium pattern-formation literature (cf. Cross & Hohenberg-style reviews); confirm whether the specific nematic-LC↔neural-field pairing has independent prior art beyond this general framework."
      - "Recheck Section 4's Falsifiable Prediction: with the stated kernel and I=0, the entry's own fixed-point equation gives u0≈0.98 (not 0) and f'(u0)≈0.076 (not 1), making τλ(k_c)≈-0.91 (stable) rather than the claimed +0.19 (unstable); determine whether adjusted parameters (e.g. a nonzero I chosen so u0=0, or re-deriving at the true u0) can recover a genuine, correctly-computed instability for a viable falsifiable test."
      - "Confirm the periodic-domain mode-quantization convention throughout: for x∈[-L,L] (length 2L), periodic modes should be k_m=πm/L; the entry uses k_m=2πm/L."
      - "Verify against the numerical-methods literature whether energy-stable convex-splitting/SAV schemes are indeed comparatively more established for nematic/Landau-de Gennes gradient flows than for Amari neural-field equations, as claimed in the asymmetric-transfer rationale."
  second_adversarial_review:
    reviewer_model: "Alibaba Qwen 3.8 Max"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "REJECT"
    verdict_rationale: "The Section 4 prediction evaluates the neural homogeneous state at u=0 with I=0 for a logistic f, contradicting the entry's own equilibrium condition u0=W0 f(u0)+I and making the claimed growth rate and explicit-Euler amplification unsupported."
    failed_checks: ["Check 4: falsifiable prediction uses a homogeneous state inconsistent with the entry's own equilibrium equation"]
    flagged_checks: ["Check 1: displayed Lyapunov functional does not generate the displayed Amari equation with nonzero I as written", "Check 1: periodic mode formula k_m=2πm/L is inconsistent with the stated interval [-L,L] having period 2L"]
    quoted_evidence: ["The homogeneous state u0 satisfies u0=W0 f(u0)+I, W0=∫w.", "and sigmoid f(u)=1/(1+e^{-4u}), the homogeneous state has f′(0)=1", "zero input I=0"]
    stage_3_watch_items: ["Search for prior work on energy-stable, convex-splitting, or Lyapunov-preserving time integrators specifically for Amari-type neural fields.", "Verify whether the Fréedericksz-transition coordinate convention and electric-field direction in Section 3 match the sin^2(theta) electric term.", "Assess bibliometric overlap between nonlocal gradient-flow neural field models and liquid-crystal director gradient flows."]
  third_adversarial_review:
    reviewer_model: "Google Gemini 3.1 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "PASS"
    verdict_rationale: "The entry correctly identifies and mathematically derives the shared nonconvex gradient flow structure between nematic director dynamics and Amari neural fields, verifying all claims with correct equations and a concrete falsifiable prediction."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: []
  fourth_adversarial_review:
    reviewer_model: "Xiaomi MiMo V2.5 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "FLAG"
    verdict_rationale: "The gradient-flow equivalence claim for the neural field is inconsistent with the stated Amari equation when I≠0, though the remainder of the mathematical analysis is sound."
    failed_checks: []
    flagged_checks: ["Check 1: gradient flow relation does not reproduce the stated Amari equation when I≠0"]
    quoted_evidence:
      - "The Amari equation on a periodic domain x∈[-L,L] is τ∂u/∂t = −u + ∫w(x−y)f(u(y,t))dy + I"
      - "τ∂u/∂t = −(1/f′(u)) δL/δu"
      - "δL/δu = f′(u)[u − w*f]"
    stage_3_watch_items:
      - "The I-term inconsistency: the stated Amari equation includes +I but the Lyapunov functional L[u] with Φ′(u)=uf′(u) generates only the I=0 dynamics. The I term can be absorbed into a modified Φ, but the entry does not state this. Check whether published treatments of the Amari Lyapunov functional handle I identically or require modification."
      - "Verify whether the energy-stable discretization transfer from nematic gradient flows to neural-field integral equations has been published or proposed in any form; both communities are large and the specific convex-splitting recipe for the nonlocal Amari Lyapunov functional may exist."
  fifth_adversarial_review:
    reviewer_model: "Z.AI GLM-5.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "PASS"
    verdict_rationale: "All equations are correctly derived and attributed, vocabulary mappings are type-compatible with stated shared structure, all three correspondence vectors are demonstrated with explicit derivations, and the falsifiable prediction contains specific numerical thresholds with clear falsification criteria."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items:
      - "The continuum-limit scale bridge (Section 3) claims 'the same second-order operator family' via the moment expansion, but the specific kernel used in the falsifiable prediction (w=2g(·;1)−g(·;2)) has W₂=∫r²w(r)dr=2(1²)−(2²)=−2<0, making the neural-field diffusion coefficient μW₂/(2τ) negative (backward parabolic) while the nematic coefficient K/γ is positive (forward parabolic). The entry does not state that W₂>0 is required for an equation-class match. This does not affect the three claimed vectors, which are demonstrated through exact dispersion relations, but the human reviewer should assess whether the 'same operator family' claim in Section 1 is defensible under this sign discrepancy."
      - "The gradient-flow form τ∂ₜu=−(1/f′(u))δL/δu in Section 3 is valid only for I=0; the stated Lyapunov functional with Φ′(u)=uf′(u) does not include the input term I that appears in the Amari equation. The entry uses I=0 in its prediction (consistent), but does not explicitly state this restriction in the general framework. Reviewer should verify whether this omission affects the claimed universality of the gradient-flow correspondence."
      - "Stage 3 should verify whether the specific transfer of convex-splitting / energy-stable discretizations from liquid-crystal gradient flows to Amari neural fields has been previously proposed, as the general gradient-flow and convex-splitting frameworks are well-established in numerical analysis."
  sixth_adversarial_review:
    reviewer_model: "OpenAI GPT-5.6 Luna"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "REJECT"
    verdict_rationale: "The entry contains a genuine Lyapunov-functional error for the stated neural-field equation with nonzero input and does not demonstrate the listed Type-I finite-wavenumber bifurcation correspondence beyond a linear zero-crossing calculation."
    failed_checks: ["Check 1: The stated neural Lyapunov functional is not a Lyapunov functional for the displayed Amari equation when I is nonzero because its variational derivative omits the input term.", "Check 3: The listed shared_typeI_finite_wavenumber_bifurcation_threshold vector is not demonstrated as Type-I; the body establishes only a finite-wavenumber linear instability threshold, with no nonlinear bifurcation/amplitude analysis."]
    flagged_checks: ["Check 4: The asymmetric transfer rationale is asserted rather than internally demonstrated, although no backwards direction is established from the entry alone."]
    quoted_evidence: [""\tau\frac{\partial u(x,t)}{\partial t}=-u(x,t)+\int_{-L}^{L}w(x-y)f(u(y,t))dy+I" together with "\frac{\delta L}{\delta u}=f'(u)[u-w*f]" and "\tau\frac{\partial u}{\partial t}=-\frac{1}{f'(u)}\frac{\delta L}{\delta u}" — the displayed variational derivative and gradient-flow identity reproduce -u+w*f but omit the +I term from the stated Amari equation, so the claimed dL/dt≤0 result does not apply to the displayed equation for general nonzero I.", ""shared_typeI_finite_wavenumber_bifurcation_threshold" — the body derives "\tau\lambda(k)=-1+f'(u_0)\hat w(k)" and the zero-crossing condition "f'(u_0)\max_k\hat w(k)=1", but this establishes a linear finite-wavenumber instability threshold, not the Type-I bifurcation class; no nonlinear bifurcation or amplitude calculation establishes the claimed Type-I correspondence."]
    stage_3_watch_items: ["Probe the asserted nematic → neural-field maturity asymmetry and the claim that energy-stable discretizations are not a standard neural-field tool.", "Probe the recognition/novelty of the proposed nematic gradient-flow ↔ symmetric-kernel Amari gradient-flow correspondence.", "Check the periodic-domain convention: the entry states x∈[-L,L] but assigns Fourier modes k_m=2πm/L; for a period-2L domain the standard quantization would instead involve πm/L, so the numerical prediction's mode discretization should be scrutinized."]
  seventh_adversarial_review:
    reviewer_model: "Microsoft Copilot 1.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "PASS"
    verdict_rationale: "The entry's equations, linearizations, operator classes, and three listed correspondence vectors are mathematically consistent and each claimed vector is demonstrated in the body."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items:
      - "The short-range expansion of the Amari convolution to a diffusion operator is a standard continuum approximation; Stage 3 should check prior-art overlap with canonical neural-field → reaction-diffusion derivations."
      - "Verify the numerical evaluation in Section 4 (the stated k_c and \u005chat w(k_c) values) for transcription or rounding errors before experimental replication."
      - "Confirm that the proposed convex-splitting discretization applied to the nonlocal Amari functional preserves the exact discrete Lyapunov structure claimed (implementation details and discrete functional definition)."
  eighth_adversarial_review:
    reviewer_model: "xAI Grok 4.5 Fast"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "PASS"
    verdict_rationale: "All four checks pass with no mathematical inconsistencies, category errors, undemonstrated vectors, or non-falsifiable predictions identifiable from the entry text alone."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: ["Verify whether the short-range continuum limit of the Amari synaptic operator is routinely accepted as producing a second-order local operator of the same family as the one-constant Frank-Oseen Laplacian in the literature of either community.", "Confirm that energy-stable convex-splitting schemes for nonconvex Lyapunov functionals of the Amari type remain non-standard in the neural-field community relative to the nematic community."]
  ninth_adversarial_review:
    reviewer_model: "Meta Muse Spark 1.1"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "PASS"
    verdict_rationale: "All equations are domain-correct and class-matched as nonconvex parabolic gradient flows, vocabulary pairs are type-compatible with shared operator structure stated, all three correspondence vectors are demonstrated with explicit derivations and mode spectra, and transfer prediction is asymmetric and quantitatively falsifiable."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: []
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ⚠*CONTROL*⚠ ENTRY 0015

## 1. CROSS-SILO SYSTEM DEFINITION
*   **Silo A (Field 1):** Quasi-two-dimensional nematic liquid-crystal director relaxation in the one-constant Frank-Oseen limit, driven by an external electric field and exhibiting the Fréedericksz transition and director pattern formation.
*   **Silo B (Field 2):** Amari-type neural field pattern formation on a homogeneous periodic domain, exhibiting Turing-like pattern selection through nonlocal excitatory/inhibitory synaptic coupling.
*   **Mathematical Isomorphism:** Both are nonconvex dissipative gradient flows (`shared_nonconvex_lyapunov_gradient_descent`) whose boundary-quantized linear spectra undergo a finite-wavenumber instability when a dimensionless control parameter crosses zero (`shared_typeI_finite_wavenumber_bifurcation_threshold`); the explicit long-wavelength continuum limit of the neural synaptic integral operator produces the same second-order spatial operator family as the nematic Laplacian, providing the required scale bridge.

## 2. DIAGNOSTIC VOCABULARY MATRIX
*   θ(x,t) ↔ u(x,t)
    *   *Operator Role:* Scalar order-parameter fields. θ is the planar director angle obtained from the unit-vector director n=(cosθ,sinθ) after restriction to a single plane; u is the dimensionless neural activity field. Both appear as the argument of a nonconvex free-energy/Lyapunov functional and both are real scalar fields in the restricted models used here.
*   Frank-Oseen free energy F[θ] ↔ neural Lyapunov functional L[u]
    *   *Operator Role:* Nonconvex functionals whose first variation supplies the dissipative driving force: γ∂_tθ=−δF/δθ versus τ∂_tu=−(1/f′(u))δL/δu. Both are non-increasing along dynamics.
*   electric-field dimensionless control Π_A ↔ synaptic-gain dimensionless control Π_B
    *   *Operator Role:* Scalar bifurcation parameters defined by Π_A=ε0ΔεE²d²/(Kπ²)−1 and Π_B=f′(u0)max_k \hat w(k)−1. Both cross zero at the pattern-onset threshold.
*   strong-anchoring boundary modes nπ/d ↔ periodic Fourier modes 2πm/L
    *   *Operator Role:* Discrete spectral mode labels in the linearized operator. Dirichlet anchoring selects nπ/d; periodic neural-field boundary conditions select 2πm/L.

## 3. CORE MATHEMATICAL PARALLELISM

In a planar nematic cell of thickness d with strong planar anchoring, let θ(x,t) be the director angle. The one-constant Frank-Oseen free energy with an electric field along x is

```math
F[\theta]=\int_0^d\left[\frac{K}{2}(\partial_x\theta)^2-\frac{\epsilon_0\Delta\epsilon E^2}{2}\sin^2\theta\right]dx
```

Overdamped Ericksen-Leslie relaxation is

```math
\gamma\frac{\partial\theta}{\partial t}=-\frac{\delta F}{\delta\theta}
=K\partial_x^2\theta+\epsilon_0\Delta\epsilon E^2\sin\theta\cos\theta
```

with θ(0)=θ(d)=0. Linearizing around θ=0 gives

```math
\gamma\frac{\partial\theta}{\partial t}
=K\partial_x^2\theta+\epsilon_0\Delta\epsilon E^2\theta
```

The discrete modes are

```math
\theta_n(x,t)=a_n(t)\sin(k_nx),\quad k_n=\frac{n\pi}{d}
```

```math
\gamma\dot a_n=[\epsilon_0\Delta\epsilon E^2-Kk_n^2]a_n
```

The threshold is

```math
E_c^2=\frac{K}{\epsilon_0\Delta\epsilon}\left(\frac{\pi}{d}\right)^2
```

and the dimensionless control parameter is

```math
\Pi_A=\frac{\epsilon_0\Delta\epsilon E^2 d^2}{K\pi^2}-1
```

On the neural-field side, the Amari equation on a periodic domain x∈[-L,L] is

```math
\tau\frac{\partial u(x,t)}{\partial t}=-u(x,t)+\int_{-L}^{L}w(x-y)f(u(y,t))dy+I
```

with even kernel w and sigmoid f, f′>0. For symmetric w the Lyapunov functional is

```math
L[u]=-\frac12\iint w(x-y)f(u(x))f(u(y))\,dx\,dy+\int \Phi(u(x))\,dx
```

```math
\Phi'(u)=u f'(u)
```

Then

```math
\frac{\delta L}{\delta u}=f'(u)[u-w*f]
```

```math
\tau\frac{\partial u}{\partial t}=-\frac{1}{f'(u)}\frac{\delta L}{\delta u}
```

so dL/dt≤0. The homogeneous state u0 satisfies u0=W0 f(u0)+I, W0=∫w. Linearizing with u=u0+εv e^{λt+ikx} gives

```math
\tau\lambda(k)=-1+f'(u_0)\hat w(k)
```

where \hat w(k)=∫w(r)e^{-ikr}dr. Discrete periodic modes k_m=2πm/L give

```math
u(x,t)=\sum_m \hat u_m(t)e^{ik_m x}
```

```math
\tau\dot{\hat u}_m=[-1+f'(u_0)\hat w(k_m)]\hat u_m
```

The threshold is

```math
f'(u_0)\max_k\hat w(k)=1
```

and the dimensionless control parameter is

```math
\Pi_B=f'(u_0)\max_k\hat w(k)-1
```

The boundary-quantized spectra are termwise corresponding:

```math
k_n^{(A)}=\frac{n\pi}{d}
\quad\leftrightarrow\quad
k_m^{(B)}=\frac{2\pi m}{L}
```

and the linearized growth laws are scalar:

```math
\gamma \lambda_n^{(A)}=\epsilon_0\Delta\epsilon E^2-K(k_n^{(A)})^2
```

```math
\tau \lambda_m^{(B)}=-1+f'(u_0)\hat w(k_m^{(B)})
```

Thus both instabilities set in when the first discrete mode crosses zero.

Because the neural operator is nonlocal while the nematic operator is local, an explicit scale bridge is required. For short-range kernels,

```math
\int w(x-y)f(u(y))dy
=W_0 f(u)+\frac{W_2}{2}\partial_x^2 f(u)+O(\partial_x^4)
```

```math
W_0=\int w(r)dr,\quad W_2=\int r^2 w(r)dr
```

Linearizing f about u0 gives

```math
\tau\partial_t v =(\mu W_0-1)v+\frac{\mu W_2}{2}\partial_x^2 v,\quad \mu=f'(u_0)
```

which is the same second-order operator family as the nematic linearization:

```math
\partial_t\theta=\frac{K}{\gamma}\partial_x^2\theta+\frac{\epsilon_0\Delta\epsilon E^2}{\gamma}\theta
```

with coefficient map

```math
\frac{K}{\gamma}\leftrightarrow\frac{\mu W_2}{2\tau},\qquad
\frac{\epsilon_0\Delta\epsilon E^2}{\gamma}\leftrightarrow\frac{\mu W_0-1}{\tau}
```

This bridge is valid only in the low-wavenumber continuum limit and does not assert exact equality of the full nonlocal neural operator and the local nematic operator.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
*   **Preferred Transfer Direction:** nematic-liquid-crystal-director-dynamics → neural-field-pattern-formation
*   **Asymmetric Maturity Rationale:** The nematic community has mature, energy-stable discretizations for nonconvex Frank-Oseen and Landau-de Gennes gradient flows (convex splitting, scalar auxiliary variable methods, deflated continuation for multiple stationary states). The neural-field community has strong analytical methods for bump construction and linear Turing analysis, but its standard numerical toolkit for Amari equations is dominated by explicit Euler or fixed-point iteration, which does not preserve the nonlocal Lyapunov functional and imposes step-size restrictions. Energy-stable discretizations for symmetric-kernel Amari gradient flows are not a standard neural-field tool.
*   **Target Bottleneck Mitigation:** Transfer the nematic convex-splitting recipe to the neural Lyapunov functional L[u]. Split L into convex and concave parts in the firing-rate variable v=f(u), treat the convex part implicitly and the concave part explicitly. This yields an unconditionally gradient-stable time integrator for symmetric-kernel Amari fields, eliminating spurious pattern drift and allowing timesteps far beyond the explicit stability limit.
*   **Falsifiable Prediction:** For a one-dimensional Amari field on x∈[-20,20] with periodic boundaries, zero input I=0, kernel

```math
w(x)=2g(x;1)-g(x;2),\qquad
g(x;\sigma)=\frac{1}{\sqrt{2\pi\sigma^2}}e^{-x^2/(2\sigma^2)}
```

and sigmoid f(u)=1/(1+e^{-4u}), the homogeneous state has f′(0)=1 and the most unstable Fourier mode has

```math
k_c^2=\frac{2}{3}\ln2,\qquad
\hat w(k_c)=2^{2/3}-2^{-4/3}\approx1.1906
```

so τλ(k_c)=0.1906>0. The imported energy-stable scheme with timestep Δt=10τ must keep the discrete Lyapunov functional L_h non-increasing to within 10^{-12} over 1000 steps. The baseline explicit Euler scheme at the same timestep has amplification factor

```math
1+10\tau\lambda(k_c)=2.906
```

for the most unstable mode and therefore diverges or violates L_h monotonicity by more than 0.1. Falsification: if the energy-stable scheme's L_h increases by more than 10^{-12} in any step, or if explicit Euler remains bounded and monotone at Δt=10τ, the transfer hypothesis is rejected.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
*   `"Ericksen-Leslie" AND "Fréedericksz transition" AND "energy-stable" AND "gradient flow"`
*   `"Amari neural field" AND "Lyapunov functional" AND "Turing instability" AND "nonlocal"`
*   `"nematic liquid crystal" AND "neural field" AND "gradient flow" AND "finite-wavenumber instability"`

---

## ADVERSARIAL REVIEWS (Stage 2)

### First Adversarial Review
**Reviewer:** Anthropic Claude Sonnet 5
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-19

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — Section 4 states "the homogeneous state has f′(0)=1," but with the stated kernel w(x)=2g(x;1)-g(x;2) (giving W0=∫w=1) and "zero input I=0," the entry's own equation "u0=W0 f(u0)+I" forces u0=f(u0); since f(0)=1/(1+e^0)=0.5≠0, u0=0 is not a solution, so f'(u0)≠f'(0)=1 and the claimed τλ(k_c)=0.1906>0 does not follow (correct linearization at u0≈0.98 gives f'(u0)≈0.076 and τλ(k_c)≈-0.91, a stable mode); separately, "k_m=2πm/L" (Sections 2–3) is inconsistent with the stated domain x∈[-L,L], which implies k_m=πm/L.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All four mapped pairs (order-parameter fields, functionals, dimensionless control parameters, discrete mode labels) pair objects of compatible mathematical type with explicit, non-hedged structural roles rather than analogy language.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed vectors are demonstrated with equations/derivations in Section 3: shared_nonconvex_lyapunov_gradient_descent via the stated F[θ] and L[u] variational relations, shared_typeI_finite_wavenumber_bifurcation_threshold via the matched threshold and growth-rate formulas, and shared_boundary_quantized_mode_spectrum via the explicit kn/km expressions (the km formula itself contains the numerical error identified in Check 1, but the vector is genuinely demonstrated, not merely asserted).
- **CHECK 4 (Transfer and Falsifiability):** FLAG — Asymmetry: the stated direction (mature nematic energy-stable numerics → less-developed neural-field numerics) is specific and not obviously reversible from the text, but is unverifiable here without literature search. Falsifiability: the prediction is well-formed and specific (not a template non-prediction), but its worked numerical instantiation depends on the erroneous base-state computation identified in Check 1, so the concrete predicted outcome cannot be trusted as stated.

#### Stage 3 Watch Items
- The general amplitude-equation / Type-I finite-wavenumber bifurcation framework unifying pattern-forming systems near threshold is well established in the nonequilibrium pattern-formation literature (cf. Cross & Hohenberg-style reviews); check whether the specific nematic-LC↔neural-field pairing itself has independent prior art beyond this general framework.
- Recompute Section 4's Falsifiable Prediction using the entry's own fixed-point equation: with I=0 and the stated kernel, u0≈0.98 and f'(u0)≈0.076, giving τλ(k_c)≈-0.91 rather than the claimed +0.19; check whether adjusted parameters can recover a genuine, correctly-computed instability and a viable falsifiable test.
- Confirm the periodic-domain convention: for x∈[-L,L] (length 2L), periodic modes should be k_m=πm/L, not k_m=2πm/L as used throughout Sections 2–3.
- Verify against the numerical-PDE literature whether energy-stable convex-splitting/SAV schemes are in fact comparatively more mature for nematic/Landau-de Gennes gradient flows than for Amari neural fields, as the asymmetric-transfer claim asserts.

### Second Adversarial Review
**Reviewer:** Alibaba Qwen 3.8 Max
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** FLAG — the core local/nonlocal equations are broadly class-consistent, but the displayed Lyapunov functional does not generate the displayed Amari equation with +I unless an input term is added or I=0, and the periodic wavenumbers k_m=2πm/L are inconsistent with a period-2L interval [-L,L].
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — the paired tokens are mathematically compatible types (scalar fields to scalar fields, functionals to functionals, dimensionless controls to dimensionless controls, discrete mode labels to discrete mode labels).
- **CHECK 3 (Correspondence Vector Support):** PASS — Section 3 supplies gradient-flow equations for shared_nonconvex_lyapunov_gradient_descent, threshold/growth-rate equations for shared_typeI_finite_wavenumber_bifurcation_threshold, and explicit mode-wavenumber equations for shared_boundary_quantized_mode_spectrum, subject to the Check 1 flags.
- **CHECK 4 (Transfer and Falsifiability):** FAIL — the transfer direction is plausibly asymmetric, but the prediction states "zero input I=0" and "the homogeneous state has f′(0)=1" for f(u)=1/(1+e^{-4u}), whereas the entry's own condition u0=W0 f(u0)+I with W0=1 for the specified kernel gives u0=f(u0) and not u0=0; therefore the claimed τλ(k_c)=0.1906 and explicit-Euler amplification factor are not supported.

#### Stage 3 Watch Items
- Search for prior work on energy-stable, convex-splitting, or Lyapunov-preserving time integrators specifically for Amari-type neural fields.
- Verify whether the Fréedericksz-transition coordinate convention and electric-field direction in Section 3 match the sin^2(theta) electric term.
- Assess bibliometric overlap between nonlocal gradient-flow neural field models and liquid-crystal director gradient flows.

### Third Adversarial Review
**Reviewer:** Google Gemini 3.1 Pro
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-19

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The mathematical derivations, including the gradient-flow structure of the Amari equation using the specific Lyapunov functional and the long-wavelength continuum approximation, are entirely correct and properly match the nematic Frank-Oseen equations.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All mappings correctly pair objects of identical mathematical type (e.g., scalar dimensionless bifurcation parameters, identical discrete wavenumber mode indices).
- **CHECK 3 (Correspondence Vector Support):** PASS — All three correspondence vectors (`shared_nonconvex_lyapunov_gradient_descent`, `shared_typeI_finite_wavenumber_bifurcation_threshold`, `shared_boundary_quantized_mode_spectrum`) are explicitly demonstrated with corresponding equations and explicit derivations in Section 3.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The proposed methodological transfer is directionally sound (bringing energy-stable time integration methods from materials science to neural fields) and the falsifiable prediction is exemplary, providing concrete integration step sizes, an exact analytical threshold for the amplification factor, and a strict numerical tolerance for falsification.

#### Stage 3 Watch Items
- None identified.

### Fourth Adversarial Review
**Reviewer:** Xiaomi MiMo V2.5 Pro
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-19

#### Results by Check
- **CHECK 1 (Equation Validity):** FLAG — The entry states the Amari equation with external input I, then presents a Lyapunov functional L[u] with Φ′(u)=uf′(u) and claims τ∂u/∂t = −(1/f′(u))δL/δu, which upon substitution of δL/δu = f′(u)[u−w∗f] yields τ∂_t u = −u + w∗f(u), missing the +I term. The gradient-flow relation only reproduces the stated Amari equation when I=0. The subsequent linearization and bifurcation analysis are unaffected since I is absorbed into the equilibrium u₀, and the falsifiable prediction explicitly sets I=0, but the equivalence claim as written in the body is inconsistent for the general case.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All four paired mappings (θ↔u, F↔L, Π_A↔Π_B, boundary-quantized mode labels) connect objects of compatible mathematical type. Operator Role explanations identify specific shared mathematical structures (nonconvex functionals with first-variation driving forces, scalar bifurcation parameters crossing zero at onset, discrete spectral labels from boundary quantization) rather than hedged similarity assertions.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed vectors are demonstrated in the body with explicit equations: (1) `shared_nonconvex_lyapunov_gradient_descent` is established by the free-energy and Lyapunov-functional constructions and their first-variation gradient-flow relations; (2) `shared_typeI_finite_wavenumber_bifurcation_threshold` is established by the linearized growth-rate expressions γλ_n^(A) and τλ_m^(B) and the threshold conditions Π_A=0, Π_B=0; (3) `shared_boundary_quantized_mode_spectrum` is established by the explicit mode structures k_n=nπ/d and k_m=2πm/L. The scale bridge connecting the nonlocal synaptic operator to the local nematic Laplacian via Taylor expansion is explicitly derived and honestly limited to the low-wavenumber continuum regime.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction (nematic → neural) is genuinely asymmetric: the nematic community has mature energy-stable discretizations (convex splitting, SAV) that are absent from the standard neural-field toolkit. The falsifiable prediction is highly specific: a concrete system (1D Amari field, x∈[−20,20], periodic BCs, w(x)=2g(x;1)−g(x;2), f(u)=1/(1+e^{−4u})), concrete computed values (k_c²=(2/3)ln2, ŵ(k_c)≈1.1906, τλ(k_c)=0.1906), a concrete timestep (Δt=10τ), and explicit falsification criteria (L_h must be non-increasing to 10^{−12}; explicit Euler amplification factor 2.906 must diverge). No canonical prior-art analogy recognized for this specific domain pairing.

#### Stage 3 Watch Items
- The I-term gap: published treatments of Amari Lyapunov functionals for nonzero input should be checked to see whether I is conventionally absorbed into Φ or whether the gradient-flow claim is restricted to I=0 in the literature.
- Novelty probe: check whether the specific convex-splitting or SAV transfer from nematic Frank-Oseen computation to symmetric-kernel Amari neural fields has been proposed or published in either community.
- The nonlocal-to-local bridge (Taylor expansion of the synaptic kernel to second order) is standard in neural-field bifurcation analysis; confirm that the entry's framing of this as a novel scale bridge for the isomorphism is not overstating what is routine long-wavelength reduction.

### Fifth Adversarial Review
**Reviewer:** Z.AI GLM-5.2
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-19

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The Frank-Oseen free energy, Ericksen-Leslie relaxation, and linearized nematic equations are standard and correctly derived. The Amari equation, Lyapunov functional, and linearized dispersion relation are correctly stated. Both linearized equations are second-order linear PDEs of the form ∂ₜφ = D∂²ₓφ + rφ, supporting the claimed structural correspondence. The moment expansion (Section 3) is a valid Taylor/Moment expansion for even kernels. The coefficient map K/γ ↔ μW₂/(2τ) and ε₀ΔεE²/γ ↔ (μW₀−1)/τ is algebraically correct. All numerical computations in Section 4 were independently verified: k²_c = (2/3)ln 2, ŵ(k_c) = 2^(2/3) − 2^(−4/3) ≈ 1.1906, f′(0)=1, τλ(k_c)=0.1906, and Euler amplification factor 1+10(0.1906)=2.906 are all correct.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All four paired mappings are between compatible mathematical types: both θ and u are real scalar fields; both F and L are nonconvex functionals with explicitly stated first-variation structure; both Π_A and Π_B are dimensionless scalar bifurcation parameters crossing zero; both k_n=nπ/d and k_m=2πm/L are discrete spectral mode labels. No category errors identified.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed vectors are demonstrated in the body. `shared_nonconvex_lyapunov_gradient_descent` is demonstrated by the gradient-flow equations γ∂ₜθ=−δF/δθ and τ∂ₜu=−(1/f′(u))δL/δu with the non-increasing property stated (Section 3). `shared_typeI_finite_wavenumber_bifurcation_threshold` is demonstrated by the linearized growth rates γλ_n = ε₀ΔεE² − Kk²_n and τλ(k) = −1 + f′(u₀)ŵ(k), both crossing zero at a finite wavenumber with Π_A=0 and Π_B=0 (Section 3). `shared_boundary_quantized_mode_spectrum` is demonstrated by the explicit spectral correspondence k_n^(A)=nπ/d ↔ k_m^(B)=2πm/L (Section 3).
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction (nematic → neural field) is genuinely asymmetric: energy-stable discretizations (convex splitting, SAV) are mature in the liquid-crystal community but not standard for Amari equations. The falsifiable prediction names a specific kernel, specific sigmoid, specific timestep (Δt=10τ), specific measurable quantity (L_h change per step), specific threshold (10⁻¹²), and a two-pronged falsification criterion (energy-stable scheme violates monotonicity OR explicit Euler remains bounded). No canonical prior-art pairing recognized.

#### Stage 3 Watch Items
- **W₂ sign discrepancy in continuum-limit bridge:** The entry's Section 3 derives the moment expansion w*f(u) ≈ W₀f(u) + (W₂/2)∂²ₓf(u) and claims the result is "the same second-order operator family as the nematic linearization." However, for the specific kernel used in the falsifiable prediction (w(x)=2g(x;1)−g(x;2)), W₂ = ∫r²w(r)dr = 2(1²) − (2²) = −2 < 0. This makes the neural-field diffusion coefficient μW₂/(2τ) negative (backward parabolic, ill-posed) while the nematic coefficient K/γ is positive (forward parabolic, well-posed). The entry does not state that W₂ > 0 is required for the equation-class match. This does not affect the three claimed correspondence vectors (which are demonstrated through exact, non-approximate dispersion relations), but the human reviewer should assess whether the "same operator family" claim is defensible under this sign discrepancy, and whether the continuum-limit bridge is intended as a core claim or supplementary support.
- **Gradient-flow form requires I=0:** The Amari equation in Section 3 is stated with input I, but the Lyapunov functional (with Φ′(u)=uf′(u)) and gradient-flow form τ∂ₜu = −(1/f′(u))δL/δu are only valid when I=0. The entry uses I=0 in the falsifiable prediction (internally consistent), but does not explicitly state this restriction in the general framework presentation. The correct Lyapunov functional for I≠0 would require an additional −I∫f(u)dx term.
- **Prior-art probe:** Stage 3 should verify whether the specific transfer of convex-splitting methods from liquid-crystal gradient flows to Amari neural-field equations has been previously proposed. The general gradient-flow framework and convex-splitting methodology are well-established in numerical analysis; the novelty question concerns the specific cross-domain application claimed here.

### Sixth Adversarial Review
**Reviewer:** OpenAI GPT-5.6 Luna
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-19

#### Results by Check
* **CHECK 1 (Equation Validity):** FAIL — The displayed Amari equation contains `+I`, but the stated Lyapunov derivative `\frac{\delta L}{\delta u}=f'(u)[u-w*f]` and gradient-flow identity omit that input term, so the claimed `dL/dt≤0` is not valid for the displayed equation when `I\ne0`.
* **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The four displayed mappings pair compatible scalar fields, functionals, dimensionless controls, and wavenumbers/mode labels, with mathematical roles specified rather than relying solely on analogy.
* **CHECK 3 (Correspondence Vector Support):** FAIL — `shared_nonconvex_lyapunov_gradient_descent` is demonstrated by the two gradient-flow constructions, and `shared_boundary_quantized_mode_spectrum` is demonstrated by the discrete mode equations; however, `shared_typeI_finite_wavenumber_bifurcation_threshold` is not demonstrated as Type-I, because the body establishes only a finite-wavenumber linear zero-crossing and gives no nonlinear bifurcation/amplitude analysis establishing the Type-I class.
* **CHECK 4 (Transfer and Falsifiability):** PASS — The stated transfer direction is internally presented as asymmetric, and the prediction gives explicit timestep, Lyapunov-monotonicity, amplification-factor, and rejection thresholds that can produce outcomes contrary to the hypothesis; no prior-art determination is made at Stage 2.

#### Stage 3 Watch Items
* Probe the claimed maturity asymmetry between nematic numerical methods and standard neural-field numerical practice.
* Probe the proposed nematic gradient-flow ↔ symmetric-kernel Amari gradient-flow correspondence for prior art.
* Scrutinize the Fourier quantization: the entry uses `x∈[-L,L]` while stating `k_m=2πm/L`, which is inconsistent with a period-`2L` interpretation and affects the concrete finite-domain prediction.

### Seventh Adversarial Review
**Reviewer:** Microsoft Copilot 1.2
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-19

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The nematic and neural linearized equations are of the same parabolic reaction–diffusion class after the short-range kernel expansion; linearizations and growth-rate formulas are consistent and correctly derived from the stated free energy and Lyapunov functional.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — Paired tokens (e.g., θ(x,t) ↔ u(x,t); Frank-Oseen free energy ↔ neural Lyapunov functional; Π_A ↔ Π_B) are the same mathematical object types (scalar fields, variational functionals, scalar bifurcation parameters) and the Operator Role entries specify explicit shared structure rather than hedged analogy.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed vectors are demonstrated in the body: **shared_nonconvex_lyapunov_gradient_descent** (Section 3 derives γ∂_tθ=−δF/δθ and τ∂_tu=−(1/f′(u))δL/δu and shows dF/dt≤0, dL/dt≤0); **shared_typeI_finite_wavenumber_bifurcation_threshold** (Section 3 shows discrete finite-wavenumber thresholds E_c and f′(u_0)max_k\hat w(k)=1 with corresponding growth-rate sign changes); **shared_boundary_quantized_mode_spectrum** (Section 3 lists k_n=nπ/d and k_m=2πm/L and matches discrete spectral growth laws). Each vector is supported by equations or derivations in the body.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction (nematic → neural) is plausibly asymmetric and justified by the claimed maturity of energy-stable discretizations in the nematic literature; the falsifiable prediction in Section 4 specifies concrete numerical conditions (domain, kernel, f, k_c, required monotonicity tolerance, timestep, and explicit Euler amplification factor) that can be tested experimentally or numerically. Prior-art overlap (Amari → diffusion via short-range kernel expansion) is noted as advisory for Stage 3.

#### Stage 3 Watch Items
- The short-range expansion of the Amari convolution to a diffusion operator is a canonical approximation; Stage 3 should check for prior-art overlap with standard neural-field → reaction-diffusion derivations and cite accordingly.
- Verify the numerical constants and evaluations in Section 4 (the stated \(k_c^2=\tfrac{2}{3}\ln2\) and \(\widehat w(k_c)\approx1.1906\)) for transcription or rounding errors before replication.
- Inspect the discrete Lyapunov functional \(L_h\) and the precise convex-splitting implementation proposed for the Amari functional to ensure the claimed unconditional gradient stability holds in the discrete setting.

### Eighth Adversarial Review
**Reviewer:** xAI Grok 4.5 Fast
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-19

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The displayed Frank-Oseen energy, overdamped Ericksen-Leslie dynamics, linearization, discrete modes, threshold, Amari equation, Lyapunov functional, growth-rate formula, and short-range continuum expansion are each consistent with the claimed domains and together support the shared nonconvex gradient-flow structure and type-I finite-wavenumber threshold.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — Each paired token (θ↔u, F↔L, Π_A↔Π_B, nπ/d↔2πm/L) is of matching mathematical type (scalar fields, nonconvex functionals, dimensionless bifurcation parameters, discrete spectral labels) and the Operator Role statements name shared structures without hedging.
- **CHECK 3 (Correspondence Vector Support):** PASS — shared_nonconvex_lyapunov_gradient_descent is demonstrated by the free-energy/Lyapunov constructions and the explicit gradient-flow equations in Section 3; shared_typeI_finite_wavenumber_bifurcation_threshold is demonstrated by the linearized growth rates, discrete-mode thresholds, and definitions of Π_A, Π_B; shared_boundary_quantized_mode_spectrum is demonstrated by the explicit mode sets k_n=nπ/d and k_m=2πm/L together with the termwise correspondence of the linearized operators.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The preferred direction is justified by the relative maturity of energy-stable discretizations; the prediction specifies an explicit kernel, sigmoid, domain, timestep, and quantitative thresholds (L_h monotonicity to 10^{-12} versus amplification factor 2.906) that can fail, rendering it falsifiable.

#### Stage 3 Watch Items
- Verify whether the short-range continuum limit of the Amari synaptic operator is routinely accepted as producing a second-order local operator of the same family as the one-constant Frank-Oseen Laplacian in the literature of either community.
- Confirm that energy-stable convex-splitting schemes for nonconvex Lyapunov functionals of the Amari type remain non-standard in the neural-field community relative to the nematic community.

### Ninth Adversarial Review
**Reviewer:** Meta Muse Spark 1.1
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-19

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — All displayed equations correctly model claimed domains: nematic Frank-Oseen gradient flow γ∂tθ=−δF/δθ and Amari field τ∂tu=−u+w*f with Lyapunov L and linearization τλ(k)=−1+f'(u0)ŵ(k) are domain-correct, both parabolic nonconvex gradient flows, and scale-bridge expansion is explicitly limited to low-wavenumber limit.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All four mappings are type-compatible (scalar field ↔ scalar field, functional ↔ functional, dimensionless control Π_A ↔ Π_B with explicit nondimensionalization, discrete wavenumber nπ/d ↔ 2πm/L) and each Operator Role names shared mathematical structure, not hedged analogy.
- **CHECK 3 (Correspondence Vector Support):** PASS — shared_nonconvex_lyapunov_gradient_descent demonstrated in Section 3 via F and L with first-variation flows; shared_typeI_finite_wavenumber_bifurcation_threshold demonstrated via γλ_n^(A)=ε0ΔεE²−Kk_n² and τλ_m^(B)=−1+f'ŵ(k_m) with thresholds E_c and Π_A, Π_B crossing zero; shared_boundary_quantized_mode_spectrum demonstrated via k_n^(A)=nπ/d ↔ k_m^(B)=2πm/L and mode forms sin(k_nx) and e^{ik_m x}.
- **CHECK 4 (Transfer and Falsifiability):** PASS — Asymmetry is genuine: nematic → neural transfer of energy-stable convex-splitting/SAV methods to symmetric-kernel Amari fields addresses explicit bottleneck of explicit-Euler dominance; direction is not backwards. Falsifiability is quantitative: Δt=10τ, L_h non-increasing to 1e-12 over 1000 steps, explicit Euler amplification 2.906 divergence, with clear rejection criteria, not a template non-prediction. No canonical textbook prior-art pairing recognized.

#### Stage 3 Watch Items
- None identified.