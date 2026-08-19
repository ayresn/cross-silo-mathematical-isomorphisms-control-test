---
sid_metadata:
  entry_id: "CONTROL-SID-0010"
  schema_version: "2.0-control"
  maturity_stage: "adversarial-flagged"
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
  first_adversarial_review:
    reviewer_model: "Anthropic Claude Sonnet 5"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "PASS"
    verdict_rationale: "All four checks are satisfied: the local (Biot) and nonlocal (peridynamic) operator pairs are individually well-formed and connected by an explicit local-limit relation rather than a claimed identity across mismatched classes, the three vocabulary mappings each specify a genuine shared structure, all three listed correspondence vectors are demonstrated with explicit equations in Section 3, and the transfer direction and falsification criterion in Section 4 meet the required specificity."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items:
      - "The entry's own citations (peridynamic porous-media transport, peridynamic effective force state, unified nonlocal fluid transport, FEM/peridynamic saturated compaction bands) describe closely adjacent work; Stage 3 should determine whether the specific triple correspondence — operator pair, energy-dissipation stationarity, and localization-threshold regularization taken together as a single organizing object — is distinct from those contributions, using the entry's own 'deliberate novelty-falsification' search string as a starting point."
      - "Section 3's variational potential Pi[u,p] is written with p and epsilon_v(u) entering directly, while the target mass-balance PDE is in rate form (S*p_dot + alpha*epsilon_v_dot); the entry does not spell out the rate/incremental-potential convention that bridges the two. This is a standard device in Biot variational formulations rather than an error, but is worth confirming on a closer technical pass."
  second_adversarial_review:
    reviewer_model: "Alibaba Qwen 3.8 Max"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "PASS"
    verdict_rationale: "The entry demonstrates rigorous mathematical consistency, with all three correspondence vectors fully supported by explicit equations and derivations, and a highly specific, falsifiable transfer hypothesis."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: ["Verify the bibliometric novelty of treating the localization threshold and energy-dissipation structure as the transferable organizing object, as the entry explicitly acknowledges existing literature on peridynamic poromechanics and nonlocal porous flow."]
  third_adversarial_review:
    reviewer_model: "DeepSeek DeepSeek V4 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "REJECT"
    verdict_rationale: "The entry contains a sign error in the displayed nonlocal local-limit bridge and a vocabulary category error pairing a vector Darcy flux with a scalar nonlocal operator."
    failed_checks:
      - "Check 1: Equation Validity — sign error in the local-limit bridge for the nonlocal pressure-transport operator Qδ"
      - "Check 2: Vocabulary Matrix Coherence — Darcy mass flux (vector) paired with nonlocal flux state (scalar operator)"
    flagged_checks:
      - "Check 3: Correspondence Vector Support — coupled_force-balance_and_mass-balance_operator_pair is only partially demonstrated"
    quoted_evidence:
      - "A nonlocal pressure-transport operator can analogously be represented as\n\n```math\n\\mathcal Q_\\delta[p](x)\n=\n\\int_{H_\\delta(x)}\nK_\\delta(x,\\xi)\\,[p(x+\\xi)-p(x)]\\,dV_{x+\\xi}.\n```"
      - "\\lim_{\\delta\\rightarrow0}\\mathcal Q_\\delta[p]\n=\n-\\nabla\\cdot\\frac{\\mathbf k}{\\mu}\\nabla p ."
      - "* **Silo A: Darcy mass flux** ↔ **Silo B: nonlocal flux state**"
    stage_3_watch_items:
      - "Prior art: peridynamic poromechanics, nonlocal porous-flow transport, and hybrid FEM/peridynamic compaction-band models already exist and are cited in the entry; verify novelty of the operator-level localization-threshold transfer."
      - "Verify sign conventions and local-limit coefficients in the cited nonlocal porous-flow literature."
      - "Probe whether the Biot storage/coupling terms S p_dot + α ε_v_dot have a demonstrated nonlocal counterpart in the body."
      - "Check dimensional consistency of the local potential Π[u,p], especially the q p term against the elastic and storage terms."
  fourth_adversarial_review:
    reviewer_model: "Google Gemini 3.1 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "REJECT"
    verdict_rationale: "The entry contains fatal mathematical errors regarding the formulation of a local model's second variation and the kinematic derivative relationship for stress, alongside a vocabulary category error."
    failed_checks:
      - "Check 1: Equation Validity (Incorrect mathematical formulation of the local softening model)"
      - "Check 2: Vocabulary Matrix Coherence (Category error in mapping and mathematical error in operator description)"
    flagged_checks: []
    quoted_evidence:
      - "For a local softening model, the second variation has the Fourier-mode form\n\n```math\n\delta^2\Pi\n\sim\n\left[\nH_{\rm tan}+k^2\,\ell_{\rm loc}^2\n\right]|\widehat{\eta}(k)|^2 ,\n```\n\nso the local localization threshold is associated with loss of positive definiteness,\n\n```math\nH_{\rm tan}+k^2\ell_{\rm loc}^2=0 .\n```"
      - "Silo A: effective stress / pore-pressure coupling ↔ Silo B: effective force state / nonlocal deformation state"
      - "in Silo A the stress is the displacement derivative of the poromechanical energy"
    stage_3_watch_items:
      - "Verify the novelty of the structural correspondence, given the entry's explicit acknowledgment that direct peridynamic poromechanics literature already exists."
  fifth_adversarial_review:
    reviewer_model: "Xiaomi MiMo V2.5 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "PASS"
    verdict_rationale: "All three correspondence vectors are demonstrated with explicit equations on both sides; the coupled operator pair, energy–dissipation structure, and localization-threshold regularization are each shown with matching mathematical formulations that are internally consistent and class-compatible."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items:
      - "The entry explicitly acknowledges that 'existing literature already contains direct peridynamic poromechanics and porous-media-flow formulations' and states novelty is 'explicitly uncertain.' The claimed novelty rests on treating the localization threshold and energy–dissipation structure as the transferable organizing object rather than on proposing peridynamics for porous flow itself. Stage 3 must verify whether this narrower structural claim has already been articulated in the existing literature."
      - "All four reference URLs (ScienceDirect articles S0021999113008474, S0022509620303938, S0045782521005909, S0749641925001883) failed to load. Stage 3 should verify these references independently and confirm they support the claims attributed to them."
      - "The entry cites [ScienceDirect][4] (hybrid FEM/peridynamic saturated compaction-band work) as evidence that the proposed transfer is 'incremental structural hypothesis rather than an unoccupied research territory.' Stage 3 should determine whether this reference already contains the operator-level energy–dissipation correspondence the entry claims."
  sixth_adversarial_review:
    reviewer_model: "Z.AI GLM-5.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "PASS"
    verdict_rationale: "All four checks pass: equations are valid and correctly attributed, vocabulary mappings pair compatible types with named shared structure, all three correspondence vectors are demonstrated with equations, and the transfer is genuinely asymmetric with a quantitatively falsifiable prediction."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items:
      - "Prior art: The entry itself repeatedly acknowledges existing peridynamic poromechanics, nonlocal porous-flow, and hybrid FEM/peridynamic compaction-band formulations. Stage 3 must determine whether the specific structural framing — energy-dissipation stationarity as the transferable organizing object rather than 'peridynamics for porous flow' per se — is genuinely novel."
      - "The entry labels the second-variation form δ²Π ~ [H_tan + k²ℓ_loc²]|η̂(k)|² as belonging to a 'local softening model'; Stage 3 should verify whether this represents a gradient-enhanced (weakly nonlocal) model rather than a purely local one, and whether the terminology is standard in the poromechanics community."
      - "The falsification criterion specifies a wavelength band 0.5δ ≤ λ* ≤ 4δ and a 10% band-width stability threshold under 4× grid refinement; Stage 3 should check whether these quantitative bounds are derived from existing nonlocal regularization theory or are novel predictions."
  seventh_adversarial_review:
    reviewer_model: "Microsoft Copilot 1.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "PASS"
    verdict_rationale: "The entry's equations, operator mappings, and demonstrated correspondences are mathematically consistent and each of the three listed correspondence vectors is supported by explicit equations or operator identities in the body."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items:
      - "Verify bibliometric novelty: Stage 3 should confirm whether the cited peridynamic-poromechanics literature already establishes the same operator-level regularization claim."
      - "Check the rigor of the local-limit expansions and assumptions (e.g., the stated expansion \\(\\widehat{\\mathcal L_\\delta}(k)=C_2 k^2+O(\\delta^2 k^4)\\) and the conditions for \\(k\\delta\\ll1\\))."
      - "Confirm positivity and coercivity conditions assumed for the nonlocal kernels \\(K_\\delta\\) and energy density \\(W_\\delta\\) that underpin the second-variation arguments."
      - "Examine numerical/benchmark details underlying the falsifiability criterion (grid-refinement protocol, how \\(\\delta\\) is held relative to mesh size, and measurement of band width)."
  eighth_adversarial_review:
    reviewer_model: "xAI Grok 4.5 Fast"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "PASS"
    verdict_rationale: "All four checks pass with equations matching claimed domains and structures, coherent type-compatible vocabulary mappings that name shared operators, all three listed vectors fully demonstrated by explicit operator identities and Fourier analysis in Section 3, and an asymmetric transfer supported by a concrete measurable falsification criterion."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: ["Confirm that the local-limit bridge and energy-equivalence statements for the nonlocal operators are not overstated relative to the cited peridynamic-poromechanics literature already flagged by the entry itself."]
  ninth_adversarial_review:
    reviewer_model: "Meta Muse Spark 1.1"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "PASS"
    verdict_rationale: "All three claimed correspondence vectors are demonstrated with explicit operators and local-limit identities, equations are correctly attributed to Biot poromechanics and state-based peridynamics with no class mismatch, vocabulary mappings are type-compatible with shared operator roles, and Section 4 provides asymmetric transfer with measurable falsification thresholds."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: ["Bibliometric novelty check required: entry itself cites existing peridynamic porous-media flow and peridynamic poromechanics formulations (2013 peridynamic pressure-driven transport, 2021 unified non-local transport, 2025 hybrid FEM/Peridynamic compaction-band) that may subsume the claimed operator correspondence; Stage 3 must verify novelty of energy-dissipation regularization framing vs direct peridynamic poromechanics."]
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

