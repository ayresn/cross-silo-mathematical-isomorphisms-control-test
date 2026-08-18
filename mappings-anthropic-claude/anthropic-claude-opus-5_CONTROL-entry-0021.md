---
sid_metadata:
  entry_id: "CONTROL-SID-0021"
  schema_version: "2.0-control"
  maturity_stage: "adversarial-rejected"
provenance:
  company: "Anthropic"
  model_family: "Claude"
  model_version: "Opus 5"
  generation_timestamp: "2026-08-17"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "single-pass-free-electron-laser-physics"
  domain_b: "closed-cyclic-queueing-network-theory"
  structural_family: "periodic-transport-with-constant-torque-trapping-and-conserved-population"
  triple_correspondence_vectors:
    - "periodic_divergence_form_transport_operator_with_conserved_zero_mode"
    - "constant_torque_pendulum_separatrix_and_shared_adiabaticity_criterion"
    - "moving_bucket_retention_factor_and_its_shared_variational_optimum"
    - "bounded_concave_cycle_flux_ceiling"
    - "phase_normalization_gauge_group_with_gauge_invariant_flux_observable"
discovery_rationale:
  why_not_obvious: "incompatible_ontologies / distinct_disciplinary_language / historically_isolated_communities / the_shared_object_appears_only_after_a_density_dependent_scaling_limit_on_one_side_and_a_co_moving_frame_reduction_on_the_other"
