---
sid_metadata:
  entry_id: "CONTROL-SID-0010"
  schema_version: "2.0-control"
  maturity_stage: "candidate"
provenance:
  company: "OpenAI"
  model_family: "GPT"
  model_version: "5.6 Luna"
  generation_timestamp: "2026-08-17"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "deformable-porous-media-flow"
  domain_b: "nonlocal-continuum-mechanics"
  structural_family: "loss-of-ellipticity-regularized-localization"
  triple_correspondence_vectors:
    - "coupled_force-balance_and_mass-balance_operator_pair"
    - "variational_energy-dissipation_stationarity_pair"
    - "localization_threshold_regularized_by_nonlocal_interaction_length"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language / historically_isolated_communities / representation_mismatch"
prior_discovery_metrics:
  structural_isomorphism_score: 7.2
  vocabulary_divergence_score: 7.8
  expected_methodological_transfer_score: 5.1
  community_separation_score: 5.9
  representation_mismatch_score: 7.0
  expected_transfer_effort: "high"
  novelty_prior:
    estimate: 2.4
    uncertainty: "±1.5"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "low"
  primary_failure_risk: "bibliometric_novelty_failure"
  bibliometric_validation: "pending"
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ⚠*CONTROL*⚠ ENTRY 0010

## 1. CROSS-SILO SYSTEM DEFINITION

* **Silo A (Field 1):** Deformable porous-media flow, restricted to quasi-static saturated poromechanics in which displacement and pore pressure are coupled through mechanical equilibrium and fluid mass balance, with localization/softening as the target phenomenon.
* **Silo B (Field 2):** Nonlocal continuum mechanics, specifically state-based/peridynamic formulations of deforming continua in which integral interactions replace local spatial derivatives and an interaction horizon regularizes localization.
* **Mathematical Isomorphism:** Under a linearized, saturated, quasi-static restriction, the coupled poromechanical equilibrium–mass operator admits a variational energy/dissipation representation whose localization singularity can be regularized by replacing the local strain-gradient quadratic form with a finite-horizon nonlocal quadratic form; the demonstrated correspondences are the coupled force-balance/mass-balance operator pair, energy-dissipation stationarity, and localization-threshold regularization by interaction length. Existing literature already contains direct peridynamic poromechanics and porous-media-flow formulations, so novelty of this narrower structural claim is explicitly uncertain and requires bibliometric validation. ([ScienceDirect][1])

## 2. DIAGNOSTIC VOCABULARY MATRIX

* **Silo A: effective stress / pore-pressure coupling** ↔ **Silo B: effective force state / nonlocal deformation state**

  * *Operator Role:* Both enter the mechanical equilibrium operator as the derivative of an energy with respect to the kinematic variable: in Silo A the stress is the displacement derivative of the poromechanical energy, while in Silo B the force state is the corresponding derivative with respect to the nonlocal deformation state. Both are second-order force-density objects after spatial integration.

* **Silo A: Darcy mass flux** ↔ **Silo B: nonlocal flux state**

  * *Operator Role:* Both are dissipative flux operators driven by a pressure/hydraulic-potential difference; the local divergence operator in Silo A is replaced by an integral interaction operator in Silo B, with the nonlocal operator required to converge to the local one as the horizon tends to zero. This local-limit property is explicitly established for nonlocal porous-flow formulations. ([ScienceDirect][1])

* **Silo A: localization/softening threshold** ↔ **Silo B: horizon-regularized localization threshold**

  * *Operator Role:* Both are expressed through loss of positive definiteness of the second variation of an energy functional; Silo B adds a finite interaction length to the quadratic form, preventing the local zero-wavelength localization mode from being represented as an arbitrarily sharp field.

## 3. CORE MATHEMATICAL PARALLELISM

For Silo A, consider the linearized saturated quasi-static Biot-type system. The solid equilibrium equation and fluid mass balance can be written, after eliminating body-force terms, as a coupled elliptic/parabolic operator acting on displacement (u) and pore pressure (p):

```math
-\nabla\!\cdot\!\left[\mathbb C:\varepsilon(u)-\alpha p\,\mathbf I\right]=\mathbf f,
```

```math
S\,\dot p+\alpha\,\dot{\varepsilon_v(u)}
-\nabla\!\cdot\!\left(\frac{\mathbf k}{\mu}\nabla p\right)=q.
```

The associated incremental potential/dissipation structure is

```math
\Pi[u,p]
=
\frac12\int_\Omega
\varepsilon(u):\mathbb C:\varepsilon(u)\,d\Omega
-\int_\Omega\alpha p\,\varepsilon_v(u)\,d\Omega
+\frac12\int_\Omega S p^2\,d\Omega
-\int_\Omega q p\,d\Omega,
```