---

## ADVERSARIAL REVIEWS (Stage 2)

### First Adversarial Review
**Reviewer:** Anthropic Claude Sonnet 5
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The Silo A equations form the standard coupled elliptic(-in-u)/parabolic(-in-p) Biot system and the Silo B equations form standard state-based peridynamic force-state and nonlocal-flux operators, and the claimed correspondence is an explicit local-limit relation (lim_{δ→0} N_δ[u] = -∇·σ, lim_{δ→0} Q_δ[p] = -∇·(k/μ∇p)) rather than an assertion of identity between incompatible operator classes.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — Each of the three Section 2 pairs (effective stress/pore-pressure coupling ↔ effective force state/nonlocal deformation state; Darcy mass flux ↔ nonlocal flux state; localization/softening threshold ↔ horizon-regularized localization threshold) states a specific shared mathematical structure — an energy-conjugate derivative, a potential-driven dissipative flux, and loss of positive-definiteness of the second variation, respectively — rather than resting on hedged similarity language, and none matches the enumerated category-error patterns.
- **CHECK 3 (Correspondence Vector Support):** PASS — Each listed vector is demonstrated in Section 3 with explicit equations: "coupled force-balance and mass-balance operator pair" via the N_δ/Q_δ correspondence and its stated local-limit bridge (labeled "First"); "variational energy-dissipation stationarity pair" via Π/Π_δ and D/D_δ (labeled "Second"); "localization threshold regularized by nonlocal interaction length" via the Fourier-mode second-variation comparison of H_tan+k²ℓ²_loc against the nonlocal symbol L̂_δ(k) (labeled "Third").
- **CHECK 4 (Transfer and Falsifiability):** PASS — The stated transfer direction (nonlocal mechanics → porous-media localization analysis) is scoped to a specific sub-capability, horizon-based regularization without imposed crack geometry, rather than to general poromechanics competence, which makes the asymmetry claim defensible rather than reversed. The Section 4 prediction specifies a measurable dominant-wavelength/band-width criterion (0.5δ ≤ λ* ≤ 4δ; band width changing by no more than 10% under 4× mesh refinement) that is falsifiable rather than a template non-prediction. No domain pairing here is recognized as canonical textbook prior art beyond what the entry already self-cites.

