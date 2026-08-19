---
sid_metadata:
  entry_id: "CONTROL-SID-0013"
  schema_version: "2.0-control"
  maturity_stage: "adversarial-flagged"
provenance:
  company: "Alibaba"
  model_family: "Qwen"
  model_version: "3.8 Max"
  generation_timestamp: "2026-08-17"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "clinical-neurophysiology-cortical-spreading-depolarization"
  domain_b: "quantum-mechanics"
  structural_family: "front-stability-spectral-operators"
  triple_correspondence_vectors:
    - "self_adjoint_csd_front_stability_to_stationary_schrodinger_operator"
    - "translational_zero_mode_to_susy_zero_energy_bound_state"
    - "far_field_radiation_dispersion_to_free_particle_scattering_continuum"
    - "fredholm_zero_mode_solvability_source_projection"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language / incompatible_ontologies / historically_isolated_communities"
prior_discovery_metrics:
  structural_isomorphism_score: 7.8
  vocabulary_divergence_score: 9.0
  expected_methodological_transfer_score: 8.2
  community_separation_score: 9.2
  representation_mismatch_score: 8.0
  expected_transfer_effort: "high"
  novelty_prior:
    estimate: 7.5
    uncertainty: "±1.5"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "constitutive_law_mismatch_due_to_multiscale_ionic_metabolic_variables"
  bibliometric_validation: "pending"
  first_adversarial_review:
    reviewer_model: "Anthropic Claude Sonnet 5"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "FLAG"
    verdict_rationale: "No check produced a FAIL-level finding (no equation-class mismatch, category-error mapping, undemonstrated vector, or backwards/template prediction), but Section 3's vector-4 speed formula introduces an undemonstrated baseline term and Section 4's dose calculation contains a verifiable arithmetic error that overstates the predicted dose-sparing factor by roughly 50%."
    failed_checks: []
    flagged_checks:
      - "Check 1: baseline term `c_0` in the vector 4 front-speed formula is asserted, not derived, from the stated substitution `η(x)=−b(x)`"
      - "Check 4: arithmetic error in `M_{P,c}` (stated as `(4/3)B_{P,c}`; should be `2B_{P,c}`), which overstates the predicted dose-sparing factor R"
      - "Check 4c: prior-art advisory — SUSY-QM factorization of a kink/front stability operator into a Pöschl–Teller potential is classical in soliton theory"
    quoted_evidence: []
    stage_3_watch_items:
      - "The potential recovered in vector 1, `V_A(x)=4−6sech²x`, is exactly the well-known φ⁴ kink stability potential from soliton theory (SUSY factorization of kink/front operators is textbook material, e.g. Cooper–Khare–Sukhatme-style SUSY QM reviews). Verify whether the specific transfer to clinical CSD front models is genuinely novel."
      - "Operator equivalence (vector 1) implies the full spectrum transfers: this Pöschl–Teller depth (n(n+1)=6) predicts a second discrete bound state near `E_A=3` (an internal shape/breathing mode) beyond the zero mode, which the entry never discusses. Worth probing for physiological meaning or prior literature."
      - "Ask the authors to derive `c_0` in vector 4's formula `c=c_0−(1/N)∫|U_0'(x)|b(x)dx`; substituting the stated `η(x)=−b(x)` into the preceding general formula does not itself produce a `c_0` term."
      - "Section 4 arithmetic should be corrected: `M_{P,c}=2B_{P,c}=c_0=0.05` (not 0.0333), giving `R=2/tanh(3)≈2.01` (not 3.015). Both clear the stated R<1.5 falsification bar, so the qualitative claim likely survives, but the reported figures need fixing."
  second_adversarial_review:
    reviewer_model: "DeepSeek DeepSeek V4 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "REJECT"
    verdict_rationale: "The Section 4 falsifiable dose-sparing prediction contains a clear integration error for the zero-mode-shaped inhibition, so its quantitative claim does not follow from the stated profile."
    failed_checks: ["Check 4: The prediction computes M_{P,c}=4/3 B_{P,c} for b_P(x)=B_P sech² x, but ∫_{-∞}^{∞} sech² x dx = 2, so the predicted dose and dose-sparing factor R are quantitatively wrong."]
    flagged_checks: ["Check 1: Section 3 vector 4 introduces a c0 term after stating η(x)=-b(x) without deriving the baseline-bias contribution; non-fatal because Section 4 later supplies a baseline speed.", "Check 4c: Prior-art advisory — reaction-diffusion front stability ↔ supersymmetric quantum mechanics (Pöschl-Teller sech² potential/kink translational mode) is a canonical analogy; Stage 3 should probe novelty."]
    quoted_evidence: ["B_{P,c}=\\frac{c_0}{2}, \\qquad M_{P,c}=\\int_{-\\infty}^{\\infty}b_P(x)\\,dx = \\frac{4}{3}B_{P,c} = \\frac{2c_0}{3}. For `c_0=0.05`, `B_{P,c}=0.025, M_{P,c}=0.0333.`"]
    stage_3_watch_items: ["Recompute the integrated dose for b_P(x)=B_P sech² x: the correct value is M_{P,c}=2B_P, changing the dose-sparing factor to 2/tanh3 ≈ 2.01, not 3/tanh3.", "Probe prior art on reaction-diffusion front stability ↔ Schrödinger/SUSY (Pöschl-Teller potential, φ^4 kink, Nagumo/FitzHugh-Nagumo front stability).", "Check the derivation of the c0 term in Demonstrated vector 4; the entry must explicitly include the baseline excitability bias in η(x)."]
  third_adversarial_review:
    reviewer_model: "Google Gemini 3.1 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "REJECT"
    verdict_rationale: "The entry contains a direct calculus error in Section 4, evaluating the integral of sech^2(x) as 4/3 instead of 2, which mathematically invalidates the stated quantitative predictions of the falsifiable hypothesis."
    failed_checks: ["Check 4: Incorrect definite integration in the falsifiable prediction derivation."]
    flagged_checks: ["Check 4: Advisory prior-art recognition (kink stability and SUSY QM)"]
    quoted_evidence: ["M_{P,c}=\\int_{-\\infty}^{\\infty}b_P(x)\\,dx\n=\n\\frac{4}{3}B_{P,c}\n=\n\\frac{2c_0}{3}."]
    stage_3_watch_items: 
      - "The underlying structural isomorphism (mapping the linear stability operator of a 1D reaction-diffusion front to a Schrödinger equation via supersymmetric quantum mechanics / Pöschl-Teller potentials) is a canonical, textbook result in mathematical physics (e.g., Cooper, Khare, & Sukhatme, 'Supersymmetry in Quantum Mechanics'). The reviewer must evaluate whether its specific application to Cortical Spreading Depolarization constitutes sufficient domain novelty."
      - "If advancing this entry, the dose-sparing prediction ratio $R$ must be recalculated using the correct integration value ($M_{P,c} = 2B_{P,c} = c_0$, yielding an actual theoretical ratio of $R \\approx 2.01$, not the claimed $3.015$)."
  fourth_adversarial_review:
    reviewer_model: "Xiaomi MiMo V2.5 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "FLAG"
    verdict_rationale: "The core isomorphism (Sections 1–3) is mathematically sound with all four correspondence vectors rigorously demonstrated, but the falsifiable prediction in Section 4 contains a specific integral computation error that inflates the dose-sparing factor from ≈2.01 to ≈3.015."
    failed_checks: []
    flagged_checks:
      - "Check 4b: Incorrect integral computation in the dose-sparing factor derivation"
      - "Check 4c: Recognized canonical analogy — linearized reaction-diffusion front stability ↔ stationary Schrödinger operator with SUSY kink factorization"
    quoted_evidence:
      - "M_{P,c}=\\int_{-\\infty}^{\\infty}b_P(x)\\,dx = \\frac{4}{3}B_{P,c} = \\frac{2c_0}{3}"
      - "R=\\frac{M_{U,c}}{M_{P,c}} = \\frac{3}{\\tanh 3} \\approx 3.015"
    stage_3_watch_items:
      - "The integral M_{P,c} = ∫ B_P sech²(x) dx = 2B_P, not (4/3)B_P. The value 4/3 comes from ∫ sech⁴(x) dx, which appears in the normalization N but not in the dose integral. Correct dose-sparing factor is R = 2/tanh(3) ≈ 2.01, not 3/tanh(3) ≈ 3.015. The qualitative conclusion (zero-mode shaping more efficient than uniform) and the falsification threshold R < 1.5 still hold with corrected numbers."
      - "The mathematical framework — linearized bistable front stability operator mapped to a Schrödinger operator, kink translational mode as SUSY zero-energy state, Fredholm solvability for front perturbation — is well-established in the nonlinear waves and soliton physics literature (Rajaraman's Solitons and Instantons, Pego–Kapitula–Sandstede spectral stability theory, Christ–Lee on kink stability). The specific application to cortical spreading depolarization is what may be novel; Stage 3 should verify this."
      - "The entry correctly scopes its claim to the linearized spectral problem and explicitly disclaims identity between full nonlinear parabolic CSD dynamics and unitary quantum evolution. Verify that no broader claim is implied elsewhere."
  fifth_adversarial_review:
    reviewer_model: "Z.AI GLM-5.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "FLAG"
    verdict_rationale: "Core isomorphism in Section 3 is mathematically correct and all four correspondence vectors are demonstrated, but Section 4 contains a computational error in the integrated dose calculation and the domain pairing is recognizable as canonical prior art."
    failed_checks: []
    flagged_checks: ["CHECK 4: Computational error in integrated inhibitory dose — entry claims M_{P,c} = (4/3)B_{P,c} but the correct value is 2B_{P,c} since ∫sech²x dx = 2, not 4/3; this propagates to an incorrect dose-sparing ratio R = 3/tanh(3) ≈ 3.015 instead of the correct R = 2/tanh(3) ≈ 2.01", "CHECK 4: Prior-art recognition — reaction-diffusion front linearized stability operator ↔ stationary Schrödinger operator with Pöschl-Teller potential is a canonical analogy in mathematical physics and pattern formation"]
    quoted_evidence: []
    stage_3_watch_items: ["Prior art: the bistable front linearization yielding a Pöschl-Teller/SUSY-QM Schrödinger operator is a well-known correspondence in field theory (φ⁴ kink stability), pattern formation textbooks, and SUSY QM. Stage 3 should query for novelty against the published CSD-specific application.", "Computational error in Section 4: M_{P,c} = (4/3)B_{P,c} should be 2B_{P,c}; the entry appears to confuse ∫sech²x dx = 2 with ∫sech⁴x dx = 4/3. The critical amplitude B_{P,c} = c₀/2 is correct, but the dose and ratio are wrong. Corrected R ≈ 2.01, not 3.015.", "Clinical realism of the proposed zero-mode-shaped inhibitory intervention should be assessed by Stage 3 for translational feasibility in CSD suppression."]
  sixth_adversarial_review:
    reviewer_model: "OpenAI GPT-5.6 Luna"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "REJECT"
    verdict_rationale: "The core Section 3 operator correspondence is internally consistent, but Section 4 contains a concrete mathematical error in the zero-mode-shaped intervention dose calculation, invalidating the stated quantitative falsification benchmark."
    failed_checks: ["Check 4: the falsifiable transfer prediction contains an incorrect integrated-dose calculation for the zero-mode-shaped inhibition, so its stated dose-sparing factor is mathematically unsupported."]
    flagged_checks: []
    quoted_evidence: ["The predicted critical amplitude and integrated dose are\n\n`math\nB_{P,c}=\frac{c_0}{2},\n\qquad\nM_{P,c}=\int_{-\infty}^{\infty}b_P(x)\,dx\n=\n\frac{4}{3}B_{P,c}\n=\n\frac{2c_0}{3}.\n`", "The predicted dose-sparing factor is\n\n`math\nR=\frac{M_{U,c}}{M_{P,c}}\n=\n\frac{3}{\tanh 3}\n\approx\n3.015.\n`"]
    stage_3_watch_items: ["Section 4 also states that the two interventions have the same spatial support |x|≤3, while b_P(x)=B_P sech²x is written without truncation; the human reviewer should determine how the intended finite support is to be interpreted.", "The Section 3 far-field correspondence calls the continuum a free-particle continuum although the mapped asymptotic potential is V_B^*(±∞)=4; this is a shifted free-particle continuum rather than a zero-offset free-particle Hamiltonian.", "The proposed cross-silo correspondence itself is algebraically explicit in Section 3; Stage 3 should independently assess its bibliometric status and prior-art context."]
  seventh_adversarial_review:
    reviewer_model: "Microsoft Copilot 1.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "REJECT"
    verdict_rationale: "A demonstrable arithmetic/integral error in Section 4 produces incorrect critical-dose expressions (M_{P,c} and the dose-sparing ratio R), invalidating the falsifiable prediction."
    failed_checks: ["Check 4: Falsifiable prediction arithmetic error in Section 4 (incorrect integral evaluation for M_{P,c} and consequent incorrect R)"]
    flagged_checks: []
    quoted_evidence: ["\"The predicted critical amplitude and integrated dose are\n\n```math\nB_{P,c}=\\frac{c_0}{2},\n\\qquad\nM_{P,c}=\\int_{-\\infty}^{\\infty}b_P(x)\\,dx\n=\n\\frac{4}{3}B_{P,c}\n=\n\\frac{2c_0}{3}.\n```\"","\"The predicted dose-sparing factor is\n\n```math\nR=\\frac{M_{U,c}}{M_{P,c}}\n=\n\\frac{3}{\\tanh 3}\n\\approx\n3.015.\n```\""]
    stage_3_watch_items: ["Verify the integrals used in Section 4 (\\int sech^2 = 2, \\int sech^4 = 4/3) and recompute M_{P,c} and R; check numerical evaluation of tanh(3) used in dose comparisons; examine whether the incorrect M_{P,c} propagates into any experimental thresholds or falsification criteria."]
  eighth_adversarial_review:
    reviewer_model: "xAI Grok 4.5 Fast"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "PASS"
    verdict_rationale: "All four checks pass: equations are class-consistent and support the claimed operator correspondence, vocabulary mappings are type-compatible with explicit shared structures, all listed vectors are fully demonstrated by derivation, and the transfer prediction is asymmetric with a concrete measurable falsifier."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: []
  ninth_adversarial_review:
    reviewer_model: "Meta Muse Spark 1.1"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "PASS"
    verdict_rationale: "All four checks pass: equations are correctly derived self-adjoint Schrödinger operators with matching continua, vocabulary mappings are type-compatible with explicit structure, all four listed correspondence vectors are demonstrated with derivations, and transfer is asymmetric with quantitative falsifiable dose-sparing predictions."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: ["Textbook Pöschl-Teller / SUSY QM factorization of bistable kink stability operator (Rajaraman Solitons and Instantons; Cooper Khare Sukhatme SUSY QM) is canonical - Stage 3 should verify novelty of its specific application to CSD front blocking via Fredholm projection", "Dose-sparing predictions rely on dimensionless normal form f(u)=4u(1-u)(2u-1); check whether full ionic/metabolic multiscale CSD models preserve exact operator identity"]
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ⚠*CONTROL*⚠ ENTRY 0013

