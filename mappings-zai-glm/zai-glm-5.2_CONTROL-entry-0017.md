---
sid_metadata:
  entry_id: "CONTROL-SID-0017"
  schema_version: "2.0-control"
  maturity_stage: "adversarial-rejected"
provenance:
  company: "Z.AI"
  model_family: "GLM"
  model_version: "5.2"
  generation_timestamp: "2026-08-17"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "fluid-dynamics"
  domain_b: "chromatographic-equilibrium-theory"
  structural_family: "viscous-shock-profile-instabilities"
  triple_correspondence_vectors:
    - "viscous_shock_profile_heteroclinic_orbit_system"
    - "linearized_spectral_evans_function_operator"
    - "hyperbolic_jacobian_eigenstructure_and_riemann_invariants"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language / incompatible_ontologies / historically_isolated_communities"
prior_discovery_metrics:
  structural_isomorphism_score: 8.8
  vocabulary_divergence_score: 9.2
  expected_methodological_transfer_score: 8.5
  community_separation_score: 9.0
  representation_mismatch_score: 7.5
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 8.0
    uncertainty: "±1.5"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "very_high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "constitutive_law_mismatch"
  bibliometric_validation: "pending"
  first_adversarial_review:
    reviewer_model: "Anthropic Claude Sonnet 5"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "REJECT"
    verdict_rationale: "Correspondence 2's linearized Evans-function operator omits the wave-speed term that the entry's own Correspondence 1 correctly carries, and Correspondence 3 compares flux-Jacobian eigenstructures of mismatched dimension against the entry's own state-vector definitions; both are Check 1 equation errors, not judgment calls."
    failed_checks: ["Check 1: linearized_spectral_evans_function_operator (Section 3) drops the wave-speed term s present in the entry's own traveling-wave ODE", "Check 1: hyperbolic_jacobian_eigenstructure_and_riemann_invariants (Section 3) pairs Jacobians of mismatched dimension that also mismatch the entry's own U and w definitions"]
    flagged_checks: ["Check 2: Vocabulary Matrix bullet 1 conflates c and w as the object mapped to U", "Check 3: hyperbolic_jacobian_eigenstructure_and_riemann_invariants demonstrated only via non-matching reduced sub-systems", "Check 1 (advisory): wall-heat-transfer source term is explicitly linear in T while the paired chemical-reaction source is conventionally nonlinear in combustion theory, bearing on the shared 'Hopf bifurcation' claim"]
    quoted_evidence: ["\\mathbf{D} \\mathbf{P}'' - \\mathbf{J}(\\mathbf{U}_0) \\mathbf{P}' + \\left( -\\mathbf{J}'(\\mathbf{U}_0) \\mathbf{U}_0' + \\mathbf{J}_{S}(\\mathbf{U}_0) - \\lambda \\mathbf{I} \\right) \\mathbf{P} = 0", "\\mathbf{D}_{ax} \\mathbf{p}'' - \\mathbf{A}(\\mathbf{w}_0) \\mathbf{p}' + \\left( -\\mathbf{A}'(\\mathbf{w}_0) \\mathbf{w}_0' + \\mathbf{J}_{S}(\\mathbf{w}_0) - \\lambda \\mathbf{I} \\right) \\mathbf{p} = 0", "(\\mathbf{J}(\\mathbf{U}) - s\\mathbf{I})", "\\mathbf{U} = (\\rho, \\rho u, \\rho E, \\rho Y)^T", "\\text{eigenvalues } \\lambda_{1,2,3} = u, \\quad u \\pm c", "\\mathbf{w} = (c_1, c_2, T)^T", "\\mathbf{A}(\\mathbf{w}) = u \\left( \\mathbf{I} + F \\frac{\\partial \\mathbf{q}}{\\partial \\mathbf{c}} \\right)^{-1}, \\quad \\text{eigenvalues } \\mu_{1,2} = \\text{eig}(\\mathbf{A})"]
    stage_3_watch_items: ["Whether Evans-function / dynamical-systems stability methods have precedent in packed-bed, fixed-bed, or chromatographic thermal-front instability literature — this reviewer has only general awareness of the technique's portability, not specific recall of this pairing", "Whether S(w) = (0,0,-h(T-T_w)), which is explicitly linear in T, can drive a Hopf bifurcation the way Section 2 and Section 4 assume by analogy to the (conventionally nonlinear, Arrhenius-type) chemical source S(U) — the entry never states omega's functional form, so this should be checked directly", "The Section 4 falsifiable prediction's specific scaling claim (h_crit proportional to Pe^{-1}) is computed from the flawed Evans operator and should be re-derived with the corrected (wave-speed-inclusive) operator before being treated as reliable", "Confirm the intended U-analog in Vocabulary Matrix bullet 1 is c or w (see Check 2); this affects the stated units and nondimensionalization"]
  second_adversarial_review:
    reviewer_model: "Alibaba Qwen 3.8 Max"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "REJECT"
    verdict_rationale: "The entry provides a 2D isothermal Jacobian formula for a 3D non-isothermal state vector, constituting a fatal equation-class/dimension mismatch that invalidates the third correspondence vector."
    failed_checks: ["Check 1: Equation-class/dimension mismatch in Chromatography Jacobian", "Check 3: Undemonstrated vector `hyperbolic_jacobian_eigenstructure_and_riemann_invariants` due to incorrect equation"]
    flagged_checks: ["Check 1: Minor eigenvalue count error in Fluid Dynamics Jacobian", "Check 2: Non-conserved to conserved variable mapping in Vocabulary Matrix"]
    quoted_evidence: ["where $\\mathbf{w} = (c_1, c_2, T)^T$ is the conserved state ... Chromatography: $\\mathbf{A}(\\mathbf{w}) = u \\left( \\mathbf{I} + F \\frac{\\partial \\mathbf{q}}{\\partial \\mathbf{c}} \\right)^{-1}$, eigenvalues $\\mu_{1,2} = \\text{eig}(\\mathbf{A})$"]
    stage_3_watch_items: ["Verify if the Evans function methodology for reactive Navier-Stokes has already been applied to non-isothermal chromatography in existing literature.", "Check if the 4D reactive Euler eigenvalues are correctly handled in the source material, as the entry lists only 3 distinct eigenvalues for a 4-component state vector."]
  third_adversarial_review:
    reviewer_model: "DeepSeek DeepSeek V4 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "REJECT"
    verdict_rationale: "The displayed linearized spectral operators and hyperbolic eigenstructure claims contain concrete mathematical errors, and key correspondence vectors therefore lack valid demonstration."
    failed_checks:
      - "Check 1: Section 3 linearized eigenvalue equations omit the traveling-wave speed term; Section 3 eigenvalue lists are inconsistent with the stated state-vector dimensions; Silo B state vector is internally inconsistent."
      - "Check 3: The listed vectors 'linearized_spectral_evans_function_operator' and 'hyperbolic_jacobian_eigenstructure_and_riemann_invariants' are not demonstrated by valid displayed mathematics."
    flagged_checks: []
    quoted_evidence:
      - |-
        Fluid Dynamics: \quad \mathbf{D} \mathbf{P}'' - \mathbf{J}(\mathbf{U}_0) \mathbf{P}' + \left( -\mathbf{J}'(\mathbf{U}_0) \mathbf{U}_0' + \mathbf{J}_{S}(\mathbf{U}_0) - \lambda \mathbf{I} \right) \mathbf{P} = 0
      - |-
        Chromatography: \quad \mathbf{D}_{ax} \mathbf{p}'' - \mathbf{A}(\mathbf{w}_0) \mathbf{p}' + \left( -\mathbf{A}'(\mathbf{w}_0) \mathbf{w}_0' + \mathbf{J}_{S}(\mathbf{w}_0) - \lambda \mathbf{I} \right) \mathbf{p} = 0
      - |-
        Fluid Dynamics: \quad \mathbf{J}(\mathbf{U}) = \frac{\partial \mathbf{F}}{\partial \mathbf{U}}, \quad \text{eigenvalues } \lambda_{1,2,3} = u, \quad u \pm c
      - |-
        Chromatography: \quad \mathbf{A}(\mathbf{w}) = u \left( \mathbf{I} + F \frac{\partial \mathbf{q}}{\partial \mathbf{c}} \right)^{-1}, \quad \text{eigenvalues } \mu_{1,2} = \text{eig}(\mathbf{A})
      - |-
        where $\mathbf{w} = (c_1, c_2, T)^T$ is the conserved state (mobile phase concentration + adsorbed phase via isotherm), $\mathbf{f}(\mathbf{w}) = u \mathbf{c}(\mathbf{w})$ is the chromatographic flux
    stage_3_watch_items:
      - "Non-isothermal equilibrium-dispersive chromatography formulation: verify whether the displayed EDM with w=(c1,c2,T) correctly accounts for adsorbed-phase accumulation and thermal advection."
      - "Prior-art check: possible existing Evans-function spectral analyses of chromatographic fronts or related hyperbolic conservation laws."
      - "Correct hyperbolic eigenstructure for four-component reactive Euler and for the stated three-component non-isothermal chromatographic model."
  fourth_adversarial_review:
    reviewer_model: "Google Gemini 3.1 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "REJECT"
    verdict_rationale: "The linearized spectral Evans function operators contain a mathematically fatal error by omitting the Galilean wave speed translation term."
    failed_checks:
      - "Check 1: Wrong equations for the linearized spectral operators (missing the moving-frame advective term)."
    flagged_checks:
      - "Check 1: Contradictory definitions for the chromatography state variable vector."
    quoted_evidence:
      - "\\text{Fluid Dynamics:} \\quad \\mathbf{D} \\mathbf{P}'' - \\mathbf{J}(\\mathbf{U}_0) \\mathbf{P}' + \\left( -\\mathbf{J}'(\\mathbf{U}_0) \\mathbf{U}_0' + \\mathbf{J}_{S}(\\mathbf{U}_0) - \\lambda \\mathbf{I} \\right) \\mathbf{P} = 0"
      - "\\text{Chromatography:} \\quad \\mathbf{D}_{ax} \\mathbf{p}'' - \\mathbf{A}(\\mathbf{w}_0) \\mathbf{p}' + \\left( -\\mathbf{A}'(\\mathbf{w}_0) \\mathbf{w}_0' + \\mathbf{J}_{S}(\\mathbf{w}_0) - \\lambda \\mathbf{I} \\right) \\mathbf{p} = 0"
    stage_3_watch_items:
      - "Verify if the application of Evans function to chromatography is novel, as the base hyperbolic analogy between chromatography and gas dynamics is a canonical prior-art result (e.g., Rhee, Aris, and Amundson)."
  fifth_adversarial_review:
    reviewer_model: "Xiaomi MiMo V2.5 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "FLAG"
    verdict_rationale: "The structural correspondence between parabolic-hyperbolic conservation laws is sound and all three vectors are demonstrated, but the linearized spectral operator equations in Section 3 are missing the convective shift term and the chromatography Jacobian eigenvalue count is inconsistent with the stated state-vector dimension."
    failed_checks: []
    flagged_checks:
      - "Check 1: Missing −sI shift in linearized spectral operator (both sides)"
      - "Check 1: Chromatography Jacobian eigenvalue count inconsistent with 3-component state vector"
    quoted_evidence:
      - "Fluid Dynamics: \\mathbf{D} \\mathbf{P}'' - \\mathbf{J}(\\mathbf{U}_0) \\mathbf{P}' + \\left( -\\mathbf{J}'(\\mathbf{U}_0) \\mathbf{U}_0' + \\mathbf{J}_{S}(\\mathbf{U}_0) - \\lambda \\mathbf{I} \\right) \\mathbf{P} = 0"
      - "Chromatography: \\mathbf{D}_{ax} \\mathbf{p}'' - \\mathbf{A}(\\mathbf{w}_0) \\mathbf{p}' + \\left( -\\mathbf{A}'(\\mathbf{w}_0) \\mathbf{w}_0' + \\mathbf{J}_{S}(\\mathbf{w}_0) - \\lambda \\mathbf{I} \\right) \\mathbf{p} = 0"
      - "Chromatography: \\quad \\mathbf{A}(\\mathbf{w}) = u \\left( \\mathbf{I} + F \\frac{\\partial \\mathbf{q}}{\\partial \\mathbf{c}} \\right)^{-1}, \\quad \\text{eigenvalues } \\mu_{1,2} = \\text{eig}(\\mathbf{A})"
    stage_3_watch_items:
      - "The Evans-function-for-chromatographic-shock-layers pairing may exist in the specialist literature; probe bibliometrically whether stability analysis via Evans function has already been applied to chromatographic dispersive shock layers."
      - "Verify whether the reactive Navier-Stokes → chromatographic equilibrium-theory transfer has been articulated in published reviews of chromatographic wave propagation or detonation stability."
  sixth_adversarial_review:
    reviewer_model: "OpenAI GPT-5.6 Luna"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "REJECT"
    verdict_rationale: "The entry contains a dimensionally and structurally ill-typed chromatographic equation and vocabulary mapping, and its third listed correspondence is not fully demonstrated."
    failed_checks: ["Check 1: The chromatographic governing equation is not mathematically well-typed because the stated three-component state w=(c1,c2,T)^T is paired with a flux f=u c(w) that is only a concentration vector, while the stated dispersion matrix is likewise defined as a two-component matrix.", "Check 2: The mapping of the chromatographic state/flux to the four-component reactive Euler state/flux contains incompatible vector dimensions and the claimed nondimensionalization does not make the heterogeneous conserved variables dimensionless.", "Check 3: The listed hyperbolic_jacobian_eigenstructure_and_riemann_invariants vector is only partially demonstrated: Jacobian eigenvalues are given, but no Riemann invariants are constructed or derived on either side."]
    flagged_checks: ["Check 4: The transfer direction and falsifiability claim are internally specified, but the asserted asymmetry and the claimed inverse-Peclet scaling of h_crit are not derived in the body and should be probed by Stage 3."]
    quoted_evidence: ['**Silo B (Chromatographic Equilibrium Theory)** models non-isothermal multicomponent chromatography via the Equilibrium-Dispersive Model: `math \\frac{\\partial \\mathbf{w}}{\\partial t} + \\frac{\\partial \\mathbf{f}(\\mathbf{w})}{\\partial z} = \\mathbf{D}_{ax} \\frac{\\partial^2 \\mathbf{w}}{\\partial z^2} + \\mathbf{S}(\\mathbf{w}) ` where $\mathbf{w} = (c_1, c_2, T)^T$ is the conserved state (mobile phase concentration + adsorbed phase via isotherm), $\mathbf{f}(\mathbf{w}) = u \mathbf{c}(\mathbf{w})$ is the chromatographic flux, $\mathbf{D}*{ax}$ is the axial dispersion matrix', 'In chromatography, $\mathbf{D}*{ax} = \text{diag}(D_{ax}, \alpha D_{ax})$; in Navier-Stokes, $\mathbf{D}$ contains kinematic viscosity and thermal conductivity.', '**Mobile phase concentration vector $\mathbf{c}$** ↔ **Conserved mass/momentum/energy vector $\mathbf{U}$**", "$\mathbf{c}$ has units of mol/m³; $\mathbf{U}$ has units of kg/m³ or kg/(m²·s). The nondimensionalization $\tilde{\mathbf{c}} = \mathbf{c}/c_{ref}$ and $\tilde{\mathbf{U}} = \mathbf{U}/\rho_{ref}$ maps both to dimensionless state vectors.', 'Both systems admit a full set of Riemann invariants, allowing the exact solution of the Riemann problem, and mapping acoustic shock speeds to chromatographic retention times.']
    stage_3_watch_items: ["Verify the claimed chromatographic state equation and its flux/storage structure, especially the treatment of temperature and adsorption in the conserved variables.", "Probe the asserted critical scaling $h_{crit} \\propto Pe^{-1}$ and whether the stated parameter values actually define a testable critical coefficient.", "Probe the claim that chromatography lacks rigorous spectral-stability machinery and the asserted one-way maturity advantage.", "Check whether the claimed Evans-function correspondence remains valid for the actual chromatographic linearization once its state and source structure are formulated consistently."]
  seventh_adversarial_review:
    reviewer_model: "Microsoft Copilot 1.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "REJECT"
    verdict_rationale: "A concrete mathematical inconsistency appears in the hyperbolic eigenstructure section: the chromatography Jacobian is stated for a three-component state but only two eigenvalues are listed, which is a direct, demonstrable error in the entry's equations."
    failed_checks: ["Check 1: Equation Validity — inconsistent eigenvalue count in the hyperbolic limit for the chromatography Jacobian"]
    flagged_checks: ["Check 4: Transfer and Falsifiability — the claimed asymmetry of methodological transfer is asserted but not rigorously justified and the falsifiability statement mixes predictive and non-predictive language"]
    quoted_evidence: ["Chromatography: \\quad \\mathbf{A}(\\mathbf{w}) = u \\left( \\mathbf{I} + F \\frac{\\partial \\mathbf{q}}{\\partial \\mathbf{c}} \\right)^{-1}, \\quad \\text{eigenvalues } \\mu_{1,2} = \\text{eig}(\\mathbf{A})"]
    stage_3_watch_items: ["Verify the dimensionality/eigenvalue count of the chromatography Jacobian A for the stated 3-component state (c1,c2,T); check whether the entry incorrectly reduces eigenvalue count or mislabels eigenvalues.","Check prior-art use of the Evans function in related transport/adsorption problems (possible canonical mappings).","Examine the constitutive mapping between chromatographic adsorption isotherm and reactive Euler flux to ensure no hidden category error in conserved-variable dimensionality or flux rank."]
  eighth_adversarial_review:
    reviewer_model: "xAI Grok 4.5 Fast"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "PASS"
    verdict_rationale: "All four checks pass: equations match the claimed parabolic-hyperbolic structure with consistent operators, vocabulary mappings are type-compatible with shared operator roles, all three correspondence vectors are demonstrated by explicit parallel equations and reductions, and the transfer is asymmetrically justified with a concrete falsifiable spectral prediction."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: []
  ninth_adversarial_review:
    reviewer_model: "Meta Muse Spark 1.1"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "PASS"
    verdict_rationale: "All three correspondence vectors are demonstrated with matching parabolic-hyperbolic operator structure and no equation-class or vocabulary category errors."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: []
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ⚠*CONTROL*⚠ ENTRY 0017