#### Stage 3 Watch Items
- The entry's own citations already describe closely adjacent peridynamic porous-media and poromechanics work; the bibliometric review should test whether the specific triple correspondence — taken together as one organizing object, rather than any one vector alone — is distinct from those contributions.
- The bridge between the instantaneous variational potential Π[u,p] in Section 3 and the rate-form mass-balance PDE (S·ṗ + α·ε̇_v) is not made fully explicit; confirming the intended rate/incremental-potential convention would strengthen the entry without changing its current internal consistency.

### Second Adversarial Review
**Reviewer:** Alibaba Qwen 3.8 Max
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The local Biot poroelasticity equations and their nonlocal peridynamic counterparts are correctly formulated and belong to compatible operator classes, with the local-limit bridge properly established.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The vocabulary mappings correctly pair objects of compatible mathematical types (e.g., energy derivatives to force states, dissipative flux operators) without category errors.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed vectors (coupled operator pair, energy-dissipation stationarity, and horizon-regularized localization threshold) are explicitly demonstrated in Section 3 with equations and Fourier analysis.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction is logically asymmetric, and the falsifiability criterion provides specific, measurable numerical thresholds (10% band width change, wavelength bounds) rather than a vague template prediction.

#### Stage 3 Watch Items
- Verify the bibliometric novelty of treating the localization threshold and energy-dissipation structure as the transferable organizing object, as the entry explicitly acknowledges existing literature on peridynamic poromechanics and nonlocal porous flow.

