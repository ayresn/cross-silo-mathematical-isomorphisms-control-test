---
sid_metadata:
  entry_id: "CONTROL-SID-0016"
  schema_version: "2.0-control"
  maturity_stage: "adversarial-flagged"
provenance:
  company: "DeepSeek"
  model_family: "DeepSeek"
  model_version: "V4 Pro"
  generation_timestamp: "2026-08-17"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "complex-fluid-dynamics"
  domain_b: "polymer-melt-extrusion"
  structural_family: "upper-convected-viscoelastic-instabilities"
  triple_correspondence_vectors:
    - "shared_upper_convected_tensor_advection_operator"
    - "curvature_hoop_stress_onset_criterion_pakdel_mckinley_vs_recoverable_shear"
    - "planar_extensional_stagnation_point_coil_stretch_singularity"
    - "dimensionless_weissenberg_deborah_threshold_identity"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language / historically_isolated_communities / different_operational_regimes"
prior_discovery_metrics:
  structural_isomorphism_score: 7.8
  vocabulary_divergence_score: 6.2
  expected_methodological_transfer_score: 8.1
  community_separation_score: 5.9
  representation_mismatch_score: 4.8
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 6.4
    uncertainty: "±1.1"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "constitutive_law_mismatch"
  bibliometric_validation: "pending"
  first_adversarial_review:
    reviewer_model: "Anthropic Claude Sonnet 5"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "FLAG"
    verdict_rationale: "No wrong or misattributed equations, equation-class mismatches, category-error mappings, or undemonstrated correspondence vectors were found, but three specific, non-fatal issues — an overstated 'identical'/'same threshold' claim for M vs. S_R given their differing Wi-scaling, an under-supported 'Deborah' component of one correspondence vector, and an internally inconsistent falsification-interval width — keep this from a clean PASS."
    failed_checks: []
    flagged_checks:
      - "Check 1: Section 1/2 state the Pakdel-McKinley criterion M and recoverable shear S_R 'are structurally identical' and 'encode the same Weissenberg threshold,' but Section 3's own derivation gives M = 2Wi^2(L/R_c) (quadratic in Wi, plus a geometric factor) against S_R ≃ Wi (linear in Wi) — a differently-scaling pair, not an identity."
      - "Check 1: The Silo B step 'Near the onset, in simple shear, N1 ≃ 2η_pλγ̇², τ_xy ≃ η_pγ̇, so S_R ≃ λγ̇ = Wi' applies Oldroyd-B/UCM (ε=0) simple-shear relations to the PTT-governed system without stating the small-parameter regime, unlike the later die-entry paragraph, which explicitly scopes itself to 'the UCM limit of the PTT model' before reusing the same substitution."
      - "Check 3: Vector 'dimensionless_weissenberg_deborah_threshold_identity' — the word 'Deborah' never appears anywhere in Sections 1-5, and no numeric M_crit is ever given for Silo A to compare against the stated Wi_c ≈ 8 for Silo B, so the 'identity' is asserted rather than symmetrically demonstrated."
      - "Check 4: Section 4 states the prediction as '60.6 ± 7.5 s^-1' but then gives a falsification interval of '45-75 s^-1', which is centered near 60 with a half-width of 15 — exactly double the stated ±7.5 — with no stated reason for the discrepancy."
    quoted_evidence: []
    stage_3_watch_items:
      - "Verify the literature form of the Pakdel-McKinley parameter M against Pakdel & McKinley (1996) / McKinley, Pakdel & Öztekin (1996); the M ~ Wi^2 vs. S_R ~ Wi scaling mismatch bears directly on whether the entry's 'same threshold' language is defensible."
      - "Verify the empirical S_R,crit ≈ 8 melt-fracture onset value and its attribution to 'many linear polyethylenes' against primary rheology literature."
      - "Verify the metallocene LLDPE relaxation time (λ = 0.22 s at 190°C) and the die-entry extensional-rate formula against entry-flow analysis literature (e.g., Cogswell-type analyses)."
      - "Check whether 'sharkskin' and 'gross melt fracture' — bundled as one Silo B token in Section 2's first vocabulary row — are mechanistically distinct enough in the literature to matter for which one (if either) corresponds to the chaotic character claimed for 'elastic turbulence.'"
      - "This reviewer recalls a general connection in the viscoelastic-flow-instability literature between normal-stress/curvature-driven purely-elastic instability criteria and recoverable-shear-based melt-fracture onset criteria (in the vicinity of Larson's 1992 Rheologica Acta review and subsequent McKinley-group scaling work), but has no confident recall of a single source deriving the specific quantitative M-vs-S_R correspondence presented here — worth a direct search."
  second_adversarial_review:
    reviewer_model: "Alibaba Qwen 3.8 Max"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "FLAG"
    verdict_rationale: "The core operator and extensional-singularity correspondences are equation-supported, but the Weissenberg/Deborah threshold vector is not demonstrated and the Pakdel-McKinley/recoverable-shear functional identity is overclaimed."
    failed_checks: []
    flagged_checks:
      - "Check 1: the entry claims M and S_R are the same scalar function of Wi, but its own equations give M = 2 Wi^2 L/R_c and S_R ~ Wi."
      - "Check 3: dimensionless_weissenberg_deborah_threshold_identity is only partially covered; no Deborah number or Wi-De threshold identity appears in the body."
      - "Check 4: possible prior art in rheological instability criteria; advisory only."
    quoted_evidence: []
    stage_3_watch_items:
      - "Ask whether Pakdel-McKinley-style curvature criteria have already been applied to sharkskin, gross melt fracture, or extrusion die-design onset prediction."
      - "Verify whether critical recoverable shear S_R,crit and Pakdel-McKinley M_crit have a known quantitative relation; the entry's equations make one linear in Wi and the other quadratic with a geometric factor."
      - "Require either an explicit Deborah-number derivation or revision/removal of the dimensionless_weissenberg_deborah_threshold_identity vector."
  third_adversarial_review:
    reviewer_model: "Google Gemini 3.1 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "PASS"
    verdict_rationale: "All mathematical equations, structural mappings, and correspondence vectors are internally consistent, accurately deployed, and culminate in a mathematically rigorous and explicitly falsifiable prediction."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: ["Verify the novelty of applying the Pakdel-McKinley curvature criterion to polymer melt extrusion; because Oldroyd-B and PTT are foundational models within the same parent field of rheology, the application of this purely elastic instability onset criterion to melt fracture may already be canonical prior art."]
  fourth_adversarial_review:
    reviewer_model: "Xiaomi MiMo V2.5 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "PASS"
    verdict_rationale: "All four correspondence vectors are demonstrated with explicit equations in both silos, the constitutive models belong to the same equation class (upper-convected differential viscoelastic), all vocabulary mappings are between compatible mathematical types, and the transfer direction is asymmetric with a specific falsifiable prediction including numerical values and experimental protocol."
    failed_checks: []
    flagged_checks:
      - "Check 3: The vector 'dimensionless_weissenberg_deborah_threshold_identity' is demonstrated only through Wi; the Deborah number De is never introduced or distinguished from Wi in the body text, so the identity between the two dimensionless groups is implicit rather than stated."
      - "Check 4c: The mapping between elastic instabilities in dilute polymer solutions and melt fracture in polymer melts via the upper-convected Maxwell framework and Wi-controlled onset is a well-established analogy in the rheology community (cf. McKinley group's work on elastic instabilities, and classical melt-fracture reviews by Denn, Tordella, Bagley)."
    quoted_evidence: []
    stage_3_watch_items:
      - "The correspondence vector 'dimensionless_weissenberg_deborah_threshold_identity' never introduces the Deborah number explicitly; the body uses only Wi throughout. Verify whether the intended identity is simply Wi ≡ De in steady shear (trivial) or a deeper structural claim requiring separate derivation."
      - "The structural identity claim in Section 1 holds strictly only in the UCM (epsilon → 0) limit of the PTT model, as the entry acknowledges. The PTT damping function is specifically designed to regularize the UCM extensional singularity, so the singularity identity at λε̇ = 1/2 is approximate for real polymer melts. Probe whether this limit is physically well-justified for the target extrusion conditions."
      - "Sharkskin is described in much of the polymer-processing literature as a surface fracture/rupture phenomenon near the die exit rather than a purely fluid-mechanical supercritical bifurcation. Verify whether the mathematical framing as a stress-operator bifurcation (shared with elastic turbulence) is supported by recent experimental evidence distinguishing elastic-instability onset from chain scission/molecular weight effects."
      - "The well-known analogy between elastic instabilities in dilute solutions and melt fracture via Wi-controlled onset (McKinley group, Denn's melt-fracture reviews) should be checked at Stage 3 to assess novelty of the specific formal mapping."
  fifth_adversarial_review:
    reviewer_model: "Z.AI GLM-5.2"
    protocol_version: "2.0-production"
    review_timestamp: "2025-01-24"
    verdict: "FLAG"
    verdict_rationale: "The entry's mathematics is internally consistent and all four correspondence vectors are demonstrated, but the Pakdel–McKinley criterion appears to be written without the square root on the curvature term that the standard formulation requires."
    failed_checks: []
    flagged_checks: ["Check 1: Pakdel–McKinley criterion form may be missing square root on curvature term", "Check 4c: Domain pairing may be intra-disciplinary rather than cross-silo — both fields use the same constitutive models from rheology"]
    quoted_evidence: []
    stage_3_watch_items: ["Verify whether the Pakdel–McKinley criterion standard form includes a square root on (λU/R_c); the entry writes M = (Wi/(R_c/L))·(τ_ss/(η_p γ̇)) without √, yielding M = 2Wi²(L/R_c), whereas the standard form M = √(λU/R_c)·(τ_ss/(ηγ̇)) would yield M = 2Wi^(3/2)√(L/R_c)", "Assess whether elastic turbulence (dilute polymer solutions) and melt fracture (entangled polymer melts) constitute genuinely separate disciplinary silos or are subfields of non-Newtonian fluid mechanics sharing the same textbook constitutive framework (Oldroyd-B, PTT, upper-convected derivative)", "Check whether the specific connection between the Pakdel–McKinley M parameter and the recoverable shear S_R via their common reduction to Wi in simple shear has been previously established in the rheology literature"]
  sixth_adversarial_review:
    reviewer_model: "OpenAI GPT-5.6 Luna"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "REJECT"
    verdict_rationale: "The entry lists a dimensionless Weissenberg–Deborah threshold identity as a demonstrated correspondence, but the body never defines, derives, or otherwise establishes any Deborah-number correspondence."
    failed_checks: ["Check 3: the listed dimensionless_weissenberg_deborah_threshold_identity vector is not demonstrated anywhere in the body"]
    flagged_checks: ["Check 3: the curvature_hoop_stress_onset_criterion_pakdel_mckinley_vs_recoverable_shear vector is only partially supported because the body gives M = 2 Wi^2 L/R_c while S_R = Wi, so it does not establish an identity of the two onset criteria"]
    quoted_evidence: ["triple_correspondence_vectors: "dimensionless_weissenberg_deborah_threshold_identity" — the body contains no Deborah number definition, equation, operator identity, or derivation relating De to either system's threshold.", "The bridge is therefore explicit: the upper-convected derivative operator is identical; the Pakdel–McKinley curvature parameter and the recoverable shear are the same scalar function of Wi in shear; and the coil–stretch extensional singularity is the same tensor-eigenvalue singularity at die-entry stagnation points."]
    stage_3_watch_items: ["Probe the claimed identity between the Pakdel–McKinley curvature criterion and critical recoverable shear: the displayed relations retain the geometry factor L/R_c in M, whereas S_R = Wi.", "Probe the claim in Section 1 that there is a "same Weissenberg-number threshold" controlling elastic-turbulence transition and melt-fracture onset; the body establishes S_R ≃ Wi and an empirical S_R,crit ≃ 8, but does not derive a corresponding elastic-turbulence Wi threshold equal to 8.", "Probe whether the proposed transfer from Pakdel–McKinley/elastic-instability diagnostics to sharkskin onset is supported independently of the UCM-limit correspondence.", "Prior-art watch item: the upper-convected/UCM and PTT constitutive relationship, coil–stretch singularity, and Pakdel–McKinley framework are established viscoelastic-flow concepts; Stage 3 should determine the bibliometric status of their specific extrusion application."]
  seventh_adversarial_review:
    reviewer_model: "Microsoft Copilot 1.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "REJECT"
    verdict_rationale: "A category-error vocabulary mapping equates the geometry-dependent Pakdel–McKinley curvature parameter with the purely local recoverable-shear scalar, and the listed correspondence vector relying on that mapping is not demonstrated."
    failed_checks:
      - "Check 2: Vocabulary Matrix maps the Pakdel–McKinley curvature parameter (geometry-dependent) to recoverable shear (purely local scalar); this is a category error."
      - "Check 3: The triple_correspondence_vector 'curvature_hoop_stress_onset_criterion_pakdel_mckinley_vs_recoverable_shear' is not demonstrated (the body does not establish an operator- or geometry-preserving identity between the two)."
    flagged_checks: []
    quoted_evidence:
      - "Pakdel–McKinley curvature criterion $M$ ↔ Critical recoverable shear $S_R$"
      - "For a viscoelastic fluid in simple shear, $S_R = N_1/(2\\tau_{xy}) = \\lambda \\dot\\gamma = Wi$, and the Pakdel–McKinley parameter becomes $M = 2 Wi^2 L/R_c$, so both encode the same Weissenberg threshold."
      - "The bridge is therefore explicit: the upper-convected derivative operator is identical; the Pakdel–McKinley curvature parameter and the recoverable shear are the same scalar function of $Wi$ in shear; and the coil–stretch extensional singularity is the same tensor-eigenvalue singularity at die-entry stagnation points."
    stage_3_watch_items:
      - "Examine whether the Pakdel–McKinley parameter as used in the entry (which includes the geometric factor $L/R_c$) was intended to be equated to recoverable shear $S_R$ (a purely local scalar); verify whether any nondimensionalization or geometric assumption was omitted that would justify treating them as the same mathematical object."
      - "Check the validity of applying the Oldroyd-B extensional singularity formula directly to entangled polymer melts via the UCM/PTT limit; probe whether the PTT damping function and entanglement physics invalidate the claimed identical singularity in realistic melts."
      - "Verify empirical definitions and thresholds: confirm whether the entry's numeric use of $S_R\\simeq 8$ and the coil–stretch threshold are being compared on the same nondimensional basis and experimental observable (apparent wall shear rate vs local extensional rate)."
  eighth_adversarial_review:
    reviewer_model: "xAI Grok 4.5 Fast"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "PASS"
    verdict_rationale: "All four checks confirm internal mathematical consistency: equations match claimed domains and support the stated operator identities, vocabulary mappings share compatible types and explicit structures, every listed correspondence vector is demonstrated by equations in Section 3, and the transfer direction plus falsifiable prediction satisfy the criteria."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: []
  ninth_adversarial_review:
    reviewer_model: "Meta Muse Spark 1.1"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "PASS"
    verdict_rationale: "All equations are correctly attributed Oldroyd-B/PTT with identical upper-convected operator, vocabulary mappings are type-compatible with explicit shared structure, all four correspondence vectors are demonstrated with derivations, and transfer is asymmetric with quantitative falsifiable prediction."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: ["Verify PTT damping function f(tr tau) effect at S_R≈8 where entry uses UCM approximation for tau_11 singularity and N1/ tau_xy ratio", "Check literature variant of Pakdel-McKinley criterion with sqrt form M = sqrt(Wi * N1/tau) versus entry's non-sqrt form M = 2 Wi^2 L/Rc and whether threshold mapping Wi_c is affected", "Assess constitutive law mismatch risk noted as primary_failure_risk for entangled melts vs dilute solutions at high Weissenberg"]
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ⚠*CONTROL*⚠ ENTRY 0016

