---
sid_metadata:
  entry_id: "CONTROL-SID-0011"
  schema_version: "2.0-control"
  maturity_stage: "candidate"
provenance:
  company: "Google"
  model_family: "Gemini"
  model_version: "3.1 Pro"
  generation_timestamp: "2026-08-17"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "viscous-thin-film-lubrication"
  domain_b: "petroleum-reservoir-fractional-flow"
  structural_family: "degenerate-fourth-order-parabolic-flows"
  triple_correspondence_vectors:
    - "degenerate_fourth_order_parabolic_operator"
    - "lyapunov_free_energy_functional"
    - "nonlinear_convective_flux_tensor"
discovery_rationale:
  why_not_obvious: "incompatible_ontologies"
prior_discovery_metrics:
  structural_isomorphism_score: 9.2
  vocabulary_divergence_score: 8.8
  expected_methodological_transfer_score: 9.5
  community_separation_score: 9.0
  representation_mismatch_score: 8.5
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 8.9
    uncertainty: "±0.5"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "very_high"
  constitutive_equivalence_confidence: "high"
  primary_failure_risk: "differing_mobility_degeneracy_exponents"
  bibliometric_validation: "pending"
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ⚠*CONTROL*⚠ ENTRY 0011

## 1. CROSS-SILO SYSTEM DEFINITION
*   **Silo A (Field 1):** Viscous Thin-Film Lubrication (VTFL), focusing on the spreading, dewetting, and contact-line dynamics of microscopically thin fluid layers driven by capillarity, gravity, and intermolecular forces.
*   **Silo B (Field 2):** Petroleum Reservoir Fractional Flow (PRFF), specifically the macroscopic phase-field (Cahn-Hilliard-Darcy) modeling of unstable multiphase fluid displacement and spontaneous imbibition in porous media.
*   **Mathematical Isomorphism:** Both systems are strictly governed by a degenerate fourth-order parabolic partial differential equation encompassing a nonlinear convective flux and an energy-dissipating gradient flow, where the geometric interface height of the free-surface film corresponds exactly to the volumetric phase saturation within the rigid porous matrix.

## 2. DIAGNOSTIC VOCABULARY MATRIX
*   Film thickness $h(\mathbf{x}, t)$ ↔ Water Saturation $S(\mathbf{x}, t)$
    *   *Operator Role:* Primary continuous scalar state variable governing the nonlinear PDE. The physical dimension of $h$ (length) is reconciled with the dimensionless saturation $S$ via the affine mapping $S = h / H_{max}$, where $H_{max}$ is the reference equilibrium film thickness.
*   Surface Tension $\gamma$ ↔ Capillary Gradient Energy Parameter $\kappa$
    *   *Operator Role:* Strictly positive pre-factor of the highest-order regularizing spatial derivative ($\nabla^2$) within the thermodynamic potential, dictating the energy penalty for sharp spatial gradients.
*   Disjoining Pressure $\Pi(h)$ ↔ Bulk Spinodal Force $-\Psi'(S)$
    *   *Operator Role:* Algebraic thermodynamic driving force. In VTFL, van der Waals interactions trigger dewetting; in PRFF, the non-convex double-well potential derivative drives phase separation. Both generate negative diffusion in their respective spinodal regimes.
*   Viscous Mobility $M(h) = \frac{h^3}{3\mu}$ ↔ Mutual Mobility $M(S) = \lambda_T(S) f(S)(1-f(S))$
    *   *Operator Role:* State-dependent degenerate pre-factor multiplying the chemical potential gradient in the parabolic transport tensor, ensuring the flux vanishes smoothly as the physical state variable approaches absolute zero.

## 3. CORE MATHEMATICAL PARALLELISM
In Viscous Thin-Film Lubrication (VTFL), the spatio-temporal evolution of a fluid film driven by gravity, capillarity, and intermolecular forces is modeled via the lubrication approximation, yielding the Thin-Film Equation:
```math
\frac{\partial h}{\partial t} + \nabla \cdot \left( \frac{\rho \mathbf{g}}{3\mu} h^3 \right) = \nabla \cdot \left( M(h) \nabla \left( -\gamma \nabla^2 h - \Pi(h) \right) \right)
```
This equation is a mass-conserving gradient flow that minimizes the macroscopic free energy functional of the film, defined by the interplay of interfacial area and intermolecular potentials:
```math
\mathcal{E}_{VTFL}[h] = \int_{\Omega} \left[ \frac{\gamma}{2}|\nabla h|^2 + U(h) \right] d\mathbf{x}
```
where $U'(h) = -\Pi(h)$. The flow involves a nonlinear convective flux tensor $\nabla \cdot (\frac{\rho \mathbf{g}}{3\mu} h^3)$ that drives kinematic shocks, which are regularized by the fourth-order degenerate parabolic capillary operator.