### Third Adversarial Review
**Reviewer:** DeepSeek DeepSeek V4 Pro
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The displayed local-limit bridge `\lim_{\delta\rightarrow0}\mathcal Q_\delta[p] = -\nabla\cdot\frac{\mathbf k}{\mu}\nabla p` is inconsistent with the preceding definition `\mathcal Q_\delta[p](x) = \int_{H_\delta(x)} K_\delta(x,\xi)\,[p(x+\xi)-p(x)]\,dV_{x+\xi}`. For a positive symmetric kernel, the second-order expansion gives a positive coefficient times `\nabla^2 p`, whereas `-\nabla\cdot(\mathbf k/\mu\nabla p)` equals a negative coefficient times `\nabla^2 p`. The sign is wrong.
- **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — The matrix row `* **Silo A: Darcy mass flux** ↔ **Silo B: nonlocal flux state**` maps a vector constitutive flux to the scalar operator `\mathcal Q_\delta[p]` defined in Section 3. The role text describes replacing the local divergence operator with an integral operator, but the token pair itself is a type mismatch: a vector flux is not a scalar nonlocal transport operator.
- **CHECK 3 (Correspondence Vector Support):** FLAG — `coupled_force-balance_and_mass-balance_operator_pair` is only partially demonstrated. The body maps the force-divergence and flux-divergence parts, but it does not provide a nonlocal counterpart for the storage/coupling time-derivative terms `S \dot p + α \dot{\varepsilon_v(u)}` in the Biot mass balance. The energy-dissipation and localization-threshold vectors are demonstrated at the level claimed.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction is plausibly asymmetric, and the falsification criterion is quantitative: 10% band-width change under grid refinement and `0.5\delta \le \lambda_* \le 4\delta`. Advisory prior-art note: the entry itself acknowledges existing peridynamic poromechanics and nonlocal porous-flow formulations, so Stage 3 should probe novelty directly.

#### Stage 3 Watch Items
- Prior art: peridynamic poromechanics, nonlocal porous-flow transport, and hybrid FEM/peridynamic compaction-band models already exist and are cited in the entry; verify whether the claimed operator-level localization-threshold transfer is bibliographically novel.
- Verify sign conventions and local-limit coefficients in the cited nonlocal porous-flow literature; the displayed `\mathcal Q_\delta[p]` local limit appears to be opposite in sign.
- Probe whether the Biot storage/coupling terms `S \dot p + α \dot{\varepsilon_v(u)}` have a demonstrated nonlocal counterpart in the body, or whether the mapping reduces to the uncoupled flux-divergence operator.
- Check dimensional consistency of the local potential `Π[u,p]`, especially the `q p` term against the elastic and storage terms.

