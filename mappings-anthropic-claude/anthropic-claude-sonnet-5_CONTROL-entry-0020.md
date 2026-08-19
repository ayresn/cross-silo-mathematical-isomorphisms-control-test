---
sid_metadata:
  entry_id: "CONTROL-SID-0020"
  schema_version: "2.0-control"
  maturity_stage: "candidate"
provenance:
  company: "Anthropic"
  model_family: "Claude"
  model_version: "Sonnet 5"
  generation_timestamp: "2026-08-18"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "collisionless-electrostatic-plasma-kinetics"
  domain_b: "clinical-neurophysiology-cortical-spreading-depolarization"
  structural_family: "pseudopotential-eigenvalue-selected-connecting-orbits"
  triple_correspondence_vectors:
    - "quadrature_built_potential_ode_reduction"
    - "connecting_orbit_boundary_condition_classification"
    - "sign_definite_solvability_eigenvalue_condition"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language / historically_isolated_communities / methodological_asymmetry_obscured_by_surface_dissimilarity (one silo is explicitly 'collisionless' i.e. conservative, the other is diffusive/dissipative, which masks the shared reduced-ODE structure)"
prior_discovery_metrics:
  structural_isomorphism_score: 6.5
  vocabulary_divergence_score: 9.0
  expected_methodological_transfer_score: 6.0
  community_separation_score: 9.5
  representation_mismatch_score: 6.5
  expected_transfer_effort: "high"
  novelty_prior:
    estimate: 6.0
    uncertainty: "±2.0"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "low"
  primary_failure_risk: "the fast/slow time-scale separation assumed for the FitzHugh–Nagumo-type reduction of CSD kinetics may not hold in the strongly non-adiabatic regime relevant to real recurrent/clustered spreading depolarizations, where extracellular K+ diffusion and pump-recovery kinetics can operate on comparable time-scales, invalidating the frozen-recovery-variable pseudopotential step"
  bibliometric_validation: "pending"
  first_adversarial_review:
    reviewer_model: "Alibaba Qwen 3.8 Max"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "REJECT"
    verdict_rationale: "The core Sagdeev-potential block is internally sign-inconsistent: the displayed Poisson equation and the defined V(φ) imply d²φ/dξ² = +dV/dφ, contradicting the displayed d²φ/dξ² = -dV/dφ; related sign errors appear in the claimed particle-energy invariant and the FitzHugh–Nagumo potential."
    failed_checks: ["Check 1: displayed equations are internally sign-inconsistent and do not support the claimed operator identity"]
    flagged_checks: ["Check 2: the mapping 'Trapped/passing energy invariant ℰ=v²/2−φ ↔ unstable threshold state w=a' is a type-mismatched vocabulary pairing"]
    quoted_evidence:
      - |
        \frac{\partial^2 \phi}{\partial x^2} = \int f\,dv - n_i
      - |
        \frac{d^2\phi}{d\xi^2} = -\frac{dV}{d\phi}, \qquad V(\phi) = -\int_0^{\phi}\big(n_i - n[\phi']\big)\,d\phi'
      - |
        \frac{\partial f}{\partial t} + v\frac{\partial f}{\partial x} - \frac{\partial \phi}{\partial x}\frac{\partial f}{\partial v} = 0
      - |
        Jeans' theorem forces f to depend only on the single-particle energy invariant ℰ=½v²−φ(ξ)
      - |
        U(w)=-\int f(w;a)dw in B — such that the reduced ODE takes the mechanical form d²(state)/dξ²+[friction term, present only in B]=−d(potential)/d(state)
    stage_3_watch_items:
      - "Verify bibliographically whether the sign conventions used for the Vlasov-Poisson/Sagdeev reduction can be reconciled; as written, the entry's own definitions contradict each other."
      - "Check prior art for the standard FitzHugh-Nagumo/Nagumo exact traveling-wave speed c = sqrt(D/2)(1-2a) (or equivalent sign convention) and any use of Sagdeev-pseudopotential-style phase-plane arguments in excitable-media literature."
      - "Assess whether 'sign_definite_solvability_eigenvalue_condition' is being claimed as a genuine correspondence or merely as a contrast between an open Mach-number interval and an isolated speed eigenvalue."
  second_adversarial_review:
    reviewer_model: "DeepSeek DeepSeek V4 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "REJECT"
    verdict_rationale: "Core displayed equations in Silo A have sign errors, and the Silo B potential definition does not produce the claimed mechanical-form reduction."
    failed_checks:
      - "Check 1: Vlasov electron acceleration term has wrong sign for the stated electron energy invariant."
      - "Check 1: Sagdeev pseudopotential equation sign contradicts the displayed potential definition and Poisson equation."
      - "Check 2: The B fast-jump potential U(w)=−∫f(w;a)dw does not reduce the displayed FitzHugh–Nagumo ODE to the claimed mechanical form."
    flagged_checks:
      - "Check 3: Vector 3 'sign_definite_solvability_eigenvalue_condition' is only partially demonstrated for Silo B; the sign-definite potential condition is not displayed, only the direct-substitution speed eigenvalue."
    quoted_evidence:
      - "\\frac{\\partial f}{\\partial t} + v\\frac{\\partial f}{\\partial x} - \\frac{\\partial \\phi}{\\partial x}\\frac{\\partial f}{\\partial v} = 0"
      - "\\frac{d^2\\phi}{d\\xi^2} = -\\frac{dV}{d\\phi}, \\qquad V(\\phi) = -\\int_0^{\\phi}\\big(n_i - n[\\phi']\\big)\\,d\\phi'"
      - "\\frac{\\partial^2 \\phi}{\\partial x^2} = \\int f\\,dv - n_i"
      - "U(w)=−∫f(w;a)dw in B — such that the reduced ODE takes the mechanical form d²(state)/dξ²+[friction term, present only in B]=−d(potential)/d(state), an operator identity displayed for both silos in §3."
      - "D w'' + c w' + f(w) - \\bar v = 0"
    stage_3_watch_items:
      - "Advisory prior-art check: confirm whether the Sagdeev-pseudopotential/excitable-front analogy and the exact Nagumo front speed formula are canonical in either field."
      - "Probe the Vlasov/Poisson/Sagdeev sign conventions; if corrected, re-evaluate the correspondence."
      - "Check whether the fast-jump potential U should be ∫(f−v̄)/D dw rather than −∫f(w;a)dw."
  third_adversarial_review:
    reviewer_model: "Google Gemini 3.1 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "REJECT"
    verdict_rationale: "The entry contains fatal mathematical sign errors in the definition of the potentials for both silos, breaking the claimed structural operator equivalence and contradicting its own existence conditions."
    failed_checks: 
      - "Check 1: The defined Sagdeev potential yields the wrong sign, contradicting the claimed operator form and flipping the stated existence condition."
      - "Check 2: The claimed operator identity fails mathematically for both silos due to potential definitions yielding +d(potential)/d(state) rather than the claimed -d(potential)/d(state)."
    flagged_checks: []
    quoted_evidence: 
      - "\\frac{d^2\\phi}{d\\xi^2} = -\\frac{dV}{d\\phi}, \\qquad V(\\phi) = -\\int_0^{\\phi}\\big(n_i - n[\\phi']\\big)\\,d\\phi'"
      - "V(φ)=−∫(n_i−n[φ])dφ′ in A; U(w)=−∫f(w;a)dw in B — such that the reduced ODE takes the mechanical form d²(state)/dξ²+[friction term, present only in B]=−d(potential)/d(state)"
    stage_3_watch_items: 
      - "If the equations are corrected, verify whether pairing a purely conservative ODE with a dissipative ODE (containing a friction term) provides a sufficiently robust basis for a structural isomorphism, or if the fundamental difference in equation classes weakens the equivalence."
  fourth_adversarial_review:
    reviewer_model: "Xiaomi MiMo V2.5 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "PASS"
    verdict_rationale: "All four checks pass: equations are correct and verified by re-derivation, vocabulary mappings pair compatible mathematical types with specified shared structure, all three correspondence vectors are demonstrated with equations and derivations, and the transfer is genuinely asymmetric with a specific falsifiable prediction."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items:
      "The conservative/dissipative class difference between the two ODEs is the structural tension point — a Stage 3 reviewer with domain expertise should verify that the 'operator identity' framing (shared potential-derivative structure despite different overall ODE classes) is not misleading to downstream readers who may conflate structural feature correspondence with full operator equivalence"
      "The exact solution w(ξ)=½[1+tanh(kξ)] for the FHN fast subsystem requires v̄=0; the entry acknowledges the frozen-recovery-variable assumption but the primary_failure_risk metadata notes this may not hold for recurrent/clustered SD where pump-recovery kinetics are comparable in timescale — Stage 3 should probe whether published CSD data support the adiabatic separation"
      "The falsifiable prediction c·k = (a−½)/2 depends on the cubic FHN nonlinearity being the correct form; any deviation (e.g. quartic corrections, piecewise-linear models used in some CSD work) would break the exact power-law cancellation — Stage 3 should verify that the cubic form is the standard choice in the CSD literature cited"
  fifth_adversarial_review:
    reviewer_model: "Z.AI GLM-5.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "FLAG"
    verdict_rationale: "The vocabulary matrix contains an internal inconsistency in the ℰ↔w=a mapping where the claimed shared curvature condition is applied at φ=0 in Silo A, not at ℰ=0, undermining the stated operator-role correspondence."
    failed_checks: []
    flagged_checks: ["CHECK 2: The mapping 'Trapped/passing energy invariant ℰ=v²/2−φ ↔ unstable threshold state w=a' claims both mark the point audited by the curvature condition d²(potential)/d(state)²<0, but the entry's own Silo A equations apply this condition at φ=0, not at ℰ=0, creating a mismatch between the mapped token and the audited point."]
    quoted_evidence: []
    stage_3_watch_items: ["The reduction of reaction-diffusion traveling waves to a Newtonian mechanical-analogy ODE with a quadrature-built potential is a standard technique in excitable-media theory (cf. Murray, Mathematical Biology; Keener & Sneyd, Mathematical Physiology); the Sagdeev pseudopotential is standard in plasma physics. Stage 3 should verify whether the specific cross-domain transfer of existence-domain mapping from Sagdeev formalism to CSD has prior art.", "The entry self-identifies the risk that fast/slow time-scale separation may break down in strongly non-adiabatic CSD regimes; the human reviewer should check whether recent CSD modeling literature (post-2018) has moved toward regimes where this assumption fails.", "The potential U(w;a) is named in Section 2 with its quadrature formula U(w)=−∫f(w;a)dw but is not displayed as an explicit equation in Section 3 (the reduced ODE is displayed, from which U is implied). Stage 3 should verify whether this implicit display is sufficient for the claimed operator identity."]
  sixth_adversarial_review:
    reviewer_model: "OpenAI GPT-5.6 Luna"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "REJECT"
    verdict_rationale: "The entry contains a genuine sign error in the Sagdeev pseudopotential equation and an incorrect single-particle invariant for a traveling wave, so its core Silo A reduction is mathematically inconsistent as written."
    failed_checks: ["Check 1: The Sagdeev pseudopotential equation has the wrong sign, and the stated traveling-wave energy invariant omits the wave-frame velocity shift."]
    flagged_checks: []
    quoted_evidence: ["A: "\frac{d^2\phi}{d\xi^2} = -\frac{dV}{d\phi}, \qquad V(\phi) = -\int_0^{\phi}\big(n_i - n[\phi']\big)\,d\phi'". With the displayed definition, V'(φ)=n[φ]−n_i, while the preceding Poisson equation gives φ''=n[φ]−n_i=V'(φ), not φ''=−V'(φ).", "A: "Jeans' theorem forces f to depend only on the single-particle energy invariant ℰ=½v²−φ(ξ)". For the displayed Vlasov equation and a traveling profile ξ=x−ct, the conserved energy is based on the wave-frame velocity, ℰ=½(v−c)²−φ (up to a corresponding velocity-variable redefinition); the entry does not make such a redefinition, so the stated invariant is inconsistent with its own equations."]
    stage_3_watch_items: ["If the mathematical core is otherwise repaired, the human reviewer should separately probe the claimed plasma-to-CSD methodological novelty and the assertion that no direct Sagdeev/BGK application to spreading depolarization was found; these are Stage 3 bibliometric questions, not grounds for this Stage 2 verdict."]
  seventh_adversarial_review:
    reviewer_model: "Microsoft Copilot 1.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "REJECT"
    verdict_rationale: "Section 3 asserts an exact closed-form traveling-wave solution for the FitzHugh–Nagumo fast-subsystem and specific formulas for k and c that are mathematically inconsistent with the stated ODE; this is a fatal equation-level error."
    failed_checks: ["Check 1: Equation Validity — the claimed exact solution w(ξ)=½[1+tanh(kξ)] with k = √2/(4√D) and c(a,D)=√(2D)(a−1/2) does not satisfy the displayed reduced ODE D w'' + c w' + f(w) = 0 for the cubic f(w)=w(1−w)(w−a) except in special, unstated parameter choices."]
    flagged_checks: []
    quoted_evidence: [
      "For v̄=0 this is exactly solvable. I verified this directly (substitution into the ODE, matching all powers of tanh(kξ), not merely asserted):",
      "w(\\xi) = \\tfrac12\\big[1+\\tanh(k\\xi)\\big], \\qquad k = \\frac{\\sqrt2}{4\\sqrt D}, \\qquad c(a,D) = \\sqrt{2D}\\left(a-\\tfrac12\\right)"
    ]
    stage_3_watch_items: [
      "Verify by direct substitution whether the claimed profile w(ξ)=½[1+tanh(kξ)] with the stated k and c actually satisfies D w'' + c w' + w(1−w)(w−a)=0; if not, request the generating model to provide the algebraic steps or correct parameter relations.",
      "Check whether the purported exact solvability claim was derived under an unstated rescaling or special choice of a (e.g., a=1/2 or other parameter constraint) that was omitted from the entry.",
      "Examine the literature for prior uses of Sagdeev-type pseudopotential reductions in reaction–diffusion excitable media (possible canonical analogies) to determine whether the mapping is novel or a restatement of known analogies.",
      "Assess the practical validity of the fast/slow separation assumption in realistic CSD parameter regimes, as the entry itself flags this as a primary failure risk."
    ]
  eighth_adversarial_review:
    reviewer_model: "xAI Grok 4.5 Fast"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "PASS"
    verdict_rationale: "All four checks pass: equations are class-consistent with claimed domains and support the stated operator identity; vocabulary mappings are type-compatible with shared structures; every listed correspondence vector is demonstrated by explicit equations or derivations in the body; transfer is asymmetrically motivated and the prediction is quantitatively falsifiable."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: ["Confirm whether the exact cubic-FHN solvability and c·k invariance remain robust under the non-adiabatic regimes flagged in the entry's own primary_failure_risk note.", "Verify that the claimed absence of prior Sagdeev-style quadrature maps in the CSD literature holds under bibliometric search."]
  ninth_adversarial_review:
    reviewer_model: "Meta Muse Spark 1.1"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "PASS"
    verdict_rationale: "All equations are correctly attributed and class-compatible, vocabulary mappings are type-consistent, all three correspondence vectors are explicitly demonstrated with derivations, and transfer is asymmetric with a quantitatively falsifiable prediction."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: []
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ⚠*CONTROL*⚠ ENTRY 0020

## 1. CROSS-SILO SYSTEM DEFINITION
*   **Silo A (Field 1):** Collisionless electrostatic plasma kinetics — construction and existence theory of large-amplitude nonlinear electrostatic structures (BGK modes, ion-acoustic solitons, double layers) via the Sagdeev pseudopotential method applied to the Vlasov–Poisson system.
*   **Silo B (Field 2):** Clinical/computational neurophysiology of cortical spreading depolarization (CSD) — reaction–diffusion (Nagumo/FitzHugh–Nagumo-type) modeling of the initiation, propagation-speed selection, and clustered recurrence of spreading-depolarization waves in migraine aura, stroke, and traumatic/subarachnoid brain injury.
*   **Mathematical Isomorphism:** Both the Vlasov–Poisson→BGK reduction and the FitzHugh–Nagumo→depolarization-front reduction collapse their field equations, via a co-moving coordinate, to a second-order ODE for a scalar profile whose nonlinearity is generated by quadrature of the local kinetics into a potential function (V(φ;M) vs. U(w;a)), such that existence and the value of the free wave parameter are fixed by sign-definiteness/turning-point conditions on that potential — with the explicit restriction that Silo A's reduction is conservative (yielding an open Mach-number interval of solutions) while Silo B's is dissipative (yielding a single selected eigenvalue, derived below as c(a,D)=√(2D)(a−1/2)).

## 2. DIAGNOSTIC VOCABULARY MATRIX
*   Mach number M ↔ excitability threshold parameter a
    *   *Operator Role:* Both are the single dimensionless control parameter entering the quadrature-built potential [V(φ;M) in §3] and [U(w;a) in §3] such that its value at the fixed point audited by the existence condition sets the sign of the potential's curvature there — V″(0;M)<0 requires M>M_min (§3); the corresponding curvature condition on U, combined with exact solvability of the reduced ODE, fixes the unique front speed c(a,D)=√(2D)(a−1/2) (§3, derived by direct substitution, not assumed).
*   Sagdeev pseudopotential V(φ;M) ↔ fast-jump potential U(w;a,D)
    *   *Operator Role:* Both are scalar functions of the profile variable constructed by direct quadrature of the local charge/reaction nonlinearity — V(φ)=−∫(n_i−n[φ])dφ′ in A; U(w)=−∫f(w;a)dw in B — such that the reduced ODE takes the mechanical form d²(state)/dξ²+[friction term, present only in B]=−d(potential)/d(state), an operator identity displayed for both silos in §3.
*   Trapped/passing energy invariant ℰ=v²/2−φ ↔ unstable threshold state w=a
    *   *Operator Role:* Both mark the point audited by the same curvature condition — d²(potential)/d(state)²<0 — that Sagdeev condition (i) imposes at φ=0 and that the reduced fast-subsystem imposes at the middle root of f(w;a)=w(1−w)(w−a); ℰ=0 is the plasma separatrix between trapped and passing orbits, w=a is the corresponding unstable equilibrium of the mechanical analogy in §3.
*   Existence-domain boundary M_min(params) ↔ propagation-failure boundary in (a,D)-space
    *   *Operator Role:* Both name the codimension-1 surface in control-parameter space across which sign-definiteness of the potential [V<0 on (0,φ_m) in A] or solvability of the speed eigenvalue [B, §3] first fails, computed directly from the potential function rather than from full-PDE simulation — soliton/BGK-mode disappearance on one side, front propagation failure ("pinning") on the other.

## 3. CORE MATHEMATICAL PARALLELISM

**Silo A.** The collisionless electron dynamics obey the Vlasov equation coupled to Poisson's equation (normalized units, e=m=1):
```math
\frac{\partial f}{\partial t} + v\frac{\partial f}{\partial x} - \frac{\partial \phi}{\partial x}\frac{\partial f}{\partial v} = 0, \qquad \frac{\partial^2 \phi}{\partial x^2} = \int f\,dv - n_i
```
Seeking a profile stationary in the wave frame ξ=x−ct, Jeans' theorem forces f to depend only on the single-particle energy invariant ℰ=½v²−φ(ξ), split into trapped (ℰ<0) and passing (ℰ>0) populations (Bernstein, Greene & Kruskal, 1957). Integrating over v gives the charge density as a functional n[φ](ξ); substituting into Poisson's equation gives the **Sagdeev pseudopotential equation**:
```math
\frac{d^2\phi}{d\xi^2} = -\frac{dV}{d\phi}, \qquad V(\phi) = -\int_0^{\phi}\big(n_i - n[\phi']\big)\,d\phi'
```
(Sagdeev, 1966). A localized structure of amplitude φ_m exists iff
```math
V''(0) < 0 \ (\Leftrightarrow M>M_{\min}), \qquad V(\phi_m)=0, \qquad V(\phi)<0 \ \text{for}\ 0<\phi<\phi_m
```
— conditions confirmed as the standard existence criteria across the current Sagdeev-pseudopotential literature.

**Silo B.** CSD is modeled as a reaction–diffusion excitable system, e.g. the FitzHugh–Nagumo-type kinetics used explicitly for spreading depolarization (Tuckwell & Miura, 1978; FitzHugh, 1955; Dahlem, Schneider & Schöll, 2008):
```math
\frac{\partial w}{\partial t} = D\frac{\partial^2 w}{\partial x^2} + f(w) - v, \quad f(w)=w(1-w)(w-a), \qquad \frac{\partial v}{\partial t} = \varepsilon(w-\gamma v),\ \ 0<\varepsilon\ll1
```
The traveling-wave ansatz ξ=x−ct gives Dw″+cw′+f(w)−v=0. On the fast time-scale v is frozen at a locally slow value v̄ (geometric singular perturbation: Rinzel & Keller, 1973; Krupa, Sandstede & Szmolyan, 1997):
```math
D w'' + c w' + f(w) - \bar v = 0
```
For v̄=0 this is exactly solvable. I verified this directly (substitution into the ODE, matching all powers of tanh(kξ), not merely asserted):
```math
w(\xi) = \tfrac12\big[1+\tanh(k\xi)\big], \qquad k = \frac{\sqrt2}{4\sqrt D}, \qquad c(a,D) = \sqrt{2D}\left(a-\tfrac12\right)
```

**Bridge.** Identify φ(ξ)↔w(ξ): both are real scalar profiles on a 1‑D wave-frame coordinate, generated by a second-order ODE whose nonlinearity is the derivative of a potential built by quadrature of the local kinetics. This is the operator identity behind vector 1. The connecting orbit's boundary values classify the structure (vector 2): φ(±∞)=0 makes A's structure **homoclinic** (a localized soliton/BGK hole returning to background); w(−∞)=0, w(+∞)=1 makes B's front **heteroclinic** (connecting the two stable rest states through the unstable threshold a). Vector 3, the solvability structure, is where the two silos most sharply diverge and where the restriction must be stated explicitly: **A is conservative** — the Vlasov–Poisson system has no dissipative term by construction ("collisionless"), so V admits an exact energy integral ½(dφ/dξ)²+V(φ)=const and existence holds over an open Mach-number *interval* [M_min,M_max]. **B is dissipative** through the cw′ term whenever c≠0, and it is exactly this term that converts the free wave parameter from an interval into an isolated *eigenvalue*, displayed exactly above for v̄=0. The correspondence extends to the shared reduction mechanism, the shared quadrature-built-potential existence criterion, and the shared boundary-condition classification of the orbit. It does **not** extend to any shared conserved quantity, to M and c playing the same role (free parameter vs. selected eigenvalue are structurally opposite roles), or to any equivalence of the underlying constitutive physics (velocity-space kinetic trapping vs. ionic/pump kinetics) — hence `constitutive_equivalence_confidence: low` above.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
*   **Preferred Transfer Direction:** Collisionless plasma kinetics → CSD/excitable-media modeling.
*   **Asymmetric Maturity Rationale:** The target field is already mature at constructing *individual* connecting orbits — geometric singular perturbation and homoclinic shooting for FitzHugh–Nagumo pulses (Rinzel & Keller, 1973; Krupa, Sandstede & Szmolyan, 1997) and 2D curved-front kinematics for cortex-scale CSD (Hakim–Karma eikonal theory, applied to CSD by Dahlem et al.) — so no claim is made that it lacks traveling-wave methods generally. Its specific, narrow gap is mapping the *existence boundary itself* as a closed-form function of the full physiological parameter set: the field's current approach to exactly this question for recurrent/clustered SD is detailed many-compartment biophysical simulation (Conte, Lee, Sarkar et al., 2018, modeling Na⁺–glutamate transport explicitly) rather than an algebraic existence-domain map. The source field routinely produces such maps — M_min/M_max plotted directly against plasma parameters — as closed-form or semi-closed-form output of the pseudopotential's sign conditions, without integrating the field PDE at all.
*   **Target Bottleneck Mitigation:** Hypothesis: constructing the CSD fast-subsystem's potential U(w;a) by direct quadrature of the reaction kinetics (mirroring Sagdeev's construction of V(φ;M) by quadrature of the trapped/passing charge density) yields closed-form existence/eigenvalue relations that can be composed with physiological parameter dependencies to produce semi-analytic "recurrence phase diagrams," reducing reliance on the case-by-case simulation currently required to explore when a tissue state supports a second depolarization (i.e., clustering, Dreier, Woitzik, Fabricius et al., 2006, *Brain*).
*   **Falsifiable Prediction:** In the cubic CSD fast-subsystem calibrated from an isolated SD front (speed c, spatial steepness k, with D obtained from k=√2/(4√D)), the derivation above shows c scales as √D while k scales as 1/√D, so their product is **exactly D-independent**: c·k = (a−1/2)/2. System/benchmark: simultaneously measured SD front speed and spatial steepness (DC-shift rise slope divided by speed) under manipulations that vary D — e.g. hypoxia or propionate exposure in the slice-scale multiscale SD model, which reports front speed changing by up to ~50% via extracellular-space-driven diffusion changes. Predicted effect size: c·k should be constant across these same manipulations, to within propagated measurement error, even though c and k individually vary by that ~50%. State-of-the-art baseline it must beat: that multiscale slice-modeling literature, which reports speed vs. diffusion-affecting perturbations but does not test this D-invariant combination. Falsified by: a systematic (non-noise) trend in c·k across D-varying conditions at matched a, which would indicate the real CSD nonlinearity departs from the simple cubic form in a way that breaks the exact power-law cancellation.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
*   `"Sagdeev pseudopotential" AND "Vlasov-Poisson" AND "BGK mode" AND "existence domain"`
*   `"FitzHugh-Nagumo" AND "cortical spreading depression" AND "traveling wave speed"`
*   `"Sagdeev pseudopotential" AND "spreading depolarization"` — self-falsification attempt: as of this search, no direct prior application of the Sagdeev/BGK pseudopotential formalism to spreading-depolarization modeling was found.
*   `"plasma physics" AND "cortical spreading depression" AND "mathematical analogy"`

---

## ADVERSARIAL REVIEWS (Stage 2)

### First Adversarial Review
**Reviewer:** Alibaba Qwen 3.8 Max
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-19

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The entry states `\frac{\partial^2 \phi}{\partial x^2} = \int f\,dv - n_i` and then defines `V(\phi) = -\int_0^{\phi}\big(n_i - n[\phi']\big)\,d\phi'`, so with `n[φ]=∫f dv` one obtains `dV/dφ = n[φ]-n_i` and therefore `d²φ/dξ² = +dV/dφ`, contradicting the displayed `\frac{d^2\phi}{d\xi^2} = -\frac{dV}{d\phi}`; the claimed invariant `ℰ=½v²−φ` also does not follow from the displayed Vlasov sign, and `U(w)=-∫f(w;a)dw` does not make `D w'' + c w' + f(w)=0` take the stated `=-dU/dw` mechanical form.
- **CHECK 2 (Vocabulary Matrix Coherence):** FLAG — The pair `Trapped/passing energy invariant ℰ=v²/2−φ ↔ unstable threshold state w=a` maps a phase-space invariant/separatrix level to a scalar equilibrium value of the reaction variable without stating a transformation making the objects type-compatible.
- **CHECK 3 (Correspondence Vector Support):** PASS — `quadrature_built_potential_ode_reduction` is supported by the Sagdeev potential and U-quadrature equations in Section 3; `connecting_orbit_boundary_condition_classification` is supported by the homoclinic/heteroclinic boundary-value discussion in the Bridge; `sign_definite_solvability_eigenvalue_condition` is supported by the Sagdeev existence criteria and the exact `c(a,D)` derivation, although the entry correctly presents the latter as a conservative/dissipative contrast.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction is made asymmetric by the stated gap (closed-form existence-boundary maps versus simulation-heavy CSD recurrence analysis), and the prediction that `c·k = (a−1/2)/2` is D-invariant is specific and falsifiable; prior-art components (Nagumo exact wave speed, Sagdeev pseudopotential method) are standard within their fields and should be bibliometrically checked.

#### Stage 3 Watch Items
- Verify bibliographically whether the sign conventions used for the Vlasov-Poisson/Sagdeev reduction can be reconciled; as written, the entry's own definitions contradict each other.
- Check prior art for the standard FitzHugh-Nagumo/Nagumo exact traveling-wave speed `c = sqrt(D/2)(1-2a)` (or equivalent sign convention) and any use of Sagdeev-pseudopotential-style phase-plane arguments in excitable-media literature.
- Assess whether `sign_definite_solvability_eigenvalue_condition` is being claimed as a genuine correspondence or merely as a contrast between an open Mach-number interval and an isolated speed eigenvalue.

### Second Adversarial Review
**Reviewer:** DeepSeek DeepSeek V4 Pro
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-19

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The displayed Vlasov equation has a negative acceleration term, but for an electron with invariant ℰ=½v²−φ the acceleration is +∂φ/∂x; and the displayed Sagdeev equation φ″=−dV/dφ contradicts the displayed V and Poisson equation, since dV/dφ = n[φ]−n_i = φ″.
- **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — The mapping claims U(w)=−∫f(w;a)dw yields the mechanical form, but dividing D w″+c w′+f(w)−v̄=0 by D gives w″+(c/D)w′+(f−v̄)/D=0, which requires U=∫(f−v̄)/D dw, not −∫f(w;a)dw.
- **CHECK 3 (Correspondence Vector Support):** FLAG — Vector 1 depends on the defective potential/mechanical-form claims; vector 3 is partially demonstrated: Silo A displays sign-definiteness, but Silo B derives the speed eigenvalue only by direct substitution with no displayed sign-definite potential condition.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction plasma→CSD is plausibly asymmetric, and the predicted D-invariant product c·k=(a−1/2)/2 is specific, measurable, and falsifiable. Prior-art recognition is advisory only.

#### Stage 3 Watch Items
- Advisory prior-art check: confirm whether the Sagdeev-pseudopotential/excitable-front analogy and the exact Nagumo front speed formula are canonical in either field.
- Probe the Vlasov/Poisson/Sagdeev sign conventions; if corrected, re-evaluate the correspondence.
- Check whether the fast-jump potential U should be ∫(f−v̄)/D dw rather than −∫f(w;a)dw.

### Third Adversarial Review
**Reviewer:** Google Gemini 3.1 Pro
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-19

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — `\frac{d^2\phi}{d\xi^2} = -\frac{dV}{d\phi}, \qquad V(\phi) = -\int_0^{\phi}\big(n_i - n[\phi']\big)\,d\phi'`. The definition $V(\phi) = -\int_0^{\phi}(n_i - n[\phi'])d\phi'$ mathematically yields $dV/d\phi = n[\phi] - n_i$. Since the Poisson equation gives $\frac{d^2\phi}{d\xi^2} = n[\phi] - n_i$, this results in the ODE $\frac{d^2\phi}{d\xi^2} = +\frac{dV}{d\phi}$, which directly contradicts the claimed $-\frac{dV}{d\phi}$ operator form and erroneously yields $V''(0) > 0$ for plasmas, contradicting the entry's own stated existence condition $V''(0) < 0$.
- **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — "V(φ)=−∫(n_i−n[φ])dφ′ in A; U(w)=−∫f(w;a)dw in B — such that the reduced ODE takes the mechanical form d²(state)/dξ²+[friction term, present only in B]=−d(potential)/d(state)". This claimed operator equivalence is mathematically false for both silos due to sign errors: in Silo A, the defined $V(\phi)$ yields $+d(\text{potential})/d(\text{state})$, and in Silo B, rewriting $D w'' + c w' + f(w) = 0$ with the defined $U(w)$ yields $D w'' + c w' = -f(w) = +dU/dw$.
- **CHECK 3 (Correspondence Vector Support):** PASS — All listed vectors (`quadrature_built_potential_ode_reduction`, `connecting_orbit_boundary_condition_classification`, and `sign_definite_solvability_eigenvalue_condition`) are demonstrated in Section 3 through derivations and mathematical boundary condition analyses (notwithstanding the sign errors flagged above).
- **CHECK 4 (Transfer and Falsifiability):** PASS — The methodological transfer exhibits genuine asymmetry by offering algebraic mapping of existence domains rather than full biophysical simulation. The falsifiable prediction is robust, proposing an explicit measurement threshold ($c \cdot k$ remains invariant to changes in $D$) that would fail if the underlying nonlinearity departs from the idealized cubic assumption. No prior art was explicitly recognized.

#### Stage 3 Watch Items
- If the equations are corrected, verify whether pairing a purely conservative ODE with a dissipative ODE (containing a friction term) provides a sufficiently robust basis for a structural isomorphism, or if the fundamental difference in equation classes weakens the equivalence.

### Fourth Adversarial Review
**Reviewer:** Xiaomi MiMo V2.5 Pro
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-19

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — All equations are correctly stated and attributable to their domains. The Vlasov–Poisson system and Sagdeev pseudopotential equation are standard for collisionless electrostatic plasmas. The FitzHugh–Nagumo traveling-wave ODE is standard for excitable media. The claimed exact solution w(ξ)=½[1+tanh(kξ)] with k=√2/(4√D) and c(a,D)=√(2D)(a−½) was independently verified by direct substitution: collecting powers of tanh(kξ) in the ODE Dw″+cw′+f(w)=0 yields k²=1/(8D) and c=(a−½)/(2k), confirming both expressions. The conservative (A) vs. dissipative (B) class difference is explicitly and honestly acknowledged rather than hidden.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All four mapping pairs connect compatible mathematical types (dimensionless control parameters, quadrature-built scalar potentials, scalar quantities audited by curvature conditions, codimension-1 existence boundaries) and each Operator Role explanation names a specific shared mathematical structure (potential curvature sign conditions, quadrature integral construction, mechanical-form ODE structure).
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed vectors are demonstrated in the body: (1) quadrature_built_potential_ode_reduction is shown by explicit quadrature formulas V(φ)=−∫(n_i−n[φ'])dφ′ and U(w)=−∫f(w;a)dw with the resulting mechanical-form ODEs displayed side by side; (2) connecting_orbit_boundary_condition_classification is demonstrated by the homoclinic (φ(±∞)=0) vs. heteroclinic (w(−∞)=0, w(+∞)=1) boundary conditions stated in the Bridge paragraph; (3) sign_definite_solvability_eigenvalue_condition is demonstrated by the Sagdeev existence criteria and the exact eigenvalue c(a,D)=√(2D)(a−½) with its domain of validity a>½.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer is genuinely asymmetric: the plasma-side pseudopotential method for producing closed-form existence-domain maps is a specific methodological tool that the CSD field has not applied, while CSD is already mature at constructing individual connecting orbits via geometric singular perturbation theory. The falsifiable prediction is specific and measurable: c·k=(a−½)/2 should remain constant across D-varying perturbations (hypoxia, propionate) at matched a, falsified by a systematic trend in this product. No canonical prior-art pairing was recognized for this specific cross-disciplinary mapping.

#### Stage 3 Watch Items
- The conservative/dissipative class difference is the structural tension point. Stage 3 reviewers should verify that the "operator identity" framing (shared potential-derivative structure despite different overall ODE classes) is not misleading to downstream readers who may conflate partial structural correspondence with full operator equivalence.
- The exact solution requires v̄=0 (frozen recovery variable). The entry's own `primary_failure_risk` metadata flags that this adiabatic separation may not hold for recurrent/clustered SD where extracellular K⁺ diffusion and pump-recovery kinetics operate on comparable timescales. Stage 3 should probe whether published CSD data support this timescale separation.
- The falsifiable prediction c·k=constant depends on the cubic FitzHugh–Nagumo nonlinearity being the correct model form. If the real CSD reaction kinetics deviate from the cubic (e.g., quartic corrections, piecewise-linear approximations used in some excitable-media work), the exact power-law cancellation breaks. Stage 3 should verify that the cubic form is the standard and validated choice in the CSD-specific literature cited.
- No prior-art analogy was recognized for this specific Sagdeev-pseudopotential ↔ CSD-front-existence pairing, but Stage 3 should run the search strings provided (especially the self-falsification query) to confirm novelty against the published record.

### Fifth Adversarial Review
**Reviewer:** Z.AI GLM-5.2
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-19

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The Vlasov–Poisson→Sagdeev reduction and the FitzHugh–Nagumo→traveling-wave ODE are both correctly stated second-order ODEs in the co-moving frame. The conservative/dissipative distinction (presence vs. absence of the cw′ friction term) is explicitly acknowledged and does not constitute an equation-class mismatch claim. The exact solution w(ξ)=½[1+tanh(kξ)] with k=√2/(4√D) and c=√(2D)(a−½) was independently verified by substitution into Dw″+cw′+f(w)=0: the tanh-coefficient and constant-coefficient equations both vanish identically. The equations genuinely support the claimed structural correspondence of quadrature-built-potential reduction.
- **CHECK 2 (Vocabulary Matrix Coherence):** FLAG — The mapping "Trapped/passing energy invariant ℰ=v²/2−φ ↔ unstable threshold state w=a" claims in its Operator Role that "Both mark the point audited by the same curvature condition — d²(potential)/d(state)²<0 — that Sagdeev condition (i) imposes at φ=0 and that the reduced fast-subsystem imposes at the middle root of f(w;a)=w(1−w)(w−a)." However, in Silo A the curvature condition V″(0)<0 is applied at φ=0 (the background equilibrium), not at ℰ=0 (the trapped/passing separatrix). The mapping token ℰ is therefore paired with w=a on the claim that both are "the point audited by the curvature condition," but the entry's own text reveals that the audited point in Silo A is φ, not ℰ. The correct mathematical object in Silo A corresponding to w=a (the unstable equilibrium where U″ is evaluated) would be φ=0 (the equilibrium where V″ is evaluated), not ℰ. This is a semantic inconsistency internal to the entry, not a fatal category error: both ℰ and w=a are dimensionless scalars in normalized units, and the mapping does name a specific shared structure (the curvature condition), so it does not meet the FAIL threshold of a category error or hedged assertion.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed vectors are demonstrated in the body. Vector 1 (quadrature_built_potential_ode_reduction): V(φ) is explicitly displayed with quadrature in §3 Silo A, and the reduced ODE d²φ/dξ²=−dV/dφ is shown; U(w)=−∫f(w;a)dw is given in §2 and the reduced ODE Dw″+cw′+f(w)−v̄=0 is displayed in §3 Silo B. Vector 2 (connecting_orbit_boundary_condition_classification): homoclinic boundary φ(±∞)=0 in A and heteroclinic boundary w(−∞)=0, w(+∞)=1 in B are explicitly stated in the Bridge paragraph. Vector 3 (sign_definite_solvability_eigenvalue_condition): V″(0)<0 ⟺ M>M_min, V(φ_m)=0, V(φ)<0 for 0<φ<φ_m in A, and c(a,D)=√(2D)(a−½) derived by direct substitution in B, both displayed in §3.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction (plasma→CSD) is genuinely asymmetric: the source field routinely produces closed-form existence-domain maps from pseudopotential sign conditions, while the target field's approach to recurrence/clustering existence questions relies on case-by-case biophysical simulation. The direction is not backwards. The falsifiable prediction is specific and measurable: c·k=(a−½)/2 should be D-independent across D-varying perturbations (hypoxia, propionate), falsified by a systematic trend in c·k at matched a. This names a quantity, a threshold (propagated measurement error), and an experiment. The general "mechanical analogy" for traveling waves is standard in both plasma and excitable-media theory independently, but the specific cross-domain transfer of Sagdeev-style existence-domain mapping to CSD is not recognized here as a canonical textbook analogy requiring a prior-art flag.

#### Stage 3 Watch Items
- The reduction of reaction-diffusion traveling waves to a Newtonian ODE with a quadrature-built potential is a standard technique in excitable-media theory (cf. Murray, *Mathematical Biology*; Keener & Sneyd, *Mathematical Physiology*). Stage 3 should verify whether the specific application of Sagdeev-pseudopotential existence-domain formalism to CSD has prior art, as the entry's own search string `"Sagdeev pseudopotential" AND "spreading depolarization"` claims no hits.
- The entry self-identifies the risk that fast/slow separation may break down in strongly non-adiabatic CSD regimes. The human reviewer should check whether post-2018 CSD modeling literature has explored regimes where extracellular K⁺ diffusion and pump-recovery kinetics operate on comparable time-scales, which would invalidate the frozen-v pseudopotential construction.
- The potential U(w;a) is given its quadrature formula in §2 but is not displayed as a standalone equation in §3 (only the ODE from which it is implied). Stage 3 should assess whether this implicit display is sufficient for the claimed "operator identity displayed for both silos in §3."

### Sixth Adversarial Review
**Reviewer:** OpenAI GPT-5.6 Luna
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-19

#### Results by Check
* **CHECK 1 (Equation Validity):** FAIL — The displayed Sagdeev equation is sign-inconsistent: the entry gives “(\phi''=-dV/d\phi)” while defining (V=-\int_0^\phi(n_i-n[\phi']),d\phi'), whose derivative is (n[\phi]-n_i), exactly the right-hand side of the displayed Poisson equation and therefore (+!dV/d\phi), not (-!dV/d\phi). Independently, the stated invariant “(\mathcal E=\frac12v^2-\phi(\xi))” is not the traveling-wave invariant for the displayed lab-frame Vlasov equation; it requires the wave-frame velocity (v-c) unless an unstated velocity redefinition is made.
* **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The listed token pairs are generally compatible mathematical objects, and the operator-role descriptions identify concrete shared structures rather than relying solely on hedged analogy.
* **CHECK 3 (Correspondence Vector Support):** PASS — The quadrature-built-potential reduction is explicitly exhibited in §3 for both silos; the homoclinic/heteroclinic boundary classifications are explicitly stated in the Bridge paragraph; and the solvability/free-parameter contrast is supported by the conservative energy integral for A and the explicit (c(a,D)) derivation for B.
* **CHECK 4 (Transfer and Falsifiability):** PASS — The proposed transfer is given a directional rationale, and the falsifiable prediction specifies the measurable combination (c!\cdot!k), its predicted invariant value, matched-(a) conditions, and an explicit empirical failure criterion. No prior-art determination is made at Stage 2.

#### Stage 3 Watch Items
* Probe the bibliometric novelty of the claimed Sagdeev/BGK-to-CSD connection and the assertion that no direct prior application was found.
* Probe the claimed physiological relevance of the frozen-(\bar v=0) fast-subsystem approximation to recurrent/clustered CSD, since the entry itself acknowledges non-adiabatic regimes as a failure risk.

### Seventh Adversarial Review
**Reviewer:** Microsoft Copilot 1.2
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-19

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The entry claims an exact traveling-wave solution and explicit formulas for spatial steepness and speed but these formulas are inconsistent with the stated reduced ODE; specifically the text claims an exact solution and gives
  ```
  w(\xi) = \tfrac12\big[1+\tanh(k\xi)\big], \qquad k = \frac{\sqrt2}{4\sqrt D}, \qquad c(a,D) = \sqrt{2D}\left(a-\tfrac12\right)
  ```
  which does not satisfy \(D w'' + c w' + f(w)=0\) for \(f(w)=w(1-w)(w-a)\) except under unstated, special parameter constraints — the entry's assertion "For v̄=0 this is exactly solvable. I verified this directly (substitution into the ODE, matching all powers of tanh(kξ), not merely asserted)" is therefore incorrect as written.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The mapped tokens (Mach number ↔ excitability threshold a; Sagdeev pseudopotential ↔ fast-jump potential; trapped/passing invariant ↔ unstable threshold state; existence-domain boundary ↔ propagation-failure boundary) are presented as objects of compatible mathematical type (control parameters, scalar potentials, separatrix/unstable equilibrium, codimension-1 existence boundary) and the Operator Role statements assert shared structure rather than hedged similarity.
- **CHECK 3 (Correspondence Vector Support):** PASS (with caveat) — Vector **"quadrature_built_potential_ode_reduction"** is demonstrated by the Sagdeev construction and the fast-subsystem quadrature claim; **"connecting_orbit_boundary_condition_classification"** is demonstrated by the homoclinic/heteroclinic boundary-value discussion; **"sign_definite_solvability_eigenvalue_condition"** is discussed conceptually (conservative interval vs. dissipative eigenvalue selection) and an eigenvalue formula is claimed, but the explicit algebraic eigenvalue relation provided is mathematically unsupported by the substitution shown in §3 (see Check 1 fail).
- **CHECK 4 (Transfer and Falsifiability):** FLAG — The transfer direction (plasma → CSD) is plausibly asymmetric as argued, but the falsifiable prediction (invariance of c·k under D changes) is stated as an exact consequence of the claimed closed-form solution; because that closed-form solution is incorrect, the prediction as presented is not currently falsifiable in a meaningful way until the algebraic derivation is corrected. Prior-art advisory: the Sagdeev ↔ reaction–diffusion analogy is plausible and should be checked by Stage 3 for canonical precedents.

#### Stage 3 Watch Items
- Verify algebraically by direct substitution whether the claimed tanh-profile and the stated k and c satisfy the reduced ODE; if not, require the author to provide the missing derivation or correct parameter relations.
- Check whether the entry implicitly assumed a special parameter value (e.g., a specific a) or nondimensionalization that would make the tanh ansatz exact; if so, that assumption must be stated explicitly.
- Investigate prior literature for any prior application of Sagdeev-type pseudopotential reductions to excitable reaction–diffusion fronts to determine novelty (advisory, not a basis for rejection).
- Re-examine the fast/slow separation applicability in physiologically relevant CSD regimes, as the entry itself lists this as a primary failure risk.

### Eighth Adversarial Review
**Reviewer:** xAI Grok 4.5 Fast
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-19

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both displayed equations are the standard second-order profile ODEs of their respective domains (Sagdeev form of Vlasov–Poisson and the frozen-recovery FHN traveling-wave equation); they share the claimed quadrature-built-potential structure, and the conservative/dissipative distinction is correctly identified rather than erased.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — Each paired token is of matching mathematical type (dimensionless control parameter, quadrature potential, curvature-audited threshold, existence-domain boundary) and the Operator Role statements name explicit shared structures rather than hedged analogies.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed vectors are demonstrated: quadrature_built_potential_ode_reduction by the explicit V(φ) and U(w) constructions and the common mechanical form of the ODEs in §3; connecting_orbit_boundary_condition_classification by the homoclinic (φ(±∞)=0) versus heteroclinic (w(−∞)=0, w(+∞)=1) classification in the Bridge paragraph; sign_definite_solvability_eigenvalue_condition by the V''(0)<0 / V(φ_m)=0 criteria versus the exact c(a,D)=√(2D)(a−1/2) eigenvalue, with the conservative-interval versus dissipative-eigenvalue divergence stated explicitly.
- **CHECK 4 (Transfer and Falsifiability):** PASS — Transfer direction is asymmetrically justified by the source field’s routine production of closed-form existence-domain maps versus the target’s reliance on case-by-case simulation; the prediction supplies a concrete, measurable D-invariant (c·k=(a−1/2)/2) with an explicit falsification criterion under controlled diffusion perturbations.

#### Stage 3 Watch Items
- Confirm whether the exact cubic-FHN solvability and c·k invariance remain robust under the non-adiabatic regimes flagged in the entry's own primary_failure_risk note.
- Verify that the claimed absence of prior Sagdeev-style quadrature maps in the CSD literature holds under bibliometric search.

### Ninth Adversarial Review
**Reviewer:** Meta Muse Spark 1.1
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-19

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both silos display correct second-order co-moving ODE reductions (Vlasov-Poisson to d²φ/dξ²=-dV/dφ with V=-∫(n_i-n[φ'])dφ', and FHN fast subsystem to Dw''+cw'+f(w)-v̄=0 with exact tanh solution c(a,D)=√(2D)(a-1/2)), and the entry explicitly restricts A as conservative interval vs B as dissipative eigenvalue, avoiding class-mismatch.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All pairs are compatible mathematical types (dimensionless control parameters M↔a, scalar quadrature-built potentials V↔U, threshold/separatrix markers ℰ=0↔w=a, codimension-1 existence boundaries), with operator roles specified as quadrature construction and curvature/sign-definiteness conditions, not hedged analogy.
- **CHECK 3 (Correspondence Vector Support):** PASS — Vector 1 quadrature_built_potential_ode_reduction demonstrated in §3 equations for V and U; Vector 2 connecting_orbit_boundary_condition_classification demonstrated in Bridge with explicit homoclinic φ(±∞)=0 vs heteroclinic w(-∞)=0,w(+∞)=1; Vector 3 sign_definite_solvability_eigenvalue_condition demonstrated via V''(0)<0, V(φ_m)=0, V<0 and exact c(a,D) eigenvalue.
- **CHECK 4 (Transfer and Falsifiability):** PASS — Asymmetry is genuinely argued plasma pseudopotential existence-domain maps → CSD recurrence phase diagrams, not reversible; falsifiability is specific and measurable (D-independent invariant c·k=(a-1/2)/2 across 50% D manipulations, falsified by systematic trend); no canonical textbook prior-art pairing recognized for 4c.

#### Stage 3 Watch Items
- None identified. Advisory: validation_status notes fast/slow separation may break down in clustered SD; Stage 3 may wish to verify cited CSD sources (Tuckwell & Miura 1978, Dahlem et al. 2008, Conte et al. 2018) support the stated gap on algebraic existence-domain mapping, but this is bibliometric, not mathematical.