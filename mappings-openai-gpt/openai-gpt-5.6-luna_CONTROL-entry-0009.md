---
sid_metadata:
  entry_id: "CONTROL-SID-0009"
  schema_version: "2.0-control"
  maturity_stage: "adversarial-flagged"
provenance:
  company: "OpenAI"
  model_family: "GPT"
  model_version: "5.6 Luna"
  generation_timestamp: "2026-08-17"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "tumor-biomechanics-biphasic-growth"
  domain_b: "dendritic-metal-solidification"
  structural_family: "thin-interface-free-boundary-asymptotics / curvature-kinetic-selection"
  triple_correspondence_vectors:
    - "gradient-energy_curvature_solvability_operator"
    - "normal-flux_kinematic_free-boundary_operator"
    - "thin-interface_Peclet_curvature_similarity_pair"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language / historically_isolated_communities / incompatible_physical_constitutive_laws_but_shared_interface_asymptotics"
prior_discovery_metrics:
  structural_isomorphism_score: 8.3
  vocabulary_divergence_score: 8.7
  expected_methodological_transfer_score: 8.8
  community_separation_score: 8.1
  representation_mismatch_score: 7.9
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 8.1
    uncertainty: "±1.1"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "low"
  primary_failure_risk: "constitutive_law_mismatch"
  bibliometric_validation: "pending"
  first_adversarial_review:
    reviewer_model: "Anthropic Claude Sonnet 5"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "FLAG"
    verdict_rationale: "No FAIL-level issue was found in Checks 1-3 or Check 4(a)/(b); the sole finding is a Check 4(c) prior-art flag — Cahn-Hilliard's classical sharp-interface limit is itself Mullins-Sekerka type, a solidification-originated free-boundary model — which is advisory only and does not affect the mathematics' internal validity."
    failed_checks: []
    flagged_checks: ["Check 4(c): prior-art recognition — the entry's curvature-kinetic correspondence overlaps with the classical Cahn-Hilliard-to-Mullins-Sekerka sharp-interface result (Mullins-Sekerka itself being a solidification model) and with existing tumor-interface/dendritic-instability analogies in the mathematical-oncology literature"]
    quoted_evidence: []
    stage_3_watch_items:
      - "Cahn-Hilliard's sharp-interface limit is classically Mullins-Sekerka type (Pego 1989; Alikakos-Bates-Chen 1994), and Mullins-Sekerka (1963) itself originates as a solidification free-boundary model. This may substantially narrow the entry's actual novel content to the specific numerical-transfer proposal in Section 4, independent of the general tumor/dendrite curvature-kinetic framing."
      - "Search mathematical-oncology free-boundary literature (e.g. work descending from Cristini & Lowengrub on multiscale tumor modeling) for existing explicit tumor-interface/Mullins-Sekerka or tumor-interface/dendritic-instability analogies — the entry's own Section 3 SIAM citation already gestures toward this connection without closing the loop on it."
      - "The entry's asymmetric-novelty claim actually rests on a narrower point than the general correspondence: whether the specific thin-interface Peclet-curvature calibration / anti-trapping-style width correction (Section 4) has already been attempted for tumor Cahn-Hilliard numerics specifically. Verify this narrow claim, not the broader curvature-kinetic analogy."
      - "Confirm the Section 4 asymmetry claim under that narrow reading, since the tumor side already has rigorous sharp-interface limit theory (per the entry's own SIAM reference) that partially overlaps with solidification-derived free-boundary theory."
  second_adversarial_review:
    reviewer_model: "Alibaba Qwen 3.8 Max"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "FLAG"
    verdict_rationale: "The entry is mathematically rigorous and structurally sound, but flagged under Check 4 because the base isomorphism between diffuse-interface tumor growth and dendritic solidification (both reducing to Mullins-Sekerka/Stefan moving boundary problems) is a canonical analogy in applied mathematics that requires Stage 3 bibliometric verification for the specific thin-interface transfer."
    failed_checks: []
    flagged_checks: ["Check 4: Prior art recognition - the base mapping of diffuse-interface tumor growth to Mullins-Sekerka/Stefan problems is a canonical textbook analogy in applied mathematics (e.g., Lowengrub, Cristini, Friedman), requiring Stage 3 verification of whether the specific thin-interface asymptotic transfer has already been published."]
    quoted_evidence: []
    stage_3_watch_items: ["Verify if the specific transfer of quantitative thin-interface asymptotics (e.g., anti-trapping currents, finite-width calibration) to tumor phase-field models has already been published, as the base mapping of diffuse-interface tumor growth to Mullins-Sekerka/Stefan problems is a canonical textbook analogy."]
  third_adversarial_review:
    reviewer_model: "DeepSeek DeepSeek V4 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "FLAG"
    verdict_rationale: "No fatal equation-class or category errors were found, but two specific non-fatal internal inconsistencies and a prior-art advisory warrant flagging before Stage 3."
    failed_checks: []
    flagged_checks:
      - "Check 1: Silo B operator-map sign inconsistency and omitted β factor in the inner nutrient scaling"
      - "Check 4: Prior-art advisory for thin-interface/anti-trapping asymptotic calibration"
    quoted_evidence: []
    stage_3_watch_items:
      - "Verify novelty of applying dendritic thin-interface/anti-trapping calibration to Cahn-Hilliard tumor growth; search Karma-Rappel thin-interface asymptotics and tumor phase-field sharp-interface limits."
      - "Probe whether the β factor in the tumor nutrient equation is assumed equal to 1 in the vector-3 inner scaling, and whether this affects the stated Péclet similarity."
  fourth_adversarial_review:
    reviewer_model: "Google Gemini 3.1 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "PASS"
    verdict_rationale: "The entry successfully identifies a consistent structural correspondence between the inner-solvability operators and kinematic boundary conditions of Cahn-Hilliard tumor models and Allen-Cahn dendritic solidification, fully supporting all claimed mathematical vectors."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: 
      - "The potential notation collision in Silo A where \\mu denotes both the Cahn-Hilliard chemical potential (Vector 1) and the Darcy mobility (Vector 2); while standard in both respective subfields, it should be explicitly disambiguated during formal methodology transfer."
  fifth_adversarial_review:
    reviewer_model: "Xiaomi MiMo V2.5 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "PASS"
    verdict_rationale: "All four checks pass: equations are correctly typed and classified, vocabulary mappings pair objects of compatible mathematical type, all three correspondence vectors are demonstrated with explicit equations and derivations on both sides, and the transfer direction is genuinely asymmetric with a highly specific falsifiable prediction."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items:
      - "The general tumor-growth / dendritic-solidification phase-field analogy is well-established in the phase-field community (e.g., Cristini–Lowengrub–Wise line of work on tumor free-boundary problems explicitly borrowing solidification frameworks). Stage 3 should determine whether the specific thin-interface-calibration transfer claim — as opposed to the general analogy — has already been published."
      - "The entry acknowledges that the Silo A bulk operator is fourth-order Cahn–Hilliard while Silo B is second-order Allen–Cahn, and restricts the correspondence to the sharp-interface reduction. Stage 3 should verify that the cited thin-interface asymptotic analyses (references [3] and [7]) indeed support the specific inner-expansion results presented, particularly the Silo A solvability condition μ_Γ = γ_T κ + driving terms."
      - "The falsifiable prediction names a 5% error criterion and 3× width increase with specific numerical comparators (IGA–POD–DEIM solver). Stage 3 should check whether comparable quantitative thin-interface calibration benchmarks already exist in the tumor phase-field literature."
  sixth_adversarial_review:
    reviewer_model: "Z.AI GLM-5.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "PASS"
    verdict_rationale: "All four checks pass: equations are correctly stated and attributed, the equation-class difference (Cahn-Hilliard 4th order vs Allen-Cahn 2nd order) is explicitly acknowledged and the isomorphism correctly restricted to inner-interface asymptotics, all three correspondence vectors are demonstrated with derivations, and the falsifiable prediction names specific measurable quantities with quantitative thresholds."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: ["The thin-interface asymptotics framework for phase-field models (Karma-Rappel, Echebarria et al.) is canonical in the solidification literature; verify whether this specific cross-domain transfer to tumor biomechanics has been previously published.", "The sharp-interface limit of Cahn-Hilliard tumor models producing Mullins-Sekerka type problems is referenced via SIAM [3]; check whether any prior work has already applied anti-trapping current or thin-interface calibration techniques to tumor phase-field models.", "The 2026 IGA-POD-DEIM reference [9] is dated in the future relative to training data; verify this citation exists and contains what the entry claims it contains.", "The 2025 Cavalleri formulation is named as a constitutive model reference; verify this citation exists and is correctly characterized."]
  seventh_adversarial_review:
    reviewer_model: "Microsoft Copilot 1.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "PASS"
    verdict_rationale: "The entry consistently demonstrates three interface-level correspondences via inner-coordinate solvability, normal-flux Stefan-type relations, and thin-interface Pe/Ca bookkeeping while explicitly acknowledging and isolating the bulk-operator class mismatch."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items:
      - "This is an interface-asymptotic equivalence, not an identity between the fourth-order tumor Cahn–Hilliard bulk operator and the second-order dendritic Allen–Cahn bulk operator."
      - "The proposed second-order dendritic-style calibration is predicted to permit a **3-fold increase in computational interface width**, giving (\\eta_\\Gamma=3/60=1/20), while keeping the maximum relative error in the measured tumor-interface radius (R(t)), interfacial curvature (\\kappa(t)), and normal velocity (V_n(t)) below the **5%** criterion (1/20)."
      - "Verify the applicability of anti-trapping style corrections to a conserved-order-parameter Cahn–Hilliard tumor model with mechanical coupling; confirm whether the anti-trapping construction used in alloy models (which targets solute trapping with a non-conserved phase-field) transfers without introducing spurious mass/energy sources in the tumor model."
      - "Probe the constitutive-law sensitivity: quantify how mechanical coupling terms W_{,\\phi}(\\phi,\\mathcal E(u)) and pressure-driven normal flux coefficients alter the inner solvability constants (\\gamma_T, effective mobility calibration) compared with the dendritic calibration assumptions."
      - "Request numerical reproducibility checks: (a) reproduce the claimed 3× interface-width increase experiment in a decoupled benchmark limit; (b) report measured O(\\eta_\\Gamma) vs O(\\eta_\\Gamma^2) error scaling before and after calibration; (c) provide details of the calibration procedure (which parameters are tuned and how) and sensitivity to mesh/time discretization."
  eighth_adversarial_review:
    reviewer_model: "xAI Grok 4.5 Fast"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "PASS"
    verdict_rationale: "All four checks confirm internal mathematical consistency: equations support the claimed interface-asymptotic free-boundary structure, vocabulary pairs are type-compatible with shared operator roles, all three listed vectors are demonstrated by explicit expansions and operator maps, and the transfer prediction is asymmetric and quantitatively falsifiable."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: []
  ninth_adversarial_review:
    reviewer_model: "Meta Muse Spark 1.1"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "PASS"
    verdict_rationale: "All three correspondence vectors are demonstrated with inner-expansion equations and operator identities, vocabulary maps are type-compatible, and transfer is asymmetric and quantitatively falsifiable."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: []
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ⚠*CONTROL*⚠ ENTRY 0009

