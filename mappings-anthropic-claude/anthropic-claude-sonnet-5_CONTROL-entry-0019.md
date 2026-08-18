---
sid_metadata:
  entry_id: "CONTROL-SID-0019"
  schema_version: "2.0-control"
  maturity_stage: "candidate"
provenance:
  company: "Anthropic"
  model_family: "Claude"
  model_version: "Sonnet 5"
  generation_timestamp: "2026-08-17"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "semiconductor-device-transport-numerics"
  domain_b: "variational-phase-field-fracture"
  structural_family: "screened-elliptic-singular-perturbation-systems"
  triple_correspondence_vectors:
    - "shared_screened_poisson_yukawa_operator_for_boundary_interior_layer_profile"
    - "shared_nondimensional_singular_perturbation_parameter_governing_layer_width_and_mesh_resolution"
    - "gummel_block_gauss_seidel_vs_staggered_alternating_minimization_decoupling_with_matched_convergence_degradation"
    - "natural_neumann_essential_dirichlet_boundary_duality_of_the_frozen_convex_subproblems"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language / historically_isolated_communities (TCAD and computational-electronics numerical analysis vs. computational solid/fracture mechanics share almost no authors, venues, or conferences) / incompatible_ontologies (statistical carrier-transport thermodynamics vs. Griffith surface-energy fracture criteria) / a superficially adjacent but distinct existing analogy — the phase-field-to-heat-conduction FEM-implementation trick used e.g. in Abaqus user-element codes — that risks being mistaken for this correspondence despite invoking neither Debye screening, singular-perturbation theory, nor Gummel-type block decoupling"
prior_discovery_metrics:
  structural_isomorphism_score: 7.5
  vocabulary_divergence_score: 9.0
  expected_methodological_transfer_score: 7.0
  community_separation_score: 9.0
  representation_mismatch_score: 6.0
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 6.5
    uncertainty: "±1.5"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "low"
  primary_failure_risk: "constitutive_law_mismatch_in_the_state_dependent_screening_coefficient — κ²(x) in Domain B is driven by the elastic energy density ψ⁺(x), which can develop near-singular gradients at an actively propagating crack tip with no analog to Domain A's smoothly-varying, doping-controlled 1/λ_D²(x); the frozen-coefficient exact-fitting argument (Section 3) is a per-element approximation whose error away from smooth background regions is not bounded by anything derived in this entry"
  bibliometric_validation: "pending"
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ⚠*CONTROL*⚠ ENTRY 0019

