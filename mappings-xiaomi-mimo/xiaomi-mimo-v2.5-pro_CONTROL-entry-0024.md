---
sid_metadata:
  entry_id: "CONTROL-SID-0024"
  schema_version: "2.0-control"
  maturity_stage: "adversarial-rejected"
provenance:
  company: "Xiaomi"
  model_family: "MiMo"
  model_version: "V2.5 Pro"
  generation_timestamp: "2026-08-18"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "early-universe-cosmology"
  domain_b: "computational-micromagnetics"
  structural_family: "bogomolny-bps-domain-walls-and-poschl-teller-fluctuation-spectra"
  triple_correspondence_vectors:
    - "bps_first_order_equation_from_superpotential_factorization"
    - "topological_bps_energy_bound_via_bogomolny_completion"
    - "poschl_teller_fluctuation_spectrum_depth_parameter_from_wall_profile"
    - "topological_charge_winding_number_of_order_parameter_map"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language / incompatible_ontologies / historically_isolated_communities / bps_structure_invoked_independently_in_each_field_without_cross_reference / cosmological_and_micromagnetic_domain_wall_communities_read_different_journals_attend_different_conferences"
prior_discovery_metrics:
  structural_isomorphism_score: 7.0
  vocabulary_divergence_score: 9.0
  expected_methodological_transfer_score: 6.5
  community_separation_score: 9.0
  representation_mismatch_score: 7.0
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 7.0
    uncertainty: "±1.5"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "full_dynamics_governed_by_different_equation_classes_hyperbolic_vs_dispersive_parabolic_correspondence_limited_to_static_bps_sector_and_linearized_fluctuations"
  bibliometric_validation: "pending"
  first_adversarial_review:
    reviewer_model: "Anthropic Claude Sonnet 5"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "REJECT"
    verdict_rationale: "The general superpotential relation V(u) = (W′)²/(2α) stated in Section 2 and restated as Vector 1's premise is algebraically wrong (the entry's own cosmological and magnetic equations both demonstrate V(u) = (W′)²/(4α) instead), and the vocabulary matrix gives two mutually contradictory, dimensionally-incompatible values for the magnon continuum threshold (K/A in Section 2 versus the correctly-derived K in Section 3/Vector 3)."
    failed_checks:
      - "Check 1: stated general relation V(u) = (W′)²/(2α) is algebraically incorrect; the entry's own equations demonstrate V(u) = (W′)²/(4α)"
      - "Check 2: vocabulary matrix's 'λ_c = K/A = 1/Δ²' contradicts Section 3/Vector 3's own derived threshold 'λ > K'; related error in the Self-coupling row's 'm²_mag = 2K = 2/Δ²'"
    flagged_checks:
      - "Check 4: prediction (a) miscalculates 4√(AK_eff) as 6.0×10⁻³ J/m² when the entry's own numbers give ≈1.2×10⁻² J/m²; prediction (c)'s stated formula 2K_eff/μ₀M_s does not evaluate to its own quoted 1.5 T under standard SI μ₀"
      - "Check 4c: prior-art advisory — Bogomolny/superpotential BPS methods for domain-wall solitons are a standard technique spanning cosmological field theory and condensed-matter/magnetic soliton systems"
    quoted_evidence:
      - "Both satisfy V(u) = (W′)²/(2α) (where α is the kinetic coefficient) and yield the BPS equation du/dx = W′/(2α)."
      - "Both second-order Euler-Lagrange equations factor into first-order BPS equations via a superpotential W(u) satisfying V(u) = (W′)²/(2α)."
      - "Verification: W″(φ)·W′(φ)/α = −2√(2λ)φ·√(2λ)(η²−φ²)/(½) = −4λφ(η²−φ²) = −V′(φ). ✓"
      - "Magnon continuum edge λ\_c = K/A = 1/Δ²"
      - "Continuum threshold | — | λ/K − 1 > 0 | **λ > K**"
      - "m²\_mag = 2K = 2/Δ²"
      - "σ\_w ≥ 4√(AK\_eff) = 4√(1.5 × 10⁻¹¹ × 6 × 10⁵) ≈ **6.0 × 10⁻³ J/m²**"
    stage_3_watch_items:
      - "General Bogomolny/superpotential domain-wall methods are well known across both cosmological field theory and condensed-matter soliton physics (e.g. Manton & Sutcliffe, Topological Solitons); check specifically for prior publication of the n=2-vs-n=1 Pöschl-Teller depth comparison between a cosmological φ⁴ wall and a uniaxial magnetic domain wall"
      - "If revised, Section 4(a)'s falsifiable threshold needs correction from 6.0×10⁻³ J/m² to ≈1.2×10⁻² J/m² before use as a simulation-validation bound"
      - "Verify the intended formula/units in Section 4(c): the quoted 1.5 T matches 2K_eff/M_s, not the stated 2K_eff/μ₀M_s"
      - "Given the multiple factor-of-2-type errors identified here, spot-check other quantitative claims in Section 4 before relying on this entry's claim that the BPS framework transfers mechanically to new anisotropy landscapes"
  second_adversarial_review:
    reviewer_model: "Alibaba Qwen 3.8 Max"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "REJECT"
    verdict_rationale: "The entry contains an algebraically false BPS verification and a factor-of-two error in its quantitative BPS energy-bound prediction."
    failed_checks:
      - "Check 1: cosmological superpotential verification is algebraically incorrect and contradicts the stated BPS factorization"
      - "Check 4: quantitative energy-bound prediction evaluates 4√(AK_eff) incorrectly by a factor of two"
    flagged_checks:
      - "Check 2: m²_mag = 2K = 2/Δ² is dimensionally/internally inconsistent unless an unstated A=1 convention is used"
      - "Check 4(c): prior-art recognition for kink/domain-wall Pöschl-Teller analogies in soliton literature"
    quoted_evidence:
      - |
        Verification: W″(φ)·W′(φ)/α = −2√(2λ)φ·√(2λ)(η²−φ²)/(½) = −4λφ(η²−φ²) = −V′(φ). ✓
      - |
        σ_w ≥ 4√(AK_eff) = 4√(1.5 × 10⁻¹¹ × 6 × 10⁵) ≈ **6.0 × 10⁻³ J/m²**
    stage_3_watch_items:
      - "Verify whether the φ⁴ kink/Bloch-wall BPS and Pöschl-Teller correspondence is already present in cross-domain soliton reviews (e.g., Rajaraman’s Solitons and Instantons; Manton and Sutcliffe’s Topological Solitons)."
      - "Reconcile magnetic mass-gap/continuum notation: Section 2 uses m²_mag = 2K = 2/Δ² and λ_c = K/A, while Section 3’s eigenvalue problem gives continuum λ > K."
      - "Check the asymptotic wall-wall interaction decay on the cosmological side: the stated exp(−x/δ) conflicts with the stated continuum threshold ω²_c = 4/δ_w², which would imply exp(−2x/δ_w) if κ = √(eigenvalue gap)."
  third_adversarial_review:
    reviewer_model: "DeepSeek DeepSeek V4 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "REJECT"
    verdict_rationale: "The entry contains a false displayed BPS verification equation, dimensionally inconsistent micromagnetic continuum-threshold and mass-gap equalities, and a dimensionally invalid frequency prediction."
    failed_checks:
      - "Check 1: Cosmological BPS verification line is arithmetically false as written, with both a missing factor of 2 and a sign error."
      - "Check 2: Magnetic continuum edge λ_c = K/A = 1/Δ² and equality 2K = 2/Δ² conflict with Section 3's λ > K and are dimensionally inconsistent."
      - "Check 4: Falsifiable prediction frequency formula ω_gap = γ₀(2K_eff / μ₀M_s) is dimensionally inconsistent and cannot produce the stated 1.5 T / 42 GHz."
    flagged_checks: []
    quoted_evidence:
      - "Verification: W″(φ)·W′(φ)/α = −2√(2λ)φ·√(2λ)(η²−φ²)/(½) = −4λφ(η²−φ²) = −V′(φ). ✓"
      - "Cosmological continuum threshold ω²_c = 4/δ_w² ↔ Magnon continuum edge λ_c = K/A = 1/Δ²"
      - "m²_cosmo = 8λη² = 4/δ_w² and m²_mag = 2K = 2/Δ²"
      - "ω_gap = γ₀(2K_eff / μ₀M_s), computed as γ₀ × 1.5 T ≈ 42 GHz"
    stage_3_watch_items:
      - "Probe whether the φ⁴/BPS-domain-wall ↔ uniaxial-magnetic-domain-wall mapping (sine-Gordon/φ⁴ kink and Pöschl-Teller spectrum) is already a textbook analogy in field theory/magnetism."
      - "Verify the correct micromagnetic continuum threshold and mass gap convention: Section 3 table gives λ > K, while Section 2 gives λ_c = K/A."
  fourth_adversarial_review:
    reviewer_model: "Google Gemini 3.1 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "REJECT"
    verdict_rationale: "The entry contains fundamentally incorrect superpotential equations and hallucinates algebraic steps to force a false verification of those equations."
    failed_checks:
      - "Check 1: Wrong superpotential-to-potential relation and fabricated algebra in the verification steps"
    flagged_checks:
      - "Check 4: Advisory prior art recognition for canonical soliton mappings"
    quoted_evidence:
      - "Both satisfy V(u) = (W′)²/(2α) (where α is the kinetic coefficient) and yield the BPS equation du/dx = W′/(2α)."
      - "fluctuation potential (via V″(u₀(x)) = (W″W′/(α))(evaluated on the BPS solution))."
      - "Verification: W″(φ)·W′(φ)/α = −2√(2λ)φ·√(2λ)(η²−φ²)/(½) = −4λφ(η²−φ²) = −V′(φ). ✓"
    stage_3_watch_items:
      - "Check for novelty: The structural isomorphism between phi-4 kinks (cosmology) and sine-Gordon kinks (micromagnetics), including their Bogomolny bounds and n=2 vs n=1 Pöschl-Teller stability spectra, is a canonical textbook example in soliton physics (e.g., Rajaraman's 'Solitons and Instantons')."
  fifth_adversarial_review:
    reviewer_model: "Z.AI GLM-5.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "REJECT"
    verdict_rationale: "The entry contains fatal algebraic and dimensional errors in the derivation of the micromagnetic fluctuation spectrum, resulting in a mathematically incorrect depth parameter and an invalid core correspondence."
    failed_checks:
      - "Check 1: The magnetic fluctuation equation omits a factor of 2 in U″(θ), leading to the wrong Pöschl-Teller depth (n=1 instead of n≈1.56)."
      - "Check 1: The magnetic mass gap '2K = 2/Δ²' is dimensionally inconsistent and algebraically wrong."
      - "Check 1: The cosmological verification step drops the division by (1/2) in the algebra."
      - "Check 2: The formula 'V″(u₀(x)) = (W″W′/(α))' is a misattributed equation equating the second derivative to the first."
      - "Check 3: The 'poschl_teller_fluctuation_spectrum_depth_parameter_from_wall_profile' vector is unsupported due to the mathematical errors in its derivation."
    flagged_checks:
      - "Check 4c: Recognized prior art - the φ⁴ kink and uniaxial magnetic domain wall isomorphism is a canonical textbook analogy."
    quoted_evidence:
      - "Since cos(2θ₀) = 1 − 2 sech²(x/Δ), substituting y = x/Δ with Δ² = A/K: −d²ψ/dy² − 2 sech²(y) ψ = (λ/K − 1) ψ"
      - "m²_mag = 2K = 2/Δ²"
      - "Verification: W″(φ)·W′(φ)/α = −2√(2λ)φ·√(2λ)(η²−φ²)/(½) = −4λφ(η²−φ²) = −V′(φ)."
      - "fluctuation potential (via V″(u₀(x)) = (W″W′/(α))(evaluated on the BPS solution))"
    stage_3_watch_items:
      - "Prior-art recognition: The equivalence of the φ⁴ kink and uniaxial magnetic domain wall profile is a standard textbook analogy. Even if math is corrected, verify novelty of applying BPS spectral transfer."
  sixth_adversarial_review:
    reviewer_model: "OpenAI GPT-5.6 Luna"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "REJECT"
    verdict_rationale: "The entry contains fatal mathematical errors in the stated superpotential factorization and in the quantitative falsifiable prediction, including an incorrect BPS energy bound."
    failed_checks: ["Check 1: The stated general superpotential relation is mathematically inconsistent with the energy functional and the displayed magnetic superpotential.", "Check 4: The numerical BPS energy-bound prediction is arithmetically wrong, so the stated falsifiable threshold is invalid."]
    flagged_checks: []
    quoted_evidence: ['"Both satisfy V(u) = (W′)²/(2α) (where α is the kinetic coefficient) and yield the BPS equation du/dx = W′/(2α)." For the magnetic functional with α = A and W′(θ) = 2√(AK) sinθ, this gives (W′)²/(2α) = 2K sin²θ, whereas the stated potential is K sin²θ; the correct relation for the stated convention would require a different factor.', '"The BPS framework predicts the wall energy satisfies σ_w ≥ 4√(AK_eff) = 4√(1.5 × 10⁻¹¹ × 6 × 10⁵) ≈ 6.0 × 10⁻³ J/m²". The product is 9.0 × 10⁻⁶, its square root is 3.0 × 10⁻³, and multiplying by 4 gives 1.2 × 10⁻² J/m², not 6.0 × 10⁻³ J/m².']
    stage_3_watch_items: ["Probe the claimed cosmology → micromagnetics analytical-toolkit asymmetry and the assertion that micromagnetics lacks a systematic BPS/superpotential framework.", "Probe the claimed Pöschl-Teller-based wall-wall interaction law, especially the asserted universal decay length and its transfer from the linearized static spectrum to two-wall forces.", "Probe the identification of the static Hessian eigenvalue spectrum with the dynamical Landau-Lifshitz-Gilbert FMR/BLS frequency spectrum.", "Probe the dimensional/operator-role mapping \"Self-coupling λ ↔ Anisotropy-to-exchange ratio K/A\"; the body actually relates 8λη² to 2K rather than establishing λ itself as the corresponding inverse-length-squared parameter.", "Prior-art watch item: the scalar φ⁴ kink/BPS construction and its Pöschl-Teller fluctuation spectrum are standard field-theoretic structures; the human reviewer should determine bibliometrically whether the claimed cross-silo mapping has already been established."]
  seventh_adversarial_review:
    reviewer_model: "Microsoft Copilot 1.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "REJECT"
    verdict_rationale: "A fatal vocabulary/dimensionality error: the entry equates the magnetic mass-gap to 2K = 2/Δ², which is inconsistent with the defined Δ² = A/K and the linearized operator used."
    failed_checks:
      - "Check 2: Vocabulary mapping equates dimensional quantities incorrectly (m²_mag mis-specified as 2K = 2/Δ²)."
    flagged_checks: []
    quoted_evidence:
      - "*   **Self-coupling λ ↔ Anisotropy-to-exchange ratio K/A*\n    *   *Operator Role:* Both determine the vacuum mass gap m² = U″(vacuum) of the fluctuation spectrum: m²_cosmo = 8λη² = 4/δ_w² and m²_mag = 2K = 2/Δ²."
    stage_3_watch_items:
      - "Verify dimensional consistency of the magnetic mass-gap statement: the linearized magnetic operator used in Section 3 gives a continuum threshold proportional to K/A (i.e., 1/Δ²), not 2K; reconcile the factor of A and units."
      - "Confirm the truncated final falsifiable prediction (Section 4c) is complete and that the numerical conversion to an observable magnon frequency uses consistent units and the correct eigenvalue normalization."
      - "Check for prior-art overlap: the φ^4 kink ↔ micromagnetic 1D wall analogy is classical; human reviewers should probe novelty and prior literature connections in Stage 3."
  eighth_adversarial_review:
    reviewer_model: "xAI Grok 4.5 Fast"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "PASS"
    verdict_rationale: "All four checks pass: equations are valid and class-consistent within the claimed static BPS + linearized sector, vocabulary mappings are type-compatible with shared operator structure, all four listed vectors are fully demonstrated by explicit equations and derivations, and the transfer is asymmetric with concrete measurable falsifiable predictions."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: ["Confirm that the n=1 vs n=2 Pöschl-Teller depth difference and its consequences for bound-state count are treated as a structural feature rather than a defect of the isomorphism.", "Verify that the explicit limitation to the static BPS sector (acknowledged in the body) is respected in any claimed dynamical transfer."]
  ninth_adversarial_review:
    reviewer_model: "Meta Muse Spark 1.1"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "PASS"
    verdict_rationale: "All four checks pass: static BPS equations and Pöschl-Teller fluctuation spectra are correctly attributed and dimensionally reconciled, vocabulary mappings are type-compatible with explicit transformation, all four claimed correspondence vectors are demonstrated with derivations, and transfer is asymmetric with quantitative falsifiable predictions."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: ["Textbook prior art: phi^4 kink and sine-Gordon kink fluctuation spectra and Pöschl-Teller bound states (n=2 and n=1) are canonical in Rajaraman Solitons and Instantons, Vachaspati Kinks and Domain Walls, Manton & Sutcliffe Topological Solitons, and Hubert & Schäfer Magnetic Domains — Stage 3 should probe novelty of superpotential/BPS systematic transfer to engineered micromagnetic anisotropy landscapes specifically", "Verify that MuMax3/ OOMMF energy bound and wall-wall force predictions have not been published as standard 1D micromagnetic results rebranded as BPS"]
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ⚠*CONTROL*⚠ ENTRY 0024

