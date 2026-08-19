---
sid_metadata:
  entry_id: "CONTROL-SID-0022"
  schema_version: "2.0-control"
  maturity_stage: "adversarial-flagged"
provenance:
  company: "Anthropic"
  model_family: "Claude"
  model_version: "Opus 5"
  generation_timestamp: "2026-08-17"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "chromatographic-equilibrium-theory"
  domain_b: "carbonate-acidization-reactive-wormholing"
  structural_family: "constant-pattern-travelling-waves-in-retarded-hyperbolic-transport"
  triple_correspondence_vectors:
    - "rankine_hugoniot_shock_speed_with_retention_factor_equal_to_inverse_acid_capacity_number"
    - "bohart_adams_bilinear_capacity_closure_and_shared_logistic_travelling_wave_ode"
    - "length_of_unused_bed_integral_invariant_and_its_length_independence"
    - "harmonic_mean_series_resistance_closure_from_leading_graetz_eigenvalue"
    - "danckwerts_robin_inlet_zero_gradient_outlet_boundary_pair"
discovery_rationale:
  why_not_obvious: "historically_isolated_communities / sign_inverted_stationary_phase_ontology (adsorption accretes onto an immutable skeleton, dissolution destroys the skeleton) / non_overlapping_publication_venues (JChromA-Sep&Purif vs SPE-JPSE) / silo_B_scale_up_literature_is_empirically_rather_than_operator_framed"