### Fourth Adversarial Review
**Reviewer:** Google Gemini 3.1 Pro
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The text claims "For a local softening model, the second variation has the Fourier-mode form" containing the term `H_{\rm tan}+k^2\,\ell_{\rm loc}^2`, and asserts "so the local localization threshold is associated with loss of positive definiteness, H_{\rm tan}+k^2\ell_{\rm loc}^2=0 ." This is mathematically incorrect: a strictly local continuum model possesses no internal length scale ($\ell_{\rm loc}$) and its second variation depends solely on the local tangent moduli without any $k^2$ gradient term. Including $k^2\,\ell_{\rm loc}^2$ mathematically defines a gradient-enhanced/nonlocal model, which completely invalidates the stated contrast with peridynamics.
- **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — The entry maps "Silo A: effective stress / pore-pressure coupling ↔ Silo B: effective force state / nonlocal deformation state", which constitutes a category error by pairing a physical interaction effect ("pore-pressure coupling") with a kinematic state variable ("nonlocal deformation state"). Furthermore, the Operator Role contains a mathematical error by claiming "in Silo A the stress is the displacement derivative of the poromechanical energy"; stress is the derivative with respect to strain, not displacement.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three correspondence vectors listed in the YAML (`coupled_force-balance_and_mass-balance_operator_pair`, `variational_energy-dissipation_stationarity_pair`, `localization_threshold_regularized_by_nonlocal_interaction_length`) are demonstrated in the body via explicit operator identities and equations.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The methodological transfer direction leverages an asymmetric maturity in finite-horizon regularization. The proposal offers a specific, measurable falsification criterion based on comparing localized band width and dominant wavelengths against specified bounds under grid refinement.

#### Stage 3 Watch Items
- Verify the true novelty of the structural correspondence, as the entry explicitly notes that peridynamic formulations of both poromechanics and porous-media flow already exist in the published literature.

### Fifth Adversarial Review
**Reviewer:** Xiaomi MiMo V2.5 Pro
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-19

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The Silo A Biot-type coupled elliptic/parabolic system, its associated energy functional Π and Darcy dissipation 𝒟, and the Silo B peridynamic equilibrium operator 𝒩_δ, nonlocal transport operator 𝒬_δ, nonlocal energy Π_δ, and nonlocal dissipation 𝒟_δ are all internally consistent, class-compatible, and correctly model what the accompanying descriptions claim. The local-limit bridge (δ→0) and the Fourier-symbol analysis of the second variation are standard and correctly stated.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All three vocabulary mappings pair objects of compatible mathematical type (stress/force-state as energy-conjugate force densities, Darcy flux/nonlocal flux as dissipative transport operators, localization thresholds as loss-of-positive-definiteness conditions), and each Operator Role explanation identifies a specific shared mathematical structure rather than relying on hedged similarity language.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed vectors are demonstrated in Section 3 with explicit equations: (1) the coupled operator pair is shown with a correspondence arrow and verified through the local limit; (2) the energy–dissipation stationarity is shown with δ_uΠ=0, 𝒟≥0 on both sides and explicit functional forms; (3) the localization-threshold regularization is shown through the Fourier symbol analysis of the second variation for both local gradient and nonlocal finite-horizon models.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction (nonlocal continuum mechanics → poromechanics localization) is genuinely asymmetric: nonlocal mechanics has the more developed machinery for horizon integral operators and meshfree discretization, while the stated target deficiency (finite-horizon regularization preserving coupled energy/dissipation structure for compaction-band nucleation) is a narrower gap in the poromechanics toolkit. The falsifiable prediction specifies a concrete benchmark (saturated high-porosity sandstone), measurable quantities (dominant localization wavelength, band width under grid refinement), a specific threshold (10% band-width change under 4× refinement), a wavelength interval (0.5δ ≤ λ* ≤ 4δ), and named comparison models. Prior art: the entry is transparent that direct peridynamic poromechanics and peridynamic porous-flow formulations already exist; this is a known research area and the entry frames its novelty narrowly.