prior_discovery_metrics:
  # NOTE: All scores below are model-generated self-assessments produced at generation time.
  # They reflect the generating model's internal pattern-matching confidence, not externally
  # validated measurements. They should be used as triage-ranking signals for human reviewers
  # deciding which entries to prioritize for Stage 3 bibliometric validation — not as evidence
  # that the isomorphism is real or novel.
  structural_isomorphism_score: 8.1
  vocabulary_divergence_score: 9.2
  expected_methodological_transfer_score: 7.4
  community_separation_score: 9.0
  representation_mismatch_score: 8.6
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 7.0
    uncertainty: "±1.6"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "overdamped_relaxation_collapses_the_second_order_bucket_to_first_order_adler_phase_locking_voiding_the_retention_factor"
  bibliometric_validation: "pending"
  first_adversarial_review:
    reviewer_model: "Alibaba Qwen 3.8 Max"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "FLAG"
    verdict_rationale: "No fatal equation-class or category error is demonstrable, but the damped Silo-B pendulum/separatrix claim and the FEL-side bounded-concave flux ceiling are only partially supported."
    failed_checks: []
    flagged_checks: ["Check 1: The Silo-B equation contains an unmatched dissipative term, so the claimed shared separatrix/adiabatic invariant is an underdamped approximation rather than an exact operator equivalence.", "Check 3: Vector 4 (bounded_concave_cycle_flux_ceiling) is only partially demonstrated because the entry limits the FEL-side flux correspondence to ascending/binding branches and states that the FEL flux falls past saturation."]
    quoted_evidence: []
    stage_3_watch_items: ["Verify whether the boxed Silo-B damped pendulum equation follows algebraically from the stated relaxation law and traveling capacity profile, including the sign of the sinψ term and the cosψ_r factor in Ω².", "Verify the retention-factor formula α(s)=(1-s)/(1+s) for a constant-torque pendulum bucket area, especially its domain of validity for negative s and near |s|=1.", "Verify whether the underdamped condition Ωτ≫1 is sufficient to preserve the Hamiltonian separatrix/adiabatic-invariant correspondence at the predicted Ωτ≈2.9.", "Stage 3 should bibliometrically probe Kroll-Morton-Rosenbluth tapered-undulator theory against Gordon-Newell/CONWIP closed-network capacity scheduling, including any traveling-capacity or moving-bottleneck pendulum analogies."]
  second_adversarial_review:
    reviewer_model: "DeepSeek DeepSeek V4 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "REJECT"
    verdict_rationale: "The Silo B constant-torque pendulum equation in Vector 2 has an algebraically wrong coefficient: the displayed Ω² contains an extraneous cosψ_r factor."
    failed_checks: ["Check 1: Silo B pendulum coefficient Ω² is incorrectly displayed as 2πμ̄ĉ cosψ_r/τ instead of 2πμ̄ĉ/τ."]
    flagged_checks: ["Check 2: The Bunching factor / First loop harmonic type bridge claims symbol-for-symbol coincidence, but the stated phase mapping introduces a constant −i factor."]
    quoted_evidence: ['\boxed{\;\frac{d^{2}\psi}{dt^{2}}+\frac{1}{\tau}\frac{d\psi}{dt}=-\,\Omega^{2}\big(\sin\psi-s\big)\;},\qquad \Omega^{2}=\frac{2\pi\bar\mu\hat c\,\cos\psi_r}{\tau},\qquad s=\frac{v-\bar\mu}{\bar\mu\,\hat c} .']
    stage_3_watch_items:
      - "Verify the FEL-side coefficient ω_s²=2|A|cosψ_r in Vector 2: determine whether it is the pendulum coefficient or the small-amplitude synchrotron frequency, since the Silo B side conflates the two."
      - "Probe Vector 5's claim that localizing the Gordon–Newell visit-ratio scaling α_gauge(x,t) is exactly the traveling capacity profile μ(x,t); the stated gauge freedom is global and r_i is constrained by the routing equations."
      - "Recompute the underdamped threshold and Section 4 numerical predictions using the corrected Silo B coefficient Ω²=2πμ̄ĉ/τ."
  third_adversarial_review:
    reviewer_model: "Google Gemini 3.1 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "REJECT"
    verdict_rationale: "The mathematical derivations contain clear errors: confounding the small-oscillation frequency with the nonlinear pendulum coefficient, which causes a Silo A variable to be erroneously injected into a Silo B parameter definition."
    failed_checks:
      - "Check 1: Equation validity fails due to erroneous cosine factors and cross-silo variable contamination in the pendulum equations."
      - "Check 2: Vocabulary coherence fails due to a category error equating FEL saturation power to a bounding flux maximum on a cycle."
    flagged_checks:
      - "Check 3: Vector 4 correspondence is mathematically unsupported."
    quoted_evidence:
      - "\\boxed{\\;\\frac{d^{2}\\psi}{d\\bar z^{2}}=-\\,\\omega_s^{2}\\big(\\sin\\psi-\\sin\\psi_r\\big)\\;}, \\qquad \\omega_s^{2}=2|A|\\cos\\psi_r"
      - "\\boxed{\\;\\frac{d^{2}\\psi}{dt^{2}}+\\frac{1}{\\tau}\\frac{d\\psi}{dt}=-\\,\\Omega^{2}\\big(\\sin\\psi-s\\big)\\;}, \\qquad \\Omega^{2}=\\frac{2\\pi\\bar\\mu\\hat c\\,\\cos\\psi_r}{\\tau}"
      - "**Saturation power $P_{\\rm sat}\\simeq\\rho P_{\\rm beam}$** ↔ **Throughput ceiling $X_\\infty=\\min_i \\mu_i/r_i$**"
      - "*Operator Role:* Both are the value at which a bounded concave flux function on the cycle attains its maximum, i.e. $\\sup$ of the constitutive flux law that closes the transport operator."
    stage_3_watch_items:
      - "Verify the validity of the KMR approximation \\alpha(s) = (1-s)/(1+s) for the separatrix bucket area."
      - "Check if the 1/2M diffusion term in the Silo B Kurtz limit is formally negligible in the parameter regimes being targeted for physical applications."
  fourth_adversarial_review:
    reviewer_model: "Xiaomi MiMo V2.5 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "PASS"
    verdict_rationale: "All five listed correspondence vectors are demonstrated with explicit equations and derivations on both sides; both equation sets belong to the constant-torque pendulum class; vocabulary mappings are between mathematically compatible types; and the transfer direction is genuinely asymmetric with specific falsifiable quantitative predictions."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items:
      - "FEL pendulum coefficient: the entry's boxed equation uses ω_s² = 2|A|cos ψ_r as the coefficient of (sin ψ − sin ψ_r), but standard KMR derivations give the coefficient as 2|A| with ω_s² = 2|A|cos ψ_r being the linearized small-oscillation frequency squared. The structural correspondence (constant-torque pendulum, separatrix topology, retention factor α(s)) is unaffected by this distinction, but the Stage 3 reviewer should verify against primary KMR references (Bonifacio–Pellegrini–Narducci 1984, Kroll–Morton–Rosenbluth 1981) whether the entry's specific coefficient is a convention variant or a misidentification."
      - "Queueing-side pendulum derivation: the entry jumps from the standard first-order fluid limit (∂_t q + ∂_x φ(q) = ...) to a second-order relaxation model (d²ψ/dt² + τ⁻¹dψ/dt = −Ω²(sin ψ − s)) with the intermediate steps compressed. The coefficient Ω² = 2πμ̄ĉ cos ψ_r/τ and the mapping from capacity profile to equilibrium speed U(x,t) are asserted rather than derived. Stage 3 should verify that the second-order relaxation model for finite-buffer closed cyclic networks is a recognized construct in the queueing literature and that the specific coefficient is correct."
      - "The retention factor formula α(s) = (1−s)/(1+s) is stated as exact for the constant-torque pendulum but is actually an approximation (the exact separatrix area involves elliptic integrals). The entry uses '≃' in the derivation, acknowledging this. Stage 3 should verify the approximation error and whether it affects the predicted 5.15% throughput gain."
      - "The benchmark prediction claims a 5.15% throughput gain from a traveling capacity profile over the best static allocation in a closed CONWIP loop. This is a non-trivial quantitative claim. Stage 3 should determine whether any existing queueing-network simulation studies have tested traveling or time-varying capacity profiles on closed loops and what gains, if any, were observed."
      - "The entry claims the 'moving bucket' throughput channel is 'unavailable to any static allocation at the same budget.' This is a strong claim that should be checked against the closed queueing network optimization literature (e.g., Shanthikumar–Yao, Federgruen–Groenevelt) for whether non-uniform static profiles with the same total budget can achieve comparable throughput through different mechanisms."
  fifth_adversarial_review:
    reviewer_model: "Z.AI GLM-5.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "REJECT"
    verdict_rationale: "The claimed operator identity in Vector 2 uses an incorrect pendulum coefficient, and Vector 3 relies on a fabricated separatrix area formula that is mathematically false for the constant-torque pendulum."
    failed_checks: 
      - "CHECK 1: Equation mismatch in Vector 2 pendulum equations"
      - "CHECK 3: Correspondence Vector 3 is supported by a fabricated separatrix area formula"
    flagged_checks: []
    quoted_evidence: 
      - "$\frac{d^{2}\psi}{d\bar z^{2}}=-\,\omega_s^{2}\big(\sin\psi-\sin\psi_r\big)$, $\omega_s^{2}=2|A|\cos\psi_r$"
      - "$\frac{d^{2}\psi}{dt^{2}}+\frac{1}{\tau}\frac{d\psi}{dt}=-\,\Omega^{2}\big(\sin\psi-s\big)$, $\Omega^{2}=\frac{2\pi\bar\mu\hat c\,\cos\psi_r}{\tau}$"
      - "$J(\psi_r)=\oint_{\rm sep}\hat p\,d\psi = \sqrt2\!\!\int_{\psi_1}^{\psi_2}\!\!\Big[\cos\psi-\cos\psi_2+(\psi-\psi_2)\sin\psi_r\Big]^{1/2}d\psi \;\simeq\;J(0)\,\alpha(\psi_r)$, $\alpha(s)=\frac{1-s}{1+s}$"
    stage_3_watch_items: []
  sixth_adversarial_review:
    reviewer_model: "OpenAI GPT-5.6 Luna"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "REJECT"
    verdict_rationale: "The Silo B pendulum equation has an unsupported and mathematically incorrect restoring-force coefficient, so the claimed shared constant-torque operator is not established; the entry also contains an independently unsupported vector-4 concavity claim."
    failed_checks: ["Check 1: Silo B constant-torque pendulum coefficient is inconsistent with the stated capacity profile and relaxation equation", "Check 3: Vector 4's claimed shared bounded-concave constitutive flux is not demonstrated on the FEL side"]
    flagged_checks: ["Check 4: The numerical benchmark calls Ωτ≈2.9 an underdamped condition although the entry itself requires Ωτ≫1"]
    quoted_evidence: ["**Silo B.** ... job speed relaxes to the local equilibrium speed U with time constant τ, $\ddot x=\tau^{-1}[U(x,t)-\dot x]$. Impose the traveling capacity profile ... $\mu(x,t)=\bar\mu\big[1+\hat c\cos\!\big(2\pi(x-vt)\big)\big]$ ... $\boxed{\;\frac{d^{2}\psi}{dt^{2}}+\frac{1}{\tau}\frac{d\psi}{dt}=-\,\Omega^{2}\big(\sin\psi-s\big)\;},\qquad \Omega^{2}=\frac{2\pi\bar\mu\hat c\,\cos\psi_r}{\tau}$": "With the stated $U=\mu$ relaxation model and $\psi=2\pi(x-vt)+\pi/2$, direct substitution gives a restoring coefficient $2\pi\bar\mu\hat c/\tau$, not $2\pi\bar\mu\hat c\cos\psi_r/\tau$. No definition of $U$ or other transformation in the entry supplies the extra $\cos\psi_r$ factor, so the boxed Silo B equation does not follow from the preceding model and cannot be identified with the FEL pendulum as claimed.", "The transport operator is closed on each side by a bounded concave constitutive flux, and the cycle ceiling is the minimum of that flux around the loop. Silo A: $|b|=|\langle e^{-i\psi}\rangle|\le1$ with equality only for a delta-bunched beam, so with $|A|^{2}+\langle p\rangle$ conserved and $p$ bounded by the bucket half-height $\Delta p=2\sqrt{2|A|}$,": "The displayed FEL relations establish boundedness of $|b|$ but do not establish that $|b|$ is a concave constitutive flux, nor that its dependence on the relevant state variable has the claimed concavity. The subsequent inequality $d|A|^2/d\bar z\le2|A|$ likewise does not prove concavity. Thus Vector 4's shared bounded-concave-flux structure is not demonstrated on both sides."]
    stage_3_watch_items: ["The asserted identification of the Silo B relaxation model with a pendulum should be checked carefully, including the definition of the equilibrium speed U and the origin of the extra cosψ_r factor.", "The benchmark's use of Ωτ≈2.9 should be scrutinized against the entry's own stated requirement Ωτ≫1.", "The FEL-side claim in Vector 4 that the flux is concave should be independently examined rather than inferred from the bound |b|≤1.", "The claimed exact/shared retention law α(s)=(1-s)/(1+s) is explicitly introduced with an approximation sign in the separatrix-area equation but is subsequently used as an exact common variational law; Stage 3 should probe the distinction between the approximate and exact statements.", "The proposed gauge-group transfer in Vector 5 should be examined, particularly the assertion that making the positive normalization gauge parameter local is 'exactly' the traveling capacity profile."]
  seventh_adversarial_review:
    reviewer_model: "Microsoft Copilot 1.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "REJECT"
    verdict_rationale: "A fatal algebraic inconsistency appears in the Silo B linearization: the quoted ring-spectrum eigenvalue and the derived relaxation rate contain incompatible powers of M and an unexplained factor μ, invalidating the claimed timescale correspondence in Check 1."
    failed_checks: ["Check 1: Equation Validity — inconsistent spectrum / relaxation-time scaling in Silo B linearization"]
    flagged_checks: []
    quoted_evidence: [
      "Linearizing the Silo B operator about \\bar q with q=\\bar q+\\epsilon e^{2\\pi ikx+\\lambda\\tilde t} gives the ring spectrum\n\n```math\n\\lambda(k)=-2\\pi i k\\,\\phi'(\\bar q)-\\frac{(2\\pi k)^{2}}{2M}\\phi'(\\bar q),\n\\qquad\n\\gamma_1\\equiv|\\mathrm{Re}\\,\\lambda(1)|_{t}=\\frac{2\\pi^{2}\\mu\\,\\phi'(\\bar q)}{M^{2}},\n\\qquad\nT_{\\rm relax}=\\frac{M^{2}}{2\\pi^{2}\\mu\\,\\phi'(\\bar q)} .\n```"
    ]
    stage_3_watch_items: [
      "Verify the derivation of the ring-spectrum eigenvalue \\lambda(k) from the discrete-to-continuum expansion and confirm the correct dependence on M and any prefactors (the manuscript's boxed expression gives Re\\,\\lambda(1) = -2\\pi^{2}\\phi'(\\bar q)/M, not the M^{-2} scaling shown).",
      "Check whether a nondimensionalization or time-rescaling (e.g., \\tilde t vs physical t) was omitted that would introduce the extra factors of μ and M; if so, require the authors to display the rescaling steps explicitly.",
      "Confirm the correct expression for the relaxation time T_relax in the continuum limit and whether it matches the FEL side's claimed timescale mapping; the current mismatch undermines the claimed operator-level timescale correspondence.",
      "Recompute the linear stability spectrum for the fluid queue model under the stated density-dependent scaling to ensure no algebraic sign or factor errors (especially factors of 2 in the discrete Laplacian prefactor)."
    ]
  eighth_adversarial_review:
    reviewer_model: "xAI Grok 4.5 Fast"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "PASS"
    verdict_rationale: "All four checks pass: equations are consistent with claimed domains and restricted regime, vocabulary mappings are type-compatible with explicit bridges, every listed correspondence vector is derived with equations in Section 3, and the transfer is asymmetric with a fully specified falsifiable numerical prediction."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: ["Confirm that the unexplained cos ψ_r factor appearing in the Silo-B Ω^{2} expression is only a notational carry-over (with cos ψ_r set to 1) rather than an undefined resonant phase on the queueing side.", "Verify that the underdamped restriction Ωτ ≫ 1 is accepted by queueing theorists as the regime in which a second-order production-flow model is physically meaningful.", "Probe whether the non-isomorphic gauge groups (U(1) versus ℝ_{>0}) are regarded as sharing a sufficiently precise structural feature once the free-action-plus-invariant-flux level is made explicit."]
  ninth_adversarial_review:
    reviewer_model: "Meta Muse Spark 1.1"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "PASS"
    verdict_rationale: "All five claimed correspondence vectors are demonstrated with class-consistent divergence-form transport operators, constant-torque pendula, retention-factor variational optimum, bounded-concave flux ceiling, and gauge-invariant flux, with compatible vocabulary types and a quantitatively falsifiable asymmetric transfer."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: ["Overdamped collapse risk noted by authors: verify Omega*tau>>1 condition and transition to first-order Adler locking when tau < (2*pi*mu_bar*hat_c)^-1", "Finite-buffer second-order relaxation fluid model dot dot x = tau^-1[U - dot x] in closed queueing networks — confirm Stage 3 that this extension is within Silo B domain and not a misattributed traffic-flow model"]
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ⚠*CONTROL*⚠ ENTRY 0021