## 1. CROSS-SILO SYSTEM DEFINITION

* **Silo A (Field 1):** Tumor biomechanics-biphasic-growth: diffuse-interface Cahn–Hilliard tumor-volume-fraction dynamics coupled to nutrient reaction–diffusion and elastic/viscoelastic mechanics, with the diffuse-interface parameter representing the tumor/host transition thickness. Recent formulations explicitly couple the Cahn–Hilliard chemical potential to nutrient and strain-energy terms. ([ScienceDirect][1])
* **Silo B (Field 2):** Dendritic-metal-solidification: quantitative phase-field evolution of a non-conserved solid/liquid order parameter coupled to conserved alloy composition, with a finite computational interface width, anisotropic interfacial energy, capillary/kinetic corrections and Stefan-type solute conservation. Quantitative solidification phase fields explicitly use thin-interface asymptotics and anti-trapping corrections to reduce finite-width kinetic artifacts. ([PubMed Central (PMC)][2])
* **Mathematical Isomorphism:** Under the inner-coordinate transformation (z=d/\varepsilon), affine normalization of the scalar state variables, and restriction to the moving diffuse interface, both systems reduce to the same curvature–kinetic free-boundary structure: a gradient-energy solvability operator generates an interfacial curvature term, a conserved normal-flux operator determines (V_n), and the leading finite-width error is controlled by the pair ((\varepsilon\kappa,\varepsilon V_n/D)); this is an interface-asymptotic equivalence, not an identity between the fourth-order tumor Cahn–Hilliard bulk operator and the second-order dendritic Allen–Cahn bulk operator.

## 2. DIAGNOSTIC VOCABULARY MATRIX