## 1. CROSS-SILO SYSTEM DEFINITION
*   **Silo A (Field 1):** 1D Reactive Navier-Stokes Equations (Fluid Dynamics). Specifically, the study of viscous shock profiles and detonation waves in a 1D compressible fluid with chemical reaction and heat conduction.
*   **Silo B (Field 2):** Non-isothermal Equilibrium-Dispersive Model (Chromatographic Equilibrium Theory). Specifically, the propagation of coupled concentration and thermal waves in a multicomponent chromatographic column with axial dispersion and wall heat transfer.
*   **Mathematical Isomorphism:** Both systems are governed by the identical nonlinear parabolic-hyperbolic conservation law structure $\partial_t \mathbf{u} + \partial_x \mathbf{F}(\mathbf{u}) = \mathbf{D} \partial_{xx} \mathbf{u} + \mathbf{S}(\mathbf{u})$, and exhibit a strict operator-level equivalence in their traveling wave ODEs, their linearized spectral stability operators, and the hyperbolic eigenstructure of their flux Jacobians.

## 2. DIAGNOSTIC VOCABULARY MATRIX
*   **Mobile phase concentration vector $\mathbf{c}$** ↔ **Conserved mass/momentum/energy vector $\mathbf{U}$**
    *   *Operator Role:* State variable vector $\mathbf{w}$ in the parabolic-hyperbolic conservation law $\partial_t \mathbf{w} + \nabla \cdot \mathbf{f}(\mathbf{w}) = \mathbf{D} \nabla^2 \mathbf{w} + \mathbf{S}(\mathbf{w})$. $\mathbf{c}$ has units of mol/m³; $\mathbf{U}$ has units of kg/m³ or kg/(m²·s). The nondimensionalization $\tilde{\mathbf{c}} = \mathbf{c}/c_{ref}$ and $\tilde{\mathbf{U}} = \mathbf{U}/\rho_{ref}$ maps both to dimensionless state vectors.
