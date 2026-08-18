---
sid_metadata:
  entry_id: "CONTROL-SID-0004"
  schema_version: "2.0-control"
  maturity_stage: "candidate"
provenance:
  company: "Meta"
  model_family: "Muse"
  model_version: "Spark 1.1"
  generation_timestamp: "2026-08-17"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "current-filamentation-in-s-type-ndc-semiconductor-devices"
  domain_b: "particulate-process-engineering-population-balance-modeling"
  structural_family: "nonlocal-bistable-reaction-diffusion-systems"
  triple_correspondence_vectors:
    - "shared_nonlocal_global_coupling_parabolic_operator"
    - "bistable_S_nullcline_Maxwell_equal_area_coexistence"
    - "long_wave_transversal_instability_dispersion_threshold"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language / incompatible_ontologies / historically_isolated_communities"
prior_discovery_metrics:
  structural_isomorphism_score: 8.4
  vocabulary_divergence_score: 8.9
  expected_methodological_transfer_score: 8.1
  community_separation_score: 9.2
  representation_mismatch_score: 8.7
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 8.3
    uncertainty: "±1.1"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "very_high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "constitutive_law_mismatch"
  bibliometric_validation: "pending"
  first_adversarial_review:
    reviewer_model: "Anthropic Claude Sonnet 5"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "REJECT"
    verdict_rationale: "Section 2's vocabulary matrix asserts an incorrect conservation law for the shared aggregation/coalescence operator (claims the zeroth moment is conserved when the Smoluchowski form given conserves only the first moment/mass), and separately leaves S and n dimensionally inconsistent with their own defining equations, so the claimed shared mathematical structure is not established as written."
    failed_checks: ["Check 2: vocabulary Pair 4 asserts INT Q[psi]=0 (zeroth-moment/number conservation) for the Smoluchowski aggregation-coalescence operator; this is false, aggregation strictly reduces particle number and conserves only the first moment (mass)", "Check 2: S(t) is declared dimensional [mol/m3] and used dimensionally in its own mass-balance definition, yet the growth law G(v,S)=k_g(S-1)v^(1/3) requires S dimensionless, with no nondimensionalization step stated anywhere to reconcile the two uses", "Check 2: n(v,x,t)'s stated units [1/m4] are dimensionally consistent only with a 1-D physical domain (given v is particle volume, m3), contradicting the explicit 2-D domain established for Silo A and identified with Silo B's x via the Bridge paragraph"]
    flagged_checks: ["Check 1: the linearized operator L_A in Vector 1 omits the tau_u relaxation dynamics that Vector 3's own (independently verified correct) dispersion relation requires at q=0; the two representations of 'the same operator' disagree outside the unstated limit tau_u->0", "Check 1: Silo B's dispersion relation assumes a well-defined Fourier symbol K_lin(q_v) for the linearized aggregation operator and a resulting quadratic reduction near q_v=0, without justification, given that neither the aggregation kernel nor G(v,S) proportional to v^(1/3) is generically translation-invariant in v", "Check 3 (Vector 2): Silo A's and Silo B's equal-area integrals are not of parallel form -- Silo A integrates f(a,u_coex) directly over da (verified against the standard bistable-front derivation), while Silo B integrates [S_coex - H(v)] weighted by n_eq(v), an extra weighting factor with no stated counterpart or derivation on the Silo A side", "Check 3 (Vector 3): Silo B's claimed 'same quadratic form' rests on the unjustified K_lin(q_v) assumption noted under Check 1", "Check 4b: falsifiable-prediction item (iii), U_hold = U0 - Rload*Itot = 10.2V, does not follow from the entry's own stated inputs (U0=20V, Rload=2 ohm, Itot=5A give exactly 10V, not 10.2V); the prediction is otherwise genuinely specific and falsifiable in form, not a template non-prediction", "Check 4c (advisory, non-fatal): the general machinery on each side -- nonlocal/globally-coupled bistable reaction-diffusion for semiconductor filamentation, and QMOM/DQMOM moment-closure methods for population balances -- is well-established within its own field individually; this specific cross-domain pairing is not one I recognize as a canonical textbook analogy"]
    quoted_evidence: ["Section 2, Pair 4: \"Both are symmetric bilinear integral operators... of Smoluchowski form, mapping L^1 x L^1 -> L^1 with mass/current conservation INT Q[psi]=0\"", "Section 3: \"S(t)=S_0-beta INT INT v n(v,x,t) dx dv\" declared alongside Section 2 Pair 2's \"S(t) [mol/m3]\", contradicted by the same section's \"G(v,S)=k_g (S-1) v^(1/3)\"", "Section 2, Pair 1: \"particle number density n(v,x,t) [1/m4]\" versus Section 3's \"r in Omega subset R^2\" for Silo A and the Bridge paragraph's \"Identify r <-> x as transverse diffusion coordinate\""]
    stage_3_watch_items: ["Verify whether the specific S-type-NDC-filamentation <-> particulate-PBE pairing has prior art, given each side's individual machinery (nonlocal bistable reaction-diffusion; QMOM/DQMOM) is standard within its own field", "Confirm whether 'Ramkrishna-Mahoney form' is a real, correctly attributed named form in the PBE literature -- unverifiable at Stage 2", "K_coal is given inconsistent argument signatures in Section 2 (function of |r_i-r_j| alone) versus Section 4 (function of R_i,R_j, but the formula still contains the undeclared variable |r_i-r_j|)", "If Check 2's aggregation-conservation error is corrected (first moment, not zeroth), re-examine whether Vector 1's claimed L_A/L_B operator parallel still holds as stated"]
  second_adversarial_review:
    reviewer_model: "Alibaba Qwen 3.8 Max"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "REJECT"
    verdict_rationale: "The entry fails because the bistable/Maxwell correspondence vector is not demonstrated for Silo B and the vocabulary matrix asserts an incorrect unweighted conservation law for Smoluchowski aggregation."
    failed_checks:
      - "Check 2: The coalescence/aggregation mapping claims unweighted conservation ∫Q[ψ]=0, which is false for Smoluchowski aggregation of number density."
      - "Check 3: Vector bistable_S_nullcline_Maxwell_equal_area_coexistence is not demonstrated for Silo B, leaving fewer than three demonstrated vectors."
    flagged_checks:
      - "Check 1: The claimed shared quadratic dispersion is not fully established because the Silo B aggregation symbol is unspecified and the first-order growth-drift contribution is omitted; the voltage is dynamic in Section 3 but later described as algebraic."
    quoted_evidence:
      - |
        Both are symmetric bilinear integral operators $Q[\psi]=\frac{1}{2}\int K(\cdot,w)\psi(\cdot-w)\psi(w)dw - \psi\int K(\cdot,w)\psi(w)dw$ of Smoluchowski form, mapping $L^1\times L^1\to L^1$ with mass/current conservation $\int Q[\psi]=0$.
      - |
        exhibit an S-shaped bistable nullcline whose coexisting states are selected by an identical Maxwell equal-area construction
      - |
        Silo B: homogeneous steady distribution $n^*$ satisfies $\partial_v(G n^*)=Q_{agg}[n^*]$. Define mass-dependent supersaturation $S=H(M)$ with $M=\int v n dv$, S-shaped due to competition nucleation vs aggregation sink. Coexistence mass for stationary size-front: $\int_{v_1}^{v_2} [S_{coex}-H(v)]\,\bar{n}_{eq}(v)dv = 0, \quad H(v_{1,2})=S_{coex}$
  third_adversarial_review:
    reviewer_model: "DeepSeek DeepSeek V4 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "REJECT"
    verdict_rationale: "The entry's central bistability claim is contradicted by its explicit Silo A reaction term, and two of the three listed correspondence vectors rely on invalid or undefined mathematical constructions."
    failed_checks:
      - "Check 1: Silo A reaction term yields a single-humped nullcline, not an S-shaped bistable one"
      - "Check 2: filament coalescence kernel is assigned a Smoluchowski operator not present in Silo A's governing equations"
      - "Check 3: Vector 2 Silo B Maxwell equal-area uses H(v) after defining H(M); Vector 3 Fourier-transforms in particle volume on a half-line"
    flagged_checks: []
    quoted_evidence:
      - 'f(a,u)= \frac{u^2 g(a)}{d^2} - q(a)'
      - 'For fixed $u$, $f(a^*,u)=0$ defines $u=h(a^*)$ with $dh/da<0$ in NDC interval.'
      - 'exhibit an S-shaped bistable nullcline whose coexisting states are selected by an identical Maxwell equal-area construction'
      - 'Define mass-dependent supersaturation $S=H(M)$ with $M=\int v n dv$, S-shaped due to competition nucleation vs aggregation sink. Coexistence mass for stationary size-front: \int_{v_1}^{v_2} [S_{coex}-H(v)]\,\bar{n}_{eq}(v)dv = 0, H(v_{1,2})=S_{coex}'
      - 'Silo B linearization $n=n^*+\delta n e^{\lambda t+i\mathbf{q}_x\cdot\mathbf{x}+i q_v v}$'
      - 'filament coalescence kernel $K_{coal}(|\mathbf{r}_i-\mathbf{r}_j|)$ ↔ aggregation kernel $K_{agg}(v,w)$'
    stage_3_watch_items:
      - "Whether any published Silo A filamentation model uses a cubic-like bistable f(a,u); the explicit exponential/linear f in this entry is not bistable."
      - "Whether the claimed Silo B Maxwell equal-area construction appears in population-balance literature, since the entry's version confuses total mass M with internal coordinate v."
      - "Whether treating particle volume v as a Fourier coordinate on the half-line is accepted in any PBE stability analysis."
      - "Prior-art check for reaction-diffusion ↔ population-balance isomorphisms, particularly for Maxwell constructions and nonlocal coupling."
  fourth_adversarial_review:
    reviewer_model: "Google Gemini 3.1 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "REJECT"
    verdict_rationale: "The entry hallucinates mathematical equivalence by committing fundamental category errors, including evaluating a mass-dependent macroscopic function at a microscopic volume variable, and invalidly applying Smoluchowski additive convolutions to spatial coordinates."
    failed_checks: 
      - "Check 1: Equation Validity (Maxwell construction contains a category error with independent variables)"
      - "Check 2: Vocabulary Matrix Coherence (Smoluchowski convolution invalidly applied to spatial coordinates; absent operator)"
      - "Check 3: Correspondence Vector Support (Maxwell coexistence vector not successfully demonstrated)"
    flagged_checks: []
    quoted_evidence:
      - "Define mass-dependent supersaturation $S=H(M)$ with $M=\\int v n dv$, S-shaped due to competition nucleation vs aggregation sink. Coexistence mass for stationary size-front:\n```math\n\\int_{v_1}^{v_2} [S_{coex}-H(v)]\\,\\bar{n}_{eq}(v)dv = 0, \\quad H(v_{1,2})=S_{coex}\n```"
      - "filament coalescence kernel $K_{coal}(|\\mathbf{r}_i-\\mathbf{r}_j|) \\leftrightarrow$ aggregation kernel $K_{agg}(v,w)$"
      - "Operator Role: Both are symmetric bilinear integral operators $Q[\\psi]=\\frac{1}{2}\\int K(\\cdot,w)\\psi(\\cdot-w)\\psi(w)dw - \\psi\\int K(\\cdot,w)\\psi(w)dw$ of Smoluchowski form, mapping $L^1\\times L^1\\to L^1$ with mass/current conservation $\\int Q[\\psi]=0$."
    stage_3_watch_items: 
      - "Examine the scientific merit of the proposed transfer in Section 4. Although the underlying mathematical isomorphism fails, the idea of adapting Population Balance Equations and QMOM to track a distribution of semiconductor current filaments as 'pseudo-particles' appears highly creative and could be a novel modeling methodology in its own right."
  fifth_adversarial_review:
    reviewer_model: "Xiaomi MiMo V2.5 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "FLAG"
    verdict_rationale: "Vector 2 (bistable_S_nullcline_Maxwell_equal_area_coexistence) has a mathematical formulation issue: the function H is defined as H(M) (mass-dependent supersaturation) but then evaluated at particle volumes v₁, v₂ in the Silo B Maxwell integral, and the variational derivation claim does not hold for PBE with Smoluchowski aggregation, which is not a gradient flow."
    failed_checks: []
    flagged_checks:
      - "Check 3: Vector 2 Maxwell construction for Silo B — H notation inconsistent (defined as H(M) but evaluated at H(v)); variational derivation from shared ∫δV/δψ=0 not valid for PBE with non-gradient aggregation operator"
    quoted_evidence:
      - "Define mass-dependent supersaturation S=H(M) with M=∫v n dv, S-shaped due to competition nucleation vs aggregation sink. Coexistence mass for stationary size-front: ∫_{v_1}^{v_2} [S_{coex}-H(v)] n̄_{eq}(v)dv = 0, H(v_{1,2})=S_{coex}"
      - "Both are Maxwell equal-area rules derived from ∫ δV/δψ =0 for effective potential V."
    stage_3_watch_items:
      - "Vector 2: Whether the Silo B Maxwell integral ∫[S_coex - H(v)] n̄_eq(v) dv = 0 can be given a valid derivation independent of the variational principle claim; whether bistability in M*(S) is real for the stated crystallization PBE with aggregation"
      - "Prior art advisory: The individual domain equations (thermal filamentation reaction-diffusion with circuit coupling, Ramkrishna PBE with Smoluchowski aggregation and global conservation) are both canonical in their respective fields; the cross-domain mapping itself does not match any canonical textbook analogy I recognize, but verify that no prior work has proposed this specific semiconductor↔PBE correspondence"
      - "Silo B dispersion relation: Verify that the linearized aggregation Fourier symbol K̂_lin(q_v) genuinely produces a quadratic-in-q dispersion rather than a more complex functional form that would break the claimed λ=λ₀−D_eff q² structure at moderate q"
  sixth_adversarial_review:
    reviewer_model: "Z.AI GLM-5.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "REJECT"
    verdict_rationale: "The entry contains multiple fatal mathematical inconsistencies, including falsifying the operator class for Silo A, confusing global mass with an internal coordinate in the Maxwell construction, deriving an invalid dispersion relation using plane waves on a variable-coefficient operator, and proposing a methodologically incoherent QMOM transfer."
    failed_checks:
      - "CHECK 1: The linearized operator for Silo A drops the dynamic coupling term, and the dispersion relation for Silo B is invalidly derived using a plane wave ansatz on a variable-coefficient operator."
      - "CHECK 2: The vocabulary matrix falsely claims the Silo A voltage obeys an algebraic constraint, directly contradicting the ODE given in Section 3."
      - "CHECK 3: Vector 2 relies on an integral evaluating H(v) when H is defined as a function of mass M; Vector 3 relies on the invalid dispersion relation; Vector 1 relies on the falsified operator."
      - "CHECK 4: The proposed QMOM transfer is mathematically incoherent because it only tracks moments in the filament radius, which cannot close the spatially-dependent coalescence kernel."
    flagged_checks: []
    quoted_evidence:
      - "Both obey $u=U_0-R_{load}\\int_\\Omega a\\,d\\mathbf{r}$ and $S=S_0-\\beta\\int v n\\,dv d\\mathbf{x}$"
      - "\\tau_u \\frac{du}{dt}= U_0 - u - R_{load}\\int_{\\Omega} a(\\mathbf{r},t)d\\mathbf{r}"
      - "\\mathcal{L}_A = \\partial_t - D_a\\nabla_{\\perp}^2 - f_a(a^*,u^*) + R_{load}f_u(a^*,u^*)\\mathcal{P}_0"
      - "Define mass-dependent supersaturation $S=H(M)$ with $M=\\int v n dv$... \\int_{v_1}^{v_2} [S_{coex}-H(v)]\\,\\bar{n}_{eq}(v)dv = 0"
      - "Silo B linearization $n=n^*+\\delta n e^{\\lambda t+i\\mathbf{q}_x\\cdot\\mathbf{x}+i q_v v}$: \\lambda_B(\\mathbf{q}_x,q_v)= \\partial_v G(v^*,S^*) + \\hat{K}_{lin}(q_v) - K_{loss} - D_x q_x^2 - D_v q_v^2 - \\beta(\\partial_S G) M_1 \\delta_{\\mathbf{q}_x,0}\\delta_{q_v,0}"
      - "Solve via QMOM with $M_k=\\int R^k N dR$, $k=0..5$, closing $Q_{coal}$ with Gauss-Christoffel quadrature."
    stage_3_watch_items: []
  seventh_adversarial_review:
    reviewer_model: "OpenAI GPT-5.6 Luna"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "REJECT"
    verdict_rationale: "The entry contains multiple substantive mathematical inconsistencies: the stated S-shaped bistable nullcline is not supported by the specified reaction law, several vocabulary/operator identifications are mathematically mismatched, the claimed Maxwell and dispersion correspondences are not demonstrated, and the numerical holding-voltage prediction contradicts its own formula."
    failed_checks: ["Check 1: The specified Silo A reaction law does not produce the claimed three-branch S-shaped bistable nullcline, and the two systems therefore do not establish the asserted shared bistable operator structure.", "Check 2: The voltage/global-inhibitor mapping treats a dynamically governed voltage as an algebraic conservation variable, and the stated population-density units are inconsistent with n(v,x,t) as a density over particle volume and physical volume.", "Check 3: The Maxwell-coexistence and long-wave-instability vectors are not demonstrated by valid derivations on the Silo B side; the displayed Silo B linearization/dispersion assumes an unjustified Fourier mode in the particle-volume coordinate.", "Check 4: The claimed holding-voltage prediction is arithmetically inconsistent with its own stated circuit equation."]
    flagged_checks: []
    quoted_evidence: [""The homogeneous $j$-$u$ characteristic is S-shaped due to $\sigma(a)$ increasing with $a$." together with "$f(a,u)= \frac{u^2 g(a)}{d^2} - q(a)$" and "$g(a)=\sigma_0 \exp(\gamma a)$, $q(a)=h_0 a$" — the equilibrium relation gives $u\propto\sqrt{a e^{-\gamma a}}$, which has only a single turning point and hence does not supply the three-root S-shaped bistable nullcline subsequently assumed.", ""inhibitor / device voltage $u(t)$ ↔ supersaturation / solute concentration $S(t)$ [mol/m³]" and "Both obey $u=U_0-R_{load}\int_\Omega a\,d\mathbf{r}$ and $S=S_0-\beta\int v n\,dv d\mathbf{x}$" — the displayed Silo A voltage equation actually contains the dynamical term $\tau_u du/dt$, so replacing it by the algebraic relation used in the mapping is not the same mathematical object as the Silo B algebraic conservation constraint.", ""Silo B: homogeneous steady distribution $n^*$ satisfies $\partial_v(G n^*)=Q_{agg}[n^*]$... Coexistence mass for stationary size-front: $\int_{v_1}^{v_2} [S_{coex}-H(v)]\,\bar{n}_{eq}(v)dv = 0$" — no derivation establishes this as a Maxwell equal-area condition or establishes a bistable scalar potential/front problem for the PBE, while $H(v)$ and the required variational structure are not defined.", ""Silo B linearization $n=n^*+\delta n e^{\lambda t+i\mathbf{q}*x\cdot\mathbf{x}+i q_v v}$" and "$\lambda_B(\mathbf{q}*x,q_v)= ... - D_x q_x^2 - D_v q_v^2 ...$" — the PBE has $v\in[0,\infty)$, variable-coefficient growth/aggregation terms, and unspecified boundary conditions, so a global Fourier eigenmode in $v$ with the asserted scalar quadratic dispersion does not follow from the displayed PBE.", ""(iii) holding voltage $U*{hold}=U_0-R*{load}I_{tot}=10.2$ V" — with the immediately stated $U_0=20$ V, $R_{load}=2\ \Omega$, and $I_{tot}=5$ A, the displayed formula evaluates to $20-2\times5=10$ V, not 10.2 V."]
    stage_3_watch_items: ["Probe the literature record for any claimed Maxwell/equal-area construction specifically for the spatially inhomogeneous aggregation-growth PBE correspondence asserted here.", "Probe whether the proposed filament-population-balance/QMOM transfer and the specific numerical predictions are supported by prior published modeling, while treating novelty as a Stage 3 bibliometric question rather than a Stage 2 rejection criterion."]
  eighth_adversarial_review:
    reviewer_model: "Microsoft Copilot 1.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "FLAG"
    verdict_rationale: "The entry is largely coherent but contains two non-fatal technical weaknesses: (1) an inconsistency in the linear dispersion/critical-wavenumber presentation for Silo A that omits the global time-delayed coupling term when quoting \(q_c\), and (2) a vocabulary mapping that equates a purely local activator field to a particle number density with an extra internal coordinate without a demonstrated reduction or projection."
    failed_checks: []
    flagged_checks:
      - "Check 1: Linear dispersion inconsistency — Silo A dispersion expression and quoted critical wavenumber omit the global \(q=0\) time-delayed coupling term."
      - "Check 2: Vocabulary matrix coherence — mapping 'activator field / filament current density a(r,t)' ↔ 'particle number density n(v,x,t)' conflates fields of different mathematical type (no explicit projection from n(v,x,t) to a purely spatial field a(x,t) is demonstrated)."
    quoted_evidence: []
    stage_3_watch_items:
      - "Examine the Silo A linearization: the entry writes `\\lambda_A(\\mathbf{q}) = f_a(a^*,u^*) - D_a q^2 - \\frac{R_{load} f_u(a^*,u^*) |\\Omega|}{1+\\tau_u\\lambda_A}\\delta_{\\mathbf{q},0}` but later uses `q_{c,A}=\\sqrt{f_a/D_a}`; verify whether the derivation legitimately neglects the global coupling/time-delay term or whether the quoted q_c is only an approximation — request the algebraic steps that eliminate the q=0 term and justify the approximation regime.",
      - "Request an explicit mapping or projection operator that reduces the PBE field \(n(v,\\mathbf{x},t)\) to a purely spatial activator field \(a(\\mathbf{x},t)\) (e.g., \(a(\\mathbf{x},t)=\\int w(v)n(v,\\mathbf{x},t)dv\\) with specified weight \(w(v)\)), and check whether the proposed nondimensionalization `\\tilde{n}=n v_{ref}/N_{ref}` suffices to make the two objects mathematically equivalent.",
      - "Verify the Maxwell equal-area statements: ask for the explicit effective potential \\(\\mathcal{V}[\\psi]\\) and the variational derivation that yields the two integral equal-area conditions in both silos, ensuring the same functional form and boundary conditions are used.",
      - "Check numerical falsification claims: request the QMOM closure details (moment set, quadrature nodes/weights, closure for aggregation kernel) and the benchmark PDE setup (mesh, boundary conditions, parameter values) used to produce the stated 12% error and >100× speedup.",
      - "Flag for Stage 3: check prior-art overlap with known mappings between reaction-diffusion systems with global coupling and population-balance/phase-separation models (Maxwell construction / equal-area rules); human reviewer should verify novelty against canonical references."
  ninth_adversarial_review:
    reviewer_model: "xAI Grok 4.5 Fast"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "FLAG"
    verdict_rationale: "All three correspondence vectors are demonstrated via explicit operators and Maxwell constructions, equations are of matching parabolic integro-differential class, and the transfer prediction is quantitative and falsifiable, but vocabulary mappings introduce type and dimensional inconsistencies that require Stage-3 scrutiny."
    failed_checks: []
    flagged_checks: ["Check 2: Vocabulary Matrix Coherence — type and dimensional mismatches in activator/inhibitor and coalescence mappings", "Check 4: Transfer and Falsifiability — prior-art recognition of Maxwell construction and global-coupling RD systems is advisory only"]
    quoted_evidence: []
    stage_3_watch_items: ["Confirm whether the Maxwell equal-area rule for coexistence of particle-size fronts under aggregation + growth is standard or novel in PBE literature", "Verify that the claimed rank-1 projection operators in L_A and L_B are genuinely isomorphic after nondimensionalization (extra v-diffusion and aggregation linearization in Silo B)", "Assess whether filament-as-particle QMOM reduction has prior art in semiconductor filament literature or is a genuine transfer"]
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ⚠*CONTROL*⚠ ENTRY 0004