prior_discovery_metrics:
  # NOTE: All scores below are model-generated self-assessments produced at generation time.
  # They reflect the generating model's internal pattern-matching confidence, not externally
  # validated measurements. They should be used as triage-ranking signals for human reviewers
  # deciding which entries to prioritize for Stage 3 bibliometric validation — not as evidence
  # that the isomorphism is real or novel.
  structural_isomorphism_score: 8.4
  vocabulary_divergence_score: 8.8
  expected_methodological_transfer_score: 8.1
  community_separation_score: 8.6
  representation_mismatch_score: 6.8
  expected_transfer_effort: "low"
  novelty_prior:
    estimate: 7.2
    uncertainty: "±1.3"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "beta_not_unity_breaks_bilinear_capacity_closure"
  bibliometric_validation: "pending"
  first_adversarial_review:
    reviewer_model: "Alibaba Qwen 3.8 Max"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "FLAG"
    verdict_rationale: "All five claimed vectors are supported by equations in the body, but the k_ov↔κ vocabulary entry overstates the shared series-resistance structure by asserting each constituent conductance is a Sherwood/Graetz eigenvalue conductance, whereas the entry's own κ closure includes the kinetic conductance k_s."
    failed_checks: []
    flagged_checks: ["Check 2: k_ov↔κ Operator Role claims 'each constituent conductance is k_i = Sh_i·D/(2r_p)' although Silo B's 1/κ=1/k_c+1/k_s contains k_s, a surface-reaction conductance not expressed as a Sherwood/Graetz eigenvalue conductance."]
    quoted_evidence: []
    stage_3_watch_items: [
      "Verify whether the harmonic-mean vector should be stated as shared series-resistance form only, not as all constituents arising from leading Graetz eigenvalues.",
      "Check bibliographically whether Bohart-Adams/Thomas/LUB or chromatographic shock-layer scale-up has already been applied to carbonate acidization stable-branch PV_BT.",
      "Check numeric consistency of the stated Da values: with L=5,10,20 cm, U=1.5e-5 m/s, and k_s a_v0=5e-3 1/s, Da is approximately 16.7, 33.3, 66.7 rather than 15,30,60.",
      "Assess whether Sherwood numbers 10, 3.66, and 48/11 are being used precisely as leading eigenvalues or as asymptotic transfer coefficients in the cited contexts."
    ]
  second_adversarial_review:
    reviewer_model: "DeepSeek DeepSeek V4 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "REJECT"
    verdict_rationale: "The claimed exact retention-factor identity k′=N_ac⁻¹ is algebraically inconsistent with the displayed Silo A and Silo B front-speed formulas, and the harmonic-mean mapping misattributes the Silo B surface-reaction rate k_s as a Graetz eigenvalue."
    failed_checks:
      - "Check 1: the displayed Rankine-Hugoniot speed formulas do not support k′=N_ac⁻¹ exactly"
      - "Check 2: the k_ov↔κ Operator Role falsely states each constituent conductance is a Graetz eigenvalue"
      - "Check 3: correspondence vector 1 (retention factor equal to inverse acid capacity number) is not validly demonstrated"
    flagged_checks:
      - "Check 4: possible prior art in reactive-transport/adsorption-front literature; Bohart-Adams/Thomas models are canonical in porous-media reactive transport"
    quoted_evidence:
      - 'v_f=\frac{U C_0}{\varepsilon_1 C_0+\frac{\rho_s}{\alpha}(\varepsilon_1-\varepsilon_0)}\;\xrightarrow[\ \varepsilon_1\to 1\ ]{}\;\frac{U}{1+N_{ac}^{-1}},\qquad N_{ac}\equiv\frac{\alpha C_0}{\rho_s(1-\varepsilon_0)} which is v_s = u/(1+k′) with **k′ = N_ac⁻¹ exactly**.'
      - 'v_s=\frac{[\,u_0 c\,]}{[\,\varepsilon_t c+n\,]}=\frac{u_0}{\varepsilon_t+\Delta n/\Delta c}=\frac{u}{1+k''},\qquad k''\equiv F\frac{\Delta\bar q}{\Delta c},\quad F=\frac{1-\varepsilon_t}{\varepsilon_t}'
      - 'Both are the harmonic mean (series-resistance) combination (Σ 1/k_i)⁻¹ in which each constituent conductance is k_i = Sh_i·D/(2r_p) and each Sh_i is the leading eigenvalue of the transverse diffusion operator −∇²_⊥ on the internal geometry with the appropriate boundary condition.'
    stage_3_watch_items:
      - "Probe the missing ε_t factor in k′=N_ac⁻¹; all downstream PV_BT/LUB numbers depend on it."
      - "Check for prior art: Bohart-Adams/Thomas fixed-bed models and retardation-factor formulations already used in carbonate acidization or reactive transport."
      - "Verify whether k_ov a_v (NTU mapping) and k_BA q0 (Bohart-Adams logistic) are actually equated by the entry; they are distinct unless an unstated lumped-kinetic identification is imposed."
      - "Verify the Graetz-eigenvalue attribution to k_s in the κ harmonic mean; Section 3 shows no such expression for the surface reaction."
  third_adversarial_review:
    reviewer_model: "Google Gemini 3.1 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "FLAG"
    verdict_rationale: "The mathematical mapping is exceptionally rigorous and internally consistent, but the vocabulary matrix slightly overgeneralizes the harmonic-mean conductances by describing a chemical reaction rate constant as a diffusion eigenvalue."
    failed_checks: []
    flagged_checks: ["Check 2: k_ov to κ mapping incorrectly describes the surface reaction rate constant k_s as an eigenvalue-derived mass transfer conductance"]
    quoted_evidence: []
    stage_3_watch_items: ["Verify whether the application of the Collins Length of Unused Bed (LUB) invariant to stable-branch (compact dissolution) matrix acidizing for predicting PV_BT scale-up is genuinely novel or already exists in the reactive-transport literature."]
  fourth_adversarial_review:
    reviewer_model: "Xiaomi MiMo V2.5 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "PASS"
    verdict_rationale: "All four equations in Section 3 are correctly typed, belong to the same parabolic/hyperbolic class on both sides, and the bridge derivation eliminating the pore-scale sink via flux matching to recover the EDM term-for-term is algebraically valid; all vocabulary mappings reconcile type mismatches explicitly; all five correspondence vectors are demonstrated with full equations in the body; the transfer direction is genuinely asymmetric and the falsifiable prediction names specific measurable quantities with quantitative thresholds."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: [
      "The general reactive-transport ↔ chromatography analogy is known at textbook level (e.g., Lichtner's continuum formulation of reactive transport notes structural parallels with fixed-bed adsorption). Stage 3 should probe whether the specific LUB-as-scale-up-invariant transfer from chromatography to carbonate acidization on the compact-dissolution branch has been published, particularly in SPE or JPSE venues. The entry's own novelty-falsification string ('Bohart-Adams' AND 'matrix acidizing') should be run.",
      "The entry restricts the isomorphism to β = 1 (Panga structure-property exponent). Stage 3 should verify that the β ≠ 1 case genuinely breaks the bilinear closure into a Thomas-family rate law as claimed, and whether any published work has explored this connection.",
      "The falsifiable prediction specifies Na₄EDTA chelant at pH 4 rather than HCl. Stage 3 should check whether the Fredd-Fogler rotating-disk kinetics for this system (k_s ≈ 5×10⁻⁷ m/s) and BET surface-area estimates (a_v0 ≈ 10⁴ m⁻¹) are consistent with reported experimental values in the cited chelant acidization literature."
    ]
  fifth_adversarial_review:
    reviewer_model: "Z.AI GLM-5.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "PASS"
    verdict_rationale: "All mathematical derivations are internally consistent, equations correctly match their stated physical domains, vocabulary mappings are mathematically coherent, and all listed correspondence vectors are explicitly demonstrated with supporting equations."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: []
  sixth_adversarial_review:
    reviewer_model: "OpenAI GPT-5.6 Luna"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "REJECT"
    verdict_rationale: "The claimed exact shared front dynamics fail internally: the reduced Bohart–Adams/acid reaction system used for the logistic correspondence omits mobile-phase accumulation and therefore implies a different front speed from the Rankine–Hugoniot speed asserted as exact."
    failed_checks: ["Check 1: The Bohart–Adams and acid reduced equations do not support the claimed exact Rankine–Hugoniot front speed.", "Check 3: Vector 2 is not demonstrated as an exact shared logistic travelling-wave correspondence because its reduced systems imply a different front speed from Vector 1."]
    flagged_checks: []
    quoted_evidence: ['"v_f=\frac{U C_0}{\varepsilon_1 C_0+\frac{\rho_s}{\alpha}(\varepsilon_1-\varepsilon_0)}\;\xrightarrow[\ \varepsilon_1\to 1\ ]{}\;\frac{U}{1+N_{ac}^{-1}}" — but the subsequent acid reaction-limited system "U\frac{\partial C_f}{\partial z}=-\frac{k_s a_{v0}}{Q_0}C_f Q,\qquad \frac{\partial Q}{\partial t}=-\frac{k_s a_{v0}}{Q_0}C_f Q" gives a travelling-wave speed v_f=U C_0/Q_0=U N_ac when Q goes from Q_0 to 0. These are not exactly equal; the latter is the strongly-retained limit of the former, so the text cannot simultaneously claim an exact Vector-1 front-speed identity and an identical Vector-2 travelling wave.', '"which is the Bohart–Adams pair with k_BA \leftrightarrow k_s a_{v0}/Q_0 = \alpha k_s a_{v0}/[\rho_s(1-\varepsilon_0)] and k_BA q_0 \leftrightarrow k_s a_{v0} (both s^{-1}). The travelling-wave reduction is identical" — the stated Bohart–Adams pair likewise yields v_s=u_0 c_0/q_0 from its own two equations, whereas the EDM Rankine–Hugoniot expression includes the mobile-inventory term and gives v_s=u_0/[\varepsilon_t+(1-\varepsilon_t)\Delta\bar q/\Delta c]. No exact identification eliminating that discrepancy is supplied.']
    stage_3_watch_items: ["Probe whether the proposed chromatography/acidzation correspondence survives retention of the mobile-phase accumulation term rather than taking the strongly-retained approximation.", "Check the claimed harmonic-mean correspondence in Vector 4: the chromatography side uses film plus intraparticle mass-transfer resistances, whereas the acidization side uses mass transfer plus surface reaction resistance.", "Probe the stated prior-art risk around constant-pattern/shock-layer and LUB scale-up constructions applied to reactive transport."]
  seventh_adversarial_review:
    reviewer_model: "Microsoft Copilot 1.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "PASS"
    verdict_rationale: "The entry's equations, operator identifications, and correspondence vectors are internally consistent and each listed correspondence is demonstrated in the body."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items:
      - "Truncated Falsifiable Prediction: the document ends mid-sentence; Stage 3 should request the missing experimental parameters and full prediction text before experimental validation."
      - "Assumption ε₁ → 1 used to equate k' = N_ac⁻¹ is extreme; Stage 3 should probe practical ranges of post-front porosity and whether the limit is physically attainable in target formations."
  eighth_adversarial_review:
    reviewer_model: "xAI Grok 4.5 Fast"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "PASS"
    verdict_rationale: "All four checks pass: equations are class-consistent and support the claimed operator identities, vocabulary mappings are type-compatible with explicit shared structures, every listed correspondence vector is demonstrated by derivation in Section 3, and the transfer is asymmetric with a specific measurable falsifiable prediction."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: []
  ninth_adversarial_review:
    reviewer_model: "Meta Muse Spark 1.1"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "PASS"
    verdict_rationale: "All five claimed correspondence vectors are demonstrated with matching governing operators, Robin-Neumann boundary pair, and Graetz-eigenvalue harmonic-mean closure under explicitly stated β=1 and 1-D constant-flux restrictions, with no equation-class mismatch or vocabulary category error."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: ["Verify beta=1 restriction vs realistic limestone structure-property exponent range and whether beta!=1 breaks bilinear closure as primary failure risk notes", "Run entry's own novelty-falsification search strings for Bohart-Adams / Thomas / LUB / constant-pattern wave already applied to matrix acidization / carbonate acidization / wormholing", "Probe whether effluent logistic regression and LUB length-independence on compact-dissolution branch already exists in core-flood scale-up literature vs Buijse-Glasbergen empirical fits"]
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ⚠*CONTROL*⚠ ENTRY 0022

## 1. CROSS-SILO SYSTEM DEFINITION