## 1. CROSS-SILO SYSTEM DEFINITION
*   **Silo A (Field 1):** Clinical-neurophysiology / cortical spreading depolarization (CSD), specifically reduced one-dimensional CSD front models in which a scalar depolarization/extracellular-potassium surrogate field undergoes bistable reaction-diffusion propagation and propagation failure near a pinning threshold.
*   **Silo B (Field 2):** Quantum mechanics, specifically one-dimensional stationary Schrödinger spectral theory, supersymmetric factorization, scattering continua, and Fredholm solvability for inhomogeneous zero-mode problems.
*   **Mathematical Isomorphism:** After nondimensionalization and restriction to small perturbations about a stationary or near-stationary CSD front, the real self-adjoint linearized front-stability operator is sign-equivalent to a one-dimensional stationary Schrödinger operator, with the CSD translational zero mode mapped to a supersymmetric zero-energy bound state, the far-field CSD radiation modes mapped to the free-particle scattering continuum, and heterogeneity-induced front drift/blocking governed by the same Fredholm zero-mode projection used in quantum inhomogeneous response.

## 2. DIAGNOSTIC VOCABULARY MATRIX
*   `front stability eigenvalue λ` ↔ `dimensionless stationary energy ε`
    *   *Operator Role:* Both are scalar eigenvalues of second-order self-adjoint differential operators related by sign and time nondimensionalization. Silo A uses `λ` in `λ φ = L_A φ`; Silo B uses `ε` in `H_B ψ = ε ψ`. The explicit transformation is `ε = -λ` in the common dimensionless units, or `ε = -λ t_c` before final rescaling. Both are inverse-time quantities after the quantum energy is divided by the chosen quantum action/time scale.