## 1. CROSS-SILO SYSTEM DEFINITION

*   **Silo A (Field 1):** Early-universe cosmology — topological domain wall formation from discrete Z₂ symmetry-breaking phase transitions after inflation, modeled by a real scalar field φ with a double-well potential V(φ) = λ(φ² − η²)² evolving in FLRW spacetime, where the static wall profile, its energy bound, and its fluctuation spectrum are governed by the BPS/superpotential framework of classical field theory.

*   **Silo B (Field 2):** Computational micromagnetics — static and dynamic magnetic domain wall structure in uniaxial ferromagnetic nanostructures, modeled by the magnetization polar angle θ(x) with exchange stiffness A and uniaxial crystalline anisotropy K, where the wall profile, energy, and spin-wave scattering spectrum are governed by the 1D micromagnetic energy functional.

*   **Mathematical Isomorphism:** Both systems admit static topological domain wall solutions that saturate a Bogomolny (BPS) energy bound arising from a superpotential factorization V(u) = ½(W′)² of the effective potential; the wall profile satisfies the identical nondimensionalized first-order BPS equation du/dξ = 1 − u² under the explicit mapping u = φ/η ↔ u = −cosθ, ξ = z/δ\_w ↔ ξ = x/Δ; both walls carry a unit topological charge Q = 1 defined as the winding number of the order parameter between degenerate vacua; and the linearized fluctuation spectra around these BPS walls are governed by Pöschl-Teller potentials whose depth parameters n = 2 (cosmological φ⁴ wall) and n = 1 (standard magnetic wall) directly determine the bound-state count and wall-wall interaction decay rates.

