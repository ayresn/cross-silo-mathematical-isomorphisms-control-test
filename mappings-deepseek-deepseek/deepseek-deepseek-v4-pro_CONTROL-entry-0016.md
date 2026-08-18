---
sid_metadata:
  entry_id: "CONTROL-SID-0016"
  schema_version: "2.0-control"
  maturity_stage: "candidate"
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
*   `"critical recoverable shear" AND "coil-stretch transition" AND "die entry"`