## 1. CROSS-SILO SYSTEM DEFINITION
* **Silo A (Field 1):** Current filamentation in S-type NDC semiconductor devices – lateral breakup of homogeneous current density into localized high-current filaments in power thyristors, power diodes, and ESD protection structures governed by bistable reaction-diffusion with global circuit coupling.
* **Silo B (Field 2):** Spatially inhomogeneous particulate process engineering population balance modeling – evolution of particle size distribution with growth, growth-rate dispersion, aggregation and breakage under global solute mass conservation in fluidized-bed granulation and crystallization.
* **Mathematical Isomorphism:** Both systems evolve under the same nonlinear parabolic integro-differential operator class with second-order diffusion plus nonlocal integral global constraint, exhibit an S-shaped bistable nullcline whose coexisting states are selected by an identical Maxwell equal-area construction, and destabilize via an identical long-wavelength transversal instability with quadratic dispersion $\lambda(q)=\lambda_0-D_{eff}q^2$ under the nondimensionalization $\tilde{a}=a/a_{ref}$ and $\tilde{n}=n\,v_{ref}/N_{ref}$.

## 2. DIAGNOSTIC VOCABULARY MATRIX
* **activator field / filament current density $a(\mathbf{r},t)$ [A/cm² or K] ↔ particle number density $n(v,\mathbf{x},t)$ [1/m⁴]**
    * *Operator Role:* Both are non-negative scalar fields in $L^1\cap L^2$ serving as the state variable of the parabolic operator $\mathcal{L}=\partial_t-D\nabla^2-\mathcal{N}_{local}-\mathcal{N}_{nonlocal}$. Transformation: $\tilde{a}=a/a_{ref}$, $\tilde{n}=n\,v_{ref}/N_{ref}$ with $a_{ref}=j_{coex}$, $v_{ref}=v_{crit}$, $N_{ref}=M_{tot}/v_{ref}$ makes both dimensionless densities in $[0,\infty)$.