*   `effective excitability curvature f'(U_0)` ↔ `dimensionless quantum potential V_B^*`
    *   *Operator Role:* Both are real multiplication operators entering the diagonal part of the stability Hamiltonian. Silo A has `H_A = -∂_x^2 - f'(U_0)`. Silo B has `H_B^* = -∂_x^2 + V_B^*`. The identification is `V_B^*(x) = -f'(U_0(x))`.
*   `front translational eigenfunction U_0'` ↔ `zero-mode wavefunction ψ_0`
    *   *Operator Role:* Both are null eigenfunctions of the corresponding stability Hamiltonian. The explicit map is `ψ_0 = -U_0'`, making `ψ_0` positive for a decreasing front. Both generate the Riccati superpotential `W = -ψ_0'/ψ_0`, which factorizes the operator as `H = A^† A`.
*   `diffusivity D_K` ↔ `quantum kinetic coefficient ħ²/(2m)`
    *   *Operator Role:* Both multiply the second spatial derivative before nondimensionalization. The explicit scale bridge is `ℓ_c^2 = D_K t_c` for Silo A and `V_B^* = (2mℓ_c^2/ħ²) V_B`, `ε = (2mℓ_c^2/ħ²) ℰ` for Silo B. In the common dimensionless coordinate `x = \bar x / ℓ_c`, both kinetic coefficients are unity.
*   `propagation-failure source term η / b` ↔ `inhomogeneous Schrödinger source S`
    *   *Operator Role:* Both enter a Fredholm solvability constraint imposed by the zero mode. Silo A uses `∫ U_0'(c U_0' + η) dx = 0` to determine front speed `c`. Silo B uses `∫ ψ_0 S dx = 0` as the solvability condition for `H_B χ = S`. The object type mismatch is removed by scaling both source terms to inverse-time units and identifying `ψ_0 = -U_0'`.

## 3. CORE MATHEMATICAL PARALLELISM

Reduced CSD models often collapse the slow ionic, metabolic, and extracellular-potassium dynamics into a scalar excitability field. In a one-dimensional cortical sheet, a dimensionful front model can be written as

```math
\partial_{\bar t}\bar u
=
D_K \partial_{\bar x}^2 \bar u
+
F(\bar u;\bar\mu),
```

where `\bar u` is a normalized depolarization/extracellular-potassium surrogate, `D_K` is an effective spreading diffusivity, and `F` contains regenerative depolarization and pump/restoration terms. Introduce dimensionless variables

```math
\bar x = \ell_c x,
\qquad
\bar t = t_c t,
\qquad
\ell_c^2 = D_K t_c,
\qquad
u(x,t)=\bar u(\bar x,\bar t).
```

Near a symmetric pinning threshold, a canonical bistable CSD front is captured by

```math
\partial_t u = \partial_x^2 u + f(u),
\qquad
f(u)=4u(1-u)(2u-1).
```

This equation is not proposed as a full ionic model of CSD; it is the minimal front-stability normal form for a pinned or slowly moving depolarization wave. It admits the stationary front

```math
U_0(x)=\frac{1-\tanh x}{2},
\qquad
U_0'(x)=-\frac{1}{2}\operatorname{sech}^2 x.
```

Linearizing about this front with `u=U_0+e^{\lambda t}\phi` gives

```math
\lambda \phi = \mathcal L_A \phi,
\qquad
\mathcal L_A=\partial_x^2+f'(U_0).
```

Define the CSD stability Hamiltonian by a sign flip,

```math
H_A=-\mathcal L_A
=
-\partial_x^2 - f'(U_0),
\qquad
E_A=-\lambda.
```

For a moving front with small dimensionless speed `c`, the co-moving linearized operator is

```math
\mathcal L_c=\partial_x^2+c\partial_x+f'(U_c).
```

The convective term is removed by the exponential gauge

```math
\phi(x)=e^{-cx/2}\psi(x),
```

yielding

```math
-\mathcal L_c \phi
=
e^{-cx/2}
\left[
-\partial_x^2 - f'(U_c)+\frac{c^2}{4}
\right]\psi.
```

Thus, at the pinning threshold `c=0`, and gauge-equivalently for small `c\neq0`, the CSD linear stability problem is a one-dimensional Schrödinger-type spectral problem.