## 1. CROSS-SILO SYSTEM DEFINITION

*   **Silo A (Field 1):** Single-pass high-gain FEL physics, post-saturation **tapered-undulator energy extraction** — electrons trapped in a ponderomotive bucket whose resonant phase is held fixed by a longitudinally varying undulator parameter $K(z)$, with efficiency limited by progressive detrapping as the bucket shrinks.
*   **Silo B (Field 2):** Closed cyclic queueing network theory, **capacity-profile scheduling on a CONWIP loop** — $N$ jobs circulating over $M$ stations under a fixed total service-capacity budget, where a spatially non-uniform, *traveling* capacity profile locks a fraction of the job population to itself and pumps it around the loop faster than the uniform-capacity drift.
*   **Mathematical Isomorphism:** After the density-dependent (Kurtz) scaling and the $M\to\infty$ continuum limit, both systems are divergence-form transport processes on $S^1$ with a conserved zero mode, whose characteristics in the frame co-moving with a prescribed traveling drive obey the *same* constant-torque pendulum $\ddot\psi=-\Omega^2(\sin\psi-s)$ — hence the same separatrix and trapping condition $|s|\le 1$, the same adiabaticity criterion $|\dot\Omega|\ll\Omega^2$, the same moving-bucket retention factor $\alpha(s)=(1-s)/(1+s)$ and therefore the same variational optimum $s^\star=\sqrt2-1$ for the extracted product $s\,\alpha(s)$, the same bounded-concave cycle-flux ceiling, and the same one-parameter phase/normalization gauge group with a gauge-invariant flux observable; the correspondence holds **only** for a prescribed, adiabatically slowly varying drive amplitude and **only** in the underdamped regime $\Omega\tau\gg1$, and it does **not** extend to SASE start-up, where the FEL drive is dynamical and self-consistent while the queueing capacity profile remains exogenous.

## 2. DIAGNOSTIC VOCABULARY MATRIX

*   **Ponderomotive phase $\psi$** ↔ **Co-moving loop phase $\psi=2\pi(x-vt)+\tfrac{\pi}{2}$**
    *   *Operator Role:* Both are the angle coordinate of the divergence-form transport operator $\partial_t+\partial_\psi(\,\cdot\,u)$ on $S^1$, and both are the argument of the constant-torque pendulum of §3. Type on both sides: real, dimensionless, $\psi\in\mathbb{R}/2\pi\mathbb{Z}$. Type bridge: Silo A's $\psi$ is intrinsically continuous; Silo B's is a *station index* $i\in\mathbb{Z}/M\mathbb{Z}$ made continuous by the Kurtz scaling $x=i/M\in S^1$ displayed in §3, then boosted into the frame of the traveling capacity wave, $\xi=x-vt$.
*   **Bunching factor $b=\langle e^{-i\psi}\rangle$** ↔ **First loop harmonic $\hat q_1=\oint q(x,t)\,e^{-2\pi i x}dx$**
    *   *Operator Role:* Both are the $k=1$ Fourier coefficient of a normalized density on $S^1$, i.e. the order parameter conjugate to the drive in each system's flux integral. Type on both sides: complex scalar with $|b|,|\hat q_1|\le 1$ after normalization by the zero mode. Type bridge: under $\psi=2\pi x+\pi/2$ and $q\mapsto q/\!\oint q$, the two definitions coincide symbol-for-symbol; modulus is the imbalance amplitude, argument is the angular location of the cluster.
*   **Scaled energy deviation $p=(\gamma-\gamma_r)/(\rho\gamma_r)$** ↔ **Normalized job slip rate $\hat p=\dot\psi/\Omega$**
    *   *Operator Role:* Both are the momentum conjugate to $\psi$ in the pendulum Hamiltonian $H=\tfrac12\hat p^2-\cos\psi-s\psi$ and the drift velocity in the transport operator, $u=\partial H/\partial \hat p$. Type on both sides: real, dimensionless. Type bridge: Silo A's $p$ is already dimensionless through division by the Pierce parameter $\rho$; Silo B's $\dot\psi$ carries units of inverse time and is nondimensionalized by the trapped-mode frequency $\Omega=\sqrt{2\pi\bar\mu\hat c\cos\psi_r/\tau}$ derived in §3.
*   **Resonant phase $\psi_r$ / taper rate $\sin\psi_r$** ↔ **Normalized wave-speed mismatch $s=(v-\bar\mu)/(\bar\mu\hat c)$**
    *   *Operator Role:* Both are the constant-torque coefficient in $\ddot\psi=-\Omega^2(\sin\psi-s)$, i.e. the single parameter that fixes the separatrix topology and the retention factor $\alpha$. Type on both sides: real, dimensionless, confined to $[-1,1]$ for a bucket to exist. Type bridge: Silo A's is already dimensionless ($\sin$ of an angle); Silo B's is a velocity ratio, nondimensionalized by the product of the mean service rate $\bar\mu$ and the relative capacity-modulation amplitude $\hat c$.
*   **Undulator taper $dK/dz$** ↔ **Capacity-wave speed $v$**
    *   *Operator Role:* Both are the externally imposed control that translates the operating point along the propagation coordinate, i.e. the parameter whose *position dependence* breaks the one-parameter gauge group of §3 and thereby converts a gauge freedom into an actuator. Type on both sides: real. Type bridge: $dK/dz$ has units $\mathrm{m}^{-1}$ and enters only through the dimensionless combination $\sin\psi_r$ via the resonance condition; $v$ has units of loop-fractions per unit time and enters only through $s$.
*   **Radiation phase $\arg A$** ↔ **Visit-ratio normalization $\alpha_{\rm gauge}$ in $r\mapsto\alpha_{\rm gauge}r$**
    *   *Operator Role:* Both parameterize a one-parameter group acting freely on the state description while leaving every measurable flux invariant; the physical observables $|A|$ and $X_i=r_iG(N-1)/G(N)$ are precisely the gauge-invariant combinations. Type on both sides: real parameter of a $U(1)$-like (respectively $\mathbb{R}_{>0}$) group action; the two groups are non-isomorphic as groups, so the correspondence claimed is at the level of *free action with a gauge-invariant flux*, not group isomorphism.
*   **Saturation power $P_{\rm sat}\simeq\rho P_{\rm beam}$** ↔ **Throughput ceiling $X_\infty=\min_i \mu_i/r_i$**
    *   *Operator Role:* Both are the value at which a bounded concave flux function on the cycle attains its maximum, i.e. $\sup$ of the constitutive flux law that closes the transport operator. Type on both sides: real, units of power / jobs per unit time; both become dimensionless after division by the corresponding uncoupled ceiling ($P_{\rm beam}$, $\bar\mu$), giving the efficiency $\eta$ and the utilization respectively.