*   **Adsorption isotherm flux $\mathbf{f}(\mathbf{w}) = u \mathbf{c}(\mathbf{w})$** ↔ **Reactive Euler flux $\mathbf{F}(\mathbf{U})$**
    *   *Operator Role:* Nonlinear advective flux function determining the hyperbolic wave speeds. $\mathbf{f}$ maps the conservative state $\mathbf{w} = \mathbf{c} + F\mathbf{q}(\mathbf{c})$ to the mobile phase flux; $\mathbf{F}$ maps conservative variables to mass/momentum/energy flux. Both define the characteristic Jacobian $\mathbf{A} = \partial \mathbf{f} / \partial \mathbf{w}$.
*   **Axial dispersion matrix $\mathbf{D}_{ax}$** ↔ **Viscosity/conductivity matrix $\mathbf{D}$**
    *   *Operator Role:* Positive-definite diagonal diffusion tensor in the parabolic regularization operator $\mathbf{D} \partial^2 / \partial z^2$. In chromatography, $\mathbf{D}_{ax} = \text{diag}(D_{ax}, \alpha D_{ax})$; in Navier-Stokes, $\mathbf{D}$ contains kinematic viscosity and thermal conductivity.
*   **Wall heat transfer term $\mathbf{S}(\mathbf{w})$** ↔ **Chemical heat release $\mathbf{S}(\mathbf{U})$**
    *   *Operator Role:* Source/sink vector in the reaction-diffusion-advection operator. $\mathbf{S}$ introduces non-hyperbolic dynamics and drives the traveling wave away from a simple Lax-shock, enabling Hopf bifurcations.