* **Tumor diffuse-interface phase (\phi)** ↔ **dendritic solid/liquid phase (\varphi)**

  * *Operator Role:* Both are real-valued scalar order-parameter fields entering a gradient-energy functional and producing a curvature contribution through the normal-coordinate solvability problem; the transformation is affine normalization ( \hat\phi=(\phi-\phi_H)/(\phi_T-\phi_H)) and ( \hat\varphi=(\varphi-\varphi_L)/(\varphi_S-\varphi_L)), so both mapped objects are dimensionless real scalar fields.
* **Tumor nutrient (\sigma)** ↔ **dendritic alloy composition (c)**

  * *Operator Role:* After dimensionless normalization ( \hat\sigma=(\sigma-\sigma_\Gamma)/\Delta\sigma) and ( \hat c=(c-c_l^0)/\Delta c), both enter conserved bulk transport operators and their interface-normal fluxes; the mapped mathematical type is a real scalar field, while reaction/partition constitutive terms remain domain-specific.
* **Tumor interface thickness (\varepsilon)** ↔ **dendritic phase-field width (W)**

  * *Operator Role:* Both are positive length scales in the inner coordinate (z=d/\ell_\Gamma); the dimensionless control parameters are (Ca_\Gamma=\ell_\Gamma\kappa) and (Pe_\Gamma=\ell_\Gamma |V_n|/D), with (\ell_\Gamma=\varepsilon) for the tumor model and (\ell_\Gamma=W) for the dendritic phase-field model.

## 3. CORE MATHEMATICAL PARALLELISM

Silo A uses a Cahn–Hilliard-type phase equation, a nutrient reaction–diffusion equation, and mechanical equilibrium. A representative mechanically coupled formulation is

```math
\partial_t\phi
=
\nabla\!\cdot(M\nabla\mu)+U(\phi,\sigma,\mathcal E(u)),
```

```math
\mu
=
-\varepsilon\Delta\phi
+\varepsilon^{-1}\Psi'(\phi)
-\chi\sigma
+W_{,\phi}(\phi,\mathcal E(u)),
```

```math
\beta\,\partial_t\sigma
=
D_\sigma\Delta\sigma+S(\phi,\sigma),
\qquad
\nabla\!\cdot W_{,\mathcal E}(\phi,\mathcal E(u))=0 .
```

These terms and their mechanical coupling are independently present in tumor phase-field literature. ([ScienceDirect][1])

The corresponding Silo-B phase-field model is independently recognizable as a dendritic-solidification model because the solid/liquid order parameter obeys an Allen–Cahn-type anisotropic equation while composition is conserved. A representative binary-alloy formulation is

```math
\tau(\theta)\,\partial_t\varphi
=
\nabla\!\cdot\!\left(W^2a(\theta)^2\nabla\varphi\right)
+\mathcal F(\varphi,c,T,\theta),
```

```math
\partial_t c
=
\nabla\!\cdot
\left(
D\,q(\varphi)\nabla c
+\mathbf j_{\rm at}
\right),
```

with the independently derived anti-trapping current

```math
\mathbf j_{\rm at}
=
-a_{\rm at}(\varphi)\,
W\,\partial_t\varphi\,
\frac{\nabla\varphi}{|\nabla\varphi|}.
```

Quantitative dendritic phase-field formulations use this finite-width correction specifically to suppress spurious solute trapping and to recover sharp-interface behavior at computationally enlarged interface widths. ([PubMed Central (PMC)][2])

**Correspondence vector 1 — gradient-energy_curvature_solvability_operator.**
For Silo A, suppress the non-interface source terms in the inner layer and write the free-energy contribution as

```math
\mathcal F_T[\phi]
=
\int_\Omega
\left[
\frac{\varepsilon}{2}|\nabla\phi|^2
+\frac{1}{\varepsilon}\Psi(\phi)
+W(\phi,\mathcal E(u))
-\chi\sigma\phi
\right]\,dx .
```

With (z=d/\varepsilon) and

```math
\phi(x,t)=q(z)+\varepsilon q_1(z,s,t)+\cdots ,
\qquad
q''-\Psi'(q)=0 ,
```

the first inner solvability condition produces the interfacial curvature term. Defining

```math
\gamma_T
=
\int_{-\infty}^{\infty}(q'(z))^2\,dz ,
```

the leading interfacial chemical-potential relation has the structure

```math
\mu_\Gamma
=
\gamma_T\kappa
-\chi\sigma_\Gamma
+W_{,\phi,\Gamma}
+O(\varepsilon\kappa^2).
```

The tumor sharp-interface literature independently establishes that the (\varepsilon\to0) limit produces a curvature-controlled free-boundary problem of Mullins–Sekerka type. ([SIAM][3])

For Silo B, the corresponding gradient-energy functional is

```math
\mathcal F_D[\varphi]
=
\int_\Omega
\left[
\frac{W^2}{2}\,a(\theta)^2|\nabla\varphi|^2
+f(\varphi,c,T)
\right]\,dx ,
```

so that its phase-field evolution is an (L^2)-gradient-flow equation,

```math
\tau\,\partial_t\varphi
=
-\frac{\delta\mathcal F_D}{\delta\varphi}.
```

The inner-coordinate expansion across the solid/liquid layer produces the sharp-interface Gibbs–Thomson/kinetic condition

```math
U_\Gamma
=
-d_0\,a(\theta)\kappa
-\beta_k V_n
+O(W^2\kappa^2)
+O\!\left(W|V_n|/D\right).
```

The curvature and kinetic terms are independently standard in dendritic solidification theory. ([PubMed Central (PMC)][4])

Thus the demonstrated operator map is between the *inner solvability operators*:

```math
-\varepsilon\Delta
+\varepsilon^{-1}\Psi'(\cdot)
\quad
\xrightarrow[\;z=d/\varepsilon\;]{\text{inner solvability}}
\quad
\gamma_T\kappa+\text{driving terms},
```

```math
-W^2\nabla\!\cdot(a^2\nabla)
+\partial_\varphi f(\cdot)
\quad
\xrightarrow[\;z=d/W\;]{\text{inner solvability}}
\quad
-d_0a(\theta)\kappa-\beta_kV_n+\text{driving terms}.
```

The mapping stops at the interface reduction: the tumor bulk operator is fourth-order in (\phi), whereas the dendritic phase-field bulk operator is second-order in (\varphi).

**Correspondence vector 2 — normal-flux_kinematic_free-boundary_operator.**
For Silo A, a sharp-interface tumor formulation gives the interface velocity as a linear combination of normal fluxes. A representative mechanically coupled/free-boundary reduction is