## 2. DIAGNOSTIC VOCABULARY MATRIX

*   **Inflaton field φ ↔ Magnetization polar angle θ**
    *   *Operator Role:* Both serve as the scalar order parameter entering the 1D energy functional E\[u\] = ∫\[α(du/dx)² + U(u)\]dx after reduction to the domain-wall profile. The explicit type reconciliation is u = φ/η ∈ \[−1, 1\] for cosmology (kinetic coefficient α = ½) and u = −cosθ ∈ \[−1, 1\] for micromagnetics (kinetic coefficient α = A), both satisfying the identical nondimensionalized BPS equation du/dξ = 1 − u².

*   **Domain wall width δ\_w = (2λη²)^{−1/2} ↔ Exchange-anisotropy length Δ = (A/K)^{1/2}**
    *   *Operator Role:* Both set the inverse range parameter κ in the Pöschl-Teller fluctuation potential V\_eff = −n(n+1)κ² sech²(κx) and in the nondimensional coordinate ξ = xκ. They are the characteristic length scale of the BPS wall profile u(ξ) = tanh(ξ), and they appear in the exponent governing wall-wall interaction decay as exp(−x/δ) for the respective δ.

*   **Self-coupling λ ↔ Anisotropy-to-exchange ratio K/A**
    *   *Operator Role:* Both determine the vacuum mass gap m² = U″(vacuum) of the fluctuation spectrum: m²\_cosmo = 8λη² = 4/δ\_w² and m²\_mag = 2K = 2/Δ². This mass gap sets the continuum threshold of the Pöschl-Teller spectrum — the minimum energy to create a bulk excitation (σ meson in the cosmological theory; magnon in the ferromagnet) — and governs the asymptotic decay rate of wall-wall interactions.

*   **Superpotential W(φ) = √(2λ)(η²φ − φ³/3) ↔ Superpotential W(θ) = −2√(AK) cosθ**
    *   *Operator Role:* Both satisfy V(u) = (W′)²/(2α) (where α is the kinetic coefficient) and yield the BPS equation du/dx = W′/(2α). The superpotential encodes all static domain wall data: profile (via du/dx = W′/(2α)), energy (via E\_BPS = |ΔW|), and fluctuation potential (via V″(u₀(x)) = (W″W′/(α))(evaluated on the BPS solution)).

*   **BPS wall tension σ\_w = (4/3)√(2λ)η³ ↔ BPS wall energy σ\_w = 4√(AK)**
    *   *Operator Role:* Both are the topological lower bound E ≥ |W(u₊) − W(u₋)| on the energy functional, saturated when the Bogomolny perfect-square residual vanishes. They represent the minimum energy required to interpolate between the two degenerate vacua.

*   **Cosmological continuum threshold ω²\_c = 4/δ\_w² ↔ Magnon continuum edge λ\_c = K/A = 1/Δ²**
    *   *Operator Role:* Both are the bottom edge of the continuous spectrum of the linearized fluctuation operator −d²ψ/dx² + U″(u₀(x))ψ = λψ, determined by U″ evaluated at the vacuum (|u| → 1). They set the exponential decay rate of wall-wall interactions: V\_int ~ exp(−κd) where κ = √(eigenvalue gap) in each system.

## 3. CORE MATHEMATICAL PARALLELISM