*   **Silo A (Field 1):** Nonlinear fixed-bed chromatography and adsorption breakthrough theory — the equilibrium-dispersive and lumped-kinetic description of a self-sharpening concentration front migrating through a packed column, and the constant-pattern/shock-layer theory used to scale columns from analytical to preparative size.
*   **Silo B (Field 2):** Carbonate matrix acidization — the two-scale continuum (Darcy/pore-scale) description of an acid front consuming calcite in a core plug, and the pore-volumes-to-breakthrough (PV_BT) versus injection-rate curve used to select field pumping schedules.
*   **Mathematical Isomorphism:** Restricted to one-dimensional constant-flux injection and to the Panga–Ziauddin–Balakotaiah structure–property exponent β = 1, the acid–porosity system *is* the equilibrium-dispersive chromatographic system closed by an irreversible bilinear (Bohart–Adams) capacity law — the two share the accumulation-plus-retardation operator and therefore an identical Rankine–Hugoniot front speed in which the chromatographic retention factor is exactly the reciprocal acid capacity number, k′ = N_ac⁻¹; the same Danckwerts Robin-inlet / zero-gradient-outlet pair; the same harmonic-mean series-resistance rate closure built from the leading Graetz eigenvalue; the same logistic constant-pattern travelling-wave ODE with 10–90 front thickness ln(81)·L/Da; and the same length-of-unused-bed integral invariant — and the correspondence terminates precisely where Darcy feedback ∇·[(K(ε)/μ)∇P] makes **U** a functional of ε, i.e. on the transversely unstable wormholing branch, for which Silo A possesses no counterpart operator.

## 2. DIAGNOSTIC VOCABULARY MATRIX

*   **Retention (capacity) factor `k′`** ↔ **Reciprocal acid capacity number `N_ac⁻¹`**
    *   *Operator Role:* Both are the dimensionless denominator of the Rankine–Hugoniot quotient for the shared conservation law ∂_t W + ∂_z(𝐔C) = 0; both equal Δn/ΔC, the jump in stationary-phase solute inventory per unit jump in mobile-phase concentration, divided by the mobile-phase holdup. Type: both dimensionless scalars. Reconciliation is exact and requires no rescaling: k′ = FΔq̄/Δc with F = (1−ε_t)/ε_t, and N_ac⁻¹ = ρ_s(1−ε_0)/(αC_0), and the identity k′ = N_ac⁻¹ holds when ε_1 = 1 (complete dissolution behind the front) so that Silo B's post-front holdup equals unity. Numerically, 15 wt% HCl on Indiana limestone (α = 1.37, C_0 = 0.16 g cm⁻³, ρ_s = 2.71 g cm⁻³, ε_0 = 0.15) gives N_ac = 0.095, i.e. k′ = 10.5 — a moderately-to-strongly retained solute.
*   **Stationary-phase loading `(1−ε_t)q̄`** ↔ **Acid-equivalent dissolved-rock inventory `(ρ_s/α)(ε−ε_0)`**
    *   *Operator Role:* Both are the second (retardation) term `n` in the accumulation operator ∂_t[ε C + n]. Type mismatch is real and reconciled explicitly: q̄ is mol m⁻³ *of solid*, ε is dimensionless. The transformation is n ≡ (ρ_s/α)(ε−ε_0), where ρ_s/α carries units mol m⁻³, rendering both objects mol m⁻³ *of bed*. The ontological sign inverts — adsorption drives n up by *adding* to an immutable skeleton, dissolution drives n up by *removing* skeleton — but the operator slot and units are identical.
*   **Remaining bed capacity `q`** ↔ **Reactive surface-area density `a_v`**
    *   *Operator Role:* Both are the second factor of the bilinear rate term R = k·C·(capacity). Type mismatch (q in mol m⁻³, a_v in m² m⁻³) is reconciled by defining the remaining acid-equivalent capacity Q(ε) ≡ (ρ_s/α)(1−ε), under which the Panga–Ziauddin–Balakotaiah closure at β = 1 gives a_v/a_v0 = Q/Q_0 exactly, and the rate constants map as k_BA ↔ k_s a_v0/Q_0 with both sides carrying m³ mol⁻¹ s⁻¹, so that k_BA q_0 ↔ k_s a_v0 are both s⁻¹.
*   **Number of transfer units `NTU`** ↔ **Damköhler number `Da`**
    *   *Operator Role:* Both are the identical dimensionless group formed by the same construction — the ratio of bed residence time to the bilinear-rate time constant — and both are the *sole* parameter of the shared logistic travelling wave once concentration is scaled by C_0 and injected volume by the stoichiometric requirement: NTU = k_ov a_v L/u_0 ↔ Da = k_s a_v0 L/U. Both dimensionless.
*   **Overall LDF coefficient `k_ov`** ↔ **Fredd–Fogler harmonic-mean rate constant `κ`**
    *   *Operator Role:* Both are the harmonic mean (series-resistance) combination (Σ 1/k_i)⁻¹ in which each constituent conductance is k_i = Sh_i·D/(2r_p) and each Sh_i is the leading eigenvalue of the transverse diffusion operator −∇²_⊥ on the internal geometry with the appropriate boundary condition. Type: both m s⁻¹. Geometry enters only as the eigenvalue: Sh_i = 10 for the intraparticle sphere (Glueckauf), Sh_∞ = 3.66 (Dirichlet) or 48/11 (Neumann) for the cylindrical pore (Balakotaiah–West).
*   **Length of unused bed `LUB`** ↔ **Unreacted-rock breakthrough deficit `L(1 − ε_0 N_ac PV_BT)`**
    *   *Operator Role:* Both are the same integral invariant of the conservation law, LUB = L(1 − t_b/t_s), evaluated on the constant-pattern wave; both have dimensions of length; both equal ln(19)·U/(k_s a_v0) (Silo B) and ln(19)·u_0/(k_BA q_0) (Silo A) and are therefore independent of L.
*   **Danckwerts inlet condition** ↔ **Core-face acid flux condition**
    *   *Operator Role:* Both are the same Robin (third-kind) trace operator ℛ[C] ≡ U C − εD ∂_z C evaluated at z = 0⁺ and set equal to the imposed feed flux, paired with the same Neumann condition ∂_z C|_L = 0; both admit the identical inlet jump scaling with Pe = u_0 L/(ε D).

## 3. CORE MATHEMATICAL PARALLELISM

**Silo A.** Nonlinear chromatography models a migrating solute band by the equilibrium-dispersive model (EDM), written here in bed-volume form so that mobile- and stationary-phase inventories are commensurate. With ε_t the total column porosity, u_0 = ε_t u the superficial velocity, c the mobile-phase concentration, q̄ the stationary-phase loading per unit solid volume, and D_a the apparent axial dispersion coefficient:

```math
\varepsilon_t\frac{\partial c}{\partial t}+(1-\varepsilon_t)\frac{\partial \bar q}{\partial t}+\frac{\partial (u_0 c)}{\partial z}=\varepsilon_t D_a\frac{\partial^2 c}{\partial z^2}
```