```math
\Delta p=0
\quad\text{in }\Omega_T,
```

```math
\Delta\sigma_i-\mu_i^2\sigma_i=0
\quad\text{in }\Omega_i,
```

```math
V_n
=
-\mu\,\partial_n p
+\chi_\sigma\,\partial_n\sigma_1
\quad\text{on }\Gamma .
```

The pressure jump is curvature-controlled,

```math
p_\Gamma
=
\mathcal G^{-1}\kappa
+\text{nutrient/mechanical driving terms}.
```

These equations are explicitly used to express tumor interface motion in terms of normal pressure and nutrient gradients. ([PubMed Central (PMC)][5])

For Silo B, mass conservation across the solid/liquid front independently produces a Stefan relation of the same operator type,

```math
V_n(c_l-c_s)
=
D_l\,\partial_n c_l
-
D_s\,\partial_n c_s .
```

In the common one-sided-diffusion limit (D_s\to0),

```math
V_n
=
\frac{D_l\,\partial_n c_l}{c_l-c_s}.
```

The dendritic literature explicitly identifies this as the Stefan condition paired with the Gibbs–Thomson relation. ([ResearchGate][6])

The operator correspondence is therefore

```math
V_n
=
\mathcal K_T
\begin{bmatrix}
\partial_n p\\[2pt]
\partial_n\sigma
\end{bmatrix}
```

↔

```math
V_n
=
\mathcal K_D
\begin{bmatrix}
\partial_n c_l\\[2pt]
\partial_n c_s
\end{bmatrix},
```

where both (\mathcal K_T) and (\mathcal K_D) are scalar linear maps from a finite collection of normal fluxes to the interface-normal velocity; the coefficients remain constitutively different.

**Correspondence vector 3 — thin-interface_Peclet_curvature_similarity_pair.**
For Silo A, let (\ell_\Gamma=\varepsilon), (R) be a local radius of curvature, (V_n) the interface speed, and (D_\sigma) the nutrient diffusivity. Then

```math
Ca_\Gamma^{(T)}
=
\frac{\varepsilon}{R}
=
\varepsilon|\kappa|,
\qquad
Pe_\Gamma^{(T)}
=
\frac{\varepsilon |V_n|}{D_\sigma}.
```

The inner nutrient equation becomes, under (z=d/\varepsilon),

```math
-\frac{\varepsilon V_n}{D_\sigma}\,\partial_z\sigma
=
\partial_{zz}\sigma
+
\frac{\varepsilon^2}{D_\sigma}S(\phi,\sigma)
+\text{higher-order geometric terms},
```

so the first moving-interface correction is explicitly controlled by (Pe_\Gamma^{(T)}), while curvature corrections are controlled by (Ca_\Gamma^{(T)}).

For Silo B, with (\ell_\Gamma=W) and alloy diffusivity (D),

```math
Ca_\Gamma^{(D)}
=
W|\kappa|,
\qquad
Pe_\Gamma^{(D)}
=
\frac{W|V_n|}{D}.
```

The same inner-coordinate scaling gives

```math
-\frac{WV_n}{D}\,\partial_z c
=
\partial_{zz}c
+\text{phase-change and anti-trapping terms},
```

and the dendritic thin-interface construction is explicitly controlled by the conditions (W\kappa\ll1) and (WV_n/D\ll1). ([arXiv][7])

After the normalization

```math
\eta_\Gamma
=
\max\!\left(
\ell_\Gamma|\kappa|,
\frac{\ell_\Gamma|V_n|}{D}
\right),
```

both inner problems have the same asymptotic bookkeeping: the uncorrected finite-width solution contains (O(\eta_\Gamma)) interface errors, while a second-order thin-interface calibration can be constructed to cancel the first-order coefficient and leave (O(\eta_\Gamma^2)) residuals. The proposed SID transfer is therefore a transfer of the *calibration machinery* that maps finite computational width onto invariant sharp-interface kinetic and curvature coefficients, not a claim that tumor constitutive laws equal alloy thermodynamics.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS

* **Preferred Transfer Direction:** dendritic-metal-solidification → tumor-biomechanics-biphasic-growth
* **Asymmetric Maturity Rationale:** Dendritic solidification has a mature quantitative thin-interface toolkit comprising matched-asymptotic parameter calibration, anti-trapping flux construction, adaptive phase-field refinement, implicit temporal discretization, multigrid solvers, and explicit benchmarking against sharp-interface growth theories. ([ScienceDirect][8]) Tumor phase-field research has a mature sharp-interface theory and rapidly advancing energy-stable discretizations, including 2026 IGA–POD–DEIM and BDF2/SAV formulations, but the literature identified here does not establish an equally mature finite-(\varepsilon) calibration protocol whose purpose is to enlarge the computational interface while preserving independently measurable sharp-interface curvature/velocity coefficients. ([ScienceDirect][9])
* **Target Bottleneck Mitigation:** Import the dendritic thin-interface workflow into the mechanically coupled tumor model: perform a first- and second-order inner expansion, numerically identify the (O(\eta_\Gamma)) error in the tumor interface chemical potential and normal-velocity law, then calibrate (M(\varepsilon)), source interpolation (U(\phi,\sigma,\mathcal E)), and any admissible interface-local counterterm so that the measured ((\gamma_T,V_n)) pair is invariant with respect to computational interface width. The purpose is not to import alloy thermodynamics or the dendritic partition coefficient; it is to import the asymptotic *parameter-identification procedure* used to make a wide diffuse interface reproduce a narrow-interface free-boundary solution.
* **Falsifiable Prediction:** In a 3-D avascular tumor spheroid embedded in an elastic host with fixed nutrient supply, use the (\varepsilon\to0) extrapolation as the reference and define (\eta_\Gamma=\max(\varepsilon/R,\varepsilon|V_n|/D_\sigma)). Choose the reference calculation so that (\eta_\Gamma=1/60); the proposed second-order dendritic-style calibration is predicted to permit a **3-fold increase in computational interface width**, giving (\eta_\Gamma=3/60=1/20), while keeping the maximum relative error in the measured tumor-interface radius (R(t)), interfacial curvature (\kappa(t)), and normal velocity (V_n(t)) below the **5%** criterion (1/20). The mathematical basis is the cancellation of the (O(\eta_\Gamma)) finite-width term, leaving an (O(\eta_\Gamma^2)) asymptotic remainder; the quantitative transfer fails if the calibrated model exceeds (1/20) relative error at (\eta_\Gamma=1/20), or if a threefold width increase cannot maintain that criterion. The named numerical comparator is the 2026 IGA–POD–DEIM Cahn–Hilliard/reaction–diffusion tumor solver in its mechanically decoupled benchmark limit, with the 2025 mechanically coupled Cavalleri formulation as the constitutive model reference. ([ScienceDirect][9])

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION

* `"tumor growth" AND "Cahn-Hilliard" AND "thin-interface asymptotics" AND "interface thickness" AND "curvature"`
* `"dendritic solidification" AND "anti-trapping current" AND "thin-interface" AND "Gibbs-Thomson"`
* `"tumor growth" AND "anti-trapping current" AND "solute trapping" AND "phase field"` — deliberate falsification search for an already-published direct tumor/anti-trapping correspondence
* `"tumour" AND "quantitative phase-field" AND "finite interface thickness" AND "normal velocity" AND "sharp interface"`
* `"Cahn-Hilliard tumor" AND "Stefan condition" AND "Gibbs-Thomson" AND dendrite`

[1]: https://www.sciencedirect.com/science/article/pii/S1468121820301103?utm_source=chatgpt.com "On a phase field model of Cahn–Hilliard type for tumour growth with mechanical effects - ScienceDirect"
[2]: https://pmc.ncbi.nlm.nih.gov/articles/PMC11497217/?utm_source=chatgpt.com "On the primary spacing and microsegregation of cellular dendrites in laser deposited Ni-Nb alloys - PMC"
[3]: https://epubs.siam.org/doi/pdf/10.1137/24M1644523?download=true&utm_source=chatgpt.com "A Rigorous Approach to the Sharp Interface Limit for Phase-Field Models of Tumor Growth | SIAM Journal on Mathematical Analysis"
[4]: https://pmc.ncbi.nlm.nih.gov/articles/PMC3778506/?utm_source=chatgpt.com "An Interface-Fitted Finite Element Level Set Method with Application to Solidification and Solvation - PMC"
[5]: https://pmc.ncbi.nlm.nih.gov/articles/PMC8445073/?utm_source=chatgpt.com "Complex Far-Field Geometries Determine the Stability of Solid Tumor Growth with Chemotaxis - PMC"
[6]: https://www.researchgate.net/publication/360668336_Convective_effects_on_columnar_dendritic_solidification_--_A_multiscale_dendritic_needle_network_study?utm_source=chatgpt.com "(PDF) Convective effects on columnar dendritic solidification -- A multiscale dendritic needle network study"
[7]: https://arxiv.org/abs/cond-mat/0011010?utm_source=chatgpt.com "Sharp interface limits of phase-field models"
[8]: https://www.sciencedirect.com/science/article/pii/S0022024810001685?utm_source=chatgpt.com "Solute trapping and the effects of anti-trapping currents on phase-field models of coupled thermo-solutal solidification - ScienceDirect"
[9]: https://www.sciencedirect.com/science/article/pii/S0021999126004808?utm_source=chatgpt.com "An IGA-POD-DEIM framework for efficient simulation of a nonlinear diffuse-interface model of tumour growth based on a coupled Cahn-Hilliard–reaction-diffusion model: Energy-stable and error analysis - ScienceDirect"

---

## ADVERSARIAL REVIEWS (Stage 2)

### First Adversarial Review
**Reviewer:** Anthropic Claude Sonnet 5
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both equation systems match their claimed physical domains (tumor Cahn–Hilliard/reaction–diffusion/elasticity; dendritic Allen–Cahn/anisotropic-composition with anti-trapping current), and Section 1 correctly scopes the isomorphism to the shared interfacial (reduced) structure rather than bulk-operator identity, explicitly stating the mapping "stops at the interface reduction" given the 4th-order vs. 2nd-order bulk mismatch rather than concealing it.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All three Section 2 pairings (tumor phase ↔ dendritic phase, nutrient ↔ composition, interface thickness ε ↔ phase-field width W) map compatible mathematical types with stated explicit transformations (affine normalizations, shared inner-coordinate scaling) rather than resting on hedged-similarity language, and none matches a listed category-error pattern.
- **CHECK 3 (Correspondence Vector Support):** PASS — Vector 1 ("gradient-energy_curvature_solvability_operator") is demonstrated via matching free-energy functionals and inner expansions in Section 3 for both φ and the dendritic order parameter, with an independently checkable leading-order profile equation and surface-tension formula on the tumor side. Vector 2 ("normal-flux_kinematic_free-boundary_operator") is demonstrated via the tumor V_n law and the dendritic Stefan condition, both shown as linear maps of normal-derivative fluxes onto interface velocity. Vector 3 ("thin-interface_Peclet_curvature_similarity_pair") is demonstrated via matching Ca_Γ/Pe_Γ definitions and inner equations for both silos. All three listed vectors are supported with equations on both sides of the pairing, not merely named.
- **CHECK 4 (Transfer and Falsifiability):** FLAG — Asymmetry (a) and falsifiability (b) are both satisfied: the transfer direction rests on a specific numerical-calibration-maturity gap rather than a generic "both fields are hard" claim, and the Section 4 prediction names concrete measurable quantities (R(t), κ(t), V_n(t)), a specific width multiplier, and a specific error threshold with stated failure conditions. However, (c) prior art is recognized: Cahn–Hilliard's sharp-interface limit is classically Mullins–Sekerka type, and Mullins–Sekerka (1963) itself originates as a solidification free-boundary model — this is advisory only per protocol and does not affect the verdict on (a)/(b).

#### Stage 3 Watch Items
- Cahn–Hilliard's sharp-interface limit is classically known to be Mullins–Sekerka type (Pego 1989; Alikakos–Bates–Chen 1994), and Mullins–Sekerka (1963) itself originates as a solidification model — check whether this pre-existing mathematical bridge already covers the entry's general curvature-kinetic correspondence, independent of the tumor/dendrite application framing.
- Search for existing tumor-interface/Mullins–Sekerka or tumor-interface/dendritic-instability analogies in the mathematical-oncology free-boundary literature; the entry's own Section 3 SIAM citation already points toward this connection.
- The entry's asymmetric-novelty argument actually depends on a narrower claim than the general correspondence: whether the specific thin-interface Peclet-curvature calibration / anti-trapping-style width-correction protocol proposed in Section 4 has already been attempted for tumor Cahn–Hilliard numerics. Verify this narrow claim specifically.
- Re-examine the Section 4 asymmetry claim under that narrow reading, since the tumor side already has rigorous sharp-interface limit theory (per its own SIAM citation) that partially overlaps with solidification-derived free-boundary theory.