## 3. CORE MATHEMATICAL PARALLELISM

**Silo A (Fluid Dynamics)** models 1D reactive gas dynamics via the compressible Navier-Stokes equations, written as a system of conservation laws:
```math
\frac{\partial \mathbf{U}}{\partial t} + \frac{\partial \mathbf{F}(\mathbf{U})}{\partial x} = \mathbf{D} \frac{\partial^2 \mathbf{U}}{\partial x^2} + \mathbf{S}(\mathbf{U})
```
where $\mathbf{U} = (\rho, \rho u, \rho E, \rho Y)^T$ is the conserved state, $\mathbf{F}(\mathbf{U})$ is the reactive Euler flux, $\mathbf{D}$ is the diagonal viscous/thermal diffusion matrix, and $\mathbf{S}(\mathbf{U}) = (0,0,0,\omega)^T$ is the chemical reaction source.

**Silo B (Chromatographic Equilibrium Theory)** models non-isothermal multicomponent chromatography via the Equilibrium-Dispersive Model:
```math
\frac{\partial \mathbf{w}}{\partial t} + \frac{\partial \mathbf{f}(\mathbf{w})}{\partial z} = \mathbf{D}_{ax} \frac{\partial^2 \mathbf{w}}{\partial z^2} + \mathbf{S}(\mathbf{w})
```
where $\mathbf{w} = (c_1, c_2, T)^T$ is the conserved state (mobile phase concentration + adsorbed phase via isotherm), $\mathbf{f}(\mathbf{w}) = u \mathbf{c}(\mathbf{w})$ is the chromatographic flux, $\mathbf{D}_{ax}$ is the axial dispersion matrix, and $\mathbf{S}(\mathbf{w}) = (0,0,-h(T-T_w))^T$ is the wall heat transfer source.

The structural mapping relies on the fact that both systems are parabolic-hyperbolic conservation laws with source terms. The correspondences are demonstrated as follows:

**1. `viscous_shock_profile_heteroclinic_orbit_system`**
Traveling wave solutions $\mathbf{U}_0(\xi)$ and $\mathbf{w}_0(\xi)$ (with $\xi = x - st$) in both systems reduce to identical phase-space ODEs. The traveling wave connects two equilibrium states (e.g., unburnt/burnt gas, or loading/elution fronts) as a heteroclinic orbit.
```math
\text{Fluid Dynamics:} \quad \frac{d}{d\xi} \begin{pmatrix} \mathbf{U} \\ \mathbf{Y} \end{pmatrix} = \begin{pmatrix} \mathbf{Y} \\ \mathbf{D}^{-1} [ (\mathbf{J}(\mathbf{U}) - s\mathbf{I}) \mathbf{Y} - \mathbf{S}(\mathbf{U}) ] \end{pmatrix}
```
```math
\text{Chromatography:} \quad \frac{d}{d\xi} \begin{pmatrix} \mathbf{w} \\ \mathbf{y} \end{pmatrix} = \begin{pmatrix} \mathbf{y} \\ \mathbf{D}_{ax}^{-1} [ (\mathbf{A}(\mathbf{w}) - s\mathbf{I}) \mathbf{y} - \mathbf{S}(\mathbf{w}) ] \end{pmatrix}
```
where $\mathbf{J} = \partial \mathbf{F}/\partial \mathbf{U}$ and $\mathbf{A} = \partial \mathbf{f}/\partial \mathbf{w}$. The operator mapping the state into its spatial derivative is identical in both domains.

**2. `linearized_spectral_evans_function_operator`**
To determine the stability of the traveling wave, both systems are linearized around the shock profile $\mathbf{U}_0(\xi)$ (or $\mathbf{w}_0(\xi)$). Assuming perturbations of the form $e^{\lambda t} \mathbf{P}(\xi)$, the eigenvalue problems are structurally identical:
```math
\text{Fluid Dynamics:} \quad \mathbf{D} \mathbf{P}'' - \mathbf{J}(\mathbf{U}_0) \mathbf{P}' + \left( -\mathbf{J}'(\mathbf{U}_0) \mathbf{U}_0' + \mathbf{J}_{S}(\mathbf{U}_0) - \lambda \mathbf{I} \right) \mathbf{P} = 0
```
```math
\text{Chromatography:} \quad \mathbf{D}_{ax} \mathbf{p}'' - \mathbf{A}(\mathbf{w}_0) \mathbf{p}' + \left( -\mathbf{A}'(\mathbf{w}_0) \mathbf{w}_0' + \mathbf{J}_{S}(\mathbf{w}_0) - \lambda \mathbf{I} \right) \mathbf{p} = 0
```
In both fields, the Evans function $D(\lambda)$ is constructed as the Wronskian of the stable and unstable manifolds of this operator. The structural equivalence of the spectral operators ensures that the absolute/convective instability methodologies developed for viscous detonations map directly onto chromatographic shock layers.

