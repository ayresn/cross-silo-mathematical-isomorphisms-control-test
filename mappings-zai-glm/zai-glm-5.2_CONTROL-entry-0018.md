---
sid_metadata:
  entry_id: "CONTROL-SID-0018"
  schema_version: "2.0-control"
  maturity_stage: "candidate"
provenance:
  company: "Z.AI"
  model_family: "GLM"
  model_version: "5.2"
  generation_timestamp: "2026-08-17"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "hele-shaw-viscous-fingering-dynamics"
  domain_b: "electrodeposition-dendrite-growth"
  structural_family: "laplacian-free-boundary-with-robin-kinetic-regularization"
  triple_correspondence_vectors:
    - "laplacian_governing_equation_with_gradient_driven_kinematic_boundary_condition"
    - "robin_dynamic_boundary_condition_kinetic_undercooling_butler_volmer"
    - "kinetic_regularized_dispersion_relation_shared_form"
    - "dimensionless_kinetic_parameter_delta_controlling_regime_transition"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language / historically_isolated_communities / representation_mismatch_fluid_mechanics_vs_electrochemistry"
prior_discovery_metrics:
  structural_isomorphism_score: 8.5
  vocabulary_divergence_score: 7.5
  expected_methodological_transfer_score: 8.0
  community_separation_score: 7.0
  representation_mismatch_score: 8.0
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 7.0
    uncertainty: "±1.5"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "high"
  primary_failure_risk: "ohmic_limit_breakdown_at_high_overpotential"
  bibliometric_validation: "pending"
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ⚠*CONTROL*⚠ ENTRY 0018

## 1. CROSS-SILO SYSTEM DEFINITION
*   **Silo A (Field 1):** Hele-Shaw viscous fingering with kinetic undercooling regularization — the quasi-2D displacement of a viscous fluid by a less viscous fluid between parallel plates, where the standard Young-Laplace boundary condition is augmented by a velocity-dependent (kinetic) term.
*   **Silo B (Field 2):** Electrodeposition dendrite growth in the ohmic regime with Butler-Volmer charge-transfer kinetics — metal ion reduction at an electrode surface where the boundary condition combines Gibbs-Thomson capillary overpotential with activation (charge-transfer) overpotential.
*   **Mathematical Isomorphism:** Both systems reduce to a Laplacian free-boundary problem whose dynamic boundary condition is a Robin-type relation $u - \alpha\,\partial u/\partial n = f(\kappa)$, where the Robin coefficient $\alpha$ arises from kinetic undercooling (Silo A) or linearized Butler-Volmer activation resistance (Silo B), producing identical dispersion relations $\sigma = Vk(1 - k^2/k_c^2)/(1+\alpha k)$ governed by the same dimensionless kinetic parameter $\delta = \alpha k_c$.