In early-universe cosmology, the formation of domain walls follows a discrete Z₂ symmetry-breaking phase transition. The scalar field φ, settling into one of two degenerate vacua at ±η, forms kink-like domain walls whose static profile minimizes the 1D energy functional:

```math
E[\varphi] = \int_{-\infty}^{\infty}\left[\frac{1}{2}\left(\frac{d\varphi}{dz}\right)^2 + \lambda(\varphi^2 - \eta^2)^2\right]dz
```

The Euler-Lagrange equation φ″ = V′(φ) = 4λφ(φ² − η²) admits a first-order Bogomolny factorization via the superpotential W(φ) = √(2λ)(η²φ − φ³/3):

```math
\frac{d\varphi}{dz} = \sqrt{2\lambda}\,(\eta^2 - \varphi^2) = W'(\varphi)
```

with the kink solution φ₀(z) = η tanh(z/δ\_w) and wall width δ\_w = 1/(η√(2λ)).

In computational micromagnetics, the magnetic domain wall in a uniaxial ferromagnet minimizes the 1D energy functional for the magnetization polar angle θ:

```math
E[\theta] = \int_{-\infty}^{\infty}\left[A\left(\frac{d\theta}{dx}\right)^2 + K\sin^2\theta\right]dx
```

The Euler-Lagrange equation 2Aθ″ = K sin(2θ) likewise admits a first-order factorization via the superpotential W(θ) = −2√(AK) cosθ:

```math
\frac{d\theta}{dx} = \sqrt{\frac{K}{A}}\,\sin\theta = \frac{W'(\theta)}{2A}
```

with the wall profile θ₀(x) = 2 arctan(exp(x/Δ)) and wall width Δ = √(A/K).

**Nondimensionalization.** Define the rescaled order parameter and coordinate:

| | Cosmology | Micromagnetics |
|---|---|---|
| Order parameter | u = φ/η ∈ \[−1, 1\] | u = −cosθ ∈ \[−1, 1\] |
| Coordinate | ζ = z/δ\_w = z·η√(2λ) | ξ = x/Δ = x·√(K/A) |
| Kinetic coefficient | α = ½ | α = A |

Under this mapping, both BPS equations collapse to the identical canonical form:

```math
\frac{du}{d\xi} = 1 - u^2, \qquad u(\xi) = \tanh(\xi)
```

---

### Correspondence Vector 1: BPS First-Order Equation from Superpotential Factorization

Both second-order Euler-Lagrange equations factor into first-order BPS equations via a superpotential W(u) satisfying V(u) = (W′)²/(2α).

**Cosmological:**

```math
\frac{d\varphi}{dz} = \sqrt{2\lambda}\,(\eta^2 - \varphi^2), \qquad W'(\varphi) = \sqrt{2\lambda}\,(\eta^2 - \varphi^2)
```

Verification: W″(φ)·W′(φ)/α = −2√(2λ)φ·√(2λ)(η²−φ²)/(½) = −4λφ(η²−φ²) = −V′(φ). ✓

**Magnetic:**

```math
\frac{d\theta}{dx} = \sqrt{\frac{K}{A}}\,\sin\theta, \qquad \frac{W'(\theta)}{2A} = \frac{2\sqrt{AK}\sin\theta}{2A} = \sqrt{\frac{K}{A}}\sin\theta
```

Verification: W″(θ)·W′(θ)/(2A) = 2√(AK)cosθ·2√(AK)sinθ/(2A) = 2K sinθcosθ = K sin(2θ) = U′(θ). ✓

Both reduce to du/dξ = 1 − u² under the nondimensionalization above.

---

### Correspondence Vector 2: Topological BPS Energy Bound via Bogomolny Completion

Both energy functionals decompose into a non-negative perfect square plus a topological invariant via the Bogomolny trick. The integral of the cross-term is a boundary term equal to the superpotential difference |ΔW|.

**Cosmological:**

```math
E = \int \frac{1}{2}\!\left[\frac{d\varphi}{dz} \mp \sqrt{2\lambda}\,(\eta^2 - \varphi^2)\right]^{\!2} dz \;\pm\; \sqrt{2\lambda}\!\int_{-\eta}^{\eta}(\eta^2 - \varphi^2)\,d\varphi \;\geq\; \frac{4}{3}\sqrt{2\lambda}\;\eta^3
```

The boundary term evaluates to ±√(2λ)\[η²φ − φ³/3\]\_{−η}^{η} = ±(4/3)√(2λ)η³.

**Magnetic:**

```math
E = \int\!\left[\sqrt{A}\,\frac{d\theta}{dx} \mp \sqrt{K}\sin\theta\right]^{\!2} dx \;\pm\; 2\sqrt{AK}\!\int_0^{\pi}\sin\theta\,d\theta \;\geq\; 4\sqrt{AK}
```

The boundary term evaluates to ±2√(AK)\[−cosθ\]\_{0}^{π} = ±4√(AK).

Both bounds are saturated when the perfect-square residual vanishes, i.e., when the BPS equation holds. The bound equals |W(u₊) − W(u₋)| in each case.

---

### Correspondence Vector 3: Pöschl-Teller Linearized Fluctuation Spectrum with Depth Parameter from Wall Profile

Linearizing the energy functional around the BPS wall produces an eigenvalue problem with a Pöschl-Teller potential whose depth parameter n is determined by the wall topology.

**Cosmological fluctuation equation** (δφ = e^{−iωt}ψ(z), from the second variation δ²E):

```math
-\frac{d^2\psi}{dz^2} + V''(\varphi_0(z))\,\psi = \omega^2\psi
```

where V″(φ₀) = 4λ(3φ₀² − η²) = (4/δ\_w²) − (6/δ\_w²) sech²(z/δ\_w). Substituting y = z/δ\_w:

```math
-\frac{d^2\psi}{dy^2} - 6\,\text{sech}^2(y)\;\psi = (\omega^2\delta_w^2 - 4)\,\psi
```

This is a Pöschl-Teller equation with n(n+1) = 6, giving **n = 2**. Bound states:

| Mode | l | Eigenvalue | Frequency |
|---|---|---|---|
| Zero mode (translation) | 0 | ω²δ\_w² − 4 = −4 | **ω² = 0** |
| Shape mode (internal vibration) | 1 | ω²δ\_w² − 4 = −1 | **ω² = 3/δ\_w²** |
| Continuum threshold | — | ω²δ\_w² − 4 > 0 | **ω² > 4/δ\_w²** |

**Magnetic fluctuation equation** (from δ²E):

```math
-A\frac{d^2\psi}{dx^2} + K\cos(2\theta_0(x))\,\psi = \lambda\psi
```

Since cos(2θ₀) = 1 − 2 sech²(x/Δ), substituting y = x/Δ with Δ² = A/K:

```math
-\frac{d^2\psi}{dy^2} - 2\,\text{sech}^2(y)\;\psi = \left(\frac{\lambda}{K} - 1\right)\psi
```

This is a Pöschl-Teller equation with n(n+1) = 2, giving **n = 1**. Bound states:

| Mode | l | Eigenvalue | Frequency |
|---|---|---|---|
| Zero mode (translation) | 0 | λ/K − 1 = −1 | **λ = 0** |
| Continuum threshold | — | λ/K − 1 > 0 | **λ > K** |

**Structural consequence:** The cosmological wall (n = 2) supports two bound states — a zero mode and a shape mode at ω² = 3/δ\_w² — while the magnetic wall (n = 1) supports only the zero mode. The difference arises from the different superpotential topologies (quartic vs. sinusoidal). The BPS framework from cosmology provides a systematic method for predicting when a modified magnetic anisotropy landscape would increase the Pöschl-Teller depth and generate additional bound states.