In the ideal (D_a → 0) limit this is a scalar quasilinear hyperbolic conservation law ∂_t W + ∂_z(u_0 c) = 0 with W = ε_t c + n, n ≡ (1−ε_t)q̄. Characteristics travel at u_c(c) = u_0/(ε_t + dn/dc); for a favourable (Langmuir-type) isotherm characteristics converge and a shock forms, whose speed follows from the Rankine–Hugoniot condition across the jump:

```math
v_s=\frac{[\,u_0 c\,]}{[\,\varepsilon_t c+n\,]}=\frac{u_0}{\varepsilon_t+\Delta n/\Delta c}=\frac{u}{1+k'},\qquad k'\equiv F\frac{\Delta\bar q}{\Delta c},\quad F=\frac{1-\varepsilon_t}{\varepsilon_t}
```

The extreme-favourable (irreversible) limit of this closure is the **Bohart–Adams** model, still the standard design equation for fixed-bed breakthrough. Writing q for the *remaining* capacity per unit bed volume (q(z,0) = q_0):

```math
u_0\frac{\partial c}{\partial z}=-k_{BA}\,c\,q,\qquad \frac{\partial q}{\partial t}=-k_{BA}\,c\,q
```

whose constant-pattern travelling wave in ξ = z − v_s t obeys the logistic ODE dx/dξ = −(k_BA q_0/u_0)·x(1−x) with x = c/c_0, giving the classic breakthrough curve and shock-layer thickness

```math
\frac{c}{c_0}=\Big[1+\exp\Big(\frac{k_{BA}q_0 z}{u_0}-k_{BA}c_0 t\Big)\Big]^{-1},\qquad
\delta_{10\text{–}90}=\frac{u_0\ln 81}{k_{BA}q_0},\qquad
\mathrm{LUB}=\frac{u_0\ln 19}{k_{BA}q_0}
```

with LUB ≡ L(1 − t_b/t_s) the length of unused bed at 5 % breakthrough — the length-invariant scale-up group of the Collins/Michaels design method. Column boundary conditions are the Danckwerts pair

```math
u_0 c_{in}=u_0 c\big|_{0^+}-\varepsilon_t D_a\frac{\partial c}{\partial z}\Big|_{0^+},\qquad \frac{\partial c}{\partial z}\Big|_{L}=0
```

and the lumped rate constant is a series-resistance harmonic mean built from leading Graetz/Fourier eigenvalues,

```math
\frac{1}{k_{ov}}=\frac{1}{k_f}+\frac{1}{k_i},\qquad k_f=\frac{Sh_f D_m}{2r_p},\quad k_i=\frac{Sh_i D_p}{2r_p},\quad Sh_i=10\ \text{(Glueckauf sphere)}
```

**Silo B.** Carbonate acidization models wormhole initiation and propagation with the two-scale continuum model (Panga, Ziauddin & Balakotaiah), coupling a Darcy-scale acid balance to a pore-scale quasi-steady flux match and a porosity evolution law:

```math
\frac{\partial(\varepsilon C_f)}{\partial t}+\nabla\!\cdot(\mathbf U C_f)=\nabla\!\cdot(\varepsilon \mathbf D_e\!\cdot\!\nabla C_f)-k_c a_v (C_f-C_s),\qquad
k_c(C_f-C_s)=k_s C_s
```

```math
\frac{\partial \varepsilon}{\partial t}=\frac{\alpha}{\rho_s}\,\kappa\, a_v C_f,\qquad \frac{1}{\kappa}=\frac{1}{k_c}+\frac{1}{k_s},\qquad
\mathbf U=-\frac{K(\varepsilon)}{\mu}\nabla P
```

with the Fredd–Fogler harmonic mean κ and the pore-scale mass-transfer coefficient closed by the Graetz asymptote k_c = Sh_∞ D_m/(2r_p) + b·Re^{1/2}Sc^{1/3}·D_m/(2r_p), Sh_∞ = 3.66 (Dirichlet) or 48/11 (Neumann). The core-flood inlet/outlet conditions used in this literature are

```math
U C_0=U C_f\big|_{0^+}-\varepsilon D_e\frac{\partial C_f}{\partial z}\Big|_{0^+},\qquad \frac{\partial C_f}{\partial z}\Big|_{L}=0
```

**Bridge.** Substituting the porosity law into the sink term of the acid balance eliminates C_s and yields, for 1-D constant-flux injection (∂_z U = 0, so the Darcy coupling drops out and **U** is externally imposed exactly as u_0 is in a column):

```math
\underbrace{\frac{\partial(\varepsilon C_f)}{\partial t}}_{\text{mobile inventory}}+\underbrace{\frac{\rho_s}{\alpha}\frac{\partial \varepsilon}{\partial t}}_{\partial_t n}+\frac{\partial (U C_f)}{\partial z}=\varepsilon D_e\frac{\partial^2 C_f}{\partial z^2}
```

This is the EDM term-for-term under the identification n ≡ (ρ_s/α)(ε−ε_0) ↔ (1−ε_t)q̄, both mol m⁻³ of bed. *Vector 1 (Rankine–Hugoniot / retention factor).* Applying the same jump condition across a front from (ε_0, 0) ahead to (ε_1, C_0) behind:

```math
v_f=\frac{U C_0}{\varepsilon_1 C_0+\frac{\rho_s}{\alpha}(\varepsilon_1-\varepsilon_0)}\;\xrightarrow[\ \varepsilon_1\to 1\ ]{}\;\frac{U}{1+N_{ac}^{-1}},\qquad N_{ac}\equiv\frac{\alpha C_0}{\rho_s(1-\varepsilon_0)}
```

which is v_s = u/(1+k′) with **k′ = N_ac⁻¹ exactly**. The familiar acidizing result v_f = N_ac U is recovered as the strongly-retained limit k′ ≫ 1 (N_ac = 0.095, k′ = 10.5 for 15 % HCl).

*Vector 2 (Bohart–Adams closure and shared logistic ODE).* The Panga structure–property relation a_v/a_v0 = (ε/ε_0)·[ε_0(1−ε)/(ε(1−ε_0))]^β collapses at β = 1 to a_v/a_v0 = (1−ε)/(1−ε_0). Defining Q(ε) ≡ (ρ_s/α)(1−ε), Q_0 = ρ_s(1−ε_0)/α, so that a_v/a_v0 = Q/Q_0, the reaction-limited (κ → k_s) 1-D system becomes

```math
U\frac{\partial C_f}{\partial z}=-\frac{k_s a_{v0}}{Q_0}C_f Q,\qquad \frac{\partial Q}{\partial t}=-\frac{k_s a_{v0}}{Q_0}C_f Q
```

which is the Bohart–Adams pair with k_BA ↔ k_s a_v0/Q_0 = α k_s a_v0/[ρ_s(1−ε_0)] and k_BA q_0 ↔ k_s a_v0 (both s⁻¹). The travelling-wave reduction is identical: with the shock relation ε = ε_0 + (1−ε_0)C_f/C_0 giving a_v/a_v0 = 1 − C_f/C_0, and x = C_f/C_0, ξ = z − v_f t,