### Second Adversarial Review
**Reviewer:** Alibaba Qwen 3.8 Max
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The equations correctly model their respective domains, and the entry explicitly and correctly distinguishes between the incompatible bulk operator classes (4th-order Cahn-Hilliard vs. 2nd-order Allen-Cahn) and their shared asymptotic interface limits, avoiding any equation-class mismatch.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All mapped terms are of compatible mathematical types (dimensionless real scalar fields, positive length scales) with appropriate caveats for domain-specific constitutive terms.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed vectors (gradient-energy curvature solvability, normal-flux kinematic free-boundary, thin-interface Peclet curvature similarity) are fully demonstrated in Section 3 with explicit equations and inner-coordinate derivations.
- **CHECK 4 (Transfer and Falsifiability):** FLAG — The transfer direction and falsifiable prediction are highly specific and mathematically sound. However, the base isomorphism between diffuse-interface tumor growth and dendritic solidification (both reducing to Mullins-Sekerka/Stefan moving boundary problems) is a canonical analogy in applied mathematics (e.g., Lowengrub, Cristini, Friedman), requiring Stage 3 verification of whether the specific thin-interface asymptotic transfer has already been published.

#### Stage 3 Watch Items
- Verify if the specific transfer of quantitative thin-interface asymptotics (e.g., anti-trapping currents, finite-width calibration) to tumor phase-field models has already been published, as the base mapping of diffuse-interface tumor growth to Mullins-Sekerka/Stefan problems is a canonical textbook analogy.

### Third Adversarial Review
**Reviewer:** DeepSeek DeepSeek V4 Pro
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** FLAG — The Silo B operator map `-W^2\nabla\!\cdot(a^2\nabla)+\partial_\varphi f(\cdot)` is not equal to `-\delta\mathcal F_D/\delta\varphi` for the stated functional, since `\delta\mathcal F_D/\delta\varphi = -\nabla\!\cdot(W^2 a^2\nabla\varphi)+f_\varphi`; this is a sign-convention inconsistency rather than a fatal error. Separately, the vector-3 inner nutrient equation omits the factor `β` present in the stated tumor nutrient equation `β\partial_t\sigma = D_\sigma\Delta\sigma+S`, giving `-(ε V_n/D_\sigma)\partial_z\sigma` where `-(β ε V_n/D_\sigma)\partial_z\sigma` would follow unless `β=1` is assumed.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The mapped pairs are type-compatible: scalar order-parameter fields, scalar composition/nutrient fields, and positive length scales; no rate-to-state, spatial-domain-to-time, or dimensional-to-dimensionless category errors were found.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed vectors are supported in Section 3: the gradient-energy solvability operators are displayed for both silos, the normal-flux free-boundary operators are given on both sides, and the thin-interface Péclet/curvature similarity pair is defined and scaled for both silos.
- **CHECK 4 (Transfer and Falsifiability):** FLAG — The transfer direction is defensible and the prediction is specific and measurable. However, the thin-interface/anti-trapping calibration strategy is recognizable as a Karma-Rappel-type phase-field asymptotic construction; this is an advisory prior-art flag for Stage 3, not a rejection ground.

#### Stage 3 Watch Items
- Verify novelty of applying dendritic thin-interface/anti-trapping calibration to Cahn-Hilliard tumor growth; search Karma-Rappel thin-interface asymptotics and tumor phase-field sharp-interface limits.
- Probe whether the β factor in the tumor nutrient equation is assumed equal to 1 in the vector-3 inner scaling, and whether this affects the stated Péclet similarity.
- Confirm whether the Silo B operator-map sign inconsistency is purely conventional or indicates a deeper mismatch in the Gibbs-Thomson/kinetic sign convention.

### Fourth Adversarial Review
**Reviewer:** Google Gemini 3.1 Pro
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Equations are accurately reproduced and the distinction between the 4th-order Cahn-Hilliard bulk operator and 2nd-order Allen-Cahn bulk operator is correctly bounded by restricting the isomorphism to the shared inner-solvability limit.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All mappings pair objects of identical mathematical type (dimensionless scalars, transport fields, and interface length scales) with accurate mathematical roles.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three correspondence vectors listed in the metadata (gradient-energy curvature solvability, normal-flux kinematics, and thin-interface scaling) are fully demonstrated in Section 3 with explicit mathematical operator mapping and derivations.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction appropriately leverages the highly mature matched-asymptotics toolkit of dendritic phase fields (e.g., anti-trapping corrections), and the falsifiable prediction proposes a strictly quantifiable 3-fold relaxation in computational interface width against a 5% error threshold.

#### Stage 3 Watch Items
- The potential notation collision in Silo A where $\mu$ denotes both the Cahn-Hilliard chemical potential (Vector 1) and the Darcy mobility (Vector 2); while standard in their respective subfields, this should be explicitly disambiguated during formal methodology transfer.

### Fifth Adversarial Review
**Reviewer:** Xiaomi MiMo V2.5 Pro
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Silo A equations are correctly identified as fourth-order parabolic Cahn–Hilliard (conserved φ) coupled to second-order parabolic nutrient reaction–diffusion and elliptic mechanical equilibrium; Silo B equations are correctly identified as second-order parabolic Allen–Cahn (non-conserved φ) coupled to second-order parabolic conserved composition with anti-trapping current. The entry explicitly acknowledges the bulk operator class difference and restricts the correspondence to the sharp-interface reduction, which is the correct mathematical framing.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All three mapping pairs (φ↔φ̃ as real scalar order parameters, σ↔c as real scalar conserved fields, ε↔W as positive length scales serving as inner-coordinate stretching parameters) are between objects of identical mathematical type, with explicit affine normalizations and shared structural roles (gradient-energy functionals, inner solvability, dimensionless control parameters Ca_Γ and Pe_Γ).
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed vectors are demonstrated with equations on both sides: Vector 1 (gradient-energy solvability → curvature terms) through explicit inner expansions producing μ_Γ and U_Γ; Vector 2 (normal flux → kinematic velocity) through sharp-interface V_n = K[normal fluxes] on both sides; Vector 3 (thin-interface Péclet–curvature similarity) through unified η_Γ parameter and matched inner-coordinate scalings. No vector is merely named or gestured at.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction (dendritic → tumor) is genuinely asymmetric: dendritic solidification has decades of mature thin-interface calibration infrastructure while tumor phase-field models lack an equally developed finite-ε calibration protocol. The falsifiable prediction is highly specific: 3-fold computational interface width increase (η_Γ from 1/60 to 1/20) with <5% relative error in R(t), κ(t), and V_n(t), with explicit failure criteria and a named numerical comparator.