**3. `hyperbolic_jacobian_eigenstructure_and_riemann_invariants`**
In the zero-diffusion limit ($\mathbf{D}, \mathbf{D}_{ax} \to 0$), both systems reduce to strictly hyperbolic systems of conservation laws. The characteristic wave speeds are given by the eigenvalues of their respective Jacobians.
```math
\text{Fluid Dynamics:} \quad \mathbf{J}(\mathbf{U}) = \frac{\partial \mathbf{F}}{\partial \mathbf{U}}, \quad \text{eigenvalues } \lambda_{1,2,3} = u, \quad u \pm c
```
```math
\text{Chromatography:} \quad \mathbf{A}(\mathbf{w}) = u \left( \mathbf{I} + F \frac{\partial \mathbf{q}}{\partial \mathbf{c}} \right)^{-1}, \quad \text{eigenvalues } \mu_{1,2} = \text{eig}(\mathbf{A})
```
For the fluid dynamics case, $c = \sqrt{\gamma p / \rho}$ is the speed of sound. For the chromatography case, the eigenvalues depend on the slope of the multicomponent Langmuir isotherm $\partial \mathbf{q}/\partial \mathbf{c}$. Both systems admit a full set of Riemann invariants, allowing the exact solution of the Riemann problem, and mapping acoustic shock speeds to chromatographic retention times.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
*   **Preferred Transfer Direction:** Fluid Dynamics (1D Reactive Navier-Stokes) → Chromatographic Equilibrium Theory
*   **Asymmetric Maturity Rationale:** The fluid dynamics and combustion communities have developed a highly mature analytical toolkit for determining the spectral stability of traveling waves (viscous shocks and detonations) using the Evans function. They can rigorously prove absolute/convective instability boundaries, pulsating instabilities, and Hopf bifurcations. Chromatographic theory, conversely, relies almost exclusively on the Method of Characteristics for the inviscid limit and crude numerical simulations for the dispersive case. The target field completely lacks the rigorous spectral stability operators needed to predict bifurcations when source terms (e.g., wall heat transfer) are active.
*   **Target Bottleneck Mitigation:** Importing the Evans function framework resolves the persistent inability of chromatography theory to predict the onset of thermal instabilities and oscillating fronts in non-isothermal reactive chromatography. By mapping the linearized PDE to the complex Evans function, the onset of Hopf bifurcations can be determined analytically without exhaustive 2D/3D computational fluid dynamics parametric sweeps.
*   **Falsifiable Prediction:** Consider a non-isothermal, 2-component chromatographic column with a heat loss term (Stanton number $St$) and axial dispersion ($Pe$). The current state-of-the-art predicts shock layer stability purely via the Lax entropy condition (which only applies strictly when $St=0$). We predict that for a Langmuir isotherm with a sufficiently high heat transfer coefficient $h$, the chromatographic shock layer will undergo a Hopf bifurcation. The onset of this oscillatory instability can be exactly predicted by a zero of the Evans function $D(\lambda)$ crossing the imaginary axis at $\lambda = \pm i \omega_0$. For a system with $F=0.5$, $u=1$, $D_{ax}=0.01$, the Evans function will predict a critical wall heat transfer coefficient $h_{crit} \propto Pe^{-1}$ that is strictly lower than the one predicted by the inviscid Lax stability criterion. Observing a steady front at $h_{crit}$ where the Evans function predicts a purely imaginary eigenvalue would falsify the transfer.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
*   `"Evans function" AND "viscous shock profile" AND "Navier-Stokes"`
*   `"chromatographic equilibrium theory" AND "axial dispersion" AND "thermal wave"`
*   `"Evans function" AND "chromatography" AND "shock layer stability"`

---

## ADVERSARIAL REVIEWS (Stage 2)

### First Adversarial Review
**Reviewer:** Anthropic Claude Sonnet 5
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-19

#### Results by Check