Silo B uses the one-dimensional time-independent Schrödinger equation

```math
\left[
-\frac{\hbar^2}{2m}\partial_{\bar x}^2
+
V_B(\bar x)
\right]\Psi
=
\mathcal E \Psi.
```

Using the same length scale `\ell_c`, define

```math
x=\frac{\bar x}{\ell_c},
\qquad
V_B^*(x)=\frac{2m\ell_c^2}{\hbar^2}V_B(\ell_c x),
\qquad
\varepsilon=\frac{2m\ell_c^2}{\hbar^2}\mathcal E.
```

Then the dimensionless quantum equation is

```math
\left[
-\partial_x^2+V_B^*(x)
\right]\Psi
=
\varepsilon \Psi.
```

The explicit bridge is

```math
V_B^*(x)=-f'(U_0(x)),
\qquad
\varepsilon=E_A=-\lambda,
\qquad
\psi=\phi
```

with the restriction that the quantum wavefunction is taken in its real sector for bound-state and zero-mode calculations. The correspondence is an operator-level correspondence for linear perturbations about a front; it does not claim that the full nonlinear parabolic CSD dynamics is identical to unitary quantum time evolution.

### Demonstrated vector 1: self-adjoint CSD front-stability operator ↔ stationary Schrödinger operator

For the CSD front,

```math
f'(U_0(x))=2-6\tanh^2 x.
```

Therefore

```math
H_A=-\partial_x^2+V_A(x),
\qquad
V_A(x)=-f'(U_0(x))=6\tanh^2 x-2.
```

The quantum dimensionless operator is

```math
H_B^*=-\partial_x^2+V_B^*(x).
```

Under

```math
V_B^*(x)=V_A(x)=6\tanh^2 x-2,
```

the operators are identical on the same real Hilbert space.

### Demonstrated vector 2: translational zero mode ↔ supersymmetric zero-energy bound state

Differentiating the stationary front equation

```math
U_0''+f(U_0)=0
```

gives

```math
\mathcal L_A U_0'=0.
```

Since `H_A=-\mathcal L_A`, the positive zero mode is

```math
\psi_0(x)=-U_0'(x)=\frac{1}{2}\operatorname{sech}^2 x,
\qquad
H_A\psi_0=0.
```

Define the Riccati superpotential

```math
W(x)=-\frac{\psi_0'(x)}{\psi_0(x)}=2\tanh x.
```

Then

```math
V_A(x)=W^2-W',
```

because

```math
W^2-W'=4\tanh^2 x-2\operatorname{sech}^2 x
=
6\tanh^2 x-2.
```

Thus

```math
H_A=A^\dagger A,
\qquad
A=\partial_x+W(x),
\qquad
A^\dagger=-\partial_x+W(x).
```

In supersymmetric quantum mechanics, the corresponding factorized Hamiltonian is independently recognized as

```math
H_B^*=A^\dagger A,
\qquad
V_B^*=W^2-W',
\qquad
A\psi_0=0,
```

with zero-energy ground state

```math
\psi_0(x)\propto \exp\left[-\int^x W(y)\,dy\right]
=
\operatorname{sech}^2 x.
```

This is precisely the CSD translational Goldstone mode after normalization.

### Demonstrated vector 3: far-field radiation dispersion ↔ free-particle scattering continuum

Far ahead of and behind the CSD front, `U_0\to0` or `U_0\to1`, and

```math
f'(0)=f'(1)=-4.
```

A small CSD radiation mode `\phi\sim e^{ikx+\lambda t}` therefore satisfies

```math
\lambda(k)=-k^2-4.
```

Since `E_A=-\lambda`, the CSD stability Hamiltonian has continuum dispersion

```math
E_A(k)=k^2+4.
```

On the quantum side, the mapped potential has asymptotic value

```math
V_B^*(\pm\infty)=4.
```

Therefore asymptotic Schrödinger scattering states `\Psi\sim e^{ikx}` obey

```math
\varepsilon(k)=k^2+4.
```

Thus the CSD radiation continuum and the quantum free-particle continuum have identical dispersion in the mapped units.

### Demonstrated vector 4: Fredholm zero-mode solvability ↔ quantum zero-mode orthogonality

For a weak stationary source `s(x)` added to the CSD front equation, the first-order correction `\chi` satisfies

```math
\mathcal L_A \chi + s(x)=0.
```

Because `\mathcal L_A` has the translational null eigenfunction `U_0'`, the Fredholm solvability condition is

```math
\int_{-\infty}^{\infty} U_0'(x)s(x)\,dx=0.
```

For a weakly moving front in a heterogeneous CSD environment,

```math
s(x)=cU_0'(x)+\eta(x),
```

so

```math
c
=
-\frac{\displaystyle\int_{-\infty}^{\infty}U_0'(x)\eta(x)\,dx}
{\displaystyle\int_{-\infty}^{\infty}\left[U_0'(x)\right]^2\,dx}.
```

Writing an inhibitory heterogeneity as `\eta(x)=-b(x)` and using `\psi_0=-U_0'` gives

```math
c
=
c_0-\frac{1}{N}
\int_{-\infty}^{\infty} |U_0'(x)|\,b(x)\,dx,
\qquad
N=\int_{-\infty}^{\infty}\left[U_0'(x)\right]^2 dx.
```

For the canonical front,

```math
N=\int_{-\infty}^{\infty}\frac{1}{4}\operatorname{sech}^4 x\,dx
=
\frac{1}{3}.
```

The quantum Fredholm counterpart is the inhomogeneous Schrödinger equation

```math
H_B^*\chi=S(x).
```

Since `H_B^*\psi_0=0`, a solution exists only if

```math
\int_{-\infty}^{\infty}\psi_0(x)S(x)\,dx=0.
```

With `\psi_0=-U_0'`, this is the same zero-mode projection condition that determines CSD drift, pinning, and propagation failure.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
*   **Preferred Transfer Direction:** quantum-mechanics → clinical-neurophysiology-cortical-spreading-depolarization
*   **Asymmetric Maturity Rationale:** Quantum mechanics possesses a highly mature toolkit for one-dimensional spectral design: supersymmetric factorization, inverse scattering, bound-state perturbation theory, Fredholm solvability, and matched-filter potential shaping. CSD research is mature in optical imaging, electrophysiological detection, animal models, and numerical reaction-diffusion simulation, but lacks a comparably developed closed-form inverse-design framework for minimal-dose spatial patterning of inhibitory conductances, potassium clearance, or metabolic rescue needed to block propagation without globally suppressing cortical activity.
*   **Target Bottleneck Mitigation:** The hypothesis is that importing quantum zero-mode solvability and supersymmetric sensitivity analysis converts CSD suppression from a brute-force parameter sweep into an analytic inverse design problem. Specifically, the spatial profile of an inhibitory intervention should be shaped by the CSD front zero mode so that the intervention projects maximally onto the Fredholm solvability vector that controls front speed. This directly addresses the bottleneck of stopping CSD while minimizing total inhibitory dose, a clinically relevant constraint because excessive global suppression or metabolic burden can worsen injury.
*   **Falsifiable Prediction:** Use the dimensionless benchmark CSD equation from Section 3 with a small baseline speed `c_0`, for example `c_0=0.05`, generated by a small constant excitability bias. Compare two interventions over the same spatial support `|x|\le 3`:

    Zero-mode-shaped inhibition:

```math
b_P(x)=B_P\operatorname{sech}^2 x.
```

    The predicted critical amplitude and integrated dose are

```math
B_{P,c}=\frac{c_0}{2},
\qquad
M_{P,c}=\int_{-\infty}^{\infty}b_P(x)\,dx
=
\frac{4}{3}B_{P,c}
=
\frac{2c_0}{3}.
```

    For `c_0=0.05`,

```math
B_{P,c}=0.025,
\qquad
M_{P,c}=0.0333.
```

    Uniform inhibition over the finite support:

```math
b_U(x)=B_U\,\mathbf{1}_{|x|\le 3}.
```

    The predicted critical amplitude and integrated dose are

```math
B_{U,c}=\frac{c_0}{3\tanh 3},
\qquad
M_{U,c}=6B_{U,c}
=
\frac{2c_0}{\tanh 3}.
```

    For `c_0=0.05`,

```math
M_{U,c}=0.1005.
```

    The predicted dose-sparing factor is

```math
R=\frac{M_{U,c}}{M_{P,c}}
=
\frac{3}{\tanh 3}
\approx
3.015.
```

    The measurable quantity is the total integrated inhibitory dose required to reduce the CSD front speed to zero. The named baseline is a uniform inhibition profile over the same six-width spatial window, equivalent to a standard uniform-dose intervention sweep. The prediction is falsified if high-resolution simulation of the stated PDE, or a quantitatively scaled slice/optogenetic benchmark, yields a dose-sparing factor `R<1.5`, or if the zero-mode-shaped profile fails to block propagation at `M=1.1 M_{P,c}` while the direct numerical front speed remains positive.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
*   `"cortical spreading depolarization" AND "reaction-diffusion front" AND "Fredholm solvability"`
*   `"supersymmetric quantum mechanics" AND "zero-energy bound state" AND "kink translational mode"`
*   `"cortical spreading depolarization propagation failure" AND "stationary Schrödinger operator" AND "zero-mode inhibition"`

---

## ADVERSARIAL REVIEWS (Stage 2)

### First Adversarial Review
**Reviewer:** Anthropic Claude Sonnet 5
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** FLAG — Every equation displayed in Section 3 was independently re-derived and checks out exactly: `U_0(x)=(1-tanh x)/2` solves `U_0''+f(U_0)=0`; `f'(U_0(x))=2-6tanh²x`; the superpotential `W=2tanh x` gives `W²-W'=6tanh²x-2=V_A(x)` exactly (confirming the SUSY factorization); the far-field dispersion `ε(k)=k²+4` is correct; `N=∫(U_0')²dx=1/3` is correct; and the moving-front gauge transformation `φ=e^{-cx/2}ψ` is correctly carried through. However, in "Demonstrated vector 4," the formula `c=c_0−(1/N)∫|U_0'(x)|b(x)dx` introduces a baseline term `c_0` that the stated substitution doesn't produce: setting `η(x)=−b(x)` into the preceding `c=−∫U_0'η dx/N` (as literally written) yields `c=−(1/N)∫|U_0'|b dx` with no `c_0` term, so `c_0`'s origin is asserted rather than derived here.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All five Section 2 mappings pair type-compatible objects (eigenvalue↔eigenvalue, potential↔potential, zero-eigenfunction↔zero-eigenfunction, kinetic coefficient↔kinetic coefficient, source term↔source term), and each gives an explicit identification (e.g. `V_B*(x)=−f'(U_0(x))`; `ψ_0=−U_0'`) rather than hedged language. None matches a listed category-error pattern.
- **CHECK 3 (Correspondence Vector Support):** PASS — All four YAML-listed vectors are demonstrated with equations in Section 3, not merely named: vector 1 by the literal operator identity `V_B*=V_A=6tanh²x−2`; vector 2 by the verified SUSY factorization `H_A=A†A` with `H_Aψ_0=0`; vector 3 by matching asymptotic dispersion `ε(k)=k²+4` on both sides; vector 4 by the matched solvability integrals `∫U_0'η dx=0` and `∫ψ_0S dx=0`. Four demonstrated vectors, above the three-vector floor.
- **CHECK 4 (Transfer and Falsifiability):** FLAG — Asymmetry is genuine and not backwards: 1D spectral inverse-design (SUSY factorization, Fredholm solvability) is plausibly the more mature toolkit on the quantum-mechanics side. The prediction is a real quantitative claim, not a template non-prediction. However, Section 4's dose calculation contains an arithmetic error: with `b_P(x)=B_P sech²x`, the entry's `M_{P,c}=∫b_P(x)dx=(4/3)B_{P,c}` is wrong, since `∫sech²x dx` over the real line is 2, not 4/3 — the correct value is `M_{P,c}=2B_{P,c}=c_0=0.05`, not the stated 0.0333. This changes the predicted dose-sparing factor from the entry's `R=3/tanh(3)≈3.015` to the correct `R=2/tanh(3)≈2.01`; both clear the entry's own falsification threshold of `R<1.5`, so the qualitative claim likely survives, but the reported number is wrong. Separately (Check 4c, advisory only): linearizing a kink/front solution into a Schrödinger-type operator and applying SUSY QM factorization is classical in soliton theory — recorded as prior art for Stage 3, not grounds for rejection.