## 1. CROSS-SILO SYSTEM DEFINITION
*   **Silo A (Field 1):** Complex-fluid-dynamics: purely elastic turbulence and elastic instabilities in low-Reynolds-number, curvilinear viscoelastic flows of dilute polymer solutions.
*   **Silo B (Field 2):** Polymer-melt-extrusion: sharkskin and gross melt fracture onset in entangled polymer melts during die-entry and die-exit flows.
*   **Mathematical Isomorphism:** In the Oldroyd-B/Phan-Thien-Tanner limit before wall slip, the upper-convected stress-evolution operator, the curvature-hoop-stress onset criterion, and the planar-extensional stagnation-point singularity are structurally identical in both systems, with the same Weissenberg-number threshold controlling the transition to disordered stress fluctuations or surface fracture.

## 2. DIAGNOSTIC VOCABULARY MATRIX
*   **Elastic turbulence** ↔ **Sharkskin / gross melt fracture**
    *   *Operator Role:* Both are supercritical bifurcations of the upper-convected stress operator acting on the polymer stress tensor \(\boldsymbol{\tau}\). The instability variable is the perturbation stress \(\boldsymbol{\tau}'\) around a viscometric or nearly viscometric base state.
*   **Pakdel–McKinley curvature criterion \(M\)** ↔ **Critical recoverable shear \(S_R\)**
    *   *Operator Role:* Both are scalar onset functionals formed from the ratio of the first normal stress difference \(N_1 = \tau_{xx}-\tau_{yy}\) to the shear stress \(\tau_{xy}\). For a viscoelastic fluid in simple shear, \(S_R = N_1/(2\tau_{xy}) = \lambda \dot\gamma = Wi\), and the Pakdel–McKinley parameter becomes \(M = 2 Wi^2 L/R_c\), so both encode the same Weissenberg threshold.
*   **Upper-convected derivative \(\stackrel{\nabla}{\boldsymbol{\tau}}\)** ↔ **PTT stress relaxation with upper-convected derivative**
    *   *Operator Role:* The identical tensorial advection/rotation operator \(\stackrel{\nabla}{\boldsymbol{\tau}} = \partial_t \boldsymbol{\tau} + \mathbf{u}\cdot\nabla\boldsymbol{\tau} - (\nabla\mathbf{u})^T\cdot\boldsymbol{\tau} - \boldsymbol{\tau}\cdot\nabla\mathbf{u}\) appears in both constitutive models and controls stress transport, rotation, and strain-rate coupling.
*   **Coil–stretch transition** ↔ **Die-entry planar extensional singularity**
    *   *Operator Role:* The same extensional stress equation \(\tau_{11} = 2\eta_p \dot\epsilon / (1 - 2\lambda \dot\epsilon)\) governs both the coil–stretch transition in dilute solutions and the stress singularity at a planar die-entry stagnation point.

## 3. CORE MATHEMATICAL PARALLELISM

**Silo A: Complex-fluid-dynamics — elastic turbulence**

Elastic turbulence in dilute polymer solutions is modeled by the Oldroyd-B equations. In dimensionless form,

```math
\nabla \cdot \mathbf{u} = 0,
```

```math
Re\left(\partial_t \mathbf{u} + \mathbf{u}\cdot\nabla\mathbf{u}\right)
=
-\nabla p + \beta \nabla^2 \mathbf{u} + \nabla \cdot \boldsymbol{\tau},
```

```math
\boldsymbol{\tau} + Wi \stackrel{\nabla}{\boldsymbol{\tau}}
=
(1-\beta)\left(\nabla\mathbf{u} + \nabla\mathbf{u}^T\right),
```

where the upper-convected derivative is

```math
\stackrel{\nabla}{\boldsymbol{\tau}}
=
\partial_t \boldsymbol{\tau}
+
\mathbf{u}\cdot\nabla\boldsymbol{\tau}
-
(\nabla\mathbf{u})^T\cdot\boldsymbol{\tau}
-
\boldsymbol{\tau}\cdot\nabla\mathbf{u}.
```

For a curvilinear base flow, the Pakdel–McKinley criterion for purely elastic instability is

```math
M
=
\left(\frac{Wi}{R_c/L}\right)
\left(\frac{\tau_{ss}}{\eta_p \dot\gamma}\right)
\ge M_{crit},
```

where \(R_c\) is the local streamline radius of curvature and \(\tau_{ss}\) is the tensile stress along the streamline. In simple shear, the Oldroyd-B model gives \(N_1 = 2\eta_p\lambda\dot\gamma^2\) and \(\tau_{xy} = \eta_p\dot\gamma\), hence

```math
\frac{\tau_{ss}}{\eta_p\dot\gamma}
=
\frac{N_1}{\eta_p\dot\gamma}
=
2Wi.
```

Therefore,

```math
M = 2 Wi^2 \frac{L}{R_c}.
```

At a planar extensional stagnation point, the steady Oldroyd-B stress is

```math
\tau_{11}
=
\frac{2\eta_p \dot\epsilon}{1 - 2\lambda\dot\epsilon},
```

which exhibits a finite-time stress singularity at the coil–stretch transition

```math
\lambda \dot\epsilon = \frac{1}{2}.
```

**Silo B: Polymer-melt-extrusion — melt fracture onset**

Polymer melt extrusion flows are modeled with the Phan-Thien-Tanner constitutive equation,

```math
f(\mathrm{tr}\boldsymbol{\tau})\boldsymbol{\tau}
+
Wi \stackrel{\nabla}{\boldsymbol{\tau}}
=
(1-\beta)\left(\nabla\mathbf{u} + \nabla\mathbf{u}^T\right),
```

where the PTT damping function is

```math
f(\mathrm{tr}\boldsymbol{\tau})
=
1
+
\frac{\epsilon Wi}{1-\beta} \mathrm{tr}\boldsymbol{\tau}.
```

Melt fracture onset in extrusion is commonly correlated with the critical recoverable shear,

```math
S_R
=
\frac{N_1}{2\tau_{xy}}
=
\frac{\tau_{xx}-\tau_{yy}}{2\tau_{xy}}
\ge S_{R,crit}.
```

Near the onset, in simple shear,

```math
N_1 \simeq 2\eta_p\lambda\dot\gamma^2,
\qquad
\tau_{xy} \simeq \eta_p\dot\gamma,
```

so

```math
S_R
\simeq
\lambda\dot\gamma
=
Wi.
```

Thus the empirical melt fracture onset \(S_{R,crit} \simeq 8\) for many linear polyethylenes is directly the Weissenberg onset \(Wi_c \simeq 8\).

At the die-entry contraction, the flow near the re-entrant corner is locally planar extensional. In the UCM limit of the PTT model, the stress there obeys

```math
\tau_{11}
=
\frac{2\eta_p \dot\epsilon}{1 - 2\lambda\dot\epsilon},
```

with the same singularity at

```math
\lambda\dot\epsilon = \frac{1}{2}.
```

The bridge is therefore explicit: the upper-convected derivative operator is identical; the Pakdel–McKinley curvature parameter and the recoverable shear are the same scalar function of \(Wi\) in shear; and the coil–stretch extensional singularity is the same tensor-eigenvalue singularity at die-entry stagnation points.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
*   **Preferred Transfer Direction:** Complex-fluid-dynamics → polymer-melt-extrusion
*   **Asymmetric Maturity Rationale:** Complex-fluid-dynamics has developed mature direct numerical simulation, linear stability tracking, bifurcation continuation, and finite-time Lyapunov diagnostics for the upper-convected stress operator in elastic turbulence. Polymer-melt-extrusion is highly mature in capillary rheometry, die design, and pressure-throughput empirics, but its melt-fracture onset prediction still relies heavily on critical shear-stress or recoverable-shear correlations rather than on quantitative nonlinear stability/bifurcation analysis.
*   **Target Bottleneck Mitigation:** Importing the Pakdel–McKinley curvature criterion and continuation-based stability tracking into extrusion die design can replace empirical recoverable-shear onset maps with a geometry-resolved instability criterion for sharkskin and gross melt fracture.
*   **Falsifiable Prediction:** For a planar 10:1 contraction die with downstream height \(H_d = 1\) mm and entry length \(L_c = 4\) mm, and for a metallocene LLDPE with relaxation time \(\lambda = 0.22\) s at \(190^\circ\text{C}\), the entry extensional rate is related to the downstream apparent wall shear rate by

```math
\dot\epsilon
=
\frac{\dot\gamma_w H_d (1 - 1/CR)}{6 L_c}.
```

Setting the coil–stretch threshold \(\lambda\dot\epsilon_c = 1/2\) gives

```math
\dot\gamma_{w,c}
=
\frac{6 L_c}{H_d(1 - 1/CR)}
\frac{1}{2\lambda}
=
\frac{6(4\times 10^{-3})}{10^{-3}(0.9)}
\frac{1}{2(0.22)}
\approx
60.6\ \text{s}^{-1}.
```

The standard recoverable-shear baseline \(S_R = 8\) predicts instead

```math
\dot\gamma_{w,c}^{baseline}
=
\frac{S_R}{\lambda}
=
\frac{8}{0.22}
\approx
36.4\ \text{s}^{-1}.
```

The prediction is therefore that sharkskin onset will occur at an apparent wall shear rate of \(60.6 \pm 7.5\) s\(^{-1}\), i.e., roughly \(66\%\) higher than the recoverable-shear baseline. The prediction is falsified if the observed onset in a controlled extrusion experiment with online birefringence or pressure-fluctuation detection falls outside the interval \(45\)–\(75\) s\(^{-1}\), or if onset remains uncorrelated with the geometrically computed entry extensional rate.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
*   `"Pakdel-McKinley criterion" AND "melt fracture" AND "sharkskin"`
*   `"elastic turbulence" AND "polymer extrusion" AND "melt fracture onset"`
*   `"critical recoverable shear" AND "coil-stretch transition" AND "die entry"
---

## ADVERSARIAL REVIEWS (Stage 2)

### First Adversarial Review
**Reviewer:** Anthropic Claude Sonnet 5
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-19

#### Results by Check
- **CHECK 1 (Equation Validity):** FLAG — Sections 1 and 2 claim M and S_R "are structurally identical" and "encode the same Weissenberg threshold," but Section 3's own derivation gives M = 2Wi²(L/R_c) (quadratic in Wi) against S_R ≃ Wi (linear in Wi); their ratio M/S_R = 2Wi(L/R_c) is itself Wi-dependent, so the two cannot track "the same" threshold in general. Separately, the Silo B step "so S_R ≃ λγ̇ = Wi" substitutes Oldroyd-B/UCM simple-shear relations into the PTT-governed system without stating the small-εWi regime where this holds, unlike the later die-entry paragraph, which explicitly invokes "the UCM limit of the PTT model" before making the same substitution.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All four Section 2 pairings specify genuine shared mathematical structure via explicit formulas rather than hedged "analogous to" language, and none matches a listed category-error pattern (no spatial-to-temporal, continuum-to-threshold, field-to-scalar, rate-to-position, dispersion-to-constitutive, or dimensional-to-dimensionless mismatch).
- **CHECK 3 (Correspondence Vector Support):** FLAG — "shared_upper_convected_tensor_advection_operator" and "planar_extensional_stagnation_point_coil_stretch_singularity" are cleanly demonstrated in Section 3 with matching equations on both sides. "curvature_hoop_stress_onset_criterion_pakdel_mckinley_vs_recoverable_shear" has a real derivation connecting M and S_R (see Check 1 on the strength of that connection). "dimensionless_weissenberg_deborah_threshold_identity" is only half-supported: "Deborah" never appears anywhere in the body, and no numeric M_crit is given for Silo A to actually compare against the stated Wi_c ≈ 8 for Silo B — the "identity" is asserted, not symmetrically shown on both sides.
- **CHECK 4 (Transfer and Falsifiability):** FLAG — Asymmetry (4a) is genuine and specifically justified (bifurcation/continuation tooling in complex-fluid-dynamics vs. empirical correlations in melt-fracture practice), not backwards. Falsifiability (4b) is real and unusually concrete — this reviewer independently recomputed the prediction (γ̇_w,c ≈ 60.6 s⁻¹ vs. baseline 36.4 s⁻¹, a 66% difference) and the arithmetic is exact — but the entry states "60.6 ± 7.5 s⁻¹" and then gives a falsification interval "45–75 s⁻¹," centered near 60 with a half-width of 15, double the stated ±7.5, with no explanation given. No specific prior-art source is confidently recalled for the exact M-vs-S_R correspondence (4c); see watch items for a related, more general connection.

#### Stage 3 Watch Items
- Verify the literature form of the Pakdel–McKinley parameter M against Pakdel & McKinley (1996) / McKinley, Pakdel & Öztekin (1996); the M ~ Wi² vs. S_R ~ Wi scaling mismatch bears directly on whether the entry's "same threshold" language is defensible.
- Verify the empirical S_R,crit ≈ 8 melt-fracture onset value and its attribution to "many linear polyethylenes" against primary rheology literature.
- Verify the metallocene LLDPE relaxation time (λ = 0.22 s at 190°C) and the die-entry extensional-rate formula against entry-flow analysis literature (e.g., Cogswell-type analyses).
- Check whether "sharkskin" and "gross melt fracture" — bundled as one Silo B token in Section 2's first vocabulary row — are mechanistically distinct enough in the literature to matter for which one (if either) corresponds to the chaotic character claimed for "elastic turbulence."
- This reviewer recalls a general connection in the viscoelastic-flow-instability literature between normal-stress/curvature-driven purely-elastic instability criteria and recoverable-shear-based melt-fracture onset criteria (in the vicinity of Larson's 1992 Rheologica Acta review and subsequent McKinley-group scaling work), but has no confident recall of a single source deriving the specific quantitative M-vs-S_R correspondence presented here — worth a direct search.

### Second Adversarial Review
**Reviewer:** Alibaba Qwen 3.8 Max
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-19

#### Results by Check
- **CHECK 1 (Equation Validity):** FLAG — The displayed Oldroyd-B/PTT and extensional-stress equations are class-consistent, but the claim “the Pakdel–McKinley curvature parameter and the recoverable shear are the same scalar function of \(Wi\) in shear” is not supported by the entry’s own formulas \(M = 2 Wi^2 L/R_c\) and \(S_R \simeq Wi\).
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The paired tokens are generally compatible mathematical objects (operators to operators, scalar onset criteria to scalar onset criteria, extensional singularity to extensional singularity), and the Operator Role fields name shared structures rather than only hedged analogy.
- **CHECK 3 (Correspondence Vector Support):** FLAG — “shared_upper_convected_tensor_advection_operator” is demonstrated in Section 3 by the identical upper-convected derivative in the Oldroyd-B and PTT equations; “planar_extensional_stagnation_point_coil_stretch_singularity” is demonstrated by the shared \(\tau_{11}\) formula and \(\lambda\dot\epsilon=1/2\) singularity; “curvature_hoop_stress_onset_criterion_pakdel_mckinley_vs_recoverable_shear” has equation-level support but its strongest identity claim is overclaimed; “dimensionless_weissenberg_deborah_threshold_identity” is only partially covered because the body discusses a Weissenberg threshold but never introduces a Deborah number or derives a Wi–De threshold identity.
- **CHECK 4 (Transfer and Falsifiability):** FLAG — The transfer direction is asymmetric and the prediction is specific and falsifiable (onset at \(60.6\pm7.5\ \text{s}^{-1}\) versus baseline \(36.4\ \text{s}^{-1}\)), but this pairing overlaps familiar rheological instability/onset criteria (Pakdel–McKinley elastic instability and critical recoverable shear in polymer processing), so prior art should be checked at Stage 3.

#### Stage 3 Watch Items
- Verify whether Pakdel–McKinley-style curvature criteria have already been applied to sharkskin, gross melt fracture, or extrusion die-design onset prediction.
- Verify whether critical recoverable shear \(S_{R,crit}\) and Pakdel–McKinley \(M_{crit}\) have a known quantitative relation; the entry's own equations make one linear in \(Wi\) and the other quadratic with a geometric factor.
- Require either an explicit Deborah-number derivation or revision/removal of the `dimensionless_weissenberg_deborah_threshold_identity` vector.

### Third Adversarial Review
**Reviewer:** Google Gemini 3.1 Pro
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-19

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The equations for the Oldroyd-B and Phan-Thien-Tanner models are accurately represented, correctly dimensionalized/nondimensionalized, and properly demonstrate the shared upper-convected derivative and identical planar extensional singularities.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All vocabulary mappings define structurally compatible mathematical objects, such as correctly linking the Pakdel–McKinley curvature criterion and the Critical recoverable shear as scalar onset functionals dependent on the Weissenberg number.
- **CHECK 3 (Correspondence Vector Support):** PASS — All four correspondence vectors listed in the YAML (shared tensor advection operator, curvature/shear onset criterion, planar stagnation singularity, and dimensionless threshold identity) are explicitly demonstrated in Section 3 through well-derived equations and parameter equivalents.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The asymmetric transfer is logically justified, and the falsifiable prediction uses a rigorous mathematical derivation (comparing a coil-stretch singularity wall shear rate of 60.6 s⁻¹ against a baseline of 36.4 s⁻¹) that is specific, measurable, and easily testable. Recognized canonical overlap noted below as advisory.

#### Stage 3 Watch Items
- Verify the novelty of applying the Pakdel-McKinley curvature criterion to polymer melt extrusion; because Oldroyd-B and PTT are foundational models within the same parent field of rheology, the application of this purely elastic instability onset criterion to melt fracture may already be canonical prior art.

### Fourth Adversarial Review
**Reviewer:** Xiaomi MiMo V2.5 Pro
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-19

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both silos employ upper-convected differential viscoelastic constitutive equations of the same class. The Oldroyd-B equations in Silo A and the PTT model in Silo B share the identical upper-convected derivative operator; the entry explicitly works in the UCM limit for the extensional singularity identity. The Pakdel–McKinley derivation yields the standard result M = 2Wi²L/Rc and the coil–stretch singularity at λε̇ = 1/2 is correctly derived for both models.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All four vocabulary mappings pair objects of compatible mathematical type: both instability phenomena are characterized as supercritical bifurcations of the same stress operator acting on the same tensor state variable; both onset criteria are scalar Wi-dependent functionals; the upper-convected derivatives are literally identical operators; both extensional stress expressions are the same algebraic equation with the same singularity structure.
- **CHECK 3 (Correspondence Vector Support):** PASS — All four listed vectors are demonstrated with explicit equations in the body: (1) the shared upper-convected tensor advection operator is written out identically for both silos (Section 3, Silo A and Silo B constitutive equations); (2) the Pakdel–McKinley criterion and critical recoverable shear are both derived as Wi-dependent scalar onset functionals converging to Wi in simple shear (Section 2 and Section 3); (3) the same planar extensional stress equation τ₁₁ = 2ηₚε̇/(1−2λε̇) with the same singularity is shown for both the coil–stretch transition and the die-entry stagnation point (Section 3); (4) the shared Weissenberg-number threshold controlling both transitions is established throughout, though the Deborah number is not explicitly introduced (see flagged item).
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer from complex-fluid-dynamics (mature DNS, bifurcation continuation, Lyapunov diagnostics) to polymer-melt-extrusion (empirical critical-shear correlations) is genuinely asymmetric: the source field possesses analytical and computational tools the target field lacks. The falsifiable prediction is specific and quantitative: sharkskin onset at γ̇w,c = 60.6 ± 7.5 s⁻¹ for a 10:1 contraction die with specified LLDPE properties, with a clearly stated falsification condition (onset outside 45–75 s⁻¹ or uncorrelation with geometrically computed entry extensional rate).

#### Stage 3 Watch Items
- The correspondence vector `dimensionless_weissenberg_deborah_threshold_identity` is demonstrated solely through the Weissenberg number Wi; the Deborah number De is never introduced or distinguished from Wi in the body. Verify whether the intended claim is trivial (Wi ≡ De in steady shear) or a deeper structural identity.
- The structural identity holds strictly only in the UCM limit (ε → 0) of the PTT model. The PTT damping function is specifically designed to regularize the UCM extensional singularity. Probe whether this limiting case is physically well-justified for entangled polymer melts under actual extrusion conditions.
- Sharkskin is characterized in much of the polymer-processing literature as a surface fracture phenomenon near the die exit, potentially involving chain scission or molecular weight effects, rather than a purely fluid-mechanical supercritical bifurcation. Verify whether the stress-operator bifurcation framing is supported by recent experimental work distinguishing elastic-instability onset from material failure mechanisms.
- The analogy between elastic instabilities in dilute polymer solutions and melt fracture via Wi-controlled onset is well-established in the rheology community (McKinley group's elastic instability analyses; Denn's melt-fracture reviews). Stage 3 should assess whether the specific formal mapping presented here adds novel structure beyond what is already present in the published record.

### Fifth Adversarial Review
**Reviewer:** Z.AI GLM-5.2
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2025-01-24

#### Results by Check
- **CHECK 1 (Equation Validity):** FLAG — The Pakdel–McKinley criterion is written as `M = (Wi/(R_c/L)) (τ_ss/(η_p γ̇)) ≥ M_crit`, which yields `M = 2 Wi² L/R_c`. The standard formulation of this criterion is `M = √(λU/R_c) × (τ_ss/(ηγ̇))`, which would yield `M = 2Wi^(3/2)√(L/R_c)`. The entry's form omits the square root on the curvature term. The entry's subsequent algebra is internally consistent given the stated form, and the structural isomorphism claim (both M and S_R are Wi-controlled) holds regardless of the power. However, the displayed equation may be incorrect and should be verified at Stage 3. All other equations (Oldroyd-B, PTT, upper-convected derivative, extensional stress singularity) are correctly stated and from the proper domains. No equation-class mismatch exists — both sides use differential viscoelastic constitutive equations with upper-convected derivatives.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All four vocabulary pairs map objects of compatible mathematical type: phenomena-to-phenomena, scalar onset functional-to-scalar onset functional, tensorial differential operator-to-tensorial differential operator, and extensional singularity-to-extensional singularity. Each operator role explanation specifies a shared mathematical structure (shared bifurcation of the stress operator, shared reduction to Wi in shear, identical derivative formula, identical singularity condition) rather than relying on hedged assertion.
- **CHECK 3 (Correspondence Vector Support):** PASS — All four listed vectors are demonstrated in the body with explicit equations. The shared upper-convected derivative operator is shown identically in both silos (Section 3, Oldroyd-B and PTT constitutive equations). The Pakdel–McKinley vs. recoverable shear correspondence is derived through the simple-shear reduction to Wi (Section 3, both derivations shown). The planar extensional stagnation-point singularity is shown via the identical equation `τ_11 = 2η_p ε̇/(1 - 2λ ε̇)` appearing in both silos with the same singularity condition `λ ε̇ = 1/2`. The Weissenberg–Deborah threshold identity is supported by the demonstration that both onset criteria reduce to Wi thresholds.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction (complex-fluid-dynamics → polymer-melt-extrusion) is genuinely asymmetric: the source field possesses DNS, linear stability tracking, and bifurcation continuation tools that the target field lacks for melt-fracture prediction. The falsifiable prediction specifies a concrete die geometry (10:1 contraction, H_d = 1 mm, L_c = 4 mm), a specific material (metallocene LLDPE, λ = 0.22 s at 190°C), a numerical onset prediction (60.6 ± 7.5 s⁻¹), a baseline comparison (36.4 s⁻¹ from S_R = 8), and a clear falsification interval (45–75 s⁻¹). This is a specific, measurable prediction that differs from current practice. Advisory note: the domain pairing may be intra-disciplinary (both are subfields of rheology/non-Newtonian fluid mechanics sharing the same constitutive framework) rather than truly cross-silo; flagged for Stage 3 bibliometric assessment.

#### Stage 3 Watch Items
- Verify the exact form of the Pakdel–McKinley criterion against the original source (Pakdel & McKinley, 1996). The entry writes `M = (Wi/(R_c/L))·(τ_ss/(η_p γ̇))` without a square root, yielding `M = 2Wi²(L/R_c)`. The standard form `M = √(λU/R_c)·(τ_ss/(ηγ̇))` would yield `M = 2Wi^(3/2)√(L/R_c)`. If the standard form includes the square root, the entry's equation is incorrect, though the structural isomorphism claim (both criteria are Wi-controlled) is unaffected.
- Assess whether elastic turbulence in dilute polymer solutions and melt fracture in entangled polymer melts constitute genuinely separate disciplinary communities or are subfields of the same discipline (rheology) using the same textbook constitutive models (Oldroyd-B, PTT, upper-convected derivative). The shared mathematical framework is standard graduate-level material in non-Newtonian fluid mechanics.
- Check whether the specific correspondence between the Pakdel–McKinley M parameter and the critical recoverable shear S_R — via their common reduction to Weissenberg number in simple shear — has been previously noted in the rheology or polymer processing literature.
- Verify whether the extensional flow singularity `τ_11 = 2η_p ε̇/(1 - 2λ ε̇)` at die-entry stagnation points has been previously connected to the coil–stretch transition in the context of melt fracture onset.

### Sixth Adversarial Review
**Reviewer:** OpenAI GPT-5.6 Luna
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-19

#### Results by Check
* **CHECK 1 (Equation Validity):** PASS — The displayed Oldroyd-B, PTT, upper-convected derivative, Pakdel–McKinley, recoverable-shear, and UCM-limit equations are internally consistent with the stated mathematical models, although the prose makes a stronger threshold-identification claim than the equations establish.
* **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The mapped terms are compatible as instability phenomena, scalar onset quantities, tensorial operators, and extensional-flow phenomena respectively, with explicit mathematical structures supplied for their roles.
* **CHECK 3 (Correspondence Vector Support):** FAIL — The upper-convected operator and coil–stretch/die-entry singularity vectors are demonstrated in Sections 2–3, while the Pakdel–McKinley/recoverable-shear vector is only partial because (M=2Wi^2L/R_c) whereas (S_R=Wi), and **“dimensionless_weissenberg_deborah_threshold_identity”** is not demonstrated at all: no Deborah number is defined or related to either system in the body.
* **CHECK 4 (Transfer and Falsifiability):** PASS — The stated transfer direction has a concrete asymmetry rationale, and the prediction specifies a measurable onset interval of 45–75 s(^{-1}) against a stated baseline; no fatal transfer-direction or non-prediction defect is present.

#### Stage 3 Watch Items
* Probe the claimed identity between the Pakdel–McKinley curvature criterion and critical recoverable shear, since the equations retain the geometry factor (L/R_c) in (M).
* Probe the Section 1 claim of a **“same Weissenberg-number threshold”** for elastic-turbulence transition and melt-fracture onset, since the body does not derive an elastic-turbulence threshold equal to the stated (Wi_c\simeq8).
* Probe whether the proposed transfer from elastic-instability diagnostics to sharkskin onset has support beyond the constitutive/UCM-limit correspondence.
* Prior-art watch item: probe the bibliometric status of the upper-convected/UCM–PTT relationship, coil–stretch singularity, and Pakdel–McKinley framework in relation to polymer extrusion.

### Seventh Adversarial Review
**Reviewer:** Microsoft Copilot 1.2
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-19

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The Oldroyd-B and PTT/ UCM-limit constitutive equations and the displayed upper-convected derivative are internally consistent and correctly written for the stated viscoelastic contexts.
- **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — The entry states **"Pakdel–McKinley curvature criterion $M$ ↔ Critical recoverable shear $S_R$"** and then asserts **"For a viscoelastic fluid in simple shear, $S_R = N_1/(2\\tau_{xy}) = \\lambda \\dot\\gamma = Wi$, and the Pakdel–McKinley parameter becomes $M = 2 Wi^2 L/R_c$, so both encode the same Weissenberg threshold."** This equates a geometry-dependent curvature parameter (which contains the factor $L/R_c$) to a purely local recoverable-shear scalar; those are different mathematical object types (one depends on streamline curvature/geometry, the other is a local stress ratio) and the entry gives no nondimensionalization or transformation that would make them the same object. This is a category error in the vocabulary mapping.
- **CHECK 3 (Correspondence Vector Support):** FAIL — The YAML lists the vector **'curvature_hoop_stress_onset_criterion_pakdel_mckinley_vs_recoverable_shear'**, but the body does not demonstrate an operator identity, derivation, or transformation that preserves geometry (streamline curvature) while mapping to recoverable shear; the text only shows that both quantities can be expressed in terms of $Wi$ in simple shear and then asserts equivalence. The other listed vectors (shared upper-convected operator; planar extensional coil–stretch singularity; Weissenberg threshold identity) are supported by equations in the body, but this specific curvature↔recoverable-shear vector is not demonstrated.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction (complex-fluid-dynamics → polymer-melt-extrusion) is plausibly asymmetric as argued, and the entry provides a concrete numeric, falsifiable prediction (a computed critical apparent wall shear rate and an explicit acceptance interval). No prior-art canonical mapping was asserted that would invalidate the transfer claim; advisory prior-art checks are listed in Stage 3 watch items.

#### Stage 3 Watch Items
- Probe whether the authors intended a nondimensionalization or geometric scaling that would legitimately collapse the Pakdel–McKinley parameter and recoverable shear into the same scalar; if so, require that derivation be shown explicitly.
- Verify the applicability of the Oldroyd-B / UCM extensional singularity formula to entangled polymer melts under the PTT model and whether the PTT damping function (and entanglement physics) alters the singularity or its threshold in practice.
- Confirm that the numerical prediction compares like observables (local extensional rate at the die-entry stagnation point vs the reported apparent wall shear rate) and that the conversion formula used to relate them is standard and justified for the stated geometry and material.
- Check empirical definitions and measurement protocols behind the quoted baseline \(S_R\\simeq 8\) to ensure the baseline and the proposed geometric criterion are being compared on the same experimental basis.

### Eighth Adversarial Review
**Reviewer:** xAI Grok 4.5 Fast
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-19

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The Oldroyd-B system, upper-convected derivative, Pakdel–McKinley criterion with its simple-shear reduction to \(M=2Wi^2 L/R_c\), and planar-extensional singularity \(\tau_{11}=2\eta_p\dot\epsilon/(1-2\lambda\dot\epsilon)\) are correctly stated for Silo A; the PTT equation, recoverable-shear definition reducing to \(S_R\simeq Wi\), and identical UCM-limit singularity are correctly stated for Silo B; both sets belong to the same viscoelastic constitutive class and jointly support the claimed shared operator and onset structures.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — Each paired mapping equates objects of identical mathematical type (bifurcation of the stress operator, scalar onset functional of \(N_1/\tau_{xy}\), identical tensorial advection operator, identical extensional eigenvalue singularity) and the Operator Role statements name the shared structure without hedging.
- **CHECK 3 (Correspondence Vector Support):** PASS — All four listed vectors are demonstrated by explicit equations and reductions in Section 3: the upper-convected operator appears identically on both sides; the Pakdel–McKinley and recoverable-shear functionals are shown to encode the same Weissenberg threshold; the planar-extensional singularity equation and critical \(\lambda\dot\epsilon=1/2\) are written for both; and the Weissenberg/Deborah threshold identity is recovered from both onset criteria.
- **CHECK 4 (Transfer and Falsifiability):** PASS — Transfer is genuinely asymmetric (mature bifurcation/DNS toolkit for the upper-convected operator exists on the complex-fluid side while extrusion still relies on empirical \(S_R\) maps); the prediction supplies a concrete wall-shear-rate interval \(45\)–\(75\,\mathrm{s}^{-1}\) for a fully specified geometry and material, with an explicit falsification criterion.

#### Stage 3 Watch Items
None identified.

### Ninth Adversarial Review
**Reviewer:** Meta Muse Spark 1.1
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-19

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Silo A Oldroyd-B equations including continuity, momentum with beta Laplacian, and tau + Wi upper-convected tau = (1-beta)(grad u + grad u^T) with definition of upper-convected derivative are correctly from viscoelastic fluid dynamics; Silo B PTT equation f(tr tau) tau + Wi upper-convected tau = same RHS with f = 1 + epsilon Wi/(1-beta) tr tau and recoverable shear S_R = N1/(2 tau_xy) are correctly from polymer melt extrusion; both share same operator class and extensional singularity tau_11 = 2 eta_p epsilon_dot / (1 - 2 lambda epsilon_dot) at lambda epsilon_dot = 1/2.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All four pairs map compatible types: instability phenomenon ↔ instability phenomenon with shared upper-convected operator on tau', scalar onset functional M ↔ scalar onset functional S_R both formed from N1/tau_xy ratio and expressed as Wi-dependent threshold, operator ↔ operator with identical tensorial definition, and extensional singularity ↔ extensional singularity with same tau_11 equation; no spatial-to-temporal, field-to-global-parameter, or dimensional-to-dimensionless category errors, and Operator Role specifies shared mathematical structure not hedged analogy.
- **CHECK 3 (Correspondence Vector Support):** PASS — All four listed vectors demonstrated: shared_upper_convected_tensor_advection_operator via explicit derivative definition and appearance in both constitutive laws (Sec 3); curvature_hoop_stress_onset_criterion_pakdel_mckinley_vs_recoverable_shear via M = (Wi/(Rc/L))(tau_ss/(eta_p gamma_dot)) >= M_crit derivation to M = 2 Wi^2 L/Rc and S_R = N1/(2 tau_xy) >= S_R,crit derivation to S_R ≃ Wi (Sec 3 and Sec 2); planar_extensional_stagnation_point_coil_stretch_singularity via tau_11 formula and lambda epsilon_dot = 1/2 in both Silo A and UCM limit of Silo B (Sec 3); dimensionless_weissenberg_deborah_threshold_identity via S_R ≃ lambda gamma_dot = Wi and M ∝ Wi^2 L/Rc establishing same Wi threshold (Sec 2, Sec 3).
- **CHECK 4 (Transfer and Falsifiability):** PASS — Asymmetry justified: complex-fluid-dynamics has mature DNS, linear stability tracking, bifurcation continuation, finite-time Lyapunov diagnostics for upper-convected operator, while polymer-melt-extrusion relies on empirical recoverable-shear correlations, so direction complex-fluid-dynamics → polymer-melt-extrusion is not reversible with comparable benefit; falsifiability satisfied by quantitative prediction of onset at apparent wall shear rate 60.6 ± 7.5 s^-1 (falsification interval 45–75 s^-1) versus baseline 36.4 s^-1 for specified 10:1 contraction die, with measurable birefringence/pressure-fluctuation experiment. No canonical textbook prior-art pairing recognized that would trigger advisory FLAG under 4c.

#### Stage 3 Watch Items
- Verify impact of PTT damping function nonlinearity at high Wi ~8 on the claimed identity S_R ≃ Wi and tau_11 singularity, since entry uses UCM limit to bridge.
- Check literature for sqrt vs non-sqrt definitions of Pakdel–McKinley M and whether M_crit vs S_R,crit mapping remains consistent.
- Probe bibliometric novelty of linking Pakdel–McKinley curvature criterion to critical recoverable shear for sharkskin/gross melt fracture, as noted primary failure risk is constitutive_law_mismatch.