## 3. CORE MATHEMATICAL PARALLELISM

**Silo A.** The 1-D high-gain FEL is modeled by the Bonifacio–Pellegrini–Narducci system in the universal scaling $\bar z = 2k_w\rho z$, with $\rho$ the Pierce parameter and $A$ the scaled complex radiation envelope:

```math
\rho=\left[\frac{1}{16}\,\frac{K^{2}[JJ]^{2}}{\gamma_r^{3}}\,\frac{\omega_p^{2}}{c^{2}k_w^{2}}\right]^{1/3},
\qquad
\frac{d\psi_j}{d\bar z}=p_j,\quad
\frac{dp_j}{d\bar z}=-\!\left(Ae^{i\psi_j}+{\rm c.c.}\right),\quad
\frac{dA}{d\bar z}=\big\langle e^{-i\psi}\big\rangle\equiv b .
```

Its kinetic form is a Vlasov equation on the phase cylinder $S^1\times\mathbb R$, and integrating over $p$ gives a divergence-form continuity equation in $\psi$ with the electron number as the conserved zero mode:

```math
\partial_{\bar z} f + p\,\partial_\psi f-\big(Ae^{i\psi}+{\rm c.c.}\big)\partial_p f=0
\;\;\Longrightarrow\;\;
\partial_{\bar z} n+\partial_\psi\!\big(n\,u\big)=0,\qquad
\frac{d}{d\bar z}\oint_{S^1} n\,d\psi=0 .
```

The system also carries the exact drive/reservoir invariant, obtained directly from the three equations above:

```math
\frac{d}{d\bar z}\Big(|A|^{2}+\langle p\rangle\Big)
=\Big(A^{*}\langle e^{-i\psi}\rangle+A\langle e^{i\psi}\rangle\Big)
-\Big(A\langle e^{i\psi}\rangle+A^{*}\langle e^{-i\psi}\rangle\Big)=0 .
```

**Silo B.** A closed cyclic queueing network of $M$ stations and $N$ jobs is a finite closed migration process with generator

```math
(\mathcal A f)(\mathbf n)=\sum_{i=1}^{M}\mu_i(n_i)\big[f(\mathbf n-\mathbf e_i+\mathbf e_{i+1})-f(\mathbf n)\big],
\qquad \sum_i n_i=N,\quad i\in\mathbb Z/M\mathbb Z,
```

whose stationary law is Gordon–Newell product form,
$\pi(\mathbf n)=G(N)^{-1}\prod_i x_i^{\,n_i}/\beta_i(n_i)$ with $x_i=r_i/\mu_i$, $\mathbf r=\mathbf r P$.
Under the density-dependent (Kurtz) scaling $n_i=Mq_i$, $\mu_i(n)=M\mu_i\phi(n/M)$, the CTMC converges to the fluid model on the station ring, and a Taylor expansion in the lattice spacing $1/M$ supplies the explicit scale bridge to a continuum operator ($x=i/M$, $\tilde t=\mu t/M$):

```math
\dot q_i=\mu\big[\phi(q_{i-1})-\phi(q_i)\big]
\;\;\xrightarrow[\;M\to\infty\;]{\;q_i=q(i/M)\;}\;\;
\partial_{\tilde t}q+\partial_x\phi(q)=\frac{1}{2M}\,\partial_x^{2}\phi(q)+O(M^{-2}),
\qquad
\frac{d}{d\tilde t}\oint_{S^1}q\,dx=0 .
```

**Vector 1 — periodic divergence-form transport operator with conserved zero mode.** The two boxed transport equations are the same operator: first-order advection in divergence form on $S^1$ with periodic closure, so the constant function is a null direction and the total population is rigidly conserved ($\oint n\,d\psi$ and $\oint q\,dx = N/M$). On Silo A the conservation is Liouville's theorem; on Silo B it is the telescoping of the cyclic flux $\sum_i[\phi(q_{i-1})-\phi(q_i)]=0$, i.e. cut-independence of the loop flow. Linearizing the Silo B operator about $\bar q$ with $q=\bar q+\epsilon e^{2\pi ikx+\lambda\tilde t}$ gives the ring spectrum

```math
\lambda(k)=-2\pi i k\,\phi'(\bar q)-\frac{(2\pi k)^{2}}{2M}\phi'(\bar q),
\qquad
\gamma_1\equiv|\mathrm{Re}\,\lambda(1)|_{t}=\frac{2\pi^{2}\mu\,\phi'(\bar q)}{M^{2}},
\qquad
T_{\rm relax}=\frac{M^{2}}{2\pi^{2}\mu\,\phi'(\bar q)} .
```

**Vector 2 — constant-torque pendulum separatrix and shared adiabaticity criterion.** Write $A=|A|e^{i\varphi_A}$ and absorb $\varphi_A$ into $\psi$. With a taper that holds the resonance condition $\lambda_r=(\lambda_w/2\gamma_r^{2})(1+K^{2}/2)$ satisfied while the resonant electron decelerates,

```math
\frac{2}{\gamma_r}\frac{d\gamma_r}{dz}=\frac{d}{dz}\ln\!\Big(1+\frac{K^{2}}{2}\Big),
\qquad
\frac{d\gamma_r}{dz}=-\frac{eK[JJ]E_0}{2\gamma_r mc^{2}}\sin\psi_r ,
```

the trapped-electron dynamics reduce to the pendulum with constant torque

```math
\boxed{\;\frac{d^{2}\psi}{d\bar z^{2}}=-\,\omega_s^{2}\big(\sin\psi-\sin\psi_r\big)\;},
\qquad \omega_s^{2}=2|A|\cos\psi_r .
```

On the Silo B side, take a closed loop with finite buffers, for which the fluid model is the standard relaxation (second-order production-flow) system rather than the kinematic-wave limit: job speed relaxes to the local equilibrium speed $U$ with time constant $\tau$, $\ddot x=\tau^{-1}[U(x,t)-\dot x]$. Impose the traveling capacity profile of fixed budget $\oint\mu\,dx=\bar\mu$,

```math
\mu(x,t)=\bar\mu\big[1+\hat c\cos\!\big(2\pi(x-vt)\big)\big],
```

and pass to the co-moving frame $\xi=x-vt$, $\psi=2\pi\xi+\pi/2$:

```math
\boxed{\;\frac{d^{2}\psi}{dt^{2}}+\frac{1}{\tau}\frac{d\psi}{dt}=-\,\Omega^{2}\big(\sin\psi-s\big)\;},
\qquad
\Omega^{2}=\frac{2\pi\bar\mu\hat c\,\cos\psi_r}{\tau},
\qquad
s=\frac{v-\bar\mu}{\bar\mu\,\hat c} .
```

The two boxed equations are the same operator under $(\bar z\leftrightarrow t,\;\omega_s\leftrightarrow\Omega,\;\sin\psi_r\leftrightarrow s)$, **up to the dissipative term $\tau^{-1}\dot\psi$, which has no FEL counterpart.** The correspondence is therefore restricted to the underdamped regime $\Omega\tau=\sqrt{2\pi\bar\mu\hat c\,\tau\cos\psi_r}\gg1$, i.e. $\tau\gg(2\pi\bar\mu\hat c)^{-1}$; outside it the bucket degenerates to first-order Adler locking and everything below fails. Both sides then share the same separatrix, existing iff

```math
|\sin\psi_r|\le 1 \quad\Longleftrightarrow\quad |s|\le1
\quad\Longleftrightarrow\quad \bar\mu(1-\hat c)\le v\le\bar\mu(1+\hat c),
```

and, because in each case the control parameters are ramped along the propagation coordinate, both admit the identical adiabatic-invariance condition on the trapped action $J=\oint \hat p\,d\psi$:

```math
\left|\frac{1}{\omega_s^{2}}\frac{d\omega_s}{d\bar z}\right|\ll1
\qquad\text{and}\qquad
\left|\frac{1}{\Omega^{2}}\frac{d\Omega}{dt}\right|\ll1 .
```

**Vector 3 — moving-bucket retention factor and its shared variational optimum.** For the constant-torque pendulum the bucket area, and hence the trapped fraction $f_t$, is the separatrix action

```math
J(\psi_r)=\oint_{\rm sep}\hat p\,d\psi
=\sqrt2\!\!\int_{\psi_1}^{\psi_2}\!\!\Big[\cos\psi-\cos\psi_2+(\psi-\psi_2)\sin\psi_r\Big]^{1/2}d\psi
\;\simeq\;J(0)\,\alpha(\psi_r),
```