#### Stage 3 Watch Items
- The general tumor-growth / dendritic-solidification phase-field analogy is well-established (Cristini–Lowengrub–Wise line of work). Stage 3 should determine whether the specific thin-interface-calibration transfer has already been published, as distinct from the general analogy.
- Verify that the cited thin-interface asymptotic analyses (references [3] SIAM and [7] arXiv:cond-mat/0011010) support the specific inner-expansion solvability results presented for both silos.
- Check whether comparable quantitative thin-interface calibration benchmarks already exist in the tumor phase-field literature, which would narrow the novelty claim.

### Sixth Adversarial Review
**Reviewer:** Z.AI GLM-5.2
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The Cahn-Hilliard tumor equations (4th-order in φ through the chemical potential) and the Allen-Cahn dendritic equations (2nd-order in φ) are both correctly stated for their respective domains. The entry explicitly acknowledges the bulk operator mismatch: "this is an interface-asymptotic equivalence, not an identity between the fourth-order tumor Cahn–Hilliard bulk operator and the second-order dendritic Allen–Cahn bulk operator." The inner solvability reductions on both sides correctly produce curvature-kinetic conditions (Gibbs-Thomson type: μ_Γ = γ_T κ + ... for tumors, U_Γ = -d_0 a(θ)κ - β_k V_n + ... for dendrites) and Stefan-type flux-velocity relations, which are the same equation class at the sharp-interface level. No equation-class mismatch at the level where the correspondence is claimed.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All three mapped pairs are between objects of compatible mathematical type. Tumor φ ↔ dendritic φ are both real scalar order-parameter fields with explicit affine normalizations to dimensionless form. Tumor σ ↔ dendritic c are both real scalar fields entering conserved transport operators. Tumor ε ↔ dendritic W are both positive length scales in the inner coordinate. Each Operator Role explanation names shared mathematical structure (gradient-energy functional, inner solvability problem, dimensionless control parameters Ca_Γ and Pe_Γ) rather than relying on hedged language.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed vectors are demonstrated with equations and derivations in Section 3. Vector 1 (gradient-energy_curvature_solvability_operator) is demonstrated via inner-coordinate expansions of both free-energy functionals, showing the solvability conditions q''-Ψ'(q)=0 and the resulting curvature terms on both sides. Vector 2 (normal-flux_kinematic_free-boundary_operator) is demonstrated via the tumor V_n = -μ∂_n p + χ_σ ∂_n σ_1 and the dendritic Stefan condition V_n(c_l-c_s) = D_l∂_n c_l - D_s∂_n c_s, with explicit operator maps K_T and K_D. Vector 3 (thin-interface_Peclet_curvature_similarity_pair) is demonstrated via the paired inner nutrient/composition equations showing identical asymptotic bookkeeping controlled by (ℓ_Γ|κ|, ℓ_Γ|V_n|/D).
- **CHECK 4 (Transfer and Falsifiability):** PASS — The asymmetry is genuine: dendritic solidification possesses a mature thin-interface calibration toolkit (anti-trapping currents, matched-asymptotic parameter identification, benchmarking against sharp-interface theories) while the entry identifies that tumor phase-field research has sharp-interface limits but not an equally mature finite-ε calibration protocol. The direction is correct (not backwards). The falsifiable prediction names specific measurable quantities (R(t), κ(t), V_n(t)), a specific threshold (5% relative error), a specific experiment (3-fold interface width increase from η_Γ=1/60 to η_Γ=1/20), and a specific falsification condition. The named numerical comparator (2026 IGA-POD-DEIM solver) is specific enough for Stage 3 verification. Prior-art advisory: the thin-interface asymptotics framework for phase-field models is standard in the solidification literature (Karma-Rappel, Echebarria et al.), but the specific cross-domain transfer to tumor biomechanics is the novelty claim that Stage 3 should verify.

#### Stage 3 Watch Items
- Verify whether thin-interface asymptotics and/or anti-trapping current techniques have been previously applied to Cahn-Hilliard tumor phase-field models in any form.
- The sharp-interface reduction of Cahn-Hilliard to Mullins-Sekerka type problems is well-established (Pego 1989, Caginalp 1989); the SIAM reference [3] should be checked for whether it already contains finite-width calibration content beyond the ε→0 limit.
- References [9] (2026 IGA-POD-DEIM) and the 2025 Cavalleri formulation are dated relative to training data; verify these citations exist and contain what the entry claims.
- The 5% error threshold and 3-fold width increase factor are specific quantitative claims; check whether the dendritic solidification literature supports comparable improvement factors that would make this prediction well-calibrated.
- The Karma-Rappel thin-interface analysis (Phys. Rev. E, 1996/1998) and Echebarria et al. (Phys. Rev. E, 2004) are the canonical sources for the dendritic side; verify the entry's anti-trapping current formulation matches these references exactly.