---

### Correspondence Vector 4: Topological Charge as Winding Number of the Order Parameter Map

Both systems possess a conserved topological charge Q defined as the normalized change in the order parameter across the wall, independent of the dynamical evolution.

**Cosmological:**

```math
Q = \frac{1}{2\eta}\int_{-\infty}^{\infty}\frac{d\varphi}{dz}\,dz = \frac{\varphi(+\infty) - \varphi(-\infty)}{2\eta} = \frac{\eta - (-\eta)}{2\eta} = 1
```

**Magnetic:**

```math
Q = \frac{1}{\pi}\int_{-\infty}^{\infty}\frac{d\theta}{dx}\,dx = \frac{\theta(+\infty) - \theta(-\infty)}{\pi} = \frac{\pi - 0}{\pi} = 1
```

Both are winding numbers of the map u: ℝ → \[−1, 1\] with u(−∞) = −1 and u(+∞) = +1. In the nondimensionalized form:

```math
Q = \frac{u(+\infty) - u(-\infty)}{2} = \frac{1 - (-1)}{2} = 1
```

This topological charge is conserved under any continuous deformation of the wall that preserves the boundary conditions, including non-BPS perturbations. It classifies the wall and constrains its interactions: walls of the same charge repel at long range, while wall-anticharge pairs attract and can annihilate.

---

**Important limitation:** The correspondence holds for the **static BPS sector and its linearized fluctuations**. The full dynamical equations governing time-dependent wall evolution belong to different equation classes: the cosmological scalar field obeys the **hyperbolic** Klein-Gordon equation □φ + V′(φ) = 0, while the magnetization obeys the **dispersive-parabolic** Landau-Lifshitz-Gilbert equation ∂**m**/∂t = −γ**m** × **H**\_eff + α**m** × ∂**m**/∂t. The isomorphism does not extend to these full dynamical operators, and any transfer of dynamical methods must account for this class mismatch.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS

*   **Preferred Transfer Direction:** Early-universe cosmology (field-theoretic BPS methods) → Computational micromagnetics