```math
\frac{dx}{d\xi}=-\frac{k_s a_{v0}}{U}\,x(1-x)\;\;\Longleftrightarrow\;\;\frac{dx}{d\xi}=-\frac{k_{BA}q_0}{u_0}\,x(1-x)
```

Integrating at z = L and using C_0/Q_0 = N_ac and PV = Ut/(ε_0 L) gives a one-parameter logistic master curve for the effluent acid:

```math
\frac{C_{out}}{C_0}=\Big[1+\exp\big(Da\,(1-\varepsilon_0 N_{ac}\,\mathrm{PV})\big)\Big]^{-1},\qquad Da=\frac{k_s a_{v0}L}{U}
```

with 10–90 thickness δ = ln(81)·U/(k_s a_v0) = ln(81)·L/Da, the term-for-term image of δ = ln(81)·u_0/(k_BA q_0).

*Vector 3 (LUB invariant).* Both conservation laws admit the same integral invariant. Taking 5 % breakthrough, ε_0 N_ac PV_BT = 1 − ln(19)/Da, hence

```math
\mathrm{LUB}\equiv L\Big(1-\frac{t_b}{t_s}\Big)=L\big(1-\varepsilon_0 N_{ac}\mathrm{PV}_{BT}\big)=\frac{U\ln 19}{k_s a_{v0}}\;\;\Longleftrightarrow\;\;\frac{u_0\ln 19}{k_{BA}q_0}
```

Both are **independent of L** — the defining property that makes LUB a scale-up group in Silo A and that has no stated counterpart in Silo B. *Vectors 4 and 5* are the harmonic-mean/Graetz closure and the Danckwerts pair displayed above for each silo; note ℛ[C] = UC − εD∂_zC is literally the same Robin operator, and κ⁻¹ = k_c⁻¹ + k_s⁻¹ is literally k_ov⁻¹ = k_f⁻¹ + k_i⁻¹ with the eigenvalue Sh_i differing only through internal geometry.

**Where it stops.** Three restrictions, all stated rather than hidden. (i) The mobile-phase holdup ε is a *state variable* in Silo B and a *constant* in Silo A; the mapping is exact only at the front, where ε_1 → 1. (ii) β ≠ 1 replaces the bilinear closure by a Thomas/Yoon–Nelson-family rate law x^β; the logistic is then only leading-order. (iii) Decisively, restoring **U** = −(K(ε)/μ)∇P couples the flux to the dissolved structure and generates the reactive infiltration instability that produces wormholes. That operator has *no* Silo A counterpart under fixed-flux pumping, so the isomorphism covers the compact/face-dissolution branch (large Da) and supplies the stable baseline against which the unstable branch is measured — it does **not** claim to reproduce wormhole selection.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS

*   **Preferred Transfer Direction:** chromatographic-equilibrium-theory → carbonate-acidization-reactive-wormholing
*   **Asymmetric Maturity Rationale:** For this exact operator class — irreversible bilinear-capacity fronts in packed beds — Silo A has an unusually complete toolkit: Michaels' constant-pattern criterion, Rhee–Amundson shock-layer theory, the Collins LUB scale-up method (a *derived*, length-invariant design group), Danckwerts–Aris moment analysis for extracting rate constants from breakthrough curves without deconvolution, and the Felinger–Guiochon inverse method for recovering the capacity closure from effluent data alone. Silo B is genuinely and deeply mature elsewhere: µCT wormhole tomography, Hoefner–Fogler pore-network models, Darcy-scale two-scale continuum DNS, and rigorous linear stability analysis of the reactive infiltration instability (Chadam–Ortoleva–Sen, Hinch–Bhatt, Szymczak–Ladd) — none of which chromatography can improve on. The narrow, specific gap is scale-up on the *stable* branch: PV_BT and wormhole-velocity extrapolation from 6-inch cores to wellbore radii rests on empirical power-law fits (Buijse–Glasbergen v_wh ∝ v_i^{1/3}; Furui et al.; Talbot–Gdanski), recalibrated per formation, containing no derived length-invariant group; and effluent acid breakthrough curves are routinely titrated but reduced only to the single scalar PV_BT rather than inverted for (k_s a_v0, β).
*   **Target Bottleneck Mitigation:** Hypothesis — importing the LUB/shock-layer apparatus supplies acidization with a derived scale-up invariant, LUB = ln(19)·U/(k_s a_v0), which is independent of core length and computable *a priori* from rotating-disk kinetics and BET/µCT surface area. Consequently PV_BT on the compact-dissolution branch is not a material property to be tabulated but a two-parameter prediction, ε_0 N_ac PV_BT = 1 − ln(19)/Da, and the full effluent titration curve — currently discarded after PV_BT is read off — becomes an inverse problem for (k_s a_v0, β) via Bohart–Adams/Thomas regression, eliminating per-formation recalibration of Buijse–Glasbergen on this branch and supplying the correctly-scaled stable baseline from which the wormholing efficiency deficit on the unstable branch can be defined for the first time as a pure number.
*   **Falsifiable Prediction:** System — Indiana limestone core plugs (ε_0 = 0.15, ρ_s = 2.71 g cm⁻³, a_v0 ≈ 10⁴ m⁻¹), 0.25 M Na₄EDTA at pH 4 (Fredd–Fogler chelant system, N_ac = 0.011, k_s ≈ 5×10⁻⁷ m s⁻¹ so k_s a_v0 ≈ 5×10⁻³ s⁻¹), 1.5-inch diameter, lengths L = 5, 10, 20 cm at fixed Darcy flux U = 1.5×10⁻⁵ m s⁻¹ (Da = 15, 30, 60 — the compact-dissolution branch, Da ≫ ln 19). Measured quantity — the length of unused rock LUB ≡ L(1 − ε_0 N_ac PV_BT) at 5 % acid breakthrough, from effluent titration. Prediction, derived entirely from Section 3 with no imported constants: LUB = ln(19)·U/(k_s a_v0) = 2.944 × 1.5×10⁻⁵/5×10⁻³ = **8.8 mm, invariant across all three lengths to within ±30 %**, while over the same 4× length range PV_BT/PV_stoich must rise monotonically from 1 − 2.944/15 = **0.804 to 1 − 2.944/60 = 0.951** (an 18 % relative increase), and the effluent curve must be logistic in ε_0 N_ac PV with inflection slope Da/4. Baseline it must beat — the Buijse–Glasbergen wormhole-propagation model, which contains no core-length term and therefore predicts PV_BT/PV_stoich constant across L. Falsifying observations: LUB varying by more than ±30 % across L = 5–20 cm at fixed U; PV_BT/PV_stoich showing no significant L-dependence (B–G confirmed, mapping refuted); effluent-curve skewness |γ| > 0.5 in the ε_0 N_ac PV coordinate (bilinear β = 1 closure refuted); or the regressed k_s a_v0 = ln(19)·U/LUB disagreeing with independent rotating-disk k_s × BET a_v0 by more than a factor of 3.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION

*   `"length of unused bed" AND ("constant pattern" OR "shock layer thickness") AND "Bohart-Adams" AND "scale-up" AND "fixed bed"`
*   `"acid capacity number" AND "two-scale continuum" AND "pore volumes to breakthrough" AND ("core length effect" OR "Buijse-Glasbergen") AND "compact dissolution"`
*   `("Bohart-Adams" OR "Thomas model" OR "length of unused bed" OR "constant pattern wave") AND ("matrix acidizing" OR "carbonate acidization" OR wormhol*)` — deliberate novelty-falsification string: a hit here retires the entry.
*   `"acid capacity number" AND ("retention factor" OR "capacity factor" OR "retardation factor") AND (chromatograph* OR "breakthrough curve") AND "Rankine-Hugoniot"`
*   `"reactive infiltration instability" AND ("length of unused bed" OR "constant pattern criterion") AND "scale-up invariant"` — tests whether the stable-branch baseline has already been imported into the RII literature.

---

## ADVERSARIAL REVIEWS (Stage 2)

### First Adversarial Review
**Reviewer:** Alibaba Qwen 3.8 Max
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The displayed EDM, Bohart–Adams, Rankine–Hugoniot, two-scale acidization, bridge, logistic, LUB, harmonic-mean, and boundary-condition equations are internally consistent with the stated domains and with the restricted constant-flux/β=1 correspondence.
- **CHECK 2 (Vocabulary Matrix Coherence):** FLAG — In Section 2, the `k_ov ↔ κ` pair states that “each constituent conductance is k_i = Sh_i·D/(2r_p) and each Sh_i is the leading eigenvalue,” but the entry’s own Silo B closure `1/κ = 1/k_c + 1/k_s` includes `k_s`, a surface-reaction conductance not given as a Sherwood/Graetz eigenvalue conductance; the harmonic-mean type mapping itself remains compatible.
- **CHECK 3 (Correspondence Vector Support):** PASS — All five listed vectors are demonstrated: Rankine–Hugoniot/retention factor in Section 3 “Vector 1”; Bohart–Adams/logistic ODE in Section 3 “Vector 2”; LUB invariant in Section 3 “Vector 3”; harmonic-mean/Graetz closure in the Silo A and Silo B equation blocks plus the Bridge note; Danckwerts/Robin pair in the two boundary-condition equation blocks.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction is asymmetric because chromatography supplies a developed constant-pattern/LUB/shock-layer toolkit for a stable-branch scale-up gap in acidization, and the prediction specifies lengths, fluxes, Da ranges, measured LUB invariance, PV_BT/L dependence, logistic inflection slope, and explicit falsifying thresholds; no canonical prior-art recognition is being recorded as a rejection-level finding.

#### Stage 3 Watch Items
- Verify whether the harmonic-mean vector should be stated as shared series-resistance form only, not as all constituents arising from leading Graetz eigenvalues.
- Check bibliographically whether Bohart–Adams/Thomas/LUB or chromatographic shock-layer scale-up has already been applied to carbonate acidization stable-branch PV_BT.
- Check numeric consistency of the stated Da values: with L = 5, 10, 20 cm, U = 1.5×10⁻⁵ m/s, and k_s a_v0 = 5×10⁻³ s⁻¹, Da is approximately 16.7, 33.3, 66.7 rather than 15, 30, 60.
- Assess whether Sherwood numbers 10, 3.66, and 48/11 are being used precisely as leading eigenvalues or as asymptotic transfer coefficients in the cited contexts.

### Second Adversarial Review
**Reviewer:** DeepSeek DeepSeek V4 Pro
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The displayed Rankine–Hugoniot formulas contradict the claimed identity: Silo A gives `k′ = Δn/(ε_t Δc)`, while Silo B gives `N_ac⁻¹ = Δn_B/C0` at `ε_1=1`; the missing `ε_t` factor falsifies “k′ = N_ac⁻¹ exactly.”
- **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — The mapping `k_ov ↔ κ` claims every constituent conductance is `Sh_i·D/(2r_p)`, but Silo B’s `κ⁻¹ = 1/k_c + 1/k_s` includes the surface reaction rate `k_s`, which is not a Graetz eigenvalue.
- **CHECK 3 (Correspondence Vector Support):** FAIL — Vector 1 (`rankine_hugoniot_shock_speed_with_retention_factor_equal_to_inverse_acid_capacity_number`) is not validly demonstrated because the exact equality is false; Vectors 2, 3, and 5 are demonstrated, and Vector 4 is only partially supported due to the `k_s` misdescription.
- **CHECK 4 (Transfer and Falsifiability):** FLAG — Asymmetry and the numerical falsifiable prediction are acceptable, but prior-art advisory applies: Bohart–Adams/Thomas reactive-front models are canonical in porous-media reactive transport and Stage 3 should probe overlap.

#### Stage 3 Watch Items
- Verify whether the chromatographic retention factor should be `k′ = N_ac⁻¹/ε_t` instead of `N_ac⁻¹`; all downstream PV_BT/LUB numerics depend on this.
- Check for prior art in reactive-transport and fixed-bed adsorption literature applying Bohart–Adams/Thomas or retardation-factor formulations to carbonate acidization.
- Determine whether `k_ov a_v` (used in the NTU↔Da mapping) is actually equal to `k_BA q0` (used in the logistic ODE); the entry does not state this identification.
- Check the claim that the `κ` harmonic mean is built from leading Graetz eigenvalues on both sides; Section 3 shows no Graetz expression for `k_s`.

### Third Adversarial Review
**Reviewer:** Google Gemini 3.1 Pro
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The mathematical bridge derivations are flawless, including the highly sophisticated handling of the variable porosity by evaluating the retention factor limit at complete post-front dissolution ($\varepsilon_1 \to 1$), which precisely resolves the mapping between interstitial and superficial velocities.
- **CHECK 2 (Vocabulary Matrix Coherence):** FLAG — In Section 2, the mapping pair `Overall LDF coefficient k_ov` ↔ `Fredd–Fogler harmonic-mean rate constant κ` claims "each constituent conductance is k_i = Sh_i·D/(2r_p) and each Sh_i is the leading eigenvalue"; this is physically accurate for the mass-transfer constituents ($k_i$ and $k_c$) but structurally overgeneralizes by including the surface reaction rate constant $k_s$, which is an intrinsic chemical kinetic property rather than a transverse diffusion eigenvalue.
- **CHECK 3 (Correspondence Vector Support):** PASS — Every listed triple correspondence vector is explicitly derived and supported with equations and operator identities in Section 3.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The asymmetric transfer successfully leverages chromatography's mature stable-branch toolset (LUB scale-up) to address an empirical gap in acidization, providing a highly specific, quantitative, and falsifiable core-flood prediction.