#### Stage 3 Watch Items
- **Novelty verification essential:** The entry acknowledges that peridynamic poromechanics, peridynamic porous-flow, and hybrid FEM/peridynamic compaction-band formulations already exist. The narrow claim — that the localization threshold and energy–dissipation structure constitute the transferable organizing object — must be checked against the existing literature to determine whether this reframing is novel or already implicit in prior work.
- **Reference verification:** All four ScienceDirect reference URLs failed to load during this review. Stage 3 must independently retrieve and verify articles S0021999113008474, S0022509620303938, S0045782521005909, and S0749641925001883, and confirm that the claims attributed to each reference are accurate.
- **Check whether reference [4] already contains the claimed isomorphism:** The entry cites a hybrid FEM/peridynamic saturated compaction-band paper and concedes the proposed transfer is "incremental." If this reference already articulates the energy–dissipation/operator-level correspondence, the entry's novelty claim collapses entirely.

### Sixth Adversarial Review
**Reviewer:** Z.AI GLM-5.2
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The Biot equilibrium equation (elliptic) and mass-balance equation (parabolic) are correctly stated, as are the peridynamic integral equilibrium operator and the nonlocal pressure-transport operator; both systems share compatible operator classes (differential elliptic/parabolic ↔ integral operators with correct local-limit convergence), and the energy/dissipation functionals on both sides are consistent with their respective equilibrium equations. The Fourier-symbol analysis of the nonlocal operator $\hat{\mathcal{L}}_\delta(k) = 2\int_{H_\delta} K_\delta(\xi)[1-\cos(k\cdot\xi)]d\xi$ and its Taylor expansion $\hat{\mathcal{L}}_\delta(k) = C_2 k^2 + O(\delta^2 k^4)$ for $k\delta \ll 1$ are standard and correct. No equation-class mismatch, no misattributed equations.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All three mapping pairs pair compatible mathematical types (stress/coupling ↔ force state; Darcy flux ↔ nonlocal flux state; localization threshold ↔ horizon-regularized threshold) and each Operator Role explanation specifies a named shared mathematical structure (energy derivative with respect to kinematics; dissipative flux driven by pressure difference with stated local-limit transformation; loss of positive definiteness of the second variation), not mere analogy.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed vectors are demonstrated in the body with explicit equations on both sides: (1) the coupled operator pair mapping $(-\nabla\cdot\boldsymbol\sigma, -\nabla\cdot\frac{\mathbf{k}}{\mu}\nabla p) \longleftrightarrow (\mathcal{N}_\delta[u], \mathcal{Q}_\delta[p])$ with local-limit bridge equations (Section 3, "First" correspondence); (2) the energy-dissipation stationarity pair with $\Pi[u,p]$, $\mathcal{D}[p]$, $\Pi_\delta[u,p]$, $\mathcal{D}_\delta[p]$ and the stationarity/dissipativity conditions on both sides (Section 3, "Second" correspondence); (3) the localization-threshold regularization with the local second-variation Fourier form, the nonlocal Fourier symbol and its expansion, and the stated conclusion that the finite horizon suppresses high-$k$ modes (Section 3, "Third" correspondence).
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction (nonlocal continuum mechanics → poromechanics localization) is genuinely asymmetric: the peridynamic community possesses the finite-horizon regularization and meshfree discretization machinery, while poromechanics lacks a regularization preserving coupled energy/dissipation structure without imposed crack geometry. The entry honestly acknowledges that hybrid FEM/peridynamic compaction-band formulations already exist, characterizing the transfer as incremental. The falsifiable prediction is specific and quantitative: a finite dominant localization wavelength at $k_*\delta = O(1)$, with explicit falsification thresholds (band-width change >10% under 4× grid refinement, or dominant wavelength outside $0.5\delta \leq \lambda_* \leq 4\delta$). Prior-art advisory: the entry self-identifies as overlapping with known peridynamic poromechanics literature and explicitly requests bibliometric validation.

