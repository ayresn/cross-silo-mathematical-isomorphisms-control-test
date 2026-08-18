---
sid_metadata:
  entry_id: "CONTROL-SID-0022"
  schema_version: "2.0-control"
  maturity_stage: "candidate"
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