## 2. DIAGNOSTIC VOCABULARY MATRIX
*   Pressure field $p$ [Pa] ↔ Electrolyte potential $\phi$ [V]
    *   *Operator Role:* Both are real scalar fields satisfying $\nabla^2 u = 0$ in the respective domain ($x>0$). The transformation $p \leftrightarrow \phi$ is direct (same mathematical type, real scalar) up to a dimensional rescaling $p = (\gamma/\gamma')\phi$ where $\gamma, \gamma'$ are the respective surface tension coefficients. The governing operator is identical: the Laplacian.
*   Darcy mobility $K_D = b^2/(12\mu)$ [m²/(Pa·s)] ↔ Electrochemical mobility $K_E = M\sigma_e/(nF\rho)$ [m²/(V·s)]
    *   *Operator Role:* Both relate the field gradient to the interface normal velocity via $v_n = K\,\partial u/\partial n$. In Silo A, Darcy's law gives $v_n = -(b^2/12\mu)\,\partial p/\partial n$ (with sign convention where $n$ points into the viscous fluid). In Silo B, Faraday's law plus Ohm's law gives $v_n = (M\sigma_e/(nF\rho))\,\partial\phi/\partial n$ (with $n$ pointing into the electrolyte). The sign difference is absorbed by the identification $p \leftrightarrow -\phi$; under this, both take the form $v_n = -K\,\partial u/\partial n$ with $K>0$.
*   Kinetic undercooling coefficient $\beta_k$ [Pa·s/m] ↔ Butler-Volmer exchange resistance $R_{BV} = RT/(\alpha_{tr} z F j_0)$ [V·m²/A]
    *   *Operator Role:* Both enter the Robin boundary condition as the coefficient of the normal derivative. The kinetic length $\alpha = \beta_k K_D$ (Silo A) and $\alpha' = R_{BV}\sigma_e$ (Silo B) both have units of [m] and appear identically in the Robin BC: $u - \alpha\,\partial u/\partial n = f(\kappa)$.
*   Surface tension $\gamma$ [N/m] ↔ Capillary overpotential coefficient $c' = \gamma_s\Omega/(ze)$ [V·m]
    *   *Operator Role:* Both multiply the curvature $\kappa$ on the right-hand side of the Robin BC. The mapping $\gamma \leftrightarrow c'$ converts surface energy [N/m] into an equivalent electrostatic potential per unit curvature, with the atomic volume $\Omega$ [m³] and elementary charge $e$ [C] providing the dimensional bridge.
*   Capillary length $d_0 = 1/k_c = \sqrt{\gamma/(P_2)}$ [m] ↔ Electrochemical capillary length $d_0' = 1/k_c' = \sqrt{c'/\Phi_0}$ [m]
    *   *Operator Role:* Both define the critical wavenumber $k_c$ at which the surface tension stabilizes short wavelengths. In Silo A, $k_c^2 = 12\mu V/(\gamma b^2)$. In Silo B, $k_c'^2 = \Phi_0 z e/(\gamma_s\Omega)$. Both enter the dispersion relation identically as the ratio $k^2/k_c^2$.

## 3. CORE MATHEMATICAL PARALLELISM

**Silo A — Hele-Shaw with Kinetic Undercooling.** In a Hele-Shaw cell of gap $b$, a viscous fluid (viscosity $\mu$) occupies $x > 0$ and is displaced by air (negligible viscosity) at $x < 0$. The gap-averaged velocity obeys Darcy's law $\mathbf{u} = -(b^2/12\mu)\nabla p$, and incompressibility yields the Laplace equation for pressure. The interface at $x = \eta(y,t)$ obeys a kinematic condition and a dynamic boundary condition combining surface tension with a kinetic undercooling term proportional to the interface velocity:

```math
\nabla^2 p = 0 \quad (x > 0)
```

```math
v_n = -\frac{b^2}{12\mu}\,\frac{\partial p}{\partial n}, \qquad p - \alpha\,\frac{\partial p}{\partial n} = \gamma\,\kappa
```

where $\alpha = \beta_k b^2/(12\mu)$ is the kinetic length, $\gamma$ is surface tension, and $\kappa = \eta_{yy}$ is the interface curvature. Linearizing about a flat interface moving at velocity $V = b^2 P_2/(12\mu)$ with perturbation $\eta = \epsilon\,e^{\sigma t + iky}$ yields the dispersion relation:

```math
\sigma = \frac{Vk\!\left(1 - k^2/k_c^2\right)}{1 + \alpha k}, \qquad k_c^2 = \frac{12\mu V}{\gamma b^2}
```

**Silo B — Electrodeposition with Butler-Volmer Kinetics.** In the ohmic regime (high-concentration electrolyte, neglecting concentration gradients), the electrolyte potential satisfies Laplace's equation. The electrode grows into the electrolyte ($x > 0$) with growth velocity given by Faraday's law. The boundary condition at the electrode-electrolyte interface combines the Gibbs-Thomson capillary overpotential with the linearized Butler-Volmer activation overpotential:

```math
\nabla^2 \phi = 0 \quad (x > 0)
```

```math
v_n = \frac{M\sigma_e}{nF\rho}\,\frac{\partial \phi}{\partial n}, \qquad \phi - \alpha'\,\frac{\partial \phi}{\partial n} = \phi_{\mathrm{eq}} - c'\,\kappa
```

where $\alpha' = RT\sigma_e/(\alpha_{tr} z F j_0)$ is the kinetic length (from the exchange current density $j_0$ and transfer coefficient $\alpha_{tr}$), $c' = \gamma_s\Omega/(ze)$ is the capillary coefficient, $M$ is molar mass, $\sigma_e$ is electrolyte conductivity, and $\kappa = \eta_{yy}$ is curvature. Linearizing about a flat interface growing at velocity $V_0 = M\sigma_e\Phi_0/(nF\rho)$ with $\eta = \epsilon\,e^{\sigma t + iky}$ yields:

```math
\sigma = \frac{V_0 k\!\left(1 - k^2/k_c'^2\right)}{1 + \alpha' k}, \qquad k_c'^2 = \frac{\Phi_0\, z e}{\gamma_s \Omega}
```

**Structural Bridge.** The isomorphism is established by the identification $p \leftrightarrow \phi$, $\gamma \leftrightarrow c'$, $\alpha \leftrightarrow \alpha'$, $K_D \leftrightarrow K_E$, and $V \leftrightarrow V_0$. Under this mapping:

1. **Governing operator:** $\nabla^2 p = 0 \leftrightarrow \nabla^2 \phi = 0$ — identical elliptic operators.
2. **Kinematic condition:** $v_n = -K_D\,\partial p/\partial n \leftrightarrow v_n = -K_E\,\partial \phi/\partial n$ — identical gradient-to-velocity maps with different material constants.
3. **Robin boundary condition:** $p - \alpha\,\partial p/\partial n = \gamma\kappa \leftrightarrow \phi - \alpha'\,\partial\phi/\partial n = -c'\kappa$ — both are Robin-type conditions $u - \alpha\,\partial u/\partial n = f(\kappa)$ with the same sign on the Robin coefficient and the curvature entering with the same sign (the sign difference in $f(\kappa)$ is absorbed by the consistent curvature convention $\kappa = \eta_{yy}$ on both sides).
4. **Dispersion relation:** Both reduce to $\sigma = Vk(1 - k^2/k_c^2)/(1 + \alpha k)$ — the kinetic term $(1+\alpha k)^{-1}$ modifies the classical Saffman-Taylor / Mullins-Sekerka dispersion identically.

The **dimensionless kinetic parameter** controlling the regime transition is $\delta = \alpha k_c$ in both systems. For $\delta = 0$ (no kinetic regularization), the most unstable wavenumber is $k^* = k_c/\sqrt{3}$ (the classical result). For $\delta > 0$, $k^*$ is determined by:

```math
1 - 3q^2 - 2\delta\, q^3 = 0, \qquad q = k^*/k_c
```

For $\delta \gg 1$ (kinetic-dominated regime), $q^* \approx (2\delta)^{-1/3}$, and the most unstable wavelength scales as $\lambda^* \sim \alpha^{1/3}\,d_0^{2/3}$ rather than $\lambda \sim d_0$.

The correspondence holds under the restriction that the electrodeposition is in the **ohmic limit** (negligible concentration overpotential), which requires high supporting electrolyte concentration or current densities below the diffusion-limited threshold. The Hele-Shaw kinetic undercooling is an ad hoc mathematical regularization, while the electrodeposition Robin coefficient is physically derived from the Butler-Volmer equation — a representation mismatch that strengthens the isomorphism, since the same operator structure emerges from fundamentally different constitutive origins.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
*   **Preferred Transfer Direction:** Hele-Shaw viscous fingering → Electrodeposition dendrite growth
*   **Asymmetric Maturity Rationale:** The Hele-Shaw community has developed, over three decades, a mature analytical and computational toolkit for the Robin-regularized Laplacian free-boundary problem specifically: (i) boundary integral methods with Robin kernels for nonlinear interface evolution (Kropinski, Hou, et al.), (ii) solvability theory for dendritic tip selection including kinetic effects (Ben Amar, Combescot, et al.), and (iii) weakly nonlinear amplitude equations derived via multiple-scale analysis on the Robin BC. The electrodeposition community possesses sophisticated experimental characterization (in situ microscopy, impedance spectroscopy) and standard Mullins-Sekerka linear stability analysis, but lacks nonlinear pattern-selection theory incorporating the Butler-Volker Robin coefficient. The specific capability gap is nonlinear dendrite spacing prediction in the kinetically dominated regime ($\delta \gg 1$), where the standard Mullins-Sekerka framework (which assumes $\delta = 0$) fails.
*   **Target Bottleneck Mitigation:** Importing the Hele-Shaw solvability theory for $\delta \gg 1$ predicts that the dendrite spacing transitions from the classical $d_0$-scaling ($\lambda \propto V^{-1/2}$) to a kinetic-dominated scaling $\lambda^* \propto \alpha^{1/3} d_0^{2/3}$ (weakly dependent on $V$). This resolves the persistent failure of Mullins-Sekerka theory to predict dendrite spacings in systems with low exchange current density (e.g., lithium), where observed spacings are orders of magnitude larger than $d_0$-based predictions.
*   **Falsifiable Prediction:** For lithium electrodeposition from 1M LiPF$_6$ in EC:DMC at $T = 300\,\mathrm{K}$, $J = 100\,\mathrm{A/m^2}$, with $j_0 \approx 1\,\mathrm{A/m^2}$, $\sigma_e \approx 1\,\mathrm{S/m}$, $\gamma_s \approx 0.5\,\mathrm{J/m^2}$, $\Omega \approx 2\times10^{-29}\,\mathrm{m^3}$, $z=1$, $\alpha_{tr} = 0.5$: the predicted kinetic length is $\alpha' = RT\sigma_e/(\alpha_{tr} z F j_0) \approx 5.2\,\mathrm{cm}$, the capillary length is $d_0 = \sqrt{\gamma_s\Omega/(ze\Phi_0)} \approx 0.8\,\mu\mathrm{m}$ (with $\Phi_0 = J/\sigma_e = 100\,\mathrm{V/m}$), giving $\delta' = \alpha' k_c' \approx 6.5\times 10^4$. The most unstable wavelength is predicted to be $\lambda^* \approx 2\pi(2\alpha')^{1/3} d_0^{2/3} \approx 220\,\mu\mathrm{m}$, versus the standard Mullins-Sekerka baseline $\lambda_{\mathrm{MS}} = 2\pi\sqrt{3}\,d_0 \approx 8.7\,\mu\mathrm{m}$. **The prediction:** the initial instability wavelength measured by in situ optical microscopy during galvanostatic Li deposition at $100\,\mathrm{A/m^2}$ on a planar Cu substrate will exceed $100\,\mu\mathrm{m}$, deviating from $\lambda_{\mathrm{MS}}$ by more than one order of magnitude. **Falsification:** if the measured initial wavelength is within a factor of 3 of $\lambda_{\mathrm{MS}}$ (i.e., $< 26\,\mu\mathrm{m}$), the kinetic-regularized isomorphism is falsified for this system.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
*   `"kinetic undercooling" AND "Hele-Shaw" AND "Robin boundary" AND "dispersion relation"`
*   `"Butler-Volmer" AND "Robin boundary condition" AND "electrodeposition" AND "morphological stability"`
*   `"viscous fingering" AND "electrodeposition" AND "kinetic" AND "dendrite spacing"`
*   `"Laplacian growth" AND "Robin" AND "kinetic undercooling" AND "Butler-Volmer"`
*   `"solvability theory" AND "kinetic undercooling" AND "dendrite" AND "selection"`