#### Stage 3 Watch Items
- **Prior art (advisory, not grounds for rejection):** The pairing of peridynamics/nonlocal continuum mechanics with poromechanics is an active research area. The entry cites four ScienceDirect references and repeatedly acknowledges existing peridynamic poromechanics, nonlocal porous-flow, and hybrid FEM/peridynamic saturated compaction-band formulations. Stage 3 must determine whether the specific claim — treating the localization threshold and energy-dissipation structure as the transferable organizing object — is novel beyond these existing works.
- **Labeling precision:** The second-variation form $\delta^2\Pi \sim [H_{\rm tan}+k^2\ell_{\rm loc}^2]|\hat{\eta}(k)|^2$ is labeled as belonging to a "local softening model" in Section 3. The $k^2\ell_{\rm loc}^2$ term implies a gradient enhancement or internal-length-scale model, which is not strictly "local" in the point-wise constitutive sense. Stage 3 should verify whether this terminology is standard in the poromechanics community or represents an imprecision that could affect the novelty framing.
- **Quantitative falsification bounds:** The specific interval $0.5\delta \leq \lambda_* \leq 4\delta$ and the 10% band-width stability threshold should be checked against existing nonlocal regularization theory to determine whether these are derived predictions or arbitrarily chosen bounds.

### Seventh Adversarial Review
**Reviewer:** Microsoft Copilot 1.2
**Protocol:** v2.0  
**Verdict:** PASS  
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The Biot-type coupled equations and their variational/dissipation forms are correctly stated for quasi-static linearized poromechanics, and the nonlocal integral operators and their local-limit expansions are presented in a form consistent with state-based peridynamic formulations; there is no equation-class mismatch between the paired operators.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — Each mapped token pair (effective stress ↔ force state; Darcy flux ↔ nonlocal flux state; localization threshold ↔ horizon-regularized threshold) is a mapping between compatible mathematical object types and the Operator Role entries specify shared structure rather than hedged similarity.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed vectors are demonstrated in the body with equations or operator identities: (1) the coupled force-balance/mass-balance operator pair is shown in the local and nonlocal forms with explicit local-limit statements (Section 3, operator pair and limits); (2) the energy–dissipation stationarity structure is given for both local and nonlocal systems with explicit variational derivatives and dissipative quadratic forms (Section 3, \\(\\Pi,\\mathcal D\\) and \\(\\Pi_\\delta,\\mathcal D_\\delta\\)); (3) the localization-threshold regularization is supported by the second-variation Fourier-mode expression and the nonlocal Fourier symbol expansion (Section 3, second-variation and \\(\\widehat{\\mathcal L_\\delta}(k)\\) expansion).
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction (nonlocal continuum mechanics → poromechanics) is plausibly asymmetric and justified; the entry provides a concrete, measurable falsification criterion (grid refinement and wavelength interval test) rather than a non-specific claim. Prior-art recognition is noted in the entry and should be checked at Stage 3 (advisory).

#### Stage 3 Watch Items
- Verify bibliometric novelty and whether the cited references already establish the same operator-level regularization claim.
- Inspect the assumptions and rigor behind the local-limit expansion \\(\\widehat{\\mathcal L_\\delta}(k)=C_2 k^2+O(\\delta^2 k^4)\\) and the regime of validity for \\(k\\delta\\ll1\\).
- Confirm that the nonlocal kernel \\(K_\\delta\\) and energy density \\(W_\\delta\\) satisfy the positivity/coercivity conditions required for the second-variation arguments and the suppression of high-k modes.
- Review the proposed numerical falsification protocol for practical feasibility: how \\(\\delta\\) is held fixed relative to mesh refinement, the definition and measurement of band width, and the choice of the 10% threshold.