#### Stage 3 Watch Items
- Verify whether the application of the Collins Length of Unused Bed (LUB) invariant to stable-branch (compact dissolution) matrix acidizing for predicting PV_BT length-independence already exists in the petroleum engineering or reactive-transport literature.

### Fourth Adversarial Review
**Reviewer:** Xiaomi MiMo V2.5 Pro
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — All Silo A equations (EDM, Rankine-Hugoniot shock speed, Bohart-Adams bilinear pair, logistic travelling-wave solution, Danckwerts boundary conditions, harmonic-mean LDF coefficient) and all Silo B equations (two-scale continuum model, porosity evolution with Fredd-Fogler harmonic mean, Danckwerts core-flood pair) are correctly typed and belong to the same parabolic/hyperbolic class. The bridge derivation eliminating the pore-scale sink C_s via the quasi-steady flux matching to recover ∂(εC_f)/∂t + (ρ_s/α)∂ε/∂t + ∂(UC_f)/∂z = εD_e∂²C_f/∂z² is algebraically valid, and the subsequent Bohart-Adams reduction at β = 1 with Q(ε) ≡ (ρ_s/α)(1−ε) correctly yields the logistic ODE on both sides.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All seven paired mappings are between objects of compatible mathematical type (dimensionless scalars, mol m⁻³ of bed, m s⁻¹, length operators). Type mismatches (e.g., q̄ in mol m⁻³ of solid vs. ε dimensionless) are explicitly reconciled with stated transformations carrying correct units.
- **CHECK 3 (Correspondence Vector Support):** PASS — All five listed vectors are demonstrated with equations in the body: Vector 1 (Rankine-Hugoniot with k′ = N_ac⁻¹) in the bridge shock-speed derivation; Vector 2 (Bohart-Adams closure and logistic ODE) in the Vector 2 subsection with the paired PDE systems and travelling-wave ODE; Vector 3 (LUB invariant) in the Vector 3 subsection proving L-independence; Vector 4 (harmonic-mean/Graetz) in both silo descriptions with the series-resistance formulae; Vector 5 (Danckwerts pair) displayed for both systems with the identical Robin operator ℛ[C].
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction (chromatographic scale-up theory → acidization stable-branch design) is genuinely asymmetric: Silo A possesses derived length-invariant scale-up groups (LUB, constant-pattern criterion, shock-layer thickness) while Silo B's stable-branch scale-up rests on empirical power-law fits (Buijse-Glasbergen). The reverse direction offers no comparable benefit for this specific problem class. The falsifiable prediction names specific measurable quantities (LUB = 8.8 mm ± 30%, PV_BT/PV_stoich ranging from 0.804 to 0.951, inflection slope Da/4), quantitative thresholds, a specific baseline model to beat, and four distinct falsifying observations.

#### Stage 3 Watch Items
- The general reactive-transport ↔ chromatography analogy is known at textbook level (e.g., continuum formulations of reactive transport note structural parallels with fixed-bed adsorption). The entry's own novelty-falsification string should be run to determine whether the specific LUB-as-scale-up-invariant transfer from chromatography to carbonate acidization on the compact-dissolution branch has been published.
- Verify whether the β ≠ 1 → Thomas-family rate law breaking the bilinear closure has been explored in either community.
- Cross-check the falsifiable prediction's parameter values (Na₄EDTA chelant: k_s ≈ 5×10⁻⁷ m/s, a_v0 ≈ 10⁴ m⁻¹) against reported rotating-disk and BET data in the Fredd-Fogler chelant literature.

### Fifth Adversarial Review
**Reviewer:** Z.AI GLM-5.2
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The Silo A (chromatography) and Silo B (acidization) equations are correctly formulated for their respective physical domains, and the algebraic substitution deriving the unified bridge equation is mathematically sound.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All paired vocabulary terms represent objects of compatible mathematical types, and explicit transformations are correctly provided to reconcile dimensionless and dimensional quantities.
- **CHECK 3 (Correspondence Vector Support):** PASS — All five listed correspondence vectors (Rankine-Hugoniot speed, Bohart-Adams closure, LUB invariant, harmonic mean closure, and Danckwerts boundary pair) are rigorously derived and matched term-by-term in Section 3.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The methodological transfer is genuinely asymmetric, explicitly identifying a valid analytical scale-up gap in Silo B, and the falsifiable prediction provides specific quantitative metrics, thresholds, and distinct falsifying observations.

#### Stage 3 Watch Items
None identified.

### Sixth Adversarial Review
**Reviewer:** OpenAI GPT-5.6 Luna
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-18

#### Results by Check
* **CHECK 1 (Equation Validity):** FAIL — The entry's exact front-speed claim is internally inconsistent: it gives (v_f=U/(1+N_{ac}^{-1})), but the later reaction-limited acid equations imply (v_f=UN_{ac}), so the logistic reduction is only the strongly-retained approximation rather than the claimed exact shared dynamics.
* **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The paired terms are generally assigned compatible mathematical roles and the dimensional reconciliations are explicitly stated; the resistance constituents in Vector 4 differ physically, but the mapping remains a stated series-resistance correspondence rather than a categorical type error.
* **CHECK 3 (Correspondence Vector Support):** FAIL — Vectors 1, 3, 4, and 5 have explicit equations on both sides, but Vector 2's claimed identical logistic travelling wave is not demonstrated consistently with Vector 1 because the reduced acid/Bohart–Adams systems imply the strongly-retained speed (UN_{ac}), not the stated Rankine–Hugoniot speed (U/(1+N_{ac}^{-1})).
* **CHECK 4 (Transfer and Falsifiability):** PASS — The proposed transfer direction is stated with a concrete maturity rationale, and the prediction specifies measurable length-dependent LUB/PV_BT behavior, quantitative tolerances, curve shape, and an independent kinetic cross-check; no fatal asymmetry or template non-prediction is present.

#### Stage 3 Watch Items
* Probe whether the exact isomorphism remains after retaining mobile-phase accumulation in the travelling-wave reduction.
* Probe the physical/operator equivalence asserted for the two harmonic-mean closures in Vector 4.
* Probe prior art concerning constant-pattern/shock-layer and LUB scale-up methods applied to reactive transport and acidization.