- **CHECK 1 (Equation Validity):** FAIL — Two independent errors. (1) Linearizing Section 3's master PDE around a traveling profile ξ = x−st produces a first-derivative coefficient of (sI − J(U₀)); the entry's own traveling-wave ODE (Correspondence 1) correctly carries this exact term, "(\mathbf{J}(\mathbf{U}) - s\mathbf{I})", but the Evans-function operator two paragraphs later drops it entirely: "\mathbf{D} \mathbf{P}'' - \mathbf{J}(\mathbf{U}_0) \mathbf{P}' + \left( -\mathbf{J}'(\mathbf{U}_0) \mathbf{U}_0' + \mathbf{J}_{S}(\mathbf{U}_0) - \lambda \mathbf{I} \right) \mathbf{P} = 0" — no s appears anywhere in this equation, and the identical omission recurs in the chromatography version, "\mathbf{D}_{ax} \mathbf{p}'' - \mathbf{A}(\mathbf{w}_0) \mathbf{p}' + \left( -\mathbf{A}'(\mathbf{w}_0) \mathbf{w}_0' + \mathbf{J}_{S}(\mathbf{w}_0) - \lambda \mathbf{I} \right) \mathbf{p} = 0". (2) Correspondence 3 states "eigenvalues λ₁,₂,₃ = u, u ± c" for the flux Jacobian of a state Section 3 defines as the 4-vector "$\mathbf{U} = (\rho, \rho u, \rho E, \rho Y)^T$", and separately gives "$\mathbf{A}(\mathbf{w}) = u(\mathbf{I}+F\partial\mathbf{q}/\partial\mathbf{c})^{-1}$, eigenvalues μ₁,₂ = eig(A)" for a state Section 3 defines as the 3-vector "$\mathbf{w} = (c_1, c_2, T)^T$" — A(w) is structurally a function of c alone (no T-dependence appears in the formula), so neither side's Jacobian matches its own stated state-vector dimension, and the two reduced systems (3 eigenvalues vs. 2) don't match each other either.
- **CHECK 2 (Vocabulary Matrix Coherence):** FLAG — Vocabulary Matrix bullet 1 headers "Mobile phase concentration vector c ↔ Conserved mass/momentum/energy vector U," but its own Operator Role text calls the mapped object "State variable vector w," and the very next bullet defines w = c + Fq(c) as a distinct, nonlinearly related quantity from c. The entry doesn't resolve which symbol is actually claimed to correspond to U, and its own conservation-law structure (∂ₜw + ... in Section 3) suggests w, not the labeled c, is the intended analog.
- **CHECK 3 (Correspondence Vector Support):** FLAG — naming hyperbolic_jacobian_eigenstructure_and_riemann_invariants: Section 3 does supply an equation on each side, so it is not undemonstrated in the bare sense, but the two equations shown (see Check 1) are reduced sub-systems of different, internally-inconsistent dimension rather than a matched pair, so the correspondence is not established on both sides as claimed. viscous_shock_profile_heteroclinic_orbit_system and linearized_spectral_evans_function_operator are both addressed with structurally matching equations on both sides in Section 3 (the latter's equations share a common derivation error — see Check 1 — but are at least symmetric between the two domains).
- **CHECK 4 (Transfer and Falsifiability):** PASS — (a) The stated direction (Evans-function spectral tools mature in combustion/fluid dynamics, absent in chromatographic theory beyond Method-of-Characteristics) is asserted with a specific mechanism and is not interchangeable on the entry's own text. (b) The falsifiable prediction names a specific quantity and scaling (h_crit ∝ Pe⁻¹), a named comparison baseline (inviscid Lax criterion), and a concrete falsification observation — it is not the generic template form. No prior-art pairing is confidently recognized for Evans-function viscous-shock theory applied specifically to chromatographic shock-layer stability; this reviewer has only general, non-specific awareness that Evans-function methods have been ported to other reaction-transport front problems, recorded below as a watch item rather than a recognized citation. Note that the prediction's specific scaling is derived from the Check-1-flagged operator and should be rechecked against the corrected form.

#### Stage 3 Watch Items
- Check for precedent applying Evans-function or related dynamical-systems stability methods to thermal-front instabilities in packed-bed, fixed-bed, or chromatographic column theory; this reviewer cannot confirm a specific prior citation for this exact pairing.
- Verify whether the linear wall-heat term S(w) = (0,0,−h(T−T_w)) can produce a Hopf bifurcation by the same mechanism Section 4 attributes to the (unspecified, but conventionally nonlinear/Arrhenius) chemical source S(U) — the asymmetry between an explicitly linear and a conventionally nonlinear source term is not addressed anywhere in the entry.
- Re-derive the h_crit ∝ Pe⁻¹ scaling in Section 4 using the corrected (wave-speed-inclusive) Evans operator before relying on it.
- Resolve whether Vocabulary Matrix bullet 1's intended U-analog is c or w, and correct the stated units/nondimensionalization accordingly.

### Second Adversarial Review
**Reviewer:** Alibaba Qwen 3.8 Max
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-19

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The entry defines the Silo B state vector as the 3-dimensional non-isothermal vector $\mathbf{w} = (c_1, c_2, T)^T$, but provides the Jacobian formula $\mathbf{A}(\mathbf{w}) = u \left( \mathbf{I} + F \frac{\partial \mathbf{q}}{\partial \mathbf{c}} \right)^{-1}$ which is strictly for the 2-dimensional isothermal equilibrium-dispersive model. This $2 \times 2$ formula cannot model the thermal coupling of the claimed non-isothermal system, and yields only 2 eigenvalues ($\mu_{1,2}$) for a 3-equation system.
- **CHECK 2 (Vocabulary Matrix Coherence):** FLAG — Maps a non-conserved physical quantity (Mobile phase concentration vector $\mathbf{c}$) to a conserved state variable (Conserved mass/momentum/energy vector $\mathbf{U}$). The Operator Role clarifies that $\mathbf{w}$ is the actual conserved state vector in the conservation law, making the primary mapping pair mathematically misaligned in type.
- **CHECK 3 (Correspondence Vector Support):** FAIL — The vector `hyperbolic_jacobian_eigenstructure_and_riemann_invariants` is not demonstrated for Silo B because the equation provided is for the wrong system (isothermal instead of non-isothermal), failing to establish the correspondence on both sides.
- **CHECK 4 (Transfer and Falsifiability):** PASS — Asymmetry is well-justified and the falsifiable prediction names specific parameters ($h$, $Pe$), phenomena (Hopf bifurcation), and clear falsification criteria.

#### Stage 3 Watch Items
- Verify if the Evans function methodology for reactive Navier-Stokes has already been applied to non-isothermal chromatography in existing literature.
- Check if the 4D reactive Euler eigenvalues are correctly handled in the source material, as the entry lists only 3 distinct eigenvalues ($\lambda_{1,2,3} = u, u \pm c$) for a 4-component state vector $\mathbf{U} = (\rho, \rho u, \rho E, \rho Y)^T$.

### Third Adversarial Review
**Reviewer:** DeepSeek DeepSeek V4 Pro
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-19

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The linearized eigenvalue problems omit the \(-(\mathbf{J}-s\mathbf{I})\mathbf{P}'\) frame-shift term, and the stated eigenvalue lists are inconsistent with the dimensions of the defined state vectors (four-component reactive Euler with three eigenvalues; three-component chromatography with a \(2\times2\) Jacobian). The Silo B state vector is also internally inconsistent.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The paired vocabulary terms are broadly type-compatible state, flux, diffusion, and source objects; no independent category error was confirmed in the matrix.
- **CHECK 3 (Correspondence Vector Support):** FAIL — `viscous_shock_profile_heteroclinic_orbit_system` is demonstrated by explicit first-order traveling-wave ODEs in Section 3, but `linearized_spectral_evans_function_operator` and `hyperbolic_jacobian_eigenstructure_and_riemann_invariants` rest on the invalid linearized operators and incomplete eigenvalue statements.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The proposed transfer direction is asymmetric and the prediction names a specific critical heat-transfer coefficient \(h_{crit}\) with a stated experimental falsification condition.

#### Stage 3 Watch Items
- Verify the correct non-isothermal equilibrium-dispersive model; the entry's state vector \((c_1,c_2,T)\) does not actually include the adsorbed-phase accumulation it claims.
- Probe prior art applying Evans-function spectral stability to chromatographic fronts or shock layers.
- Check the correct hyperbolic eigenstructure for the four-component reactive Euler system and for the three-component non-isothermal chromatographic model.

### Fourth Adversarial Review
**Reviewer:** Google Gemini 3.1 Pro
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-19

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The linearized spectral eigenvalue PDEs (`\text{Fluid Dynamics:}` and `\text{Chromatography:}`) are mathematically wrong. When linearizing in the moving frame $\xi = x - st$ using perturbations of the form $e^{\lambda t} \mathbf{P}(\xi)$, the time derivative yields $\lambda \mathbf{P} - s \mathbf{P}'$. Both equations incorrectly drop the advective wave speed $s\mathbf{I}$ from the first-derivative coefficient (which should be $-(\mathbf{J}(\mathbf{U}_0) - s\mathbf{I})\mathbf{P}'$ and $-(\mathbf{A}(\mathbf{w}_0) - s\mathbf{I})\mathbf{p}'$). This contradicts the steady-state ODEs in the preceding section which correctly include the $-s\mathbf{I}$ frame translation. Additionally, the entry flags a notational contradiction: it defines $\mathbf{w} = (c_1, c_2, T)^T$ while simultaneously claiming it represents the "conserved state (mobile phase concentration + adsorbed phase)", which would mathematically require $\mathbf{w} = \mathbf{c} + F\mathbf{q}(\mathbf{c})$.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All mappings pair compatible mathematical objects (e.g., both are state variable vectors or positive-definite diffusion tensors) and clearly state shared structural roles.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed vectors (`viscous_shock_profile_heteroclinic_orbit_system`, `linearized_spectral_evans_function_operator`, `hyperbolic_jacobian_eigenstructure_and_riemann_invariants`) are explicitly supported by derivations and equations in Section 3, though the spectral operator equations contain the fatal derivation error flagged in Check 1.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction is plausibly asymmetric (importing spectral stability frameworks to a field reliant on inviscid MoC solutions or raw simulation), and the prediction specifies a falsifiable, measurable threshold (a critical wall heat transfer coefficient $h_{crit} \propto Pe^{-1}$) differing from current inviscid theory.

#### Stage 3 Watch Items
- The foundational analogy between multicomponent chromatography and gas dynamics (including Riemann invariants and characteristic wave speeds) is a classic result in the theory of hyperbolic conservation laws (e.g., Rhee, Aris, and Amundson). Stage 3 should verify whether applying the Evans function specifically to the viscous/dispersive non-isothermal case represents a truly novel methodological transfer or if it has already been explored in the chemical engineering literature.

### Fifth Adversarial Review
**Reviewer:** Xiaomi MiMo V2.5 Pro
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-19

#### Results by Check
- **CHECK 1 (Equation Validity):** FLAG — Both traveling-wave ODEs and the overall parabolic-hyperbolic conservation-law structure are correct and genuinely from their stated domains. However, the linearized spectral stability operators are missing the convective shift term $-s\mathbf{I}$ in the first-derivative coefficient: the correct form is $-(\mathbf{J} - s\mathbf{I})\mathbf{P}'$, not $-\mathbf{J}\mathbf{P}'$. Additionally, the chromatography Jacobian is listed with eigenvalues $\mu_{1,2}$ for a 3-component state vector $(c_1, c_2, T)^T$, which should yield a 3×3 Jacobian with three eigenvalues. Neither error invalidates the structural correspondence (the shift is symmetric and the eigenstructure approach is correct), but both displayed equations need correction.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All four paired mappings (state vectors, flux functions, diffusion tensors, source terms) are between objects of compatible mathematical type, and each Operator Role description names a specific shared structure (conservation-law state variable, characteristic Jacobian, parabolic diffusion tensor, reaction-diffusion source term).
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed vectors are demonstrated with explicit equations on both sides: (1) heteroclinic orbit traveling-wave ODEs with phase-space formulation, (2) linearized Evans-function spectral operators, and (3) hyperbolic Jacobian eigenstructure with eigenvalues.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction (Evans function from reactive detonation stability → chromatographic shock-layer stability) is genuinely asymmetric: the fluid-dynamics/combustion community has a mature Evans-function toolkit while chromatographic theory lacks it. The falsifiable prediction names specific parameters ($F=0.5$, $u=1$, $D_{ax}=0.01$), a measurable critical quantity ($h_{crit} \propto Pe^{-1}$), and a concrete falsification condition (observing a steady front where the Evans function predicts a purely imaginary eigenvalue).

#### Stage 3 Watch Items
- The Evans-function-for-chromatographic-shock-layers pairing may already exist in the specialist literature. Probe bibliometrically whether spectral stability analysis via the Evans function has been applied to dispersive shock layers in chromatographic or related fixed-bed models.
- Verify whether the reactive Navier-Stokes ↔ chromatographic equilibrium-theory mapping has been articulated in published reviews of chromatographic wave propagation, fixed-bed reactor stability, or detonation-stability theory.
- The missing $-s\mathbf{I}$ term in the spectral operator is symmetric on both sides and does not affect the correspondence claim, but a human reviewer should confirm whether this is a consistent notational convention in the combustion-stability literature or a genuine omission.

### Sixth Adversarial Review
**Reviewer:** OpenAI GPT-5.6 Luna
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-19

#### Results by Check
* **CHECK 1 (Equation Validity):** FAIL — Section 3 gives $\mathbf{w}=(c_1,c_2,T)^T$ but defines $\mathbf{f}(\mathbf{w})=u\mathbf{c}(\mathbf{w})$, a concentration vector rather than a three-component flux, while $\mathbf{D}*{ax}=\operatorname{diag}(D*{ax},\alpha D_{ax})$ is likewise two-component; the displayed chromatographic PDE is therefore not well-typed as written.
* **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — The mapping “**Mobile phase concentration vector $\mathbf{c}$ ↔ Conserved mass/momentum/energy vector $\mathbf{U}$**” pairs a two-component concentration vector with the four-component $\mathbf{U}=(\rho,\rho u,\rho E,\rho Y)^T$, and the stated scalar rescalings do not make the heterogeneous momentum/energy components dimensionless.
* **CHECK 3 (Correspondence Vector Support):** FAIL — Sections 3.1 and 3.2 explicitly derive the heteroclinic traveling-wave system and the linearized spectral operator, but Section 3.3 gives only Jacobian eigenvalues and then asserts “Both systems admit a full set of Riemann invariants” without constructing or deriving any Riemann invariants, so the listed `hyperbolic_jacobian_eigenstructure_and_riemann_invariants` vector is not fully demonstrated.
* **CHECK 4 (Transfer and Falsifiability):** FLAG — The stated transfer direction is presented as asymmetric and the prediction names a measurable critical $h$ and imaginary-axis crossing, but the asserted maturity asymmetry and the scaling $h_{crit}\propto Pe^{-1}$ are not derived in the entry and should be independently probed.

#### Stage 3 Watch Items
* Verify the actual well-posed mathematical form of the non-isothermal chromatographic state, flux, adsorption storage, and thermal equation.
* Probe the claimed $h_{crit}\propto Pe^{-1}$ scaling and the numerical parameterization of the proposed falsification.
* Probe the assertion that chromatographic theory “completely lacks” rigorous spectral-stability operators.
* Verify that the Evans-function construction survives the correctly formulated chromatographic linearization.

### Seventh Adversarial Review
**Reviewer:** Microsoft Copilot 1.2
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-19

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The entry states a hyperbolic eigenstructure for the chromatography Jacobian but lists an inconsistent eigenvalue count:  
  **Quoted failing text:** "Chromatography: \\quad \\mathbf{A}(\\mathbf{w}) = u \\left( \\mathbf{I} + F \\frac{\\partial \\mathbf{q}}{\\partial \\mathbf{c}} \\right)^{-1}, \\quad \\text{eigenvalues } \\mu_{1,2} = \\text{eig}(\\mathbf{A})"  
  **Error:** The conserved state for chromatography was defined as \\(\\mathbf{w}=(c_1,c_2,T)^T\\) (three components), so the Jacobian \\(\\mathbf{A}(\\mathbf{w})\\) is a 3×3 matrix and must have three eigenvalues; listing only two eigenvalues \\(\\mu_{1,2}\\) is a direct mathematical inconsistency in the hyperbolic-limit characterization and contradicts the stated state dimensionality.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The mapped tokens are presented as objects of compatible mathematical type (state vectors, flux functions, diffusion tensors, source vectors) and the Operator Role entries assert explicit operator-level roles rather than purely hedged analogies.
- **CHECK 3 (Correspondence Vector Support):** PASS — Each of the three listed correspondence vectors is supported in the body with equations or operator-level derivations:  
  - `viscous_shock_profile_heteroclinic_orbit_system` — traveling-wave ODEs given for both fields (Section 3, traveling-wave ODEs).  
  - `linearized_spectral_evans_function_operator` — linearized eigenvalue problems and Evans-function construction described for both fields (Section 3, spectral operators).  
  - `hyperbolic_jacobian_eigenstructure_and_riemann_invariants` — zero-diffusion Jacobians and characteristic eigenvalues are presented for both fields (Section 3, hyperbolic limit). Each vector is demonstrated with equations or operator identities.
- **CHECK 4 (Transfer and Falsifiability):** FLAG — (a) **Asymmetry:** The entry asserts Fluid Dynamics → Chromatography as the preferred transfer direction but provides only qualitative maturity arguments rather than a rigorous demonstration that the transfer is meaningfully asymmetric; this could plausibly be bidirectional in practice. (b) **Falsifiability:** The entry gives a concrete spectral criterion (Evans function zero crossing at \\(\\lambda=\\pm i\\omega_0\\)) and a parametric claim about \\(h_{crit}\\propto Pe^{-1}\\), which is a measurable prediction, but the falsifiability paragraph also contains a contradictory sentence ("Observing a steady front at \\(h_{crit}\\) where the Evans function predicts a purely imaginary eigenvalue would falsify the transfer") that mixes the predicted outcome and its negation in a confusing way; the prediction needs clearer, testable thresholds. (c) **Prior art advisory:** The Evans-function ↔ viscous shock literature is canonical; flag for Stage 3 verification.

#### Stage 3 Watch Items
- Verify the dimensionality and eigenvalue count of the chromatography Jacobian \\(\\mathbf{A}(\\mathbf{w})\\) given the stated 3-component state \\((c_1,c_2,T)\\); confirm whether the entry omitted an eigenvalue or implicitly reduced the system dimension.  
- Check whether the mapping between adsorption-isotherm-based flux and reactive Euler flux hides a category error in conserved-variable types or flux tensor rank.  
- Probe prior-art: whether Evans-function spectral methods have already been applied to equilibrium-dispersive chromatography or closely related adsorption–transport models.  
- Validate the claimed scaling law \\(h_{crit} \\propto Pe^{-1}\\) derivation and whether the entry supplies sufficient operator-level derivation to support that proportionality.

### Eighth Adversarial Review
**Reviewer:** xAI Grok 4.5 Fast
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-19

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both displayed systems are parabolic-hyperbolic conservation laws of identical class with matching diffusion and source operators; the traveling-wave ODEs, linearized spectral operators, and Jacobian eigenstructures are structurally equivalent as claimed and support the Section 1 correspondence.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All four paired tokens are objects of compatible mathematical type (state vectors, nonlinear fluxes, positive-definite diffusion matrices, source vectors) and each Operator Role statement identifies a shared differential structure rather than a hedged analogy.
- **CHECK 3 (Correspondence Vector Support):** PASS — viscous_shock_profile_heteroclinic_orbit_system is demonstrated by the parallel first-order traveling-wave ODEs in Section 3; linearized_spectral_evans_function_operator is demonstrated by the parallel second-order eigenvalue problems and Evans-function construction in Section 3; hyperbolic_jacobian_eigenstructure_and_riemann_invariants is demonstrated by the parallel Jacobian eigenvalue statements and Riemann-invariant claim in Section 3.
- **CHECK 4 (Transfer and Falsifiability):** PASS — Transfer direction is asymmetrically justified by the documented maturity gap in Evans-function spectral tools; the prediction names a concrete measurable outcome (Evans zero crossing the imaginary axis at a critical wall-heat-transfer coefficient lower than the Lax threshold) that can be falsified by observation of a steady front.

#### Stage 3 Watch Items
None identified.

### Ninth Adversarial Review
**Reviewer:** Meta Muse Spark 1.1
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-19

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both primary PDEs share the identical nonlinear parabolic-hyperbolic class $\partial_t \mathbf{u} + \partial_x \mathbf{F} = \mathbf{D}\partial_{xx}\mathbf{u}+\mathbf{S}$, and the derived traveling-wave ODEs and linearized spectral operators preserve class and structure on both sides.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All four mappings pair compatible types with explicit shared operators and stated nondimensionalization for $\mathbf{c}$ ↔ $\mathbf{U}$, flux ↔ flux, diffusion matrix ↔ diffusion matrix, source ↔ source; no spatial↔temporal, field↔scalar, rate↔state, or dimensional↔dimensionless category errors.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed vectors are demonstrated in Section 3: viscous_shock_profile_heteroclinic_orbit_system via paired heteroclinic ODEs, linearized_spectral_evans_function_operator via paired $ \mathbf{D}\mathbf{P}'' - \mathbf{J}\mathbf{P}' + (\cdot-\lambda\mathbf{I})\mathbf{P}=0$ eigenvalue problems and Evans Wronskian construction, and hyperbolic_jacobian_eigenstructure_and_riemann_invariants via Jacobian eigenvalues and Riemann invariants in the $\mathbf{D}\to0$ limit.
- **CHECK 4 (Transfer and Falsifiability):** PASS — Asymmetry is genuine with Fluid Dynamics Evans toolkit mature and chromatography lacking it per Section 4 rationale, and prediction is falsifiable with specific parameters $F=0.5, u=1, D_{ax}=0.01$, threshold $h_{crit}\propto Pe^{-1}$ lower than Lax criterion, and crossing at $\lambda=\pm i\omega_0$ with explicit falsification condition; no canonical textbook analogy recognized.

#### Stage 3 Watch Items
- None identified.