#### Stage 3 Watch Items
- The potential recovered in vector 1, `V_A(x)=4−6sech²x`, is exactly the well-known φ⁴ kink stability potential from soliton theory (SUSY factorization of kink/front operators is textbook material, e.g. Cooper–Khare–Sukhatme-style SUSY QM reviews). Verify whether the specific transfer to clinical CSD front models is genuinely novel.
- Operator equivalence (vector 1) implies the full spectrum transfers: this Pöschl–Teller depth (n(n+1)=6) predicts a second discrete bound state near `E_A=3` (an internal shape/breathing mode) beyond the zero mode, which the entry never discusses. Worth probing for physiological meaning or prior literature.
- Ask the authors to derive `c_0` in vector 4's formula `c=c_0−(1/N)∫|U_0'(x)|b(x)dx`; substituting the stated `η(x)=−b(x)` into the preceding general formula does not itself produce a `c_0` term.
- Section 4 arithmetic should be corrected: `M_{P,c}=2B_{P,c}=c_0=0.05` (not 0.0333), giving `R=2/tanh(3)≈2.01` (not 3.015). Both clear the stated `R<1.5` falsification bar, so the qualitative claim likely survives, but the reported figures need fixing.

### Second Adversarial Review
**Reviewer:** DeepSeek DeepSeek V4 Pro
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** FLAG — The Section 3 vector 4 line “Writing an inhibitory heterogeneity as η(x)=-b(x) and using ψ0=-U0' gives c = c0 - 1/N ∫ |U0'| b(x) dx” does not follow from the preceding formula without explicitly introducing a baseline excitability bias; Section 4 later supplies c0, so this is non-fatal.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The mapped pairs are operator/eigenvalue/state/source pairs of compatible mathematical type, and the roles name shared operator structure.
- **CHECK 3 (Correspondence Vector Support):** PASS — All four listed vectors are demonstrated in Section 3 by explicit operators/derivations; vector 4’s Fredholm condition is demonstrated, though its c0 formula has the derivation gap flagged under Check 1.
- **CHECK 4 (Transfer and Falsifiability):** FAIL — The asymmetry rationale is plausible and the prediction is specific, but the quantitative prediction is mathematically wrong: the entry computes `M_{P,c}=∫ b_P dx = 4/3 B_{P,c}` for `b_P(x)=B_P sech² x`, whereas ∫ sech² dx = 2, so the claimed dose-sparing factor `R=3/tanh3≈3.015` does not follow. Prior-art advisory: reaction-diffusion front stability ↔ SUSY QM is a canonical analogy.

#### Stage 3 Watch Items
- Recompute the integrated dose for `b_P(x)=B_P sech² x`; correct value is `M_{P,c}=2B_P`, yielding `R=2/tanh3≈2.01`.
- Probe prior art on reaction-diffusion front stability ↔ Schrödinger/SUSY (Pöschl-Teller potential, φ^4 kink, Nagumo/FitzHugh-Nagumo).
- Verify derivation of the `c0` term in Demonstrated vector 4: the baseline excitability bias must be explicitly included in η(x).

### Third Adversarial Review
**Reviewer:** Google Gemini 3.1 Pro
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-19

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — All displayed equations in Section 3 correctly model the bistable reaction-diffusion stability and stationary Schrödinger domains without class mismatches, reliably converting a parabolic PDE linearization into the appropriate self-adjoint operator structure.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The vocabulary pairings establish strict structural equivalence between compatible mathematical objects (e.g., matching eigenvalues, explicit real multiplication operators, and null eigenfunctions) without relying on hedged language or committing category errors.
- **CHECK 3 (Correspondence Vector Support):** PASS — All four correspondence vectors listed in the metadata (`self_adjoint_csd_front_stability_to_stationary_schrodinger_operator`, `translational_zero_mode_to_susy_zero_energy_bound_state`, `far_field_radiation_dispersion_to_free_particle_scattering_continuum`, `fredholm_zero_mode_solvability_source_projection`) are fully demonstrated in Section 3 using explicit operator derivations, spectral identities, and matched integral solvability constraints.
- **CHECK 4 (Transfer and Falsifiability):** FAIL — The proposed direction exhibits sound methodological asymmetry, but the falsifiable prediction contains a strict calculus error: the text claims `M_{P,c}=\int_{-\infty}^{\infty}b_P(x)\,dx = \frac{4}{3}B_{P,c}` for $b_P(x) = B_P\operatorname{sech}^2 x$, but the definite integral of $\operatorname{sech}^2(x)$ is $2$, not $4/3$. This mathematically invalidates the predicted critical dose value and the stated dose-sparing threshold $R$. Additionally, FLAG (advisory prior art): The structural mathematical mapping of 1D reaction-diffusion kink stability to supersymmetric quantum mechanics is a canonical textbook physics result (e.g., Cooper, Khare, Sukhatme), even if the specific application to CSD is novel.

#### Stage 3 Watch Items
- The core mathematical equivalence mapping 1D kink/front linear stability to supersymmetric quantum mechanics and the Pöschl-Teller potential is an established textbook technique in theoretical physics. Evaluate whether applying this canonical mathematical identity to the specific neurophysiological domain of Cortical Spreading Depolarization satisfies the novelty criteria for this repository.
- The quantitative prediction must be corrected if the entry is rehabilitated. Because $\int_{-\infty}^{\infty} \operatorname{sech}^2 x \, dx = 2$, the integrated dose for the zero-mode intervention is $M_{P,c} = 2B_{P,c} = c_0$, meaning the correct theoretical dose-sparing factor is $R = \frac{2}{\tanh 3} \approx 2.01$, instead of the $3.015$ threshold claimed in the text.

### Fourth Adversarial Review
**Reviewer:** Xiaomi MiMo V2.5 Pro
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — All equations in Section 3 are mathematically correct and internally consistent. The linearized CSD stability operator $\mathcal{L}_A = \partial_x^2 + f'(U_0)$ and the sign-flipped Schrödinger form $H_A = -\partial_x^2 - f'(U_0)$ are both second-order self-adjoint operators on the same real Hilbert space; this is a legitimate spectral correspondence, not an equation-class mismatch. The entry explicitly disclaims identity between full parabolic CSD dynamics and unitary quantum evolution, correctly scoping the claim. All derived quantities ($f'(U_0) = 2 - 6\tanh^2 x$, $W = 2\tanh x$, $W^2 - W' = 6\tanh^2 x - 2$, $N = 1/3$) were independently verified and are correct.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All five vocabulary mappings pair objects of compatible mathematical type (scalar eigenvalues, real multiplication operators, eigenfunctions, kinetic coefficients, source terms). Each mapping includes an explicit transformation equation and a stated nondimensionalization bridge (e.g., $\varepsilon = (2m\ell_c^2/\hbar^2)\mathcal{E}$ for the eigenvalue pair). No category errors found.
- **CHECK 3 (Correspondence Vector Support):** PASS — All four listed vectors are demonstrated with explicit equations and derivations in the body: (1) operator identity verified by direct substitution in Section 3 "Demonstrated vector 1"; (2) SUSY factorization $H_A = A^\dagger A$ with $A = \partial_x + W$ and $A\psi_0 = 0$ verified in "Demonstrated vector 2"; (3) matching far-field dispersion $E_A(k) = \varepsilon(k) = k^2 + 4$ derived on both sides in "Demonstrated vector 3"; (4) Fredholm solvability $\int \psi_0 S\,dx = 0$ shown to be the same zero-mode projection on both sides in "Demonstrated vector 4."
- **CHECK 4 (Transfer and Falsifiability):** FLAG — The transfer direction (quantum mechanics → CSD neurophysiology) is genuinely asymmetric: QM possesses mature 1D spectral design tools (SUSY factorization, inverse scattering, Fredholm theory) that CSD research lacks for closed-form inverse design. The prediction names a specific measurable quantity (dose-sparing factor $R$), a specific threshold ($R < 1.5$ for falsification), and a concrete experiment. However, there is a specific mathematical error in the dose computation. With $b_P(x) = B_P\operatorname{sech}^2 x$, the integrated dose is $M_{P,c} = \int B_P\operatorname{sech}^2 x\,dx = 2B_P$, not $(4/3)B_P$ as stated. The value $4/3$ comes from $\int \operatorname{sech}^4 x\,dx$ (the normalization integral $N$), not from $\int \operatorname{sech}^2 x\,dx = 2$. This inflates the dose-sparing factor from the correct $R = 2/\tanh 3 \approx 2.01$ to the claimed $R = 3/\tanh 3 \approx 3.015$. The qualitative conclusion and falsification threshold ($R < 1.5$) survive the correction.

#### Stage 3 Watch Items
- The mathematical framework (linearized bistable front stability ↔ Schrödinger operator, kink translational mode ↔ SUSY zero-energy state, Fredholm solvability for front perturbation) is well-established in the nonlinear waves and soliton physics literature. Recognized sources include Rajaraman's *Solitons and Instantons*, Pego–Kapitula–Sandstede spectral stability theory for traveling waves, and Christ–Lee on kink stability and SUSY. Stage 3 should verify whether the specific application to cortical spreading depolarization is novel against this body of work.
- Verify that the corrected dose-sparing factor ($R \approx 2.01$ rather than $3.015$) still survives simulation benchmarks and does not collapse below the stated falsification threshold of $1.5$ when tested with realistic CSD parameters.
- Confirm that the explicit disclaimer ("The correspondence is an operator-level correspondence for linear perturbations about a front; it does not claim that the full nonlinear parabolic CSD dynamics is identical to unitary quantum time evolution") is consistently maintained throughout and that no broader claims appear in the search strings or metadata.

### Fifth Adversarial Review
**Reviewer:** Z.AI GLM-5.2
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — All equations in Section 3 are verified correct: the bistable front $U_0 = (1-\tanh x)/2$ satisfies $U_0'' + f(U_0) = 0$ with $f(u) = 4u(1-u)(2u-1)$; the linearized operator $\mathcal{L}_A = \partial_x^2 + f'(U_0)$ with $f'(U_0) = 2-6\tanh^2 x$ yields $H_A = -\partial_x^2 + 6\tanh^2 x - 2$, which is the Pöschl-Teller potential; the SUSY factorization $W = 2\tanh x$, $W^2 - W' = 6\tanh^2 x - 2$, and $H = A^\dagger A$ all check out; the far-field dispersion $E_A(k) = k^2 + 4$ matches the quantum continuum $\varepsilon(k) = k^2 + 4$; the Fredholm solvability conditions are correctly stated; the gauge transformation for moving fronts is correctly derived.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All five vocabulary pairs map objects of compatible mathematical type: scalar eigenvalues to scalar eigenvalues (with explicit $\varepsilon = -\lambda$), real multiplication operators to real multiplication operators (with explicit $V_B^* = -f'(U_0)$), null eigenfunctions to null eigenfunctions (with $\psi_0 = -U_0'$), kinetic coefficients to kinetic coefficients (with explicit scale bridge), and source terms to source terms (both entering Fredholm solvability). No category errors detected.
- **CHECK 3 (Correspondence Vector Support):** PASS — All four listed vectors are fully demonstrated in the body: (1) self-adjoint operator equivalence is shown by explicit operator identification $H_A = H_B^*$ under $V_B^* = 6\tanh^2 x - 2$; (2) translational zero mode to SUSY bound state is shown via $H_A\psi_0 = 0$, Riccati superpotential $W = 2\tanh x$, and factorization $H_A = A^\dagger A$; (3) far-field radiation to free-particle scattering is shown via matching dispersion $E_A(k) = k^2+4 = \varepsilon(k)$; (4) Fredholm solvability to quantum zero-mode orthogonality is shown via $\int U_0's\,dx = 0 \Leftrightarrow \int \psi_0 S\,dx = 0$.
- **CHECK 4 (Transfer and Falsifiability):** FLAG — The transfer direction (QM → CSD) is genuinely asymmetric: QM possesses mature spectral design tools (SUSY, inverse scattering, Fredholm theory) while CSD lacks closed-form inverse-design for inhibitory profiling. The prediction names specific measurable quantities (critical amplitude, integrated dose, dose-sparing ratio $R$) and specific falsification thresholds ($R < 1.5$, failure to block at $M = 1.1\,M_{P,c}$). However, the integrated dose calculation contains a computational error: the entry states "$M_{P,c}=\int_{-\infty}^{\infty}b_P(x)\,dx = \frac{4}{3}B_{P,c}$" but since $b_P(x) = B_P\operatorname{sech}^2 x$ and $\int_{-\infty}^{\infty}\operatorname{sech}^2 x\,dx = 2$ (not $4/3$; the value $4/3$ is $\int\operatorname{sech}^4 x\,dx$), the correct result is $M_{P,c} = 2B_{P,c} = c_0$. This propagates to an incorrect dose-sparing ratio: the entry's "$R = \frac{3}{\tanh 3} \approx 3.015$" should be $R = \frac{2}{\tanh 3} \approx 2.01$. The prediction remains falsifiable in structure, but the quantitative values are wrong. Additionally, the reaction-diffusion front stability ↔ Schrödinger operator correspondence (Pöschl-Teller potential from bistable kink) is a recognizable canonical analogy from mathematical physics and pattern formation literature, flagged as advisory for Stage 3.

#### Stage 3 Watch Items
- **Prior art (canonical analogy):** The linearized stability operator of a bistable reaction-diffusion front being sign-equivalent to a stationary Schrödinger operator with Pöschl-Teller potential is a well-known correspondence in mathematical physics (φ⁴ kink stability, SUSY QM, pattern formation textbooks). Stage 3 should assess whether the *application to CSD clinical intervention design* is novel, even if the operator correspondence itself is not.
- **Computational error in Section 4:** The entry computes $\int_{-\infty}^{\infty}\operatorname{sech}^2 x\,dx = 4/3$, but the correct value is $2$. This affects $M_{P,c}$ (should be $2B_{P,c} = c_0$, not $\frac{4}{3}B_{P,c} = \frac{2c_0}{3}$) and $R$ (should be $\approx 2.01$, not $\approx 3.015$). The critical amplitude $B_{P,c} = c_0/2$ is correct. The entry appears to have confused $\int\operatorname{sech}^2 x\,dx$ with $\int\operatorname{sech}^4 x\,dx = 4/3$. This should be corrected before the entry advances.
- **Clinical translational feasibility:** The claim that zero-mode-shaped inhibition profiles can achieve dose-sparing in CSD suppression should be evaluated for realism regarding the spatial precision of optogenetic or pharmacological interventions in cortical tissue.

### Sixth Adversarial Review
**Reviewer:** OpenAI GPT-5.6 Luna
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-18

#### Results by Check
* **CHECK 1 (Equation Validity):** PASS — The Section 3 CSD linearization, sign-flipped stability Hamiltonian, Pöschl–Teller potential, zero mode, factorization, and mapped stationary Schrödinger operator are internally consistent.
* **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The four vocabulary pairs have compatible mathematical types and each gives an explicit scaling or operator identification rather than relying solely on analogy.
* **CHECK 3 (Correspondence Vector Support):** PASS — The self-adjoint front-stability/operator vector, translational-zero-mode/SUSY-zero-state vector, far-field-dispersion/scattering-continuum vector, and Fredholm-source/zero-mode-projection vector are each explicitly supported by equations in Section 3.
* **CHECK 4 (Transfer and Falsifiability):** FAIL — The transfer direction is stated asymmetrically and the prediction is quantitatively testable, but its dose calculation is mathematically wrong: for the quoted profile (b_P(x)=B_P\operatorname{sech}^2x), (\int_{-\infty}^{\infty}b_P,dx=2B_P), not (\frac43B_P), so the quoted (M_{P,c}) and (R) do not follow.

#### Stage 3 Watch Items
* Section 4 also states that the two interventions have the same spatial support (|x|\le3), while (b_P(x)=B_P\operatorname{sech}^2x) is written without truncation; probe this support inconsistency.
* The Section 3 far-field mapping uses the phrase “free-particle scattering continuum” despite the mapped asymptotic potential being (4), i.e. a free-particle continuum with an energy offset.
* The Section 3 operator correspondence is explicit and internally coherent; Stage 3 should independently probe its bibliometric prior-art status.

### Seventh Adversarial Review
**Reviewer:** Microsoft Copilot 1.2
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The linearization, operator sign flip, Riccati factorization, dispersion relations, and Fredholm solvability conditions in Section 3 are mathematically consistent and correctly derived for the stated front `U_0(x)`.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — Mapped tokens are of compatible mathematical type (eigenvalues ↔ energies; multiplication operator `f'(U_0)` ↔ potential; translational eigenfunction ↔ zero-mode wavefunction; diffusivity ↔ kinetic coefficient; source term ↔ inhomogeneous Schrödinger source).
- **CHECK 3 (Correspondence Vector Support):** PASS — All four listed correspondence vectors are demonstrated in the body with explicit equations and derivations: (1) operator equivalence (Section 3, operator definitions and `V_A=V_B^*`), (2) translational zero mode and SUSY factorization (Section 3, Riccati superpotential and factorization), (3) far-field radiation dispersion (Section 3, dispersion `E_A(k)=k^2+4` and matching quantum continuum), (4) Fredholm solvability (Section 3, zero-mode projection condition and drift formula).
- **CHECK 4 (Transfer and Falsifiability):** FAIL — The falsifiable numerical prediction in Section 4 contains an arithmetic/integral error: the integrated dose for the zero-mode-shaped inhibition `M_{P,c}` is computed incorrectly, which propagates to an incorrect dose-sparing ratio `R` and invalidates the stated numerical falsification thresholds.