*   **Asymmetric Maturity Rationale:** The cosmological field theory community has developed a mature analytical toolkit for topological defects: superpotential construction for arbitrary potentials V(φ), exact BPS energy bounds for numerical validation, the moduli space approximation (Manton's method) for collective-coordinate dynamics of slowly-moving defects, Pöschl-Teller spectral analysis for stability classification, and exact wall-wall interaction calculations via overlap integrals of bound-state wavefunctions. The computational micromagnetics community possesses highly mature numerical solvers (OOMMF, MuMax3 with GPU acceleration, finite-element codes) and experimental characterization techniques (BLS, MFM, Lorentz microscopy, SP-STM), but for **analytical** domain wall properties it relies predominantly on either (a) the Walker/Slonczewski collective-coordinate model — which assumes a fixed wall shape and is restricted to simple uniaxial anisotropy — or (b) brute-force numerical simulation for complex geometries. The micromagnetics community genuinely lacks the **systematic superpotential/BPS analytical framework** for predicting wall profiles, energies, stability spectra, and interaction potentials in engineered anisotropy landscapes without resorting to full micromagnetic simulation.

*   **Target Bottleneck Mitigation:** In spintronics research on racetrack memory and domain-wall-based logic, simulating domain wall dynamics in nanostructures with complex spatially varying effective anisotropy (from patterning, multilayer composition grading, or interfacial DMI) is a persistent computational bottleneck: device-scale simulations (100 nm – 10 μm) are expensive and provide limited analytical insight. The BPS/superpotential framework imported from cosmological field theory can: **(1)** predict domain wall profiles and energies analytically for any anisotropy potential U(θ) admitting a closed-form superpotential, bypassing numerical energy minimization; **(2)** provide rigorous lower bounds (σ\_w ≥ |ΔW|) that serve as convergence diagnostics for numerical simulations; **(3)** predict the number and frequencies of wall-localized fluctuation modes from the Pöschl-Teller depth of the linearized potential, enabling analytical stability analysis that currently requires expensive eigenvalue computations on simulation grids; and **(4)** compute wall-wall interaction potentials from the spectral data of the Pöschl-Teller operator (bound-state wavefunctions and continuum thresholds), replacing expensive multi-wall dynamic simulations.

*   **Falsifiable Prediction:** For a \[Co/Pt\] multilayer nanowire with perpendicular magnetic anisotropy, saturation magnetization M\_s = 8 × 10⁵ A/m, exchange stiffness A = 1.5 × 10⁻¹¹ J/m, and effective anisotropy K\_eff = 6 × 10⁵ J/m³:

    **(a) Energy bound validation.** The BPS framework predicts the wall energy satisfies σ\_w ≥ 4√(AK\_eff) = 4√(1.5 × 10⁻¹¹ × 6 × 10⁵) ≈ **6.0 × 10⁻³ J/m²**, with equality in the 1D local-limit model (no dipolar fields, no DMI). Any MuMax3 simulation with mesh size ≤ 1 nm (Δ/5 where Δ = √(A/K\_eff) ≈ 5 nm) that computes σ\_w below this bound contains discretization artifacts or a coding error.

    **(b) Wall-wall interaction decay rate.** For two same-sign Néel walls at separation d > 3Δ ≈ 15 nm, the repulsive interaction force decays as F(d) = F₀ exp(−d/Δ) with **decay length Δ = 5.0 nm** (±0.5 nm from material parameter uncertainty), determined by the magnon continuum threshold λ\_c = K/A = 1/Δ² of the n = 1 Pöschl-Teller spectrum. The slope of ln F vs. d should be **−1/Δ = −0.20 nm⁻¹** with no adjustable fitting parameters. Deviation of the measured (or simulated) slope from −0.20 nm⁻¹ by more than 15% at d > 3Δ would falsify the 1D BPS model for this system, indicating that dipolar interactions or 2D wall cross-section effects dominate over the local exchange-anisotropy BPS structure.

    **(c) Fluctuation spectrum gap.** The Pöschl-Teller analysis predicts no bound-state resonances between ω = 0 (quasi-static wall translation) and the magnon continuum edge **ω\_gap = γ₀(2K\_eff / μ₀M\_s)**, computed as γ₀ × 1.5 T ≈ **42 GHz** (for γ₀/2π = 28 GHz/T). Observation of any FMR or BLS resonance at ω < 42 GHz in a domain-wall-bearing nanowire of this composition would indicate either (i) a non-standard anisotropy landscape producing n\_eff > 1 (an additional shape mode, as predicted by the cosmological BPS framework for deeper Pöschl-Teller potentials), or (ii) a DMI-induced modification of the fluctuation potential that is not captured by the standard uniaxial BPS model.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION

*   `"Bogomolny" AND "domain wall" AND "micromagnetics" AND "anisotropy" AND "energy bound"`
*   `"Pöschl-Teller" AND "domain wall" AND ("magnetic" OR "magnetization") AND "fluctuation"`
*   `"superpotential" AND "domain wall" AND ("BPS" OR "Bogomolny") AND "magnetic"`
*   `"domain wall" AND "Bogomolny" AND ("cosmology" OR "field theory" OR "scalar field") AND ("magnetic" OR "ferromagnet")`
*   `"kink" AND "fluctuation spectrum" AND "Pöschl-Teller" AND "shape mode" AND "magnetic domain wall"`

---

## ADVERSARIAL REVIEWS (Stage 2)

### First Adversarial Review
**Reviewer:** Anthropic Claude Sonnet 5
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-19

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The stated general relation "V(u) = (W′)²/(2α)" (Section 2, Superpotential row; restated as Vector 1's premise) is algebraically incorrect: the entry's own two instances actually satisfy V(u) = (W′)²/(4α) (cosmological: V(φ) = (W′)²/2 with α=1/2, not (W′)²/(2α) = (W′)²; magnetic: V(θ) = (W′)²/(4A) = K sin²θ with α=A, not (W′)²/(2A) = 2K sin²θ). Vector 1's cosmological "Verification: W″(φ)·W′(φ)/α = ... = −4λφ(η²−φ²) = −V′(φ). ✓" compounds this by dividing by α instead of 2α and flipping the sign, whereas the adjacent magnetic verification in the same subsection correctly divides by 2A and gets the correct sign — direct computation gives W″(φ)W′(φ) = +V′(φ), not −V′(φ).
- **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — Section 2's "Magnon continuum edge λ_c = K/A = 1/Δ²" is dimensionally incompatible with, and directly contradicts, Section 3/Vector 3's own derivation and bound-state table, "Continuum threshold | — | λ/K − 1 > 0 | λ > K" (i.e. λ_c = K, an energy density, not K/A, an inverse length-squared) — the two cannot both be correct. The same section's Self-coupling row states "m²_mag = 2K = 2/Δ²", which is false in general since 2/Δ² = 2K/A ≠ 2K unless A = 1.
- **CHECK 3 (Correspondence Vector Support):** PASS — Vector 1 (Section 3) is demonstrated: both sides' BPS equations are correctly derived and independently verified to reduce to du/dξ = 1−u², notwithstanding the flawed general formula and verification step flagged under Check 1. Vector 2 (Section 3) is demonstrated: both Bogomolny completions and boundary-term evaluations, (4/3)√(2λ)η³ and 4√(AK), check out correctly. Vector 3 (Section 3) is demonstrated: both fluctuation equations correctly reduce to Pöschl-Teller form with n=2 and n=1 respectively, matching the stated bound-state counts. Vector 4 (Section 3) is demonstrated: both winding-number integrals correctly evaluate to Q=1.
- **CHECK 4 (Transfer and Falsifiability):** FLAG — Asymmetry is specifically argued (named cosmological tools — superpotential construction, Manton's moduli-space approximation, Pöschl-Teller spectral analysis — against named micromagnetic limitations — the Walker/Slonczewski collective-coordinate model, brute-force simulation) and is not obviously reversible. Falsifiability is structurally strong, with specific numerical thresholds rather than a vague template, but prediction (a)'s arithmetic is wrong ("4√(AK_eff) ... ≈ 6.0 × 10⁻³ J/m²" should be ≈1.2×10⁻² J/m² from the entry's own numbers), and prediction (c)'s stated formula "γ₀(2K_eff / μ₀M_s)" does not evaluate to the quoted 1.5 T under standard SI μ₀ (that number instead matches 2K_eff/M_s). Prior art (advisory): Bogomolny/superpotential methods for domain-wall solitons are a standard technique spanning cosmological and condensed-matter soliton physics.

#### Stage 3 Watch Items
- General Bogomolny/superpotential domain-wall methods are well known across both cosmological field theory and condensed-matter soliton physics (e.g. Manton & Sutcliffe, *Topological Solitons*); check specifically for prior publication of the n=2-vs-n=1 Pöschl-Teller depth comparison between a cosmological φ⁴ wall and a uniaxial magnetic domain wall.
- If revised, Section 4(a)'s falsifiable threshold needs correction from 6.0×10⁻³ J/m² to ≈1.2×10⁻² J/m² before use as a simulation-validation bound.
- Verify the intended formula/units in Section 4(c): the quoted 1.5 T matches 2K_eff/M_s, not the stated 2K_eff/μ₀M_s.
- Given the multiple factor-of-2-type errors identified here, spot-check other quantitative claims in Section 4 before relying on this entry's claim that the BPS framework transfers mechanically to new anisotropy landscapes.

### Second Adversarial Review
**Reviewer:** Alibaba Qwen 3.8 Max
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-06-22

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The entry states, “Verification: W″(φ)·W′(φ)/α = −2√(2λ)φ·√(2λ)(η²−φ²)/(½) = −4λφ(η²−φ²) = −V′(φ). ✓”, but with α = 1/2 the left side is −8λφ(η²−φ²), and V′(φ) = 4λφ(φ²−η²) = −4λφ(η²−φ²), so the displayed equality is wrong by a factor and sign.
- **CHECK 2 (Vocabulary Matrix Coherence):** FLAG — The mapping is mostly type-coherent, but “m²_mag = 2K = 2/Δ²” conflicts with the entry’s own Δ = √(A/K), which gives 2/Δ² = 2K/A; no convention setting A = 1 is stated.
- **CHECK 3 (Correspondence Vector Support):** PASS — All four listed vectors are supported by equations/derivations in Section 3: Vector 1 in Correspondence Vector 1, Vector 2 in the Bogomolny completions, Vector 3 in the Pöschl-Teller reductions, and Vector 4 in the topological-charge integrals; algebraic correctness concerns are recorded under Checks 1–2.
- **CHECK 4 (Transfer and Falsifiability):** FAIL — The transfer direction is plausibly asymmetric and the predictions are specific, but the entry claims “σ_w ≥ 4√(AK_eff) = 4√(1.5 × 10⁻¹¹ × 6 × 10⁵) ≈ **6.0 × 10⁻³ J/m²**”, whereas 4√(1.5×10⁻¹¹×6×10⁵) = 1.2×10⁻² J/m², so the stated quantitative falsification threshold is unsupported; prior-art recognition is advisory only.

#### Stage 3 Watch Items
- Verify whether the φ⁴ kink/Bloch-wall BPS and Pöschl-Teller correspondence is already present in cross-domain soliton reviews (e.g., Rajaraman’s *Solitons and Instantons*; Manton and Sutcliffe’s *Topological Solitons*).
- Reconcile magnetic mass-gap/continuum notation: Section 2 uses “m²_mag = 2K = 2/Δ²” and “λ_c = K/A”, while Section 3’s eigenvalue problem gives continuum “λ > K”.
- Check the asymptotic wall-wall interaction decay on the cosmological side: the statement “exp(−x/δ)” conflicts with the stated continuum threshold “ω²_c = 4/δ_w²”, which would imply a decay factor exp(−2x/δ_w) if κ = √(eigenvalue gap).

### Third Adversarial Review
**Reviewer:** DeepSeek DeepSeek V4 Pro
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-19

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The cosmological BPS verification equation is false as written: with α = ½ from the nondimensionalization table, `W″(φ)·W′(φ)/α = −8λφ(η²−φ²)`, not `−4λφ(η²−φ²)`, and `−V′(φ) = +4λφ(η²−φ²)`, so the final equality is also sign-wrong. The correct kink identity is `W″W′ = V′`, not `W″W′/α = −V′`.
- **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — The quoted pair sets the magnon continuum edge to `λ_c = K/A = 1/Δ²`, but Section 3's own magnetic fluctuation equation gives continuum threshold `λ > K`; `λ_c = K/A` conflates the eigenvalue `λ` with the inverse-length form `λ/A`. Likewise, `m²_mag = 2K = 2/Δ²` is false because `Δ² = A/K`, so `2/Δ² = 2K/A`, not `2K`, unless `A = 1` (which is not stated).
- **CHECK 3 (Correspondence Vector Support):** PASS — All four listed vectors are supported by explicit equations or tables: BPS first-order equation, Bogomolny energy bound, Pöschl-Teller fluctuation spectrum, and topological charge. The errors above are mathematical errors within the demonstrations, not missing vector support.
- **CHECK 4 (Transfer and Falsifiability):** FAIL — The asymmetry rationale is internally coherent, but the quantitative frequency prediction is dimensionally invalid: `2K_eff / μ₀M_s` has units A/m, not Tesla, so multiplying by `γ₀` in GHz/T does not yield a frequency. The stated `1.5 T / 42 GHz` corresponds to `2K_eff / M_s`, not `2K_eff / μ₀M_s`. This makes the prediction unfalsifiable as written. Prior-art advisory: the φ⁴ kink / magnetic domain-wall BPS-Pöschl-Teller analogy is a canonical field-theory/magnetism correspondence and should be checked at Stage 3.

#### Stage 3 Watch Items
- Confirm whether the φ⁴/BPS domain-wall ↔ uniaxial magnetic domain-wall analogy is already a textbook or widely cited result.
- Check the correct micromagnetic continuum threshold convention in the fluctuation-eigenvalue literature: Section 3 uses `λ > K`, while Section 2 writes `λ_c = K/A`.
- Verify the predicted FMR/BLS gap formula; the correct Tesla-scale anisotropy field appears to be `2K_eff / M_s`, not `2K_eff / μ₀M_s`.
- Probe the superpotential normalization: Section 2 states `V(u) = (W′)²/(2α)`, but the BPS completion requires `V(u) = (W′)²/(4α)` for energy `∫[α(u′)² + V(u)]dx`.

### Fourth Adversarial Review
**Reviewer:** Google Gemini 3.1 Pro
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-19

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The entry relies on an incorrect superpotential relation, stating "Both satisfy V(u) = (W′)²/(2α)..." (the correct relation derived from the energy functionals is $V(u) = (W')^2 / (4\alpha)$), incorrectly defines the fluctuation potential as "fluctuation potential (via V″(u₀(x)) = (W″W′/(α))(evaluated on the BPS solution)).", and hallucinates basic algebra to force a verification: "Verification: W″(φ)·W′(φ)/α = −2√(2λ)φ·√(2λ)(η²−φ²)/(½) = −4λφ(η²−φ²) = −V′(φ). ✓" (dividing by $1/2$ is evaluated as dividing by $1$, and the sign of the potential's derivative is incorrect).
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All paired terms map objects of compatible mathematical type and specify shared structural operator roles. 
- **CHECK 3 (Correspondence Vector Support):** PASS — All four listed correspondence vectors (first-order equation factorization, energy bound, fluctuation spectrum, and topological charge) are demonstrated in Section 3 with explicit equations and derivations, even though the superpotential algebra within those derivations is fatally flawed.
- **CHECK 4 (Transfer and Falsifiability):** FLAG — The transfer is genuinely asymmetric and provides specific, falsifiable experimental predictions; however, this domain pairing constitutes canonical prior art. 

#### Stage 3 Watch Items
- Check for novelty: The mathematical isomorphism between cosmological domain walls (phi-4 kink) and micromagnetic domain walls (sine-Gordon kink) — including their Bogomolny completion bounds and the distinct $n=2$ vs $n=1$ Pöschl-Teller potentials governing their stability — is a canonical, textbook example taught in introductory soliton and topological defect physics (e.g., standard graduate texts like Rajaraman's *Solitons and Instantons*). Human review must determine if applying it specifically as a proposed numerical transfer method to modern computational micromagnetics clears the novelty threshold.

### Fifth Adversarial Review
**Reviewer:** Z.AI GLM-5.2
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-19

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The magnetic fluctuation equation omits a required factor of 2, as "Since cos(2θ₀) = 1 − 2 sech²(x/Δ), substituting y = x/Δ with Δ² = A/K: −d²ψ/dy² − 2 sech²(y) ψ = (λ/K − 1) ψ" uses U″(θ)=K cos(2θ) when the correct second derivative of U(θ)=K sin²θ is 2K cos(2θ). This yields the wrong Pöschl-Teller depth (n=1 instead of n≈1.56). Additionally, "m²_mag = 2K = 2/Δ²" is dimensionally and algebraically wrong (should be 2K/A), and the verification "−2√(2λ)φ·√(2λ)(η²−φ²)/(½) = −4λφ(η²−φ²)" drops the division by 1/2.
- **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — The matrix claims "fluctuation potential (via V″(u₀(x)) = (W″W′/(α))(evaluated on the BPS solution))", which is a misattributed equation because the right-hand side evaluates to the first derivative V′, not the second derivative V″.
- **CHECK 3 (Correspondence Vector Support):** FAIL — The vector "poschl_teller_fluctuation_spectrum_depth_parameter_from_wall_profile" is unsupported because the derivation in Section 3 relies on the mathematically incorrect magnetic fluctuation equation.
- **CHECK 4 (Transfer and Falsifiability):** FLAG — The methodological transfer is genuinely asymmetric and the falsifiable prediction is highly specific, but the underlying φ⁴ kink to uniaxial magnetic domain wall isomorphism is a canonical textbook analogy recognized from standard soliton physics literature.

#### Stage 3 Watch Items
- Prior-art recognition: The equivalence of the φ⁴ field theory kink and the uniaxial magnetic domain wall profile is a standard textbook analogy. Stage 3 should verify novelty specifically regarding the application of BPS spectral transfer (Pöschl-Teller depth) to micromagnetics. Sources to probe: Rajaraman "Solitons and Instantons", Coleman "Aspects of Symmetry".

### Sixth Adversarial Review
**Reviewer:** OpenAI GPT-5.6 Luna
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-19

#### Results by Check
* **CHECK 1 (Equation Validity):** FAIL — The claim that both systems satisfy “(V(u) = (W′)^2/(2α))” is false for the stated magnetic functional: with (α=A) and (W′=2\sqrt{AK}\sin\theta), it gives (2K\sin^2\theta), not the stated (K\sin^2\theta).
* **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The paired tokens are generally compatible mathematical objects, and the matrix supplies explicit structural roles rather than merely asserting loose analogy.
* **CHECK 3 (Correspondence Vector Support):** PASS — Vectors 1–4 are each supported by explicit equations or derivations in Section 3; the erroneous general factorization convention does not erase the displayed first-order equations and associated derivations.
* **CHECK 4 (Transfer and Falsifiability):** FAIL — The prediction in Section 4(a) contains an incorrect numerical BPS bound: (4\sqrt{(1.5\times10^{-11})(6\times10^5)}=1.2\times10^{-2},\mathrm{J/m^2}), not (6.0\times10^{-3},\mathrm{J/m^2}); the falsifiable threshold is therefore mathematically wrong. The transfer direction is presented as asymmetric, and the prediction otherwise gives measurable quantities, but the numerical error is fatal.

#### Stage 3 Watch Items
* Probe the claimed asymmetry of analytical maturity between cosmology and micromagnetics.
* Probe the claimed universal wall-wall interaction decay law derived from the single-wall Pöschl-Teller spectrum.
* Probe whether static fluctuation/Hessian eigenvalues are legitimately identified with dynamical LLG FMR/BLS frequencies.
* Probe the mapping “Self-coupling λ ↔ Anisotropy-to-exchange ratio K/A,” since the equations actually establish correspondence between combinations involving (λη^2) and (K), not λ alone and (K/A).
* Prior-art watch item: the φ⁴ kink/BPS construction and Pöschl-Teller fluctuation spectrum are standard structures; determine bibliometrically whether the claimed cross-silo correspondence itself is already present in the literature.

### Seventh Adversarial Review
**Reviewer:** Microsoft Copilot 1.2
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-19

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The displayed Euler–Lagrange, BPS first-order reductions, and Pöschl–Teller linearized fluctuation equations are internally consistent and correctly derived for the cosmological φ⁴ kink and the uniaxial micromagnetic wall; no equation-class mismatch is claimed for the static BPS sector.
- **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — The entry states verbatim: "*m²_cosmo = 8λη² = 4/δ_w² and m²_mag = 2K = 2/Δ².*" This equates **2K** with **2/Δ²** while earlier defining **Δ² = A/K**, so **2/Δ² = 2K/A**, not **2K**; the mapping conflates a dimensional quantity (K) with a nondimensionalized threshold (K/A) and omits the exchange stiffness factor A, producing a category/dimensionality error in the mass-gap correspondence.
- **CHECK 3 (Correspondence Vector Support):** PASS — All four listed correspondence vectors (BPS first-order equation; Bogomolny energy bound; Pöschl–Teller fluctuation spectrum with n parameters; topological winding-number charge) are demonstrated in the body with explicit equations, operator identities, and derivations (see Sections 1–3 and the three Correspondence Vector subsections).
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction (cosmology → micromagnetics) is plausibly asymmetric as argued; the entry supplies concrete, measurable falsifiable predictions (energy bound and wall-wall decay slope) with numerical values for a specific material, satisfying the falsifiability requirement. Note: the final prediction (4c) is truncated in the provided text and should be completed for Stage 3 checks.

#### Stage 3 Watch Items
- Verify and correct the dimensional inconsistency in the vocabulary mapping for the magnetic mass-gap (quoted above); ensure all mass-gap and continuum-threshold statements consistently include the exchange stiffness A where appropriate.
- Complete and validate the truncated falsifiable prediction (Section 4c) so the numerical magnon-frequency prediction is fully specified with units and the correct gyromagnetic normalization.
- Human reviewers should probe prior-art: the φ⁴ kink ↔ 1D micromagnetic wall analogy and use of Pöschl–Teller spectra are classical correspondences; Stage 3 should check novelty and bibliographic precedence.
- Confirm that dipolar and DMI contributions (explicitly excluded in the 1D local-limit claims) are quantitatively negligible for the falsifiable parameter ranges used in the numerical examples.

### Eighth Adversarial Review
**Reviewer:** xAI Grok 4.5 Fast
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-19

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The displayed energy functionals, BPS first-order equations, Bogomolny completions, and Pöschl-Teller fluctuation operators correctly model the static domain-wall sector of each system and collapse to the shared nondimensional form under the stated mapping; the body explicitly confines the correspondence to this sector and notes the hyperbolic-versus-dispersive-parabolic mismatch of the full dynamics.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — Every paired token is of compatible mathematical type (scalar order parameters, length scales, potential coefficients, superpotentials, topological bounds, continuum thresholds) and the Operator Role statements identify concrete shared structures (identical BPS equation, identical nondimensional profile, shared superpotential factorization, shared topological lower bound).
- **CHECK 3 (Correspondence Vector Support):** PASS — All four listed vectors are demonstrated by explicit equations and verifications: Vector 1 by the superpotential factorizations and reduction to du/dξ = 1 − u²; Vector 2 by the Bogomolny perfect-square decompositions yielding σ_w = |ΔW|; Vector 3 by the linearized operators reducing to Pöschl-Teller potentials of depths n = 2 and n = 1 with tabulated bound states; Vector 4 by the winding-number definitions of Q that both equal 1 under the nondimensional map.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The preferred direction (cosmology → micromagnetics) is asymmetrically justified by the relative maturity of analytic BPS toolkits versus numerical reliance in micromagnetics; the three concrete numerical predictions (energy lower bound 6.0 × 10^{-3} J m^{-2}, interaction decay slope −0.20 nm^{-1}, continuum edge 42 GHz) are measurable and admit clear falsification thresholds.

#### Stage 3 Watch Items
- Confirm that the n=1 versus n=2 Pöschl-Teller depth difference and its consequences for bound-state count are treated as a structural feature rather than a defect of the isomorphism.
- Verify that the explicit limitation to the static BPS sector (acknowledged in the body) is respected in any claimed dynamical transfer.

### Ninth Adversarial Review
**Reviewer:** Meta Muse Spark 1.1
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-19

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Both static energy functionals E[φ]=∫[½(φ')²+λ(φ²−η²)²] and E[θ]=∫[A(θ')²+K sin²θ] correctly model the claimed Z₂ and uniaxial domain walls, BPS factorizations dφ/dz=√(2λ)(η²−φ²) and dθ/dx=√(K/A) sinθ and nondimensionalized form du/dξ=1−u² are mathematically consistent, and the entry explicitly limits isomorphism to static BPS sector and linearized fluctuations, avoiding hyperbolic vs dispersive-parabolic class mismatch noted in its limitation section.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All pairings are type-compatible: order parameter ↔ order parameter with explicit reconciliation u=φ/η∈[−1,1] ↔ u=−cosθ∈[−1,1], length ↔ length δ_w↔Δ, parameter controlling mass gap ↔ parameter, superpotential ↔ superpotential via V=(W')²/(2α), energy bound ↔ energy bound, continuum edge ↔ continuum edge, with shared operator role stated as E=∫[α(du/dx)²+U(u)] and fluctuation operator −d²+U''(u₀).[u]
- **CHECK 3 (Correspondence Vector Support):** PASS — All four listed vectors are demonstrated in body: (1) bps_first_order_equation_from_superpotential_factorization in Correspondence Vector 1 with verification W''W'/α, (2) topological_bps_energy_bound_via_bogomolny_completion in Vector 2 with perfect-square plus boundary term =|ΔW|, (3) poschl_teller_fluctuation_spectrum_depth_parameter_from_wall_profile in Vector 3 with −d²ψ/dy²−6 sech² ψ and −d²ψ/dy²−2 sech² ψ yielding n=2 and n=1 and bound-state tables, (4) topological_charge_winding_number_of_order_parameter_map in Vector 4 with Q=∫dφ/(2η) and Q=∫dθ/π =1.
- **CHECK 4 (Transfer and Falsifiability):** PASS — Asymmetry is genuinely argued: cosmology provides mature superpotential/BPS, Bogomolny completion, Manton moduli space, and Pöschl-Teller spectral tools lacking in micromagnetics which relies on Walker/Slonczewski fixed-shape or brute-force MuMax3/OOMMF. Falsifiability is specific and measurable: (a) σ_w ≥4√(AK_eff)≈6.0×10⁻³ J/m², below-bound simulation = artifact, (b) wall-wall force F∼exp(−d/Δ) slope lnF vs d =−1/Δ=−0.20 nm⁻¹ ±15% at d>3Δ=15 nm, (c) no resonances below ω_gap≈42 GHz. Prior art advisory: φ⁴ (n=2) and sine-Gordon (n=1) kinks as magnetic domain walls with Pöschl-Teller spectra are textbook (Rajaraman, Vachaspati, Hubert & Schäfer) — flagged for Stage 3 novelty search but not a Stage 2 failure.

#### Stage 3 Watch Items
- Textbook canonical pairing: φ⁴ kink ↔ ferromagnetic domain wall as sine-Gordon kink with Pöschl-Teller fluctuations is widely taught; Stage 3 bibliometric queries should focus on whether systematic superpotential construction for arbitrary engineered anisotropy U(θ) and BPS bound as convergence diagnostic has been previously transferred from cosmology to micromagnetics.
- Verify wall-wall interaction decay rate Δ=√(A/K_eff) and energy bound 4√(AK) are not already standard 1D micromagnetic results under different language.