In Petroleum Reservoir Fractional Flow (PRFF), traditional Buckley-Leverett models fail to capture fingering and spontaneous imbibition at the macroscopic scale. Advanced macroscopic phase-field models (e.g., Cueto-Felgueroso & Juanes) resolve this by coupling Darcy flux with Cahn-Hilliard thermodynamics, generating the governing equation for water saturation $S$:
```math
\frac{\partial S}{\partial t} + \nabla \cdot \left( \mathbf{v}_T f(S) \right) = \nabla \cdot \left( M(S) \nabla \left( -\kappa \nabla^2 S + \Psi'(S) \right) \right)
```
This system similarly minimizes the total capillary free energy functional of the porous medium:
```math
\mathcal{E}_{PRFF}[S] = \int_{\Omega} \left[ \frac{\kappa}{2}|\nabla S|^2 + \Psi(S) \right] d\mathbf{x}
```

The mathematical structure is strictly identical. Upon applying the transformation $S = h / H_{max}$, both PDEs reduce to the canonical operator equivalence $u_t + \nabla \cdot \mathbf{F}(u) = \nabla \cdot \left( M(u) \nabla \mu \right)$, explicitly demonstrating the `degenerate_fourth_order_parabolic_operator` and the `nonlinear_convective_flux_tensor`. Furthermore, both systems identically dissipate their respective integrated energy functionals $\frac{d\mathcal{E}}{dt} \le 0$, demonstrating the shared `lyapunov_free_energy_functional`. The fundamental physical representation completely misaligns (a geometric height of a liquid-gas boundary vs. a volumetric ratio of two liquids inside a solid rock matrix), yet the topological constraints governing their evolution are mathematically indistinguishable.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
*   **Preferred Transfer Direction:** Viscous Thin-Film Lubrication (VTFL) → Petroleum Reservoir Fractional Flow (PRFF)
*   **Asymmetric Maturity Rationale:** Because $M(h) = h^3 \to 0$ as $h \to 0$, VTFL mathematicians have spent 30 years developing highly specialized, unconditionally positivity-preserving spatial discretization schemes (e.g., Bertozzi-Zhornitskaya numerical fluxes) that prevent unphysical negative film thicknesses. PRFF possesses robust solvers for purely hyperbolic/parabolic Darcy flow, but when targeting higher-order phase-field extensions for enhanced oil recovery, PRFF relies on standard Central Differencing or Two-Point Flux Approximation (TPFA), which violently violates saturation bounds ($S<0$ or $S>1$) at the advancing shock front, requiring ad-hoc artificial clipping that destroys mass conservation and stalls Newton-Raphson iterations.
*   **Target Bottleneck Mitigation:** Importing entropy-dissipating, positivity-preserving finite difference stencils from VTFL to evaluate the PRFF mutual mobility tensor $M(S)$ will eliminate unphysical saturation overshoots at the Buckley-Leverett shock front without resorting to non-physical truncation, resolving the dominant numerical bottleneck in macroscopic phase-field reservoir simulators.
*   **Falsifiable Prediction:** Integrating the Bertozzi-Zhornitskaya harmonic-mean numerical mobility flux into a macroscopic PRFF phase-field simulator for 1D water-oil displacement ($\kappa = 10^{-4}$) will yield zero saturation bound violations ($0 \le S \le 1$) at Courant numbers $CFL > 10$. This will achieve a >40% reduction in $L_1$ mass conservation error at the shock front compared to the state-of-the-art Fully Implicit Method (FIM) with central differencing, falsifiable if the scheme requires arbitrary saturation clipping or diverges under these parameters.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
*   `"thin-film equation" AND "positivity-preserving" AND "degenerate mobility" AND "Zhornitskaya"`
*   `"macroscopic phase-field" AND "fractional flow" AND "Cueto-Felgueroso" AND "fourth-order"`
*   `"thin film" AND "fractional flow" AND "entropy-dissipating" AND "Cahn-Hilliard"`