### Seventh Adversarial Review
**Reviewer:** Microsoft Copilot 1.2
**Protocol:** v2.0  
**Verdict:** PASS  
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The entry explicitly states the bulk-operator class mismatch and restricts the claimed isomorphism to the inner-interface solvability reduction, so the fourth-order Cahn–Hilliard bulk operator and the second-order dendritic phase-field bulk operator are not asserted to be identical and the interface-level curvature–kinetic reductions are consistent.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — Each mapped token pair (e.g., **Tumor diffuse-interface phase (φ)** ↔ **dendritic solid/liquid phase (ϕ)**; **Tumor nutrient (σ)** ↔ **dendritic alloy composition (c)**; **ε ↔ W**) are the same mathematical object type (real scalar fields or length scales) and the Operator Role entries specify concrete shared structures (affine nondimensionalization; conserved bulk transport; inner-coordinate length-scale control).
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed vectors are demonstrated in the body:  
  - **gradient-energy_curvature_solvability_operator** — shown via inner expansion \( \phi(x,t)=q(z)+\varepsilon q_1+\cdots \), solvability condition \(q''-\Psi'(q)=0\), definition of \(\gamma_T\), and the Gibbs–Thomson–style relations for both silos (Section 3, Correspondence vector 1).  
  - **normal-flux_kinematic_free-boundary_operator** — shown by tumor normal-velocity expressed as a linear map of normal pressure and nutrient gradients and the dendritic Stefan condition mapping mass flux to \(V_n\) (Section 3, Correspondence vector 2).  
  - **thin-interface_Peclet_curvature_similarity_pair** — shown by defining \(Ca_\Gamma\) and \(Pe_\Gamma\) for both models, inner-coordinate scaled transport equations, and the shared asymptotic bookkeeping for finite-width errors (Section 3, Correspondence vector 3).
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction (dendritic → tumor) is plausibly asymmetric and justified by the mature thin-interface calibration toolkit in dendritic solidification; the entry provides a concrete, falsifiable numerical prediction (3× interface width with ≤5% error on specified observables and explicit \(\eta_\Gamma\) values) and specifies the numerical comparator and failure criteria.

#### Stage 3 Watch Items
- **Constitutive-law sensitivity:** Confirm how mechanical coupling terms \(W_{,\phi}(\phi,\mathcal E(u))\) and pressure-driven flux coefficients affect inner solvability constants and whether they introduce non-cancelable O(\(\eta_\Gamma\)) contributions that would invalidate thin-interface calibration assumptions.
- **Anti-trapping applicability:** Verify whether anti-trapping currents and the dendritic calibration machinery (developed for non-conserved phase + conserved composition) can be adapted to a conserved-order-parameter Cahn–Hilliard tumor model without violating mass/energy conservation or introducing spurious sources.
- **Numerical reproducibility:** Require explicit numerical experiments reproducing the claimed 3× interface-width increase in a decoupled benchmark limit, with reported pre/post calibration error scaling (O(\(\eta_\Gamma\)) → O(\(\eta_\Gamma^2\))) and sensitivity to discretization.
- **Parameter-identification details:** Request the exact calibration procedure (which parameters are tuned, how inner-layer matching is performed numerically, and whether the calibration is local to the interface or requires global re-tuning).
- **Prior-art advisory:** The entry cites standard sharp-interface limits and thin-interface literature; Stage 3 should check for canonical prior-art overlap (e.g., established Cahn–Hilliard → Mullins–Sekerka limits, and thin-interface anti-trapping constructions) to place novelty claims in context.
- **Document verbatim excerpts for context:**  
  - "This is an interface-asymptotic equivalence, not an identity between the fourth-order tumor Cahn–Hilliard bulk operator and the second-order dendritic Allen–Cahn bulk operator."  
  - "The proposed second-order dendritic-style calibration is predicted to permit a **3-fold increase in computational interface width**, giving (\eta_\Gamma=3/60=1/20), while keeping the maximum relative error in the measured tumor-interface radius (R(t)), interfacial curvature (\kappa(t)), and normal velocity (V_n(t)) below the **5%** criterion (1/20)."

### Eighth Adversarial Review
**Reviewer:** xAI Grok 4.5 Fast
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The displayed Cahn–Hilliard/nutrient/mechanics system and Allen–Cahn/composition/anti-trapping system reduce, under the stated inner-coordinate expansions, to compatible curvature–kinetic free-boundary operators of the same structural class; bulk-order mismatch is explicitly disclaimed and does not undermine the claimed asymptotic correspondence.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — Each paired token is of matching mathematical type (dimensionless scalar order parameter, normalized scalar concentration field, positive interface length scale) and the Operator Role statements identify shared structures (gradient-energy solvability producing curvature, normal-flux maps to \(V_n\), dimensionless control parameters \(\mathrm{Ca}_\Gamma\) and \(\mathrm{Pe}_\Gamma\)).
- **CHECK 3 (Correspondence Vector Support):** PASS — All three vectors are demonstrated: gradient-energy_curvature_solvability_operator by free-energy functionals, inner expansions and solvability conditions yielding \(\gamma_T\kappa\) versus \(d_0 a(\theta)\kappa\); normal-flux_kinematic_free-boundary_operator by explicit Stefan-type maps from normal derivatives to \(V_n\); thin-interface_Peclet_curvature_similarity_pair by the definitions of \(\mathrm{Ca}_\Gamma,\mathrm{Pe}_\Gamma\) and the corresponding inner transport equations controlling \(O(\eta_\Gamma)\) errors.
- **CHECK 4 (Transfer and Falsifiability):** PASS — Transfer direction is asymmetric (mature quantitative thin-interface calibration toolkit of solidification applied to a domain whose finite-\(\varepsilon\) calibration is stated to be less developed); the prediction supplies concrete numerical thresholds (threefold width increase from \(\eta_\Gamma=1/60\) to \(1/20\), relative error \(\le5\%\) on \(R(t),\kappa(t),V_n(t)\)) that can be measured against named reference solvers and therefore falsified.

#### Stage 3 Watch Items
None identified.

### Ninth Adversarial Review
**Reviewer:** Meta Muse Spark 1.1
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Silo A Cahn-Hilliard tumor equations and Silo B Allen-Cahn dendritic equations are correctly typed as phase-field models from their stated domains, and Section 1 explicitly limits the isomorphism to inner-coordinate free-boundary reduction, avoiding a bulk fourth-order vs second-order operator identity claim.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All three pairs map compatible types (scalar order-parameter field ↔ scalar order-parameter field, conserved scalar field ↔ conserved scalar field, length scale ↔ length scale) with explicit shared structure via affine normalization, gradient-energy functional, conserved flux operators, and inner coordinate z=d/ℓ_Γ.
- **CHECK 3 (Correspondence Vector Support):** PASS — gradient-energy_curvature_solvability_operator demonstrated via F_T/F_D functionals, q''-Ψ'(q)=0, μ_Γ=γ_T κ and U_Γ=-d0 aκ-β_k V_n; normal-flux_kinematic_free-boundary_operator demonstrated via V_n=-μ∂_n p+χ_σ∂_n σ_1 and V_n(c_l-c_s)=D_l∂_n c_l-D_s∂_n c_s; thin-interface_Peclet_curvature_similarity_pair demonstrated via Ca_Γ=ℓ_Γ|κ|, Pe_Γ=ℓ_Γ|V_n|/D and inner equations -(ℓ_ΓV_n/D)∂_z = ∂_zz.
- **CHECK 4 (Transfer and Falsifiability):** PASS — Asymmetry is justified: dendritic solidification has mature thin-interface calibration and anti-trapping construction, tumor phase-field lacks equivalent finite-ε width-enlargement protocol; falsifiability is specific with η_Γ=1/60 reference, 3-fold width increase to 1/20, and <5% relative error threshold on R(t), κ(t), V_n(t) against named IGA-POD-DEIM comparator; no canonical textbook analogy recognized as prior art.

#### Stage 3 Watch Items
- None identified.