with Darcy dissipation

```math
\mathcal D[p]
=
\frac12\int_\Omega
\nabla p\cdot\frac{\mathbf k}{\mu}\nabla p\,d\Omega .
```

Thus the displacement equation is the Euler derivative of the mechanical/pore-pressure energy, while the pressure equation contains the corresponding positive dissipative quadratic form. The important structural point is not merely that both systems contain derivatives: the coupled mechanical and hydraulic operators arise from an energy–dissipation pair.

For Silo B, an independently recognizable state-based/peridynamic formulation replaces local stress-divergence and flux-divergence operations with finite-horizon interaction operators. A generic nonlocal mechanical equilibrium has the form

```math
\mathcal N_\delta[u](x)
=
\int_{H_\delta(x)}
\left\{
\underline{\mathbf T}[u](x,\xi)
-
\underline{\mathbf T}[u](x+\xi,-\xi)
\right\}\,dV_{x+\xi}
+\mathbf b(x)
=\mathbf 0 ,
```

where (H_\delta(x)) is the horizon and (\underline{\mathbf T}) is the force state. A nonlocal pressure-transport operator can analogously be represented as

```math
\mathcal Q_\delta[p](x)
=
\int_{H_\delta(x)}
K_\delta(x,\xi)\,[p(x+\xi)-p(x)]\,dV_{x+\xi}.
```

The corresponding nonlocal mechanical energy and transport dissipation can be represented as

```math
\Pi_\delta[u,p]
=
\frac14
\int_\Omega\!\int_{H_\delta(x)}
W_\delta\!\left(\underline{\mathbf Y}[u]\right)
\,dV_{x+\xi}dV_x
-\int_\Omega\alpha p\,\varepsilon_{v,\delta}(u)\,d\Omega
+\frac12\int_\Omega S p^2\,d\Omega ,
```

```math
\mathcal D_\delta[p]
=
\frac14
\int_\Omega\!\int_{H_\delta(x)}
K_\delta(x,\xi)
[p(x+\xi)-p(x)]^2
\,dV_{x+\xi}dV_x .
```

The three structural correspondences are therefore explicit. **First**, the coupled force-balance/mass-balance pair maps as

```math
\left(
-\nabla\!\cdot\boldsymbol\sigma,\;
-\nabla\!\cdot\frac{\mathbf k}{\mu}\nabla p
\right)
\quad\longleftrightarrow\quad
\left(
\mathcal N_\delta[u],\;
\mathcal Q_\delta[p]
\right),
```

with the required local-limit bridge

```math
\lim_{\delta\rightarrow0}\mathcal N_\delta[u]
=
-\nabla\!\cdot\boldsymbol\sigma,
\qquad
\lim_{\delta\rightarrow0}\mathcal Q_\delta[p]
=
-\nabla\!\cdot\frac{\mathbf k}{\mu}\nabla p .
```

This type of local-limit correspondence is established in nonlocal porous-flow literature rather than being assumed here. ([ScienceDirect][1])

**Second**, both systems possess an energy–dissipation stationarity structure. In Silo A,

```math
\delta_u\Pi=0,
\qquad
\mathcal D[p]\ge0,
```

whereas in Silo B,

```math
\delta_u\Pi_\delta=0,
\qquad
\mathcal D_\delta[p]\ge0.
```

The nonlocal porous-mechanics literature explicitly derives effective force states through energy equivalence, and stabilized nonlocal poromechanics has used equality between nonlocal and local strain-energy/dissipation measures. ([ScienceDirect][2])

**Third**, the localization threshold is regularized by the finite interaction length. For a local softening model, the second variation has the Fourier-mode form

```math
\delta^2\Pi
\sim
\left[
H_{\rm tan}+k^2\,\ell_{\rm loc}^2
\right]|\widehat{\eta}(k)|^2 ,
```

so the local localization threshold is associated with loss of positive definiteness,

```math
H_{\rm tan}+k^2\ell_{\rm loc}^2=0 .
```

The corresponding nonlocal quadratic interaction has a Fourier symbol

```math
\widehat{\mathcal L_\delta}(k)
=
2\int_{H_\delta}
K_\delta(\xi)
\left[1-\cos(k\!\cdot\!\xi)\right]d\xi ,
```

with

```math
\widehat{\mathcal L_\delta}(k)
=
C_2 k^2+O(\delta^2 k^4)
\qquad
(k\delta\ll1).
```

Consequently, the finite horizon suppresses arbitrarily high-(k) localization modes and introduces a calculable wavelength scale rather than merely relabeling the local constitutive equations.