### Eighth Adversarial Review
**Reviewer:** xAI Grok 4.5 Fast
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The Biot-type equilibrium and mass-balance operators, the associated energy/dissipation pair, the state-based force-balance integral, the nonlocal flux integral, and the Fourier second-variation symbols are consistent with the claimed quasi-static saturated poromechanics and finite-horizon nonlocal continuum settings and jointly support the stated operator-level correspondence.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — Each paired mapping equates objects of matching mathematical type (energy-derived force densities, dissipative flux operators, and second-variation thresholds) and the Operator Role statements identify the shared structures rather than merely asserting analogy.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed vectors (coupled force-balance/mass-balance operator pair, variational energy-dissipation stationarity pair, localization-threshold regularization by nonlocal interaction length) are demonstrated by explicit operator mappings, stationarity statements, and Fourier analysis in Section 3.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The preferred direction from nonlocal continuum mechanics to porous-media localization is asymmetrically justified by the relative maturity of horizon machinery versus the need for energy-preserving regularization; the prediction supplies a concrete wavelength interval and a quantitative refinement criterion that can fail.
#### Stage 3 Watch Items
- Confirm that the local-limit bridge and energy-equivalence statements for the nonlocal operators are not overstated relative to the cited peridynamic-poromechanics literature already flagged by the entry itself.

### Ninth Adversarial Review
**Reviewer:** Meta Muse Spark 1.1
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Silo A equations are standard linearized saturated quasi-static Biot: elliptic equilibrium -∇·[C:ε(u)-αpI]=f and parabolic mass balance S ṗ+α ε̇_v-∇·(k/μ ∇p)=q; Silo B equations are recognizable state-based peridynamic forms N_δ and Q_δ with correct integral operators; the claimed local-limit bridge lim_{δ→0} N_δ = -∇·σ and lim_{δ→0} Q_δ = -∇·(k/μ ∇p) preserves operator class under stated linearized restriction, with no elliptic/parabolic vs hyperbolic/dispersive or linear vs nonlinear mismatch.[u][p]
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All three pairs are type-compatible: (effective stress/pore-pressure coupling ↔ effective force state/nonlocal deformation state) both described as energy-derivatives entering equilibrium operator; (Darcy mass flux ↔ nonlocal flux state) both dissipative flux operators with explicit local-limit convergence; (localization/softening threshold ↔ horizon-regularized threshold) both defined via loss of positive-definiteness of second variation; no spatial-domain↔time-point, rate↔position, or dimensional↔dimensionless category errors, and Operator Role statements specify shared structure rather than hedged analogy.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed vectors are demonstrated in Section 3: coupled_force-balance_and_mass-balance_operator_pair via explicit mapping (-∇·σ, -∇·k/μ ∇p) ↔ (N_δ, Q_δ) plus limit identities; variational_energy-dissipation_stationarity_pair via Pi, D and Pi_δ, D_δ with δ_u Pi=0, D≥0 ↔ δ_u Pi_δ=0, D_δ≥0; localization_threshold_regularized_by_nonlocal_interaction_length via Fourier forms δ²Pi ~ [H_tan + k² l_loc²]|η̂|², threshold H_tan+k²l_loc²=0, and nonlocal symbol \hat L_δ(k)=2∫K[1-cos(k·ξ)]dξ = C₂k²+O(δ²k⁴). No speculative hedging in body.
- **CHECK 4 (Transfer and Falsifiability):** PASS — (a) Asymmetry: Nonlocal → porous-media-flow is justified by finite-horizon integral, meshfree, stabilization, and horizon/local-limit machinery lacking in local poromechanics for coupled localization, not backwards; (b) Falsifiability: predicts finite dominant wavelength with k_*δ=O(1) vs no intrinsic wavelength locally, with concrete falsification if after 4x grid refinement at fixed δ band width changes >10% or λ_* fails 0.5δ ≤ λ_* ≤ 4δ; this is measurable threshold beyond template non-prediction; (c) Prior art advisory: no textbook-canonical analogy recognized; direct peridynamic poromechanics literature exists but is noted by entry itself as requiring Stage 3 bibliometric validation.

#### Stage 3 Watch Items
- Bibliometric novelty validation required: entry cites existing peridynamic porous-media flow and poromechanics formulations (ScienceDirect 2013 pressure-driven transport, 2020 effective force state, 2021 unified non-local transport for heterogeneous saturated media, 2025 hybrid FEM/Peridynamic compaction-band) and explicitly states novelty is uncertain — verify whether energy-dissipation and localization-threshold regularization framing is distinct from those direct formulations.
- None other identified for mathematics; equations and vocabulary are internally consistent under stated linearized, saturated, quasi-static, local-limit restriction.