#### Stage 3 Watch Items
- Recompute the integrals used in Section 4: verify that \(\int_{-\infty}^{\infty}\operatorname{sech}^2 x\,dx = 2\) and \(\int_{-\infty}^{\infty}\operatorname{sech}^4 x\,dx = 4/3\); confirm the correct expression for \(M_{P,c}\) and the corrected numerical value of \(R\).
- Check whether the incorrect \(M_{P,c}\) value was used elsewhere to set experimental thresholds (the falsification criterion `R<1.5` and the `M=1.1 M_{P,c}` test).
- Verify numerical evaluation of \(\tanh 3\) used in the uniform-dose calculation and ensure consistent units/scaling in the experimental prescription.
- Advisory prior-art note for Stage 3: the mapping of kink translational modes to zero-energy bound states and the SUSY factorization used here are canonical in the literature on kink stability and supersymmetric quantum mechanics; human reviewers should check for overlap with standard references on kink stability / SUSY QM.

### Eighth Adversarial Review
**Reviewer:** xAI Grok 4.5 Fast
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The linearized CSD operator after sign flip and gauge is identical to the dimensionless stationary Schrödinger operator under the stated potential identification, with matching continuum dispersion and zero-mode properties; no class mismatch.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All five token pairs are objects of compatible type (eigenvalues, multiplication operators, eigenfunctions, kinetic coefficients, inhomogeneous sources) with explicit shared mathematical structures rather than hedged analogy.
- **CHECK 3 (Correspondence Vector Support):** PASS — All four listed vectors are demonstrated by explicit derivation and operator identity in Section 3 (self-adjoint operator identity, SUSY zero-mode factorization, continuum dispersion match, and Fredholm projection equivalence).
- **CHECK 4 (Transfer and Falsifiability):** PASS — Transfer direction is asymmetric on the stated inverse-design bottleneck; the prediction supplies concrete critical amplitudes, integrated doses, and a numerical falsification threshold (R < 1.5) on a named PDE benchmark.

