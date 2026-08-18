---
sid_metadata:
  entry_id: "CONTROL-SID-0009"
  schema_version: "2.0-control"
  maturity_stage: "candidate"
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