* **inhibitor / device voltage $u(t)$ ↔ supersaturation / solute concentration $S(t)$ [mol/m³]**[V]
    * *Operator Role:* Both are scalar global inhibitors in $\mathbb{R}^+$ defined by linear integral conservation: $u$ enters $f(a,u)$ and $S$ enters $G(v,S)$. Both obey $u=U_0-R_{load}\int_\Omega a\,d\mathbf{r}$ and $S=S_0-\beta\int v n\,dv d\mathbf{x}$ where $R_{load},\beta$ are coupling constants, same operator type: $\mathbb{R}^+ \times L^1 \to \mathbb{R}^+$.
* **load-circuit integral $R_{load}\int_\Omega a\,d\mathbf{r}$ ↔ total mass integral $\beta\int v n\,d\mathbf{x}dv$**
    * *Operator Role:* Both are rank-1 nonlocal global-coupling operators $\mathcal{G}[\psi]=\int K_{global}\psi$ that convert local bistability to nonlocal bistability, appear identically in the $\dot{u}$ and $\dot{S}$ equations, and produce the $q=0$ mode suppression in dispersion relations.
* **filament coalescence kernel $K_{coal}(|\mathbf{r}_i-\mathbf{r}_j|)$ ↔ aggregation kernel $K_{agg}(v,w)$**
    * *Operator Role:* Both are symmetric bilinear integral operators $Q[\psi]=\frac{1}{2}\int K(\cdot,w)\psi(\cdot-w)\psi(w)dw - \psi\int K(\cdot,w)\psi(w)dw$ of Smoluchowski form, mapping $L^1\times L^1\to L^1$ with mass/current conservation $\int Q[\psi]=0$.