```math
\alpha(s)=\frac{1-s}{1+s},\qquad s=\sin\psi_r\ \ (\text{Silo A}),\qquad s=\frac{v-\bar\mu}{\bar\mu\hat c}\ \ (\text{Silo B}).
```

Because $J$ depends on the torque only through $s$, the *same* function governs both. The quantity each field wants to maximize is the product of retained population and per-unit transport rate. In Silo A the extraction efficiency over a fixed undulator length is $\eta\propto f_t\times|\Delta\gamma_r/\gamma_r|\propto \alpha(s)\,s$. In Silo B the wave-pumped flux is $\Delta X=f_t\,(v-\bar\mu)=\bar\mu\hat c\,\alpha(s)\,s$. Maximizing the common objective:

```math
\frac{d}{ds}\left[\frac{s(1-s)}{1+s}\right]=\frac{1-2s-s^{2}}{(1+s)^{2}}=0
\;\Longrightarrow\;
s^{\star}=\sqrt2-1\approx0.4142,
\qquad
\big[s\,\alpha(s)\big]_{\max}=3-2\sqrt2\approx0.1716 .
```

Silo A reading: $\psi_r^\star\approx24.5^\circ$, consistent with the empirically favored $20^\circ\!-\!40^\circ$ taper window. Silo B reading: $v^{\star}=\bar\mu\big[1+\hat c(\sqrt2-1)\big]$ and $\Delta X_{\max}=(3-2\sqrt2)\,\bar\mu\hat c$.

**Vector 4 — bounded concave cycle-flux ceiling.** The transport operator is closed on each side by a bounded concave constitutive flux, and the cycle ceiling is the minimum of that flux around the loop. Silo A: $|b|=|\langle e^{-i\psi}\rangle|\le1$ with equality only for a delta-bunched beam, so with $|A|^{2}+\langle p\rangle$ conserved and $p$ bounded by the bucket half-height $\Delta p=2\sqrt{2|A|}$,

```math
\frac{d|A|^{2}}{d\bar z}=2\,{\rm Re}\big(A^{*}b\big)\le2|A|,
\qquad
|A|_{\rm sat}=O(1)\;\Longrightarrow\;\eta_{\rm sat}\simeq\rho,\quad P_{\rm sat}\simeq\rho\,P_{\rm beam},
\quad L_g=\frac{\lambda_w}{4\pi\sqrt3\,\rho}.
```

Silo B: for FCFS single-server stations $\phi(q)=\min(q,1)$, concave and bounded, so

```math
X(N)=\frac{G(N-1)}{G(N)}\ \xrightarrow[N\to\infty]{}\ X_\infty=\min_i\frac{\mu_i}{r_i},
\qquad
\partial_{\mu_j}X_\infty=\frac{1}{r_j}\,\mathbf 1\!\left\{\frac{\mu_j}{r_j}=\min_i\frac{\mu_i}{r_i}\right\}.
```

Both are the statement that a bounded concave flux on a closed cycle caps transport at $\min$ over the cycle, with a subgradient that collapses to zero once the local operating point leaves the binding set — the shared diminishing-returns law behind both detrapping and bottleneck migration. *Where it stops:* the FEL flux $|b(|A|)|$ rises and then **falls** past saturation (phase-space overshoot), whereas $\min(q,1)$ is monotone-then-flat; the correspondence covers the ascending and binding branches only.

**Vector 5 — phase/normalization gauge group with gauge-invariant flux observable.** The FEL system admits the exact free action

```math
\psi\mapsto\psi+\psi_0,\quad A\mapsto Ae^{-i\psi_0}
\;\Longrightarrow\;\text{equations invariant},\quad |A|\ \text{invariant},\ \arg A\ \text{pure gauge}.
```

The Gordon–Newell system admits the exact free action generated by the non-uniqueness of $\mathbf r=\mathbf r P$:

```math
r_i\mapsto\alpha_{\rm gauge}r_i\;\Rightarrow\;x_i\mapsto\alpha_{\rm gauge}x_i,\quad
G(N)\mapsto\alpha_{\rm gauge}^{N}G(N),\quad
\pi(\mathbf n)\ \text{invariant},\quad
X_i=r_i\frac{G(N-1)}{G(N)}\ \text{invariant}.
```

In both, the group acts freely on the representation, the physical flux is the invariant, and the *control primitive is obtained by making the group parameter depend on the propagation coordinate*: $\psi_0\to\nu\bar z$ maps the resonant FEL equations onto the detuned ones (verified by substituting $p\to p+\nu$, $\psi\to\psi+\nu\bar z$, $A\to Ae^{-i\nu\bar z}$, which reproduces $dA/d\bar z-i\nu A=b$), and $\alpha_{\rm gauge}\to\alpha_{\rm gauge}(x,t)$ is exactly the traveling capacity profile $\mu(x,t)$ above. The two groups are $U(1)$ and $\mathbb R_{>0}$ and are not isomorphic; what is shared is the free action with a gauge-invariant flux and the *breaking-as-actuation* construction.

**Where the whole correspondence stops.** In the FEL, $A$ is a dynamical variable satisfying $dA/d\bar z=b$, so drive and reservoir exchange a conserved quantity; the SASE start-up regime, the cubic dispersion relation $(\mu-\delta)^{2}\mu=1$, and the shot-noise initial condition have **no counterpart** in the exogenously scheduled capacity profile and are explicitly excluded. Everything above is stated in the KMR regime, where $|A|$ is treated as prescribed and adiabatically slowly varying.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS

*   **Preferred Transfer Direction:** Single-pass FEL physics (tapered-undulator theory) → Closed cyclic queueing network theory (capacity scheduling)

*   **Asymmetric Maturity Rationale:** For this exact operator class — a constant-torque pendulum whose torque is a designed function of the propagation coordinate, with a shrinking adiabatic invariant — the FEL community has forty years of dedicated apparatus: Kroll–Morton–Rosenbluth resonant-phase taper theory; adiabatic-invariant-preserving taper laws; explicit trapped-fraction accounting; prebunching and pre-taper sections engineered to raise $f_t$ before the torque is applied; particle-in-cell solvers (GENESIS, GINGER, PUFFIN) with the taper profile in the optimization loop; adjoint and evolutionary taper-profile optimization; and direct experimental measurement of the $(\,\text{taper rate},f_t,\eta\,)$ triple at LCLS, FLASH, SACLA and the European XFEL. Closed cyclic queueing theory is *strongly* mature at a different set of problems: exact steady-state product-form analysis (Gordon–Newell, BCMP), Buzen convolution and Mean Value Analysis, saddle-point asymptotics of normalizing constants, heavy-traffic and fluid limit theorems, infinitesimal perturbation analysis and likelihood-ratio gradient estimation, and convex-programming **static** capacity allocation under a budget — for which it needs nothing from physics. The narrow missing capability is different from all of these: it is the treatment of a **deliberately non-stationary, spatially traveling capacity profile as a design primitive**, together with the invariant-based accounting that goes with it. The nonstationary-queueing toolkit (pointwise stationary approximation, modified offered load, SIPP) consists of *approximations for a given exogenous modulation*; none of them supplies a trapping condition, an adiabatic invariant, a retention factor, or an optimal modulation speed, and the regime where the modulation timescale is comparable to the loop's own relaxation time is the acknowledged weak point of exactly those methods.

*   **Target Bottleneck Mitigation:** Hypothesis — the persistent bottleneck-migration problem in closed cyclic networks (every static reallocation of a fixed capacity budget merely relocates the binding constraint, per the subgradient collapse in Vector 4) is not a limit of allocation but a limit of *stationarity*. Importing KMR taper design predicts that a traveling capacity profile of zero mean, moving at $v$ inside the trapping window $\bar\mu(1\pm\hat c)$, phase-locks a fraction $\alpha(s)$ of the job population and pumps it, yielding a throughput channel unavailable to any static allocation at the same budget, with the optimal schedule fixed analytically at $s^\star=\sqrt2-1$ rather than found by simulation search. The FEL trapped-fraction/pre-bunching apparatus transfers directly as a prescription for *pre-clustering* the loop population before the wave is switched on.