## 1. CROSS-SILO SYSTEM DEFINITION
*   **Silo A (Field 1):** Numerical device physics for semiconductor transport — the van Roosbroeck drift–diffusion system (Poisson's equation self-consistently coupled to electron/hole continuity equations), solved in TCAD practice via Scharfetter–Gummel finite-volume discretization and Gummel-map block decoupling. Core phenomenon: exponential space-charge (Debye) screening layers at junctions and contacts.
*   **Silo B (Field 2):** Variational computational fracture mechanics — the Francfort–Marigo energy-minimization reformulation of Griffith brittle fracture, regularized via the Ambrosio–Tortorelli (AT2) elliptic functional and solved by alternate minimization (staggered scheme) between the elastic and damage sub-problems. Core phenomenon: the diffuse crack profile set by the regularization length $\ell$.
*   **Mathematical Isomorphism:** Restricted to (i) the linear response of Domain A's Poisson equation about a frozen equilibrium background and (ii) one frozen-displacement substep of Domain B's damage Euler–Lagrange equation, both collapse onto the identical screened-Poisson (Yukawa/Helmholtz) operator $-\Delta y+\kappa^2(x)y=f(x)$, with $\kappa^{-1}$ set by the Debye length $\lambda_D$ (A) or the regularization length $\ell$ (B); their respective block-decoupling solvers (Gummel's map; staggered alternate minimization) are consequently substep-by-substep iterations on the same singularly-perturbed operator family, sharing a nondimensional layer-resolution parameter $\varepsilon=\lambda_D/L$ (resp. $\ell/L$) and a matched natural/essential boundary-condition duality. The correspondence does **not** extend to either domain's fully nonlinear, far-from-equilibrium, or constraint-active (irreversibility-binding) regime.

## 2. DIAGNOSTIC VOCABULARY MATRIX
*   Debye length $\lambda_D$ ↔ regularization length $\ell$
    *   *Operator Role:* Both are the inverse screening coefficient of the identical operator $-\Delta y+\kappa^2y=f$ (Section 3): $\kappa=1/\lambda_D$ for linearized Poisson; $\kappa=\sqrt{1/\ell^2+2\psi^+/(G_c\ell)}\to1/\ell$ in the unstressed limit for the AT2 equation. Both are real, positive, length-dimensioned scalars in the same operator slot; no type transformation is required.
*   Gummel map (block Gauss–Seidel decoupling of $\psi$ from $n,p$) ↔ staggered/alternate minimization (block decoupling of $u$ from $d$)
    *   *Operator Role:* Both are nonlinear block-coordinate fixed-point iterations that freeze one field, exactly solve/minimize a convex elliptic subproblem for the other, and repeat; both monotonically decrease an underlying energy/Lyapunov functional, converge only linearly, and degrade under strong coupling (high injection in A; active crack propagation or small $\ell$ in B).
*   Ohmic contact (Dirichlet: $\psi,n,p$ fixed) ↔ pre-existing notch/crack (Dirichlet: $d=1$ fixed)
    *   *Operator Role:* Both are *essential* boundary conditions on the frozen-field quadratic functionals $J_A,J_B$ (Section 3) — externally prescribed values the variational principle cannot itself supply, contrasted with the next pair.
*   Insulating device boundary (Neumann: $\nabla\psi\cdot\mathbf n=0$) ↔ exterior specimen boundary (Neumann: $\nabla d\cdot\mathbf n=0$)
    *   *Operator Role:* Both are *natural* boundary conditions produced by the first variation of $J_A,J_B$ on any sub-boundary with no imposed flux — derived, not assumed.
*   Scaled Debye number $\delta=\lambda_D/L$ (Markowich's singular-perturbation parameter) ↔ normalized regularization ratio $\tilde\ell=\ell/L$
    *   *Operator Role:* Both are the dimensionless coefficient multiplying the Laplacian in the identical nondimensionalized singular-perturbation equation (Section 3); both set boundary/interior-layer width and the mesh-resolution requirement $h\lesssim\varepsilon L$ native to each field's own practice.

## 3. CORE MATHEMATICAL PARALLELISM
The van Roosbroeck system models steady-state transport via
```math
-\nabla\cdot(\varepsilon\nabla\psi) = q(p-n+C(x)), \qquad C(x)\equiv N_D(x)-N_A(x)
```
closed by Boltzmann statistics $n=n_ie^{(\psi-\phi_n)/V_T}$, $p=n_ie^{(\phi_p-\psi)/V_T}$ and continuity equations with drift–diffusion flux. TCAD solvers discretize the continuity equations with the Scharfetter–Gummel scheme and decouple the system with Gummel's map (freeze $n,p$, solve linear Poisson for $\psi$; freeze $\psi$, solve continuity for $n,p$; repeat). Writing $\psi=\psi_0+\delta\psi$ about a self-consistent background and linearizing the Boltzmann relations in $\delta\psi$, with $\tilde\psi\equiv\delta\psi/V_T$:
```math
-\Delta\tilde\psi + \frac{\tilde\psi}{\lambda_D^2(x)} = f_A(x), \qquad \frac{1}{\lambda_D^2(x)}\equiv\frac{q(n_0(x)+p_0(x))}{\varepsilon V_T}, \qquad f_A(x)\equiv\frac{\delta\rho_{ext}(x)}{\varepsilon V_T}
```
the Debye–Hückel screened-Poisson equation ($f_A\equiv0$ absent an explicit added charge).

The Francfort–Marigo/Ambrosio–Tortorelli (AT2) energy is
```math
E(u,d)=\int_\Omega (1-d)^2\psi^+(\varepsilon(u))\,d\Omega + \int_\Omega \psi^-(\varepsilon(u))\,d\Omega + G_c\int_\Omega\left[\frac{d^2}{2\ell}+\frac{\ell}{2}|\nabla d|^2\right]d\Omega
```
solved by alternate minimization: freeze $d$, solve linear elasticity for $u$; freeze $u$, solve for $d$ on the irreversible admissible set (Bourdin, Francfort & Marigo, 2000; Miehe, Welschinger & Hofacker, 2010). Where the irreversibility constraint is inactive, $\delta E/\delta d=0$ gives
```math
-\Delta d + \kappa^2(x)\,d = f_B(x), \qquad \kappa^2(x)\equiv\frac{1}{\ell^2}+\frac{2\psi^+(x)}{G_c\ell}, \qquad f_B(x)\equiv\frac{2\psi^+(x)}{G_c\ell}
```
with $\nabla d\cdot\mathbf n=0$ on the exterior boundary and $d=1$ on any pre-existing notch.

**Bridge.** The two boxed equations are the same operator, $-\Delta y+\kappa^2(x)y=f(x)$, under $y\leftrightarrow(\tilde\psi,d)$ — both dimensionless by construction — $\kappa^{-1}\leftrightarrow(\lambda_D,\ell_{eff})$, $f\leftrightarrow(f_A,f_B)$. Homogeneous ($f=0$), both reduce in 1-D to $y''=y/\lambda^2$, solved by $y(x)=y(0)e^{-|x|/\lambda}$: Debye screening of a point charge in A; the AT-model's own "optimal profile," the function whose normalization fixes the crack-density functional's constant in the Ambrosio–Tortorelli Γ-convergence proof (Ambrosio & Tortorelli, 1990), in B. Rescaling space by a macroscopic length $L$ turns both into the identical singular-perturbation form $\varepsilon^2\Delta_{\tilde x}y-y=O(\varepsilon^2)$, $\varepsilon=\lambda_D/L$ (A) or $\ell/L$ (B) — matching, for A, Markowich's scaled-Debye-length formulation of the semiconductor equations (Markowich, 1984; Markowich & Ringhofer, 1984; Markowich, Ringhofer & Schmeiser, 1990) and, for B, the $\ell/L\to0$ Γ-convergence regime. $\varepsilon\ll1$ forces layers in both fields and drives matched mesh-resolution rules: several nodes per Debye length in A (Selberherr, 1984); a documented $\ell/h\gtrsim2$–$5$ in B (Section 5).

The outer solvers share an independent correspondence: Gummel's map is a documented nonlinear block Gauss–Seidel decoupling of $\{\psi\}$ from $\{n,p\}$ (Bank, Rose & Fichtner, 1983) whose convergence rate "becomes worse as the coupling between equations becomes stronger at higher bias," standardly repaired by hybridizing with Newton. Staggered alternate minimization exploits the same separate-convexity block structure and is independently documented to converge only linearly, "requiring a prohibitively large number of outer iterations whenever the crack is actively propagating" (Gerasimov & De Lorenzis, 2016), with plain monolithic Newton failing analogously because of non-convexity and the irreversibility constraint (Wick, 2017) — repaired, as in A, by hybrid/globalized strategies (BFGS: Gerasimov & De Lorenzis, 2016; quasi-Newton: Kristensen & Martínez-Pañeda, 2020; stabilized staggering: Brun, Wick, Berre, Nordbotten & Radu, 2020).

Third, each frozen subproblem is the Euler–Lagrange equation of a strictly convex quadratic functional — $J_A(\tilde\psi)=\int\frac12|\nabla\tilde\psi|^2+\frac{\tilde\psi^2}{2\lambda_D^2}-f_A\tilde\psi$, $J_B(d)=\int\frac12|\nabla d|^2+\frac{\kappa^2}{2}d^2-f_Bd$ — whose first variation supplies natural Neumann data wherever no flux is imposed and requires essential Dirichlet data wherever the field is externally fixed, in both fields identically.

**Where it stops.** The correspondence holds only for linearized Poisson (not full nonlinear Poisson–Boltzmann or degenerate Fermi–Dirac statistics) in A, and only for the frozen-$u$, irreversibility-inactive interior of one substep (not the coupled nonlinear system, and not the KKT/variational-inequality region where the constraint binds) in B. $\kappa^2(x)$ and $1/\lambda_D^2(x)$ are both spatially varying, not constant; exact local solvability (Section 4) is a piecewise-frozen-coefficient approximation, standard practice in A and proposed but not yet demonstrated for B.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
*   **Preferred Transfer Direction:** semiconductor-device-transport-numerics → variational-phase-field-fracture.
*   **Asymmetric Maturity Rationale:** For the operator class $-\Delta y+\kappa^2(x)y=f(x)$, Domain A has carried, since Il'in (1969) and Scharfetter & Gummel (1969), exponentially/hyperbolically-fitted finite-volume schemes proven exact for the frozen-coefficient homogeneous equation at *any* mesh spacing, plus a mature Gummel-then-Newton globalization strategy for block-Gauss–Seidel stalling (Bank, Rose & Fichtner, 1983); a 2026 re-derivation of exact local fitting for the *oscillatory* Helmholtz operator (Jüngel, Li, Sun & Zhang, 2026, built on a "complexified Scharfetter–Gummel discretization") confirms the technique generalizes past pure advection. Domain B is genuinely mature at two *different* capabilities — adaptive mesh refinement tracking the moving crack (Burke, Ortner & Süli, 2010) and monolithic/quasi-Newton or arc-length solvers for the *outer* $u$–$d$ coupling (Gerasimov & De Lorenzis, 2016; Kristensen & Martínez-Pañeda, 2020; Wick, 2017) — but has not adopted a parameter-uniform, exactly-fitted *discretization basis* for the $d$-subproblem itself; standard practice still uses plain Lagrange elements and manages layer resolution purely through mesh density via the documented $\ell/h\gtrsim2$–$5$ guideline. Neither AMR nor outer-loop Newton acceleration closes this narrower gap, since both still discretize the same under-fitted $d$-element locally.
*   **Target Bottleneck Mitigation:** On a frozen-coefficient element $[x_i,x_{i+1}]$ of size $h$, $-y''+\kappa_i^2y=0$ with $y(x_i)=y_i$, $y(x_{i+1})=y_{i+1}$ has the exact solution
```math
y(x) = y_i\,\frac{\sinh(\kappa_i(x_{i+1}-x))}{\sinh(\kappa_ih)} + y_{i+1}\,\frac{\sinh(\kappa_i(x-x_i))}{\sinh(\kappa_ih)}
```
which reduces to linear interpolation only as $\kappa_ih\to0$, carrying an $O((\kappa_ih)^2)$ discrepancy otherwise — the source, in Domain B's own practice, of the $\ell/h\gtrsim2$–$5$ requirement. A scheme built from this exact local solution (the pure-reaction analogue of the Bernoulli/Scharfetter–Gummel construction) removes that leading error term at any $\kappa h$, exactly as SG does for the drift term in A. Hypothesis: importing this fitted discretization for the $d$-subproblem alone (outer solver and AMR strategy untouched) decouples $d$-mesh density from $\ell$, relaxing $\ell/h\gtrsim2$–$5$ toward $\ell/h\approx1$ without degrading peak load or crack path below currently accepted accuracy.
*   **Falsifiable Prediction:** On the SENT AT2 benchmark (Miehe, Welschinger & Hofacker, 2010), the exact hyperbolic-fitted $d$-discretization run at $\ell/h=1$ should reproduce the peak reaction force of standard linear-Lagrange FEM run at the community's conservative baseline $\ell/h=4$ to within a 5% band (this entry's convergence-match threshold) — a $4\times$ linear ($\approx16\times$ areal, 2D) reduction in required $d$-mesh density in the crack-tip region for matched accuracy. Falsified if: (a) the fitted $\ell/h=1$ result's peak load deviates from the $\ell/h=4$ linear-FEM reference by more than 5%, or (b) it introduces oscillation/non-monotonicity in $d$ absent from the linear scheme at matched resolution — the outcome this entry's own caveat (spatially-varying $\kappa^2$ near an active crack tip, Section 3) flags as the most likely failure mode.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
*   `"Scharfetter-Gummel" AND "phase-field fracture"`
*   `"exponentially fitted" AND "Ambrosio-Tortorelli"`
*   `"Debye length" AND "regularization length" AND "phase-field fracture"`
*   `"Gummel map" AND "alternate minimization" AND "staggered scheme"`
*   `"singular perturbation" AND "Debye length" AND "Scharfetter-Gummel"`
*   `"Ambrosio-Tortorelli" AND "regularization length" AND "mesh sensitivity"`