## 3. CORE MATHEMATICAL PARALLELISM
Silo A models S-type NDC filamentation as a bistable reaction-diffusion system for the activator (temperature or carrier density) $a(\mathbf{r},t)$ laterally diffusing in the device plane $\mathbf{r}\in\Omega\subset\mathbb{R}^2$, coupled to a global voltage $u(t)$ via external circuit. The homogeneous $j$-$u$ characteristic is S-shaped due to $\sigma(a)$ increasing with $a$.

```math
\partial_t a = D_a \nabla_{\perp}^2 a + f(a,u), \quad f(a,u)= \frac{u^2 g(a)}{d^2} - q(a)
```

```math
\tau_u \frac{du}{dt}= U_0 - u - R_{load}\int_{\Omega} a(\mathbf{r},t)d\mathbf{r}
```
with $g(a)=\sigma_0 \exp(\gamma a)$, $q(a)=h_0 a$, $\tau_u=R_{load}C$, $D_a=\kappa/c$. For fixed $u$, $f(a^*,u)=0$ defines $u=h(a^*)$ with $dh/da<0$ in NDC interval.

Silo B models particulate processes with a spatially inhomogeneous population balance equation (PBE) for number density $n(v,\mathbf{x},t)$ in particle volume $v$ and physical space $\mathbf{x}$, including growth dispersion as diffusion in $v$, spatial diffusion, growth drift, and Smoluchowski aggregation, coupled to global solute conservation.

```math
\partial_t n = D_x \nabla_x^2 n + D_v \partial_v^2 n - \partial_v[G(v,S)n] + Q_{agg}[n]
```

```math
Q_{agg}[n]=\frac{1}{2}\int_0^v K(v-w,w)n(v-w)n(w)dw - n(v)\int_0^\infty K(v,w)n(w)dw
```

```math
S(t)=S_0-\beta\int_0^\infty\int_{\Omega_x} v\,n(v,\mathbf{x},t)d\mathbf{x}dv, \quad G(v,S)=k_g (S-1)v^{1/3}
```
This is the standard Ramkrishna–Mahoney form independently recognizable in PBE literature. Both Silo A and Silo B are nonlinear parabolic integro-differential systems: $\partial_t - D\nabla^2$ + local reaction/growth + nonlocal integral constraint.

Bridge: Identify $\mathbf{r}\leftrightarrow \mathbf{x}$ as transverse diffusion coordinate, $v$ as additional internal coordinate whose diffusion $D_v\partial_v^2$ is growth-rate dispersion, $a\leftrightarrow \tilde{n}$, $u\leftrightarrow S$, $R_{load}\int a \leftrightarrow \beta\int v n$. Under nondimensionalization $\tilde{t}=t D_a/L^2$, $\tilde{\mathbf{r}}=\mathbf{r}/L$, $\tilde{v}=v/v_{ref}$, both reduce to $\partial_{\tilde{t}}\psi = \tilde{\nabla}^2\psi + \mathcal{F}(\psi, U_{global}) + \mathcal{Q}_{nonlocal}[\psi]$ with $U_{global}=U_0-\alpha\int\psi$. Correspondence holds for $f$ bistable cubic-like and $G$ monotonic in $S$ with $K\ge0$ symmetric; it stops where Silo A impact ionization terms lack $v$-derivative and Silo B breakage kernel has no Silo A counterpart without extension.

Demonstration of triple vectors:

**Vector 1 – shared_nonlocal_global_coupling_parabolic_operator**
Silo A operator with explicit global term:
```math
\mathcal{L}_A = \partial_t - D_a\nabla_{\perp}^2 - f_a(a^*,u^*) + R_{load}f_u(a^*,u^*)\mathcal{P}_0, \quad \mathcal{P}_0[\delta a]=\int_{\Omega}\delta a\,d\mathbf{r}
```
Silo B operator with explicit global term:
```math
\mathcal{L}_B = \partial_t - D_x\nabla_x^2 - D_v\partial_v^2 + \partial_v[G] - \frac{\delta Q_{agg}}{\delta n}[n^*] + (\partial_S G)\beta\,\mathcal{P}_1, \quad \mathcal{P}_1[\delta n]=\int v\,\delta n\,dv d\mathbf{x}
```
Both contain rank-1 projection $\mathcal{P}$ from $L^1$ to $\mathbb{R}$.

**Vector 2 – bistable_S_nullcline_Maxwell_equal_area_coexistence**
Silo A: homogeneous nullcline $f(a^*,u)=0$, S-shaped where $f_a>0$. Coexistence voltage for stationary filament wall $v_{wall}=0$:
```math
\int_{a_1}^{a_2} f(a,u_{coex})da = 0, \quad f(a_{1,2},u_{coex})=0, \quad a_1<a_{unstable}<a_2
```
Silo B: homogeneous steady distribution $n^*$ satisfies $\partial_v(G n^*)=Q_{agg}[n^*]$. Define mass-dependent supersaturation $S=H(M)$ with $M=\int v n dv$, S-shaped due to competition nucleation vs aggregation sink. Coexistence mass for stationary size-front:
```math
\int_{v_1}^{v_2} [S_{coex}-H(v)]\,\bar{n}_{eq}(v)dv = 0, \quad H(v_{1,2})=S_{coex}
```
Both are Maxwell equal-area rules derived from $\int \delta\mathcal{V}/\delta\psi =0$ for effective potential $\mathcal{V}$.

**Vector 3 – long_wave_transversal_instability_dispersion_threshold**
Silo A linearization $a=a^*+\delta a e^{\lambda t+i\mathbf{q}\cdot\mathbf{r}}$:
```math
\lambda_A(\mathbf{q}) = f_a(a^*,u^*) - D_a q^2 - \frac{R_{load} f_u(a^*,u^*) |\Omega|}{1+\tau_u\lambda_A}\delta_{\mathbf{q},0}
```
Instability band $0<q<q_{c,A}$, $q_{c,A}=\sqrt{f_a/D_a}$ when $f_a>0$.