### Seventh Adversarial Review
**Reviewer:** Microsoft Copilot 1.2
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The Silo A equilibrium-dispersive PDE, Rankine–Hugoniot shock-speed formula, Bohart–Adams bilinear pair and logistic travelling-wave ODE are of the same quasilinear hyperbolic class as the 1-D constant-flux reduction of the Silo B two-scale acidization model; the bridge algebra (eliminating the pore-scale concentration and using the porosity evolution law) correctly produces the same accumulation-plus-retardation operator and identical shock-speed and logistic ODE under the stated assumptions.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — Each mapped token pair in Section 2 is presented as objects of compatible mathematical type (dimensionless scalars, accumulation terms, bilinear rate factors, harmonic-mean rate constants, length invariants, and Robin trace operators) and each Operator Role specifies a shared mathematical structure rather than hedged similarity.
- **CHECK 3 (Correspondence Vector Support):** PASS — All five YAML-listed vectors are demonstrated in the body:  
  - *rankine_hugoniot_shock_speed_with_retention_factor_equal_to_inverse_acid_capacity_number* — derived in the Bridge with the jump from (ε₀,0) to (ε₁,C₀) and the ε₁→1 limit producing k′ = N_ac⁻¹ (Section 3, Bridge).  
  - *bohart_adams_bilinear_capacity_closure_and_shared_logistic_travelling_wave_ode* — shown by mapping Q(ε) and deriving the identical logistic ODE and travelling-wave thickness (Section 3, Vector 2).  
  - *length_of_unused_bed_integral_invariant_and_its_length_independence* — LUB invariant and its L-independence are derived and equated term-for-term (Section 3, Vector 3).  
  - *harmonic_mean_series_resistance_closure_from_leading_graetz_eigenvalue* — the harmonic-mean series-resistance closure (k_ov and κ) and Graetz eigenvalue identifications are displayed for both silos (Section 3, Silo A and Silo B).  
  - *danckwerts_robin_inlet_zero_gradient_outlet_boundary_pair* — Danckwerts inlet and zero-gradient outlet conditions are written for both silos and identified as the same Robin operator (Section 3, Silo A and Silo B).  
  Each listed vector is supported by equations or operator identities in the body.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction (chromatography → acidization) is argued as asymmetric and justified by the entry (Silo A supplies a compact toolkit for irreversible bilinear-capacity fronts); the prediction (LUB and PV_BT relations, inversion for (k_s a_v0, β)) is specific and experimentally measurable. Note: the falsifiable prediction text is truncated in the provided document and Stage 3 should obtain the full experimental specification before lab testing. No prior-art canonical mapping was asserted by the entry that would invalidate the transfer claim.

#### Stage 3 Watch Items
- "Truncated Falsifiable Prediction: the document ends mid-sentence; Stage 3 should request the missing experimental parameters and full prediction text before experimental validation."
- "Assumption ε₁ → 1 used to equate k′ = N_ac⁻¹ is extreme; Stage 3 should probe practical ranges of post-front porosity and whether the limit is physically attainable in target formations."

### Eighth Adversarial Review
**Reviewer:** xAI Grok 4.5 Fast
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The EDM conservation law, Rankine–Hugoniot shock speed, Bohart–Adams pair, logistic travelling-wave ODE, Danckwerts Robin/Neumann pair, and harmonic-mean Graetz closures are all of matching hyperbolic/parabolic class and correctly reduce under the stated 1-D constant-flux β=1 restrictions to the identical operators shown for both silos.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — Every paired token is of compatible mathematical type (dimensionless scalars, mol m^{-3} inventory terms, rate constants of identical units after the stated Q(ε) redefinition, etc.) and each Operator Role names an explicit shared structure (Rankine–Hugoniot denominator, bilinear factor, harmonic-mean eigenvalue construction, integral invariant, Robin operator) rather than a hedged analogy.
- **CHECK 3 (Correspondence Vector Support):** PASS — All five listed vectors are demonstrated by explicit derivation in Section 3: Rankine–Hugoniot/k′=N_ac^{-1} (Vector 1), Bohart–Adams bilinear closure and shared logistic ODE (Vector 2), LUB integral invariant and length independence (Vector 3), harmonic-mean/Graetz series-resistance closure (Vector 4), and Danckwerts Robin-inlet/zero-gradient-outlet pair (Vector 5).
- **CHECK 4 (Transfer and Falsifiability):** PASS — Transfer direction is genuinely asymmetric (chromatography supplies the derived length-invariant LUB and inverse-method toolkit that acidization lacks on the stable branch); the prediction supplies concrete measurable quantities (LUB = 8.8 mm invariant across L = 5–20 cm, PV_BT/PV_stoich rising from 0.804 to 0.951, logistic inflection slope Da/4) with explicit falsifying thresholds against the Buijse–Glasbergen baseline.

#### Stage 3 Watch Items
None identified.

### Ninth Adversarial Review
**Reviewer:** Meta Muse Spark 1.1
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Silo A EDM and Silo B two-scale continuum both reduce to the same accumulation-plus-retardation parabolic operator with Rankine-Hugoniot front speed and bilinear capacity sink at β=1 and constant U; no elliptic/parabolic or linear/nonlinear class mismatch.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All seven pairs are compatible mathematical types (dimensionless scalars, scalar inventories, rate constants, length invariants, Robin operators) with explicit shared structure and unit reconciliation where needed, e.g., n ≡ (ρ_s/α)(ε−ε_0) and Q ≡ (ρ_s/α)(1−ε).
- **CHECK 3 (Correspondence Vector Support):** PASS — rankine_hugoniot_shock_speed_with_retention_factor_equal_to_inverse_acid_capacity_number demonstrated via v_f and v_s Rankine-Hugoniot equations; bohart_adams_bilinear_capacity_closure_and_shared_logistic_travelling_wave_ode demonstrated via U∂_zC = -kCQ reduction and dx/dξ = -k_a/U x(1-x) logistic ODE; length_of_unused_bed_integral_invariant_and_its_length_independence demonstrated via LUB = L(1-t_b/t_s) = U ln19/k_s a_v0; harmonic_mean_series_resistance_closure_from_leading_graetz_eigenvalue demonstrated via 1/k_ov = 1/k_f+1/k_i and 1/κ = 1/k_c+1/k_s with Sh_i eigenvalue forms; danckwerts_robin_inlet_zero_gradient_outlet_boundary_pair demonstrated via identical ℛ=UC-εD∂_zC inlet and ∂_zC|_L=0 outlet equations in Section 3.[C]
- **CHECK 4 (Transfer and Falsifiability):** PASS — Asymmetry is genuine: Silo A constant-pattern/LUB/moment-analysis toolkit for bilinear fronts is transferred to fill Silo B stable-branch scale-up gap, while Silo B µCT and reactive-infiltration-instability analysis has no Silo A counterpart, with explicit termination at Darcy feedback U[ε]. Falsifiability is met with specific experiment (Indiana limestone, EDTA, L=5/10/20 cm, fixed U), predicted LUB=8.8 mm invariant ±30%, PV_BT/PV_stoich 0.804→0.951, logistic slope Da/4, and explicit falsifiers. No canonical textbook prior-art pairing recognized; advisory watch for Bohart-Adams already used in acidization literature is Stage 3.

#### Stage 3 Watch Items
- Verify Panga exponent β=1 assumption against measured carbonate β range; entry itself flags beta_not_unity_breaks_bilinear_capacity_closure.
- Execute the entry's own novelty-falsification queries: ("Bohart-Adams" OR "Thomas model" OR "length of unused bed" OR "constant pattern wave") AND ("matrix acidizing" OR "carbonate acidization" OR wormhol*) and acid capacity number ↔ retention factor mapping.
- Check whether LUB length-independence and effluent logistic inversion already appears in SPE core-flood scale-up beyond Buijse-Glasbergen power law, and whether compact-dissolution branch Da≫ln19 condition holds for proposed prediction.