The correspondence therefore **does not** claim constitutive equivalence between Darcy/Biot poromechanics and peridynamic constitutive laws. It claims an operator-level correspondence between their coupled equilibrium/transport operators and their energy–dissipation regularizations, under the stated saturated, quasi-static, linearized/local-limit restriction. Direct nonlocal porous-flow and poromechanics formulations already exist, including formulations for heterogeneous saturated media and unsaturated media, so the proposed novelty resides only in treating the localization threshold and energy–dissipation structure as the transferable organizing object rather than in proposing “peridynamics for porous flow” itself. ([ScienceDirect][3])

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS

* **Preferred Transfer Direction:** Nonlocal continuum mechanics → deformable-porous-media-flow localization analysis

* **Asymmetric Maturity Rationale:** Nonlocal continuum mechanics has a comparatively developed machinery for finite-horizon integral operators, meshfree discretization, discontinuity evolution, stabilization of correspondence formulations, and horizon/local-limit analysis. In contrast, deformable porous-media flow already possesses mature finite-element poromechanics, bifurcation, phase-field, and coupled hydro-mechanical tools; its narrower deficiency is not the ability to solve poromechanics generally, but a robust finite-horizon regularization that preserves the coupled energy/dissipation structure while allowing localization without an imposed crack geometry. This distinction is important because recent work already combines FEM and peridynamics for saturated porous-media compaction bands, making the proposed transfer an incremental structural hypothesis rather than an unoccupied research territory. ([ScienceDirect][4])

* **Target Bottleneck Mitigation:** Import a nonlocal interaction kernel into the coupled poromechanical second variation while retaining the Darcy/Biot pressure equation as the local-limit operator. The intended computational benefit is to replace the mesh-sensitive zero-wavelength localization mode with a finite interaction-length mode, while retaining the conventional poromechanical solution as (\delta\rightarrow0). This could provide a controlled regularization of hydro-mechanically coupled compaction-band nucleation without changing the underlying Biot constitutive variables.

* **Falsifiable Prediction:** On a saturated high-porosity sandstone compaction-band benchmark with fixed geometry, loading path, permeability (k), and constitutive parameters, compare a conventional local (u-p) finite-element formulation against its finite-horizon regularized counterpart at matched spatial resolution. The proposed operator predicts that the regularized model will exhibit a finite dominant localization wavelength satisfying the maximum of the computed nonlocal amplification factor at (k_\ast\delta=O(1)), whereas the local model has no intrinsic finite wavelength. A concrete falsification criterion is: if, after grid refinement by a factor of four at fixed (\delta), the measured band width changes by more than 10%, or if the dominant wavelength fails to remain within the interval (0.5\delta\le\lambda_\ast\le4\delta), the proposed finite-horizon regularization hypothesis is falsified. The benchmark should be compared against the established local hydro-mechanical phase-field formulation and the recent FEM/peridynamic saturated compaction-band formulation rather than against an unconstrained numerical baseline. ([ScienceDirect][4])

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION

* `"compaction localization" AND "Biot poromechanics" AND "loss of ellipticity" AND "nonlocal"`
* `"nonlocal continuum" AND "energy dissipation" AND "poromechanics" AND "localization"`
* `"peridynamic" AND "coupled poromechanics" AND "finite horizon" AND "localization wavelength"`
* `"nonlocal regularization" AND "poroelastic" AND "compaction band" AND "second variation"`
* `"peridynamic" AND "Biot" AND "compaction band" AND "energy equivalence"` — deliberate novelty-falsification search; direct papers already exist on peridynamic porous-media flow, peridynamic poromechanics, and hydro-mechanically coupled compaction bands, so a Stage-3 bibliometric review is essential before treating this as genuinely novel. ([ScienceDirect][1])

[1]: https://www.sciencedirect.com/science/article/pii/S0021999113008474?utm_source=chatgpt.com "A peridynamic formulation of pressure driven convective fluid transport in porous media - ScienceDirect"
[2]: https://www.sciencedirect.com/science/article/pii/S0022509620303938?utm_source=chatgpt.com "On the peridynamic effective force state and multiphase constitutive correspondence principle - ScienceDirect"
[3]: https://www.sciencedirect.com/science/article/pii/S0045782521005909?utm_source=chatgpt.com "A unified non-local fluid transport model for heterogeneous saturated porous media - ScienceDirect"
[4]: https://www.sciencedirect.com/science/article/pii/S0749641925001883?utm_source=chatgpt.com "Shear-compaction band evolution in dry and saturated porous media using a hybrid Finite Element Method/Peridynamic model - ScienceDirect"