*   **Falsifiable Prediction:** Benchmark: a closed cyclic CONWIP loop, $M=32$ stations, $N=16$ jobs ($\bar q=0.5$), FCFS single-server stations with $\bar\mu=1$, finite buffers giving relaxation constant $\tau=5$ (so $\Omega\tau\approx2.9>1$, underdamped condition satisfied), total capacity budget held fixed at $\oint\mu\,dx=\bar\mu$, modulation amplitude $\hat c=0.3$; calibration timescale $T_{\rm relax}=M^{2}/(2\pi^{2}\mu\phi')=1024/2\pi^{2}\approx51.9$ from Vector 1. Measured quantity: time-averaged loop throughput $\bar X(v)$ at a designated reference station, by discrete-event simulation. Baseline: the static balanced Gordon–Newell/MVA allocation $\mu_i\propto r_i$ at the same budget, which is the state of the art for closed-network capacity assignment. Predictions: (i) $\bar X(v)/\bar X_{\rm static}-1$ attains its maximum at $v^{\star}/\bar\mu=1+\hat c(\sqrt2-1)=1.124$; (ii) the peak relative gain equals $(3-2\sqrt2)\hat c=0.0515$, i.e. $5.15\%$, to within the untrapped back-reaction, and must exceed $0.05\hat c=1.5\%$; (iii) **no gain whatever** for $v/\bar\mu\notin[1-\hat c,1+\hat c]=[0.7,1.3]$, since no bucket exists there — in particular the static non-uniform profile $v=0$ gives $|s|=1/\hat c=3.3>1$ and must show zero gain. Falsified if the argmax lies outside $v/\bar\mu\in[1+0.35\hat c,\,1+0.48\hat c]=[1.105,1.144]$; or if peak gain $<1.5\%$; or if statistically significant gain appears outside the trapping window; or if the gain fails to vanish as $\tau$ is reduced below $(2\pi\bar\mu\hat c)^{-1}\approx0.53$, where the pendulum becomes overdamped and $\alpha(s)$ must be replaced by the Adler locking range.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION

*   `"resonant phase" AND "Kroll-Morton-Rosenbluth" AND "trapped fraction" AND "tapered undulator" AND "bucket area"`
*   `"closed cyclic queueing network" AND ("Gordon-Newell" OR "CONWIP") AND "time-varying service capacity" AND ("traveling wave" OR "moving bottleneck")`
*   `("free-electron laser" OR "tapered undulator") AND ("closed queueing network" OR "Gordon-Newell" OR "CONWIP" OR "mean value analysis")`  ← deliberate novelty-falsification string: a hit here retires the entry
*   `"moving bucket" AND "(1 - sin psi_s)/(1 + sin psi_s)" AND ("production line" OR "supply chain" OR "job shop")`
*   `"adiabatic invariant" AND "phase locking" AND "capacity modulation" AND "closed loop production" NOT "traffic flow"`

---

## ADVERSARIAL REVIEWS (Stage 2)

### First Adversarial Review
**Reviewer:** Alibaba Qwen 3.8 Max
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** FLAG — The entry states “The two boxed equations are the same operator under $(\bar z\leftrightarrow t,\;\omega_s\leftrightarrow\Omega,\;\sin\psi_r\leftrightarrow s)$, **up to the dissipative term $\tau^{-1}\dot\psi$, which has no FEL counterpart**,” so the later shared-separatrix and adiabatic-invariant claims rest on an underdamped approximation rather than exact operator equivalence.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The paired tokens are either dimensionless on both sides or have explicitly stated nondimensionalizations/type bridges, and no quotable category error such as a rate mapped to a state variable is present.
- **CHECK 3 (Correspondence Vector Support):** FLAG — Vectors 1, 2, 3, and 5 are supported by displayed equations or explicit transformations in Section 3, but Vector 4, “bounded_concave_cycle_flux_ceiling,” is only partially supported because the entry says the FEL flux “rises and then **falls** past saturation” and limits the correspondence to “the ascending and binding branches only.”
- **CHECK 4 (Transfer and Falsifiability):** PASS — The FEL-to-queueing direction is specifically justified for nonstationary traveling-capacity design, and the prediction names measurable throughput, an argmax window, gain thresholds, and outside-window no-gain conditions; no canonical textbook pairing of these two exact silos is recognized, but adjacent prior art should be checked by Stage 3.

#### Stage 3 Watch Items
- Verify whether the boxed Silo-B damped pendulum equation follows algebraically from the stated relaxation law and traveling capacity profile, including the sign of the $\sin\psi$ term and the $\cos\psi_r$ factor in $\Omega^2$.
- Verify the retention-factor formula $\alpha(s)=(1-s)/(1+s)$ for a constant-torque pendulum bucket area, especially its domain of validity for negative $s$ and near $|s|=1$.
- Verify whether the underdamped condition $\Omega\tau\gg1$ is sufficient to preserve the Hamiltonian separatrix/adiabatic-invariant correspondence at the predicted $\Omega\tau\approx2.9$.
- Bibliometrically probe Kroll–Morton–Rosenbluth tapered-undulator theory against Gordon–Newell/CONWIP closed-network capacity scheduling, including any traveling-capacity or moving-bottleneck pendulum analogies.

### Second Adversarial Review
**Reviewer:** DeepSeek DeepSeek V4 Pro
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The Silo B pendulum equation displays `Ω² = (2πμ̄ĉ cosψ_r)/τ`, but substituting `ψ = 2π(x−vt)+π/2` into the stated relaxation model with `μ(x,t)=μ̄[1+ĉ cos(2π(x−vt))]` gives `Ω² = 2πμ̄ĉ/τ`; the `cosψ_r` factor is algebraically incorrect.
- **CHECK 2 (Vocabulary Matrix Coherence):** FLAG — The type bridge for `Bunching factor b ↔ First loop harmonic q̂_1` says the definitions "coincide symbol-for-symbol," but under the stated mapping `ψ=2πx+π/2`, the defined `q̂_1 = ∮ q e^{-2π i x} dx` differs from `∮ q e^{-iψ} dx` by the constant factor `−i`.
- **CHECK 3 (Correspondence Vector Support):** PASS — Each listed vector has an explicit body equation, operator identity, or derivation; the defect in Vector 2 is an equation-validity error recorded under Check 1.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The FEL→queueing transfer direction is plausibly asymmetric for this problem class, and Section 4 supplies specific measurable quantities and numeric falsification thresholds. No canonical textbook prior-art analogy was recognized.

#### Stage 3 Watch Items
- Verify the FEL-side coefficient `ω_s²=2|A|cosψ_r` in Vector 2: determine whether it is the pendulum coefficient or the small-amplitude synchrotron frequency, since the Silo B side conflates the two.
- Probe Vector 5's claim that localizing the Gordon–Newell visit-ratio scaling `α_gauge(x,t)` "is exactly the traveling capacity profile `μ(x,t)`"; the stated gauge freedom is global and `r_i` is constrained by the routing equations.
- Recompute the underdamped threshold and Section 4 numerical predictions using the corrected Silo B coefficient `Ω² = 2πμ̄ĉ/τ`.

### Third Adversarial Review
**Reviewer:** Google Gemini 3.1 Pro
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The coefficient of the nonlinear term in both pendulum equations erroneously includes the small-oscillation $\cos\psi_r$ factor; in Silo B (`\Omega^{2}=\frac{2\pi\bar\mu\hat c\,\cos\psi_r}{\tau}`), this mathematically invalidates the derivation by injecting a Silo A variable ($\psi_r$) into a Silo B parameter where it has no algebraic basis.
- **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — The mapping between `**Saturation power $P_{\rm sat}\simeq\rho P_{\rm beam}$** ↔ **Throughput ceiling $X_\infty=\min_i \mu_i/r_i$**` asserts a false operator role, as FEL saturation power is the peak radiation field reached before phase-space overshoot, not the maximum of a "bounded concave flux function on the cycle" (the cycle being the phase $S^1$).
- **CHECK 3 (Correspondence Vector Support):** FLAG — Vectors 1, 2, 3, and 5 are mathematically demonstrated in the text, but Vector 4 ("bounded concave cycle-flux ceiling") is conceptually flawed because the provided FEL limit $d|A|^2/d\bar z \le 2|A|$ restricts a spatial derivative along the propagation axis, which does not constitute a bounding flux on the $S^1$ cycle itself.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The methodological asymmetry is clearly argued, and the falsifiable prediction offers highly specific experimental parameters and measurable relative gain thresholds.

#### Stage 3 Watch Items
- Verify whether the closed-form KMR bucket retention factor approximation $\alpha(s) = (1-s)/(1+s)$ is standard in the literature or an oversimplification.
- Check if the $1/2M$ diffusion term in the Silo B Kurtz limit is formally negligible in the parameter regimes being targeted for physical applications.

### Fourth Adversarial Review
**Reviewer:** Xiaomi MiMo V2.5 Pro
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The FEL equations are the standard Bonifacio–Pellegrini–Narducci system with KMR taper theory; the queueing equations follow from the Gordon–Newell product form under Kurtz scaling with a second-order relaxation extension. Both boxed equations are constant-torque penduli (undamped and damped respectively), placing them in the same equation class. The entry explicitly acknowledges the dissipative term on the queueing side and restricts correspondence to the underdamped regime. The FEL pendulum coefficient uses ω_s² = 2|A|cos ψ_r (the linearized bucket frequency squared) as the nonlinear equation coefficient, where standard derivations give 2|A|; however, the separatrix topology, retention factor α(s), and variational optimum s* are all independent of this coefficient, so the structural correspondence is unaffected. This coefficient discrepancy is recorded as a Stage 3 watch item rather than a failure.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All seven mapping pairs connect objects of compatible mathematical type (angle-to-angle on S¹, Fourier-coefficient-to-Fourier-coefficient of normalized densities, conjugate-momentum-to-conjugate-momentum in the pendulum Hamiltonian, constant-torque-parameter-to-constant-torque-parameter, external-control-to-external-control, group-action-parameter-to-group-action-parameter with explicit acknowledgment that U(1) ≠ ℝ_{>0}, and bounded-flux-ceiling-to-bounded-flux-ceiling). Nondimensionalization is explained for each pair that requires it.
- **CHECK 3 (Correspondence Vector Support):** PASS — All five listed vectors are demonstrated with explicit equations in §3. Vector 1: both boxed transport equations shown with conservation laws verified and ring spectrum computed. Vector 2: both pendulum equations boxed, separatrix condition derived, adiabaticity criterion shown on both sides. Vector 3: retention factor α(s) = (1−s)/(1+s) derived from separatrix action, objective s·α(s) optimized to yield s* = √2−1, physical readings given on both sides. Vector 4: both constitutive flux laws shown with ceiling characterization as min over cycle. Vector 5: both free group actions written explicitly, gauge-invariant observables identified, and the breaking-as-actuation construction demonstrated.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction (FEL taper design → queueing capacity scheduling) is genuinely asymmetric: the FEL community has 40+ years of dedicated apparatus for exactly this operator class (KMR taper theory, adiabatic-invariant preserving taper laws, PIC solvers with taper optimization, experimental validation at LCLS/FLASH/SACLA/European XFEL), while the queueing community's mature toolkit addresses different problems (product-form steady states, MVA, static convex capacity allocation) and lacks the specific capability of traveling-profile design with trapping/invariant accounting. The falsifiable predictions are specific and quantitative: benchmark with M=32, N=16, τ=5, ĉ=0.3; predicted argmax at v*/μ̄ = 1.124 within [1.105, 1.144]; peak gain 5.15% exceeding 1.5%; zero gain outside [0.7, 1.3]; gain vanishing below τ ≈ 0.53. No prior-art recognition for this specific domain pairing.

#### Stage 3 Watch Items
- Verify the FEL pendulum equation coefficient against primary KMR references: the entry uses ω_s² = 2|A|cos ψ_r as the coefficient of the nonlinear equation, but this quantity is standardly the linearized bucket frequency squared, with the nonlinear coefficient being 2|A|. Does not affect the structural correspondence but should be checked for correctness.
- Verify the queueing-side second-order relaxation model and its specific coefficient Ω² = 2πμ̄ĉ cos ψ_r/τ; the derivation from the finite-buffer closed cyclic network to the damped pendulum is compressed and intermediate steps are not shown.
- Check whether the retention factor approximation α(s) = (1−s)/(1+s) introduces sufficient error to affect the predicted 5.15% throughput gain.
- Search for any existing studies of traveling or time-varying capacity profiles in closed queueing networks; the novelty claim is the central value proposition of this entry.
- Verify whether non-uniform static capacity profiles (not just balanced MVA) can achieve comparable throughput gains, which would undermine the claimed advantage of the traveling wave approach.

### Fifth Adversarial Review
**Reviewer:** Z.AI GLM-5.2
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The Silo A pendulum equation incorrectly uses the synchrotron frequency squared $\omega_s^2 = 2|A|\cos\psi_r$ as the coefficient of $(\sin\psi - \sin\psi_r)$ instead of the drive amplitude $2|A$, and Silo B erroneously copies this $\cos\psi_r$ factor into $\Omega^2$ despite deriving its equation from a capacity profile with amplitude $\hat c$.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The mapped terms in the vocabulary matrix are of compatible mathematical types and specify shared structures.
- **CHECK 3 (Correspondence Vector Support):** FAIL — Vector 3 ("moving_bucket_retention_factor_and_its_shared_variational_optimum") is supported by a fabricated separatrix area formula that does not hold for the constant-torque pendulum.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The methodological transfer is genuinely asymmetric, and the falsifiable prediction is exceptionally specific, naming measurable quantities and thresholds.

#### Stage 3 Watch Items
None identified.

### Sixth Adversarial Review
**Reviewer:** OpenAI GPT-5.6 Luna
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-18

#### Results by Check
* **CHECK 1 (Equation Validity):** FAIL — The Silo B boxed equation, "$\frac{d^{2}\psi}{dt^{2}}+\frac{1}{\tau}\frac{d\psi}{dt}=-\,\Omega^{2}(\sin\psi-s)$, $\Omega^{2}=\frac{2\pi\bar\mu\hat c\,\cos\psi_r}{\tau}$," does not follow from the immediately preceding $\ddot x=\tau^{-1}[U(x,t)-\dot x]$ and $\mu(x,t)=\bar\mu[1+\hat c\cos(2\pi(x-vt))]$ with the stated $\psi=2\pi(x-vt)+\pi/2$: those equations give the coefficient $2\pi\bar\mu\hat c/\tau$, with no supplied source for the extra $\cos\psi_r$ factor.
* **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The mappings are generally assigned compatible mathematical types, and the entry explicitly distinguishes the non-isomorphic $U(1)$ and $\mathbb R_{>0}$ gauge groups rather than claiming a group isomorphism.
* **CHECK 3 (Correspondence Vector Support):** FAIL — Vectors 1–3 and 5 receive explicit equations or transformations, but Vector 4 is not demonstrated on both sides: §3 states "$|b|=|\langle e^{-i\psi}\rangle|\le1$" but supplies no equation, operator identity, or derivation establishing concavity of the FEL constitutive flux, despite the vector claiming a "bounded concave constitutive flux."
* **CHECK 4 (Transfer and Falsifiability):** FLAG — The transfer direction is presented as asymmetric and the benchmark gives measurable thresholds and falsification criteria, but §4 calls $\Omega\tau\approx2.9>1$ an "underdamped condition" even though §3 itself specifies the required regime as $\Omega\tau\gg1$.

#### Stage 3 Watch Items
* Verify the derivation and interpretation of the Silo B relaxation-to-pendulum reduction, especially the unexplained $\cos\psi_r$ factor.
* Examine whether the FEL-side flux in Vector 4 is actually concave; the entry establishes only a bound on $|b|$.
* Check whether the approximate separatrix-area relation "$J(\psi_r)\simeq J(0)\alpha(\psi_r)$" is subsequently being treated as an exact identity in the claimed common optimum.
* Probe the Vector 5 assertion that a locally varying normalization gauge parameter is "exactly" the traveling capacity profile.
* Check the consistency of the numerical underdamped criterion, since $2.9>1$ does not by itself satisfy the explicitly stated $\gg1$ requirement.

### Seventh Adversarial Review
**Reviewer:** Microsoft Copilot 1.2
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The manuscript states the discrete-to-continuum ring spectrum as  
  `\lambda(k)=-2\pi i k\,\phi'(\bar q)-\frac{(2\pi k)^{2}}{2M}\phi'(\bar q), \qquad \gamma_1\equiv|\mathrm{Re}\,\lambda(1)|_{t}=\frac{2\pi^{2}\mu\,\phi'(\bar q)}{M^{2}}, \qquad T_{\rm relax}=\frac{M^{2}}{2\pi^{2}\mu\,\phi'(\bar q)} .`  
  This is algebraically inconsistent: evaluating the boxed spectrum at \(k=1\) gives \(\mathrm{Re}\,\lambda(1)=-2\pi^{2}\phi'(\bar q)/M\) (scaling \(\propto M^{-1}\)), not the stated \(\propto \mu\,\phi'(\bar q)/M^{2}\). The extra factor of \(\mu\) and the extra power of \(M\) are unexplained and contradict the displayed eigenvalue, invalidating the claimed relaxation timescale mapping.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The paired tokens are consistently typed (angles ↔ co-moving phase; Fourier harmonic ↔ first loop harmonic; momentum ↔ normalized slip rate; control parameters ↔ speed/taper), and operator-role statements specify shared mathematical structure rather than hedged analogy.
- **CHECK 3 (Correspondence Vector Support):** PASS — Each `triple_correspondence_vectors` item is demonstrated in the body with equations or derivations:  
  - *periodic_divergence_form_transport_operator_with_conserved_zero_mode* — shown by the two divergence-form continuity equations and conserved integrals in §3.  
  - *constant_torque_pendulum_separatrix_and_shared_adiabaticity_criterion* — shown by the boxed pendulum equations and adiabatic invariance conditions.  
  - *moving_bucket_retention_factor_and_its_shared_variational_optimum* — shown by the separatrix action, definition of \(\alpha(s)\), and optimization yielding \(s^\star\).  
  - *bounded_concave_cycle_flux_ceiling* — shown by the bounded concave flux arguments and the min-ceiling expressions.  
  - *phase_normalization_gauge_group_with_gauge_invariant_flux_observable* — shown by the free group actions and invariant flux observables on both sides.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The manuscript states an asymmetric transfer direction (FEL → queueing under prescribed exogenous drive) and restricts applicability (adiabatic, underdamped regime), and it gives a concrete, testable prediction (optimal torque \(s^\star=\sqrt2-1\) and corresponding optimal speed \(v^\star\) and flux \(\Delta X_{\max}\)), which are falsifiable measurements in both domains.

#### Stage 3 Watch Items
- Re-derive the discrete linearization and continuum limit for the queue ring to confirm the correct prefactors and scaling with \(M\) and any time-rescaling that could introduce \(\mu\); the current manuscript contains a clear algebraic mismatch that must be corrected or justified.
- Request the authors to display the nondimensionalization steps for \(\tilde t\) and any rescaling that would produce the extra \(\mu\) and \(M\) factors in \(\gamma_1\) and \(T_{\rm relax}\).
- Verify that the relaxation timescale claimed to map between FEL and queueing models is not an artifact of inconsistent time units or omitted Jacobian factors in the continuum limit.
- Check the derivation of the discrete Laplacian prefactor (the \(1/(2M)\) term) and whether a different finite-difference convention or Taylor expansion coefficient was intended; small numeric prefactor errors here change the scaling of the relaxation time.
- Confirm experimental or simulation protocols that could test the predicted \(s^\star\) optimum in the queueing model and the FEL taper window mapping, as these are concrete Stage 3 validation targets.

### Eighth Adversarial Review
**Reviewer:** xAI Grok 4.5 Fast
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The displayed transport operators, conserved-zero-mode identities, constant-torque pendula (with the damping term and underdamped restriction explicitly stated), retention-factor integral, and flux-ceiling bounds all match the domains and structural claims made for each silo.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — Every paired token is of compatible mathematical type (angle on S¹, Fourier coefficient, conjugate momentum, dimensionless torque parameter, external control, gauge parameter, bounded flux ceiling) and the Operator Role statements name a shared structure rather than a hedged analogy.
- **CHECK 3 (Correspondence Vector Support):** PASS — All five listed vectors are demonstrated by explicit operator identities or derivations in Section 3 (Vector 1: boxed continuity equations and telescoping flux; Vector 2: boxed pendula, separatrix condition and adiabatic criterion; Vector 3: separatrix-area formula for α(s) and the subsequent variational maximisation; Vector 4: |b| \le 1 / min(q,1) ceilings with subgradient collapse; Vector 5: free gauge actions and invariant fluxes).
- **CHECK 4 (Transfer and Falsifiability):** PASS — The claimed direction is genuinely asymmetric (FEL possesses a mature adiabatic-torque design apparatus that cyclic-queueing theory lacks for traveling capacity profiles); the prediction supplies concrete numerical thresholds (v*/μ̄, peak relative gain, trapping window, overdamped collapse) that can be measured in discrete-event simulation and can falsify the hypothesis.

#### Stage 3 Watch Items
- Confirm that the unexplained cos ψ_r factor appearing in the Silo-B Ω^{2} expression is only a notational carry-over (with cos ψ_r set to 1) rather than an undefined resonant phase on the queueing side.
- Verify that the underdamped restriction Ωτ ≫ 1 is accepted by queueing theorists as the regime in which a second-order production-flow model is physically meaningful.
- Probe whether the non-isomorphic gauge groups (U(1) versus ℝ_{>0}) are regarded as sharing a sufficiently precise structural feature once the free-action-plus-invariant-flux level is made explicit.

### Ninth Adversarial Review
**Reviewer:** Meta Muse Spark 1.1
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Silo A Bonifacio-Pellegrini-Narducci system dψ_j/d\bar z=p_j, dp_j/d\bar z=-(Ae^{iψ_j}+c.c.), dA/d\bar z=<e^{-iψ}> and Vlasov→continuity ∂_{\bar z}n+∂_ψ(n u)=0 and invariant d/d\bar z(|A|^2+<p>)=0, and Silo B generator (A f)(n)=Σμ_i(n_i)[f(n-e_i+e_{i+1})-f(n)], product-form π(n)=G(N)^{-1}∏x_i^{n_i}/β_i(n_i), and Kurtz limit ∂_{\tilde t}q+∂_xφ(q)= (2M)^{-1}∂_x^2φ(q) all model claimed domains, and boxed pendula d^2ψ/d\bar z^2=-ω_s^2(sinψ-sinψ_r) and d^2ψ/dt^2+τ^{-1}dψ/dt=-Ω^2(sinψ-s) share second-order constant-torque class with explicit underdamped restriction Ωτ≫1, no elliptic/parabolic or linear/nonlinear class mismatch.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — Seven pairs are type-compatible: angle coordinate on S^1→angle on S^1, complex order parameter b=<e^{-iψ}>→complex first harmonic \hat q_1, dimensionless momentum p→dimensionless slip \hat p=\dotψ/Ω, dimensionless torque sinψ_r→dimensionless speed mismatch s, control dK/dz→control v with both entering only via dimensionless s, gauge parameters arg A→α_gauge, and flux ceiling P_sat→X_∞, each Operator Role cites shared operator (divergence-form transport, pendulum Hamiltonian H=½\hat p^2-cosψ-sψ, separatrix |s|≤1, gauge-invariant flux) not hedged analogy.
- **CHECK 3 (Correspondence Vector Support):** PASS — All listed vectors demonstrated in §3: periodic_divergence_form_transport_operator_with_conserved_zero_mode via ∂_{\bar z}n+∂_ψ(n u)=0, ∂_{\tilde t}q+∂_xφ(q) and ∮n dψ, ∮q dx conservation; constant_torque_pendulum_separatrix_and_shared_adiabaticity_criterion via boxed pendula, condition |sinψ_r|≤1↔|s|≤1 and adiabatic condition |Ω^{-2}dΩ/dt|≪1; moving_bucket_retention_factor_and_its_shared_variational_optimum via J(ψ_r), α(s)=(1-s)/(1+s), and d/ds[s(1-s)/(1+s)]=0→s*=√2-1; bounded_concave_cycle_flux_ceiling via |b|≤1, d|A|^2/d\bar z≤2|A| and X(N)=G(N-1)/G(N)→X_∞=min_i μ_i/r_i; phase_normalization_gauge_group_with_gauge_invariant_flux_observable via ψ→ψ+ψ_0, A→Ae^{-iψ_0} and r_i→α_gauge r_i with invariants |A|, X_i.
- **CHECK 4 (Transfer and Falsifiability):** PASS — Asymmetric: FEL KMR taper theory, adiabatic invariant J=∮\hat p dψ, trapped-fraction accounting, GENESIS-type optimization as source for traveling-capacity design, while Silo B maturity is static product-form/Buzen/MVA/heavy-traffic/SIPP which lacks trapping/retention/optimum-speed primitive; falsifiable: predicts time-averaged throughput \bar X(v) in M=32,N=16 CONWIP loop with \bar μ=1,\hat c=0.3,τ=5, argmax at v*/\bar μ=1+\hat c(√2-1)=1.124 within [1.105,1.144], peak gain (3-2√2)\hat c=5.15% must exceed 1.5%, zero gain outside [0.7,1.3] and vanishing gain when τ<0.53, no canonical prior-art pairing recognized.

#### Stage 3 Watch Items
- Overdamped relaxation collapse risk self-identified as primary failure risk: probe whether finite-buffer second-order fluid model \ddot x=τ^{-1}[U-\dot x] with underdamped condition Ωτ≫1 is standard in closed cyclic queueing theory or borrowed from traffic/production-flow literature, and whether retention factor α(s) survives discrete-event back-reaction.
- Verify that no textbook FEL↔queueing traveling-wave analogy exists that would make this a known interdisciplinary analogy, and confirm novelty-falsification string search yields no hit.
- None identified for equation misattribution or category error.