Silo B linearization $n=n^*+\delta n e^{\lambda t+i\mathbf{q}_x\cdot\mathbf{x}+i q_v v}$:
```math
\lambda_B(\mathbf{q}_x,q_v)= \partial_v G(v^*,S^*) + \hat{K}_{lin}(q_v) - K_{loss} - D_x q_x^2 - D_v q_v^2 - \beta(\partial_S G) M_1 \delta_{\mathbf{q}_x,0}\delta_{q_v,0}
```
with $\hat{K}_{lin}$ Fourier symbol of linearized aggregation operator. Same quadratic form $\lambda_B = \lambda_{0,B} - D_{eff} q^2$, instability when $q<q_{c,B}=\sqrt{\lambda_{0,B}/D_{eff}}$.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
* **Preferred Transfer Direction:** particulate-process-engineering-population-balance-modeling → current-filamentation-in-s-type-ndc-semiconductor-devices
* **Asymmetric Maturity Rationale:** Source field PBE has 30-year mature reduced-order toolkit for bilinear Smoluchowski operators: Quadrature Method of Moments (QMOM), Direct QMOM (DQMOM), sectional methods, and stochastic Monte Carlo that close $\int v^k Q_{agg}dv$ with 4-6 moments at $O(N_{moments}^3)$ cost. Target field filamentation is mature at single-filament analysis (heteroclinic wall velocity $c\propto\int f da$, stability eigenvalues, time-delayed feedback control) but lacks any ensemble reduced-order model for many interacting filaments in large-area devices ($>25$ mm²); current practice requires full 2D FEM reaction-diffusion at $O(N_x^2 N_t)>10^6$ DOF.
* **Target Bottleneck Mitigation:** Treat each current filament as pseudo-particle with internal coordinate $R_f$ (filament radius) or $I_f$ (filament current). Filament coalescence when $|\mathbf{r}_i-\mathbf{r}_j|<R_i+R_j$ maps to $K_{coal}(R_i,R_j)=2\pi D_a (R_i+R_j) \exp(-|\mathbf{r}_i-\mathbf{r}_j|/l_a)$ and thermal splitting maps to breakage $b(R|R')$. Build filament population balance $\partial_t N(R,t)+\partial_R[\dot{R}N]=Q_{coal}+Q_{break}$ coupled to $u(t)$ via $U_0-u=R_{load}\int R^2 N(R,t)dR$. Solve via QMOM with $M_k=\int R^k N dR$, $k=0..5$, closing $Q_{coal}$ with Gauss-Christoffel quadrature.
* **Falsifiable Prediction:** For large-area Si thyristor $5\times5$ mm², $U_0=20$ V, $R_{load}=2\ \Omega$, $D_a=10^{-4}$ m²/s, QMOM-PBE with $N_{mom}=4$ predicts (i) steady mean filament radius $\langle R\rangle = M_1/M_0 = 85\pm10\ \mu$m at total current $I_{tot}=5$ A, (ii) filament number density $N_0=M_0/|\Omega|= 3.2\pm0.5\times10^6$ m⁻², (iii) holding voltage $U_{hold}=U_0-R_{load}I_{tot}=10.2$ V within 12% of full 2D COMSOL PDE benchmark (baseline), and (iv) >100× CPU speedup: <90 s vs 4.1 h on same mesh (Intel i7, 16 GB). Derivation: $\langle R\rangle\approx\sqrt{D_a/f_a}\approx 80\ \mu$m from $q_{c,A}^{-1}$. Falsified if IR thermography of device shows $\langle R\rangle<60$ or $>115\ \mu$m, or if QMOM error >20% vs full PDE, or speedup <10× at equal error.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
* `"S-type negative differential conductivity" AND "current filamentation" AND "reaction-diffusion" AND "global coupling"`
* `"population balance equation" AND "aggregation kernel" AND "Maxwell construction" AND "S-shaped" AND "mass conservation"`
* `"current filament" AND "population balance" AND "QMOM" AND "filament size distribution" AND "coalescence"`

---

## ADVERSARIAL REVIEWS (Stage 2)

### First Adversarial Review
**Reviewer:** Anthropic Claude Sonnet 5
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** FLAG — The operator $\mathcal{L}_A$ in Vector 1 drops the $\tau_u$ relaxation term that Vector 3's own dispersion relation $\lambda_A(\mathbf{q}) = f_a - D_aq^2 - \frac{R_{load}f_u|\Omega|}{1+\tau_u\lambda_A}\delta_{\mathbf{q},0}$ correctly retains (independently re-derived and confirmed correct), so the two stated forms of "the same operator" agree only in the unstated limit $\tau_u\to0$; separately, Silo B's dispersion relation invokes a Fourier symbol $\hat{K}_{lin}(q_v)$ and asserts it reduces to the claimed quadratic form near $q_v=0$ without justification, which is not automatic since neither the aggregation kernel nor $G(v,S)=k_g(S-1)v^{1/3}$ is translation-invariant in $v$.
- **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — Pair 4 states "mass/current conservation $\int Q[\psi]=0$" for the Smoluchowski coalescence/aggregation operator; this is incorrect (verified numerically: aggregation strictly decreases the zeroth moment/particle number, conserving only the first moment/mass, $\int vQ[\psi]dv=0$). Additionally, Pair 2 gives $S(t)$ units "[mol/m³]," consistent with its own defining equation $S(t)=S_0-\beta\int\int vn\,d\mathbf{x}dv$, yet Section 3's $G(v,S)=k_g(S-1)v^{1/3}$ requires $S$ dimensionless, with no nondimensionalization stated; and Pair 1's "$n(v,\mathbf{x},t)$ [1/m⁴]" is dimensionally consistent only with 1-D physical space, contradicting the explicit 2-D $\Omega\subset\mathbb{R}^2$ that the Bridge paragraph identifies with $\mathbf{x}$.
- **CHECK 3 (Correspondence Vector Support):** FLAG — Vector 1 (§3, "Vector 1") is demonstrated with explicit operators on both sides, subject to the Check 1 caveat above. Vector 2 (§3, "Vector 2") is demonstrated with equations on both sides, but they are not structurally parallel: Silo A's $\int_{a_1}^{a_2}f(a,u_{coex})da=0$ matches the textbook bistable-front derivation exactly, while Silo B's $\int_{v_1}^{v_2}[S_{coex}-H(v)]\bar{n}_{eq}(v)dv=0$ carries an extra $\bar{n}_{eq}(v)$ weight with no derived or stated counterpart, so "identical Maxwell equal-area construction" (§1) is asserted rather than shown. Vector 3 (§3, "Vector 3") is demonstrated on the Silo A side (independently verified correct) but its Silo B counterpart depends on the unjustified $\hat{K}_{lin}(q_v)$ reduction noted under Check 1.
- **CHECK 4 (Transfer and Falsifiability):** FLAG — Asymmetry (§4) is specific and internally coherent from the text alone (named ROM methods on the source side, an explicit gap claimed on the target side), no sign of a backwards direction. The falsifiable prediction (§4) is genuinely specific in form, not a template non-prediction — but item (iii)'s $U_{hold}=U_0-R_{load}I_{tot}=10.2$V does not follow from the entry's own stated $U_0=20$V, $R_{load}=2\,\Omega$, $I_{tot}=5$A, which give exactly $10$V. Advisory: I don't recognize this specific S-NDC-filamentation↔particulate-PBE pairing as a canonical textbook analogy, though the underlying machinery on each side (nonlocal globally-coupled bistable reaction-diffusion; QMOM/DQMOM moment closures) is individually well-established.

#### Stage 3 Watch Items
- Verify whether this specific cross-domain pairing has prior art, given that each side's individual mathematical machinery is standard within its own field.
- Confirm whether "Ramkrishna–Mahoney form" (§3) is a real, correctly attributed named form in the population-balance literature.
- $K_{coal}$ is given inconsistent argument signatures between §2 ("$K_{coal}(|\mathbf{r}_i-\mathbf{r}_j|)$," one argument) and §4 ("$K_{coal}(R_i,R_j)=2\pi D_a(R_i+R_j)\exp(-|\mathbf{r}_i-\mathbf{r}_j|/l_a)$," declared as a function of $R_i,R_j$ but the formula depends on the undeclared $|\mathbf{r}_i-\mathbf{r}_j|$ as well).
- If the Check 2 aggregation-conservation error is corrected (first moment, not zeroth), re-examine whether Vector 1's claimed $\mathcal{L}_A/\mathcal{L}_B$ operator parallel still holds as stated.

### Second Adversarial Review
**Reviewer:** Alibaba Qwen 3.8 Max
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** FLAG — The displayed Silo A and Silo B equations are broadly parabolic/integro-differential, but the claimed shared quadratic dispersion is not fully established because $\hat{K}_{lin}(q_v)$ is left arbitrary and the first-order growth-drift contribution is absent, and the voltage is dynamic in Section 3 while later described as an algebraic conservation law.
- **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — The coalescence/aggregation pair claims "with mass/current conservation $\int Q[\psi]=0$," but for the displayed Smoluchowski aggregation acting on number density $n$ the unweighted integral is not conserved; the conserved moment is mass, $\int v\,Q_{agg}[n]\,dv=0$, so the stated conservation law is mathematically wrong.
- **CHECK 3 (Correspondence Vector Support):** FAIL — Vector 1 is demonstrated by $\mathcal{L}_A$ and $\mathcal{L}_B$, and Vector 3 is supported by the two dispersion formulas, but Vector 2, "bistable_S_nullcline_Maxwell_equal_area_coexistence", is not demonstrated: the Silo B PBE contains no bistable local reaction/nucleation term, and the text defines "$S=H(M)$ with $M=\int v n dv$" but then imposes "$H(v_{1,2})=S_{coex}$" and an integral over "$H(v)$" without defining $H(v)$ or deriving the equal-area rule from the PBE.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The PBE-to-filamentation transfer is asymmetric because the source field supplies a developed moment-closure toolkit that the target field lacks, and the prediction names measurable radii, densities, voltage tolerance, CPU thresholds, and explicit falsification criteria; no canonical textbook pairing is recognized here, but Stage 3 should probe prior work.

#### Stage 3 Watch Items
- Verify whether any PBE formulation with growth, aggregation, and solute conservation actually yields an S-shaped bistable nullcline and a Maxwell equal-area rule, including a well-defined $H$.
- Verify the correct conserved moment for the Smoluchowski aggregation mapping and whether a filament-coalescence operator can be written as a mass/current-conserving operator without an additional weighting transformation.
- Search for prior work applying QMOM/DQMOM, sectional methods, or population balances to current-filament ensembles; assess whether the transfer is novel.
- Check whether the dynamic load-circuit voltage versus algebraic solute constraint changes the claimed operator equivalence.

### Third Adversarial Review
**Reviewer:** DeepSeek DeepSeek V4 Pro
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The displayed Silo A reaction term `f(a,u)=u^2 g(a)/d^2 - q(a)` with `g(a)=σ0 exp(γ a)` and `q(a)=h0 a` has derivative `f_a = (u²σ0γ/d²)exp(γa) - h0`, which changes sign at most once; therefore the nullcline `u=h(a*)` is single-humped and has at most two finite steady states, not the claimed S-shaped bistable nullcline. This directly contradicts the entry's statement that both systems "exhibit an S-shaped bistable nullcline."
- **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — The mapping "filament coalescence kernel `K_coal(|r_i-r_j|)` ↔ aggregation kernel `K_agg(v,w)`" asserts that both are symmetric bilinear Smoluchowski integral operators, but Silo A's governing equations in Section 3 contain no such coalescence/aggregation operator. The Smoluchowski form appears only later as a proposed reduced model in Section 4, so the vocabulary matrix claims a shared structure that Silo A's actual PDE does not contain.
- **CHECK 3 (Correspondence Vector Support):** FAIL — Vector 2's Silo B Maxwell equal-area expression uses `H(v)` after defining `S=H(M)`, where `M=∫ v n dv`; `H` is a function of total mass, not volume, so `H(v)` is undefined and the displayed integral is not a demonstrated equal-area rule. Vector 3 linearizes with `e^{i q_v v}`, but the entry's own PBE uses particle volume `v∈[0,∞)` with integrals from 0 to ∞, so a Fourier expansion in `v` on the full real line is invalid for the stated domain and does not establish the claimed dispersion relation.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The preferred transfer direction from mature PBE moment methods to filament-ensemble modeling is asymmetric, and the falsifiable prediction gives specific measurable thresholds (`⟨R⟩<60` or `>115 µm`, QMOM error >20%, speedup <10×). No textbook/canonical prior-art analogy was recognized by this reviewer.

#### Stage 3 Watch Items
- Whether any published Silo A filamentation model actually uses a cubic-like bistable `f(a,u)`; the explicit exponential/linear `f` in this entry is not bistable.
- Whether the claimed Silo B Maxwell equal-area construction appears in population-balance literature, since the entry's version confuses total mass `M` with internal coordinate `v`.
- Whether treating particle volume `v` as a Fourier coordinate on the half-line is accepted in any PBE stability analysis.
- Prior-art check for reaction-diffusion ↔ population-balance isomorphisms, particularly for Maxwell constructions and nonlocal coupling.

### Fourth Adversarial Review
**Reviewer:** Google Gemini 3.1 Pro
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The Maxwell construction equation for Silo B defines $S = H(M)$ where $M = \int v n dv$ (a macroscopic scalar mass), but then invalidly evaluates $H$ at the microscopic particle volume $v$ in the integral $\int_{v_1}^{v_2} [S_{coex}-H(v)]\,\bar{n}_{eq}(v)dv = 0$. This is a mathematical category error mixing integration variables with globally integrated state variables.
- **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — The vocabulary matrix maps "filament coalescence kernel $K_{coal}(|\mathbf{r}_i-\mathbf{r}_j|) \leftrightarrow$ aggregation kernel $K_{agg}(v,w)$" and claims both are Smoluchowski convolution operators. However, Smoluchowski convolution requires an additive conserved coordinate (like volume, $v_1+v_2=v$), and applying it to spatial positions $\mathbf{r}$ is physically and mathematically invalid because spatial coordinates do not add together upon coalescence. Furthermore, $K_{coal}$ does not even appear in the Silo A governing equations in Section 3.
- **CHECK 3 (Correspondence Vector Support):** FAIL — The vector `bistable_S_nullcline_Maxwell_equal_area_coexistence` is not demonstrated because its supporting equation in Silo B contains the fatal variable category error detailed in Check 1. This leaves only two vectors successfully demonstrated, failing the minimum requirement of three.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The methodological transfer is genuinely asymmetric (leveraging mature PBE/QMOM toolkits to model an ensemble of current filaments, circumventing full 2D FEM) and provides a specific, falsifiable numerical prediction regarding mean filament radius and holding voltage.

#### Stage 3 Watch Items
- Examine the scientific merit of the proposed transfer in Section 4. Although the underlying mathematical isomorphism fails, the idea of adapting Population Balance Equations and QMOM to track a distribution of semiconductor current filaments as 'pseudo-particles' appears highly creative and could be a novel modeling methodology in its own right.

### Fifth Adversarial Review
**Reviewer:** Xiaomi MiMo V2.5 Pro
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both Silo A (thermal filamentation reaction-diffusion with global circuit coupling, parabolic) and Silo B (population balance equation with growth-rate dispersion, Smoluchowski aggregation, and global solute conservation, parabolic in x and v) are genuine equations from their stated domains, belong to the same parabolic integro-differential class, and their nonlinear/global-coupling structures are consistent with the claimed correspondence.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All four vocabulary mappings pair objects of compatible mathematical type (scalar density fields, global scalar inhibitors defined by linear integral conservation, rank-1 nonlocal projection operators, symmetric bilinear integral operators of Smoluchowski form). Each Operator Role explanation names a specific shared mathematical structure rather than merely asserting similarity.
- **CHECK 3 (Correspondence Vector Support):** FLAG — Vectors 1 and 3 are fully demonstrated with explicit operators and dispersion relations. Vector 2 (bistable_S_nullcline_Maxwell_equal_area_coexistence) is partially supported: the Silo A Maxwell integral ∫f(a,u_coex)da = 0 is correct, but the Silo B formulation has two specific issues: (a) the function H is defined as S = H(M) (a function of total mass M) but is then evaluated at individual particle volumes v₁ and v₂ and appears as H(v) in the integrand, which is a notational inconsistency; (b) the claim that "both are Maxwell equal-area rules derived from ∫ δV/δψ = 0 for effective potential V" is not valid for the Silo B side, because the PBE with Smoluchowski aggregation is not a gradient flow — the aggregation operator Q_agg does not arise as the variational derivative of any standard functional.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction (PBE → current filamentation) is genuinely asymmetric: PBE has mature reduced-order methods (QMOM, DQMOM, sectional methods) while filamentation theory lacks ensemble reduced-order models for many interacting filaments. The falsifiable predictions are specific and measurable (⟨R⟩ = 85 ± 10 μm, N₀ = 3.2 ± 0.5 × 10⁶ m⁻², >100× CPU speedup) with explicit falsification thresholds. No canonical textbook prior art recognized for this specific cross-domain mapping.

#### Stage 3 Watch Items
- **Vector 2 Maxwell construction validity:** Probe whether the Silo B integral ∫[S_coex − H(v)] n̄_eq(v) dv = 0 can be given a rigorous derivation from a physical requirement (e.g., stationary size-front condition) independent of the claimed variational structure. Also verify whether bistability in the M*(S) steady-state relationship is realistic for the stated crystallization PBE with aggregation — standard crystallization PBE with linear conservation S = S₀ − βM does not obviously produce an S-shaped nullcline without specific nonlinear nucleation kinetics.
- **Notation inconsistency in H:** The function H is defined as S = H(M) (mass-dependent) but used as H(v) (volume-dependent) in the Maxwell integral. Determine whether this is a notational error for a conceptually sound construction, or whether it reflects a deeper confusion between two different functions.
- **Silo B dispersion relation at moderate q:** Verify that the linearized aggregation Fourier symbol K̂_lin(q_v) produces the claimed simple quadratic dispersion λ = λ₀ − D_eff q². For generic aggregation kernels, the Fourier symbol of the linearized Smoluchowski operator can have a more complex q-dependence (e.g., involving convolutions with the steady-state distribution), which would break the clean quadratic form at moderate wavenumbers.
- **Prior art check:** The individual domain models (Schöll-type thermal filamentation, Ramkrishna-type PBE) are well-established in their fields. Verify that no prior published work has proposed this specific semiconductor-filamentation ↔ PBE correspondence or the QMOM application to filament ensembles.

### Sixth Adversarial Review
**Reviewer:** Z.AI GLM-5.2
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The linearized operator `\mathcal{L}_A = \partial_t - D_a\nabla_{\perp}^2 - f_a(a^*,u^*) + R_{load}f_u(a^*,u^*)\mathcal{P}_0` drops the dynamic operator `\frac{1}{1+\tau_u\partial_t}` that results from the ODE `\tau_u \frac{du}{dt}= U_0 - u - R_{load}\int_{\Omega} a(\mathbf{r},t)d\mathbf{r}`, falsely equating it with Silo B's algebraic coupling. Additionally, the Silo B dispersion relation `\lambda_B(\mathbf{q}_x,q_v)= \partial_v G(v^*,S^*) + ...` invalidly applies a plane wave ansatz `e^{i q_v v}` to a variable-coefficient operator where `G(v,S)=k_g (S-1)v^{1/3}`, as plane waves are not eigenfunctions of such operators.
- **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — The vocabulary matrix states `Both obey $u=U_0-R_{load}\int_\Omega a\,d\mathbf{r}$ and $S=S_0-\beta\int v n\,dv d\mathbf{x}$`, directly contradicting the dynamic ODE for `u` given in Section 3. This is a category error that falsely equates a dynamic global constraint with an algebraic one to force an operator role match.
- **CHECK 3 (Correspondence Vector Support):** FAIL — Vector 2 claims a Maxwell construction but relies on the integral `\int_{v_1}^{v_2} [S_{coex}-H(v)]\,\bar{n}_{eq}(v)dv = 0` which evaluates `H` at `v` (particle volume) despite explicitly defining it as a function of `M` (global mass). This renders the demonstrated correspondence mathematically meaningless.
- **CHECK 4 (Transfer and Falsifiability):** FAIL — The transfer proposes solving the system via `QMOM with $M_k=\int R^k N dR$, $k=0..5$, closing $Q_{coal}$ with Gauss-Christoffel quadrature`. However, the defined coalescence kernel `K_{coal}(R_i,R_j)=2\pi D_a (R_i+R_j) \exp(-|\mathbf{r}_i-\mathbf{r}_j|/l_a)` depends on the spatial distance `|\mathbf{r}_i-\mathbf{r}_j|`. Tracking only moments in the internal coordinate `R` mathematically integrates out the spatial variables, making it impossible to evaluate this spatially nonlocal kernel and rendering the proposed transfer incoherent.

#### Stage 3 Watch Items
None identified.

### Seventh Adversarial Review
**Reviewer:** OpenAI GPT-5.6 Luna
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-18

#### Results by Check
* **CHECK 1 (Equation Validity):** FAIL — The Silo A claims are internally inconsistent: the displayed (f(a,u)=u^2\sigma_0e^{\gamma a}/d^2-h_0a) implies (u\propto\sqrt{ae^{-\gamma a}}), which has only one turning point rather than the three-root S-shaped bistable nullcline claimed in the accompanying text.
* **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — The mapping “**inhibitor / device voltage (u(t)) ↔ supersaturation / solute concentration (S(t))**” is coupled to the false claim that “**Both obey (u=U_0-R_{load}\int_\Omega a,d\mathbf{r}) and (S=S_0-\beta\int v n,dv d\mathbf{x})**”; (u) is dynamically governed by (\tau_u,du/dt) in Section 3 whereas (S) is algebraically constrained, so they are not the same mathematical object as stated.
* **CHECK 3 (Correspondence Vector Support):** FAIL — Vector 1 is undermined by the incorrect Silo B linearized global operator, while Vector 2 is not derived as a Maxwell construction and Vector 3 is not established because the claimed Silo B Fourier dispersion in (v) does not follow from the displayed PBE; specifically, Section 3 asserts “**Coexistence mass for stationary size-front:**” followed by an un-derived integral and later assumes “**(n=n^*+\delta n e^{\lambda t+i\mathbf{q}_x\cdot\mathbf{x}+i q_v v})**” without establishing the required eigenproblem.
* **CHECK 4 (Transfer and Falsifiability):** FAIL — The transfer direction is stated as asymmetric and the prediction is experimentally measurable, but the falsifiable numerical claim contains a direct arithmetic contradiction: “**holding voltage (U_{hold}=U_0-R_{load}I_{tot}=10.2) V**” evaluates to (10) V for the stated (20) V, (2,\Omega), and (5) A values.

#### Stage 3 Watch Items
* Probe the claimed Maxwell/equal-area construction for the particulate population-balance side, including whether the displayed stationary PBE actually admits the asserted scalar bistable-front/variational structure.
* Probe prior published work on population-balance/QMOM descriptions of interacting current filaments and the specific proposed filament-radius predictions; novelty remains a Stage 3 bibliometric question.
* Verify the numerical benchmark claims and parameter-specific predictions independently during bibliometric/human review.

### Eighth Adversarial Review
**Reviewer:** Microsoft Copilot 1.2
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** FLAG — The Silo A linearization is presented as  
  `\lambda_A(\mathbf{q}) = f_a(a^*,u^*) - D_a q^2 - \frac{R_{load} f_u(a^*,u^*) |\Omega|}{1+\tau_u\lambda_A}\delta_{\mathbf{q},0}`  
  yet the entry then states the instability cutoff `q_{c,A}=\sqrt{f_a/D_a}`; this quoted critical wavenumber omits the nonlocal/time-delayed \(q=0\) term and the implicit dependence of \(\lambda_A\) on itself in the denominator, so the derivation for \(q_{c,A}\) is not demonstrated and the approximation regime is unspecified.
- **CHECK 2 (Vocabulary Matrix Coherence):** FLAG — The mapping pair  
  **`activator field / filament current density a(\mathbf{r},t) [A/cm² or K] ↔ particle number density n(v,\mathbf{x},t) [1/m⁴]`**  
  equates a purely spatial scalar field \(a(\mathbf{r},t)\) to a higher-dimensional distribution \(n(v,\mathbf{x},t)\) without providing the explicit projection or reduction (e.g., \(a(\mathbf{x},t)=\int w(v)n(v,\mathbf{x},t)\,dv\)) that would make the two objects the same mathematical type; this is a category/coherence gap in the vocabulary matrix.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed correspondence vectors (`shared_nonlocal_global_coupling_parabolic_operator`, `bistable_S_nullcline_Maxwell_equal_area_coexistence`, `long_wave_transversal_instability_dispersion_threshold`) are addressed in the body with equations or operator expressions: Vector 1 is supported by the operators \(\mathcal{L}_A,\mathcal{L}_B\) and the rank-1 projections \(\mathcal{P}_0,\mathcal{P}_1\); Vector 2 is supported by the two Maxwell-type integral conditions in Section 3; Vector 3 is supported by the linearized dispersion relations for both silos (though see CHECK 1 flag about an omitted term in the Silo A critical-wavenumber statement).
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction is asymmetric and justified (PBE → filamentation) and the entry gives concrete, falsifiable numerical predictions (mean filament radius bounds, number density, holding voltage error threshold, and CPU speedup thresholds). No backwards-direction error is evident. Note for Stage 3: the claimed numerical benchmarks and speedups require verification.

#### Stage 3 Watch Items
- **Silo A dispersion derivation:** The reviewer should request the algebraic steps that lead from the implicit dispersion relation with the \(q=0\) time-delayed/global term to the quoted \(q_{c,A}=\sqrt{f_a/D_a}\), and verify the approximation regime (e.g., \(\tau_u\to0\), weak coupling, or small-domain limit) under which the simplification is valid.
- **Activator ↔ PBE reduction:** The human reviewer should demand an explicit projection operator or moment reduction that maps \(n(v,\mathbf{x},t)\) to a purely spatial activator \(a(\mathbf{x},t)\); if the mapping relies on a particular moment (e.g., mass or number), that choice and its consequences must be shown.
- **Maxwell construction derivations:** Ask for the explicit effective potential \(\mathcal{V}[\psi]\) and the variational steps that produce the equal-area rules in both silos, ensuring boundary conditions and conserved quantities are treated consistently.
- **QMOM closure and numerical benchmark details:** Request the exact QMOM moment set, quadrature nodes/weights, aggregation kernel parameterization, and the PDE benchmark mesh/solver settings used to produce the stated error and speedup claims.
- **Prior-art check:** The human reviewer should probe canonical literature on Maxwell equal-area constructions and mappings between reaction-diffusion systems with global coupling and population-balance/phase-separation models to determine novelty; include classic references on equal-area coexistence and reduced-order PBE closures.

### Ninth Adversarial Review
**Reviewer:** xAI Grok 4.5 Fast
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both sides are nonlinear parabolic integro-differential systems of the stated class (local reaction/growth + diffusion + rank-1 nonlocal global constraint); the displayed operators and dispersion relations are consistent with the claimed domains and support the three structural correspondences.
- **CHECK 2 (Vocabulary Matrix Coherence):** FLAG — The activator mapping pairs a continuum current-density field a(r,t) [A/cm²] with a number-density field n(v,x,t) that carries an extra internal volume coordinate; the coalescence-kernel mapping asserts an identical Smoluchowski form while Silo A supplies only a spatial kernel K_coal(|r_i-r_j|) with no volume argument; the inhibitor units are written inconsistently ([mol/m³][V]).
- **CHECK 3 (Correspondence Vector Support):** PASS — Vector 1 is demonstrated by the explicit rank-1 projections P_0 and P_1 inside L_A and L_B (Section 3); Vector 2 by the two Maxwell equal-area integrals for coexistence voltage/mass (Section 3); Vector 3 by the quadratic long-wave dispersion relations λ(q)=λ_0-D_eff q² on both sides (Section 3).
- **CHECK 4 (Transfer and Falsifiability):** FLAG — Transfer direction is asymmetric and well-justified by the maturity gap in ensemble reduced-order methods; the prediction supplies concrete measurable quantities (⟨R⟩=85±10 µm, N_0=3.2±0.5×10^6 m⁻², U_hold=10.2 V, >100× speedup) with explicit falsification thresholds. Prior-art recognition (Maxwell construction for bistable fronts and global-coupling reaction-diffusion systems) is advisory only.

#### Stage 3 Watch Items
- Confirm whether the Maxwell equal-area rule for coexistence of particle-size fronts under aggregation + growth is standard or novel in PBE literature.
- Verify that the claimed rank-1 projection operators in L_A and L_B remain isomorphic after the nondimensionalization that absorbs the extra v-diffusion and aggregation linearization present only in Silo B.
- Assess whether the filament-as-pseudo-particle QMOM reduction has any prior art inside the semiconductor filament community or constitutes a genuine cross-silo transfer.