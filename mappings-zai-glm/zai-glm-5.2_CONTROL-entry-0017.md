---
sid_metadata:
  entry_id: "CONTROL-SID-0017"
  schema_version: "2.0-control"
  maturity_stage: "candidate"
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