#### Stage 3 Watch Items
None identified.

### Ninth Adversarial Review
**Reviewer:** Meta Muse Spark 1.1
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — CSD linearization H_A=-∂_x^2 - f'(U0) with V_A=6tanh^2x-2 and quantum H_B*=-∂_x^2+V_B* are both self-adjoint second-order Schrödinger operators with explicit bridge V_B*=V_A and matching far-field continua E_A(k)=ε(k)=k^2+4; gauge removal of c∂_x term is derived correctly.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All five pairs are type-compatible: eigenvalue↔eigenvalue (λ↔ε with ε=-λ), multiplication operator↔multiplication operator (f'(U0)↔V_B* with V_B*=-f'), eigenfunction↔eigenfunction (U0'↔ψ0 with ψ0=-U0'), kinetic coefficient↔kinetic coefficient (D_K↔ħ²/2m), source field↔source field (η/b↔S) with explicit nondimensionalization and shared operator role.
- **CHECK 3 (Correspondence Vector Support):** PASS — All four listed vectors are demonstrated in body with equations: self_adjoint_csd_front_stability_to_stationary_schrodinger_operator in Demonstrated vector 1 (H_A=H_B*), translational_zero_mode_to_susy_zero_energy_bound_state in Demonstrated vector 2 (H_A=A†A, W=2tanh x, ψ0∝sech^2x), far_field_radiation_dispersion_to_free_particle_scattering_continuum in Demonstrated vector 3 (λ(k)=-k^2-4, E(k)=k^2+4), fredholm_zero_mode_solvability_source_projection in Demonstrated vector 4 (∫U0's=0 and ∫ψ0S=0 with c and N=1/3 derived).
- **CHECK 4 (Transfer and Falsifiability):** PASS — Asymmetry holds: quantum side has mature 1D spectral design toolkit (SUSY factorization, inverse scattering, Fredholm solvability) vs CSD bottleneck of minimal-dose inhibition patterning. Falsifiability holds: predicts B_{P,c}=c0/2, M_{P,c}=2c0/3=0.0333 for c0=0.05 vs B_{U,c}=c0/(3tanh3), M_{U,c}=2c0/tanh3=0.1005, R=3/tanh3≈3.015, falsified if R<1.5 or failure at M=1.1M_{P,c}. Advisory: underlying bistable front → Pöschl-Teller SUSY structure is textbook (Rajaraman; Cooper et al.) but domain pairing CSD↔QM is not canonical, so not a rejection – added to Stage 3 watch items.

#### Stage 3 Watch Items
- Textbook Pöschl-Teller kink stability and SUSY QM factorization is canonical mathematical physics – bibliometric search should verify novelty of applying zero-mode-shaped inhibition b_P= B_P sech^2x and Fredholm dose-sparing to CSD specifically.
- Verify whether full ionic/metabolic multiscale CSD models preserve the exact operator identity V_B*=-f'(U0) or introduce constitutive mismatch noted as primary failure risk.
- None identified beyond above.