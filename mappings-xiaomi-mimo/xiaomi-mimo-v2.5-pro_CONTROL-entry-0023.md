---
sid_metadata:
  entry_id: "CONTROL-SID-0023"
  schema_version: "2.0-control"
  maturity_stage: "adversarial-rejected"
provenance:
  company: "Xiaomi"
  model_family: "MiMo"
  model_version: "V2.5 Pro"
  generation_timestamp: "2026-08-17"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "polycrystalline-grain-growth"
  domain_b: "stochastic-finance"
  structural_family: "simplex-constrained-selection-dynamics-with-mean-field-threshold"
  triple_correspondence_vectors:
    - "simplex_constrained_fokker_planck_density_evolution_with_conservation_closure"
    - "self_consistent_mean_field_selection_drift_with_sign_changing_threshold"
    - "rank_topology_dependent_linear_excess_growth_rate_n6_kkstar"
    - "self_similar_attractor_distribution_determined_by_selection_to_noise_ratio"
discovery_rationale:
  why_not_obvious: "The Hillert mean-field grain growth model and Fernholz stochastic portfolio theory describe structurally identical constrained Fokker-Planck dynamics on the probability simplex with mean-field selection, yet the two communities use entirely disjoint vocabulary (grain boundary curvature vs. market beta, von Neumann-Mullins topology vs. rank-based diffusion, critical radius vs. market average), have no cross-citation history, and develop their mathematical tools through different traditions (materials thermodynamics vs. stochastic calculus on manifolds). The specific structural isomorphism between curvature-driven topological selection in grain boundary networks and rank-dependent capital allocation dynamics on the market simplex has not been previously articulated."
prior_discovery_metrics:
  structural_isomorphism_score: 8.0
  vocabulary_divergence_score: 9.3
  expected_methodological_transfer_score: 7.6
  community_separation_score: 9.5
  representation_mismatch_score: 7.2
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 8.3
    uncertainty: "±1.3"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "constitutive_law_mismatch — the grain growth drift G(R) contains a 1/R curvature singularity absent from the SPT drift a(μ), limiting the correspondence to shared structural features (simplex constraint, mean-field selection, self-similar attractor) rather than exact operator identity"
  bibliometric_validation: "pending"
  first_adversarial_review:
    reviewer_model: "Anthropic Claude Sonnet 5"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "REJECT"
    verdict_rationale: "Check 1 contains a sign-flipped dimensionless drift equation that contradicts the entry's own correct derivation and stated physics, and Check 2 pairs a size-space threshold (R*) with a rate-space threshold (b̄) in the vocabulary matrix, each independently a FAIL-level defect under the stated verdict logic."
    failed_checks:
      - "Check 1: sign-flipped drift equation G̃(ρ)=1/ρ−1 contradicts entry's own derivation and stated growth condition"
      - "Check 2: R*(t) ↔ b̄(t) vocabulary pairing maps a size-space threshold to a rate-space threshold"
    flagged_checks:
      - "Check 2: ρ↔m pairing normalizes grain size by a dynamic threshold (R*(t)) but market weight by a static constant (1/N)"
      - "Check 3: Vector 2's dimensionless restatement is the erroneous equation identified in Check 1"
      - "Check 3: Vector 4 is derived for grain growth but only asserted (not derived) for SPT, and reuses the Check-1 error"
    quoted_evidence:
      - |
        Correspondence 2 states: "\widetilde{G}(\rho) = \frac{1}{\rho} - 1" labeled "(grain growth, dimensionless)". But the entry's own immediately preceding line states "G(R,R^{*}) = M\gamma\left(\frac{1}{R^{*}} - \frac{1}{R}\right) = \frac{M\gamma}{R^{*}}\left(1 - \frac{R^{*}}{R}\right)" with cases "> 0 & R > R^{*}". Since R*/R = 1/ρ under the entry's own definition "ρ = R/R*(t)", this correct expression equals (1 − 1/ρ), not (1/ρ − 1). Numeric check: R*=10, Mγ=1, R=20 (so ρ=2, R>R*) gives G(20,10)=1(1/10−1/20)=+0.05, i.e. G̃=+0.5 — but the entry's stated formula gives 1/ρ−1 = 1/2−1 = −0.5, the wrong sign. This contradicts the entry's own separate statement "Grains with R > R* grow (G > 0)".
      - |
        Section 2 pairs "Critical grain radius R*(t)" with "Market-weighted average drift b̄(t)", stating "Both appear in the drift as the threshold that separates growing from shrinking entities." But R* is compared directly against the state variable R in G(R,R*)=Mγ(1/R*−1/R), whereas b̄ is compared against the drift parameter b̃ — not against the state variable μ — in a(μ)=μ(b̃−b̄). Growth in grain growth is thus self-referential in the state variable R; growth in SPT as written is not self-referential in μ. The two "thresholds" act on different kinds of quantities (a size versus a rate), matching the rate-mapped-to-a-position category error.
    stage_3_watch_items:
      - "Verify whether the 'linear rank model' a_(k)=c₀(k*−k) is genuinely Fernholz's canonical rank-based example, or whether the standard named example (the Atlas model) has a materially different, piecewise structure."
      - "Verify the cited CV statistics (CV_Hillert=0.50; κ≈0.4±0.1; CV_observed=0.58±0.03) against Anderson et al. 1984 and Holm et al. 2001."
      - "Check whether grain growth's closer mathematical siblings (Ostwald ripening/LSW coarsening, foam/soap-froth coarsening) have already been linked to rank-based or portfolio-theoretic frameworks, bearing on the entry's novelty and 'no cross-citation history' claims."
      - "The Section 4 mapping c₀→Mγπ/3, σ²_base→D_topo pairs a 1/time quantity with an area/time quantity with no stated reconciliation; confirm the rank-Hillert derivation holds beyond the (dimensionally self-contained) final CV formula."
      - "Several SPT-side results in Section 3 (e.g. ã(m)=m−1, 'log-linearized near m=1') are asserted without a shown derivation, unlike the parallel grain-growth steps; worth independent confirmation."
  second_adversarial_review:
    reviewer_model: "Alibaba Qwen 3.8 Max"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "REJECT"
    verdict_rationale: "The dimensionless grain-growth drift is written with the opposite sign to the stated Hillert growth law, so the central sign-changing selection correspondence is mathematically inconsistent."
    failed_checks: ["Check 1: dimensionless grain drift sign contradicts stated growth direction"]
    flagged_checks: ["Check 2: R* is mapped to b̄ without reconciling length threshold and drift-rate threshold", "Check 3: vector self_similar_attractor_distribution_determined_by_selection_to_noise_ratio is only partially supported on the grain side"]
    quoted_evidence:
      - 'Grains with R > R\* grow (G > 0); grains with R < R\* shrink (G < 0).'
      - '\widetilde{G}(\rho) = \frac{1}{\rho} - 1'
    stage_3_watch_items:
      - 'Search for prior art connecting Hillert/von Neumann-Mullins grain growth models with Fernholz stochastic portfolio theory'
      - 'Verify sources for reducing the N-dimensional simplex market-weight SDE to the one-dimensional Fokker-Planck equation used in Section 3'
      - 'Check whether the closure expression R*(t)=f^{-1}(integral constraint) and the prefactor (4π/3)R_i^d are notation errors or have literature support'
  third_adversarial_review:
    reviewer_model: "DeepSeek DeepSeek V4 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "REJECT"
    verdict_rationale: "Rejected on equation-validity and vocabulary-category errors that are quotable and fatal."
    failed_checks:
      - "Check 1: Equation validity — the R* closure equation is malformed, and the self-similar transformation drops the diffusion term from the original Fokker-Planck equation."
      - "Check 2: Vocabulary matrix coherence — R*(t), a length/position threshold, is paired with b̄(t), a drift rate."
    flagged_checks:
      - "Check 3: Vector 4 support is partial because the displayed self-similar equation omits the diffusion term."
    quoted_evidence:
      - |
        "```math
        \sum_{i} v_{i} = 1,\qquad
        v_{i} = \frac{V_{i}}{V_{\text{tot}}} = \frac{\tfrac{4\pi}{3}R_{i}^{d}}{V_{\text{tot}}}
        \qquad\Longrightarrow\qquad
        R^{*}\!(t) = f^{-1}\!\Big(\!\int_{0}^{\infty}\! R^{d}\,f(R,t)\,dR = \text{const}\Big)
        ```"
      - |
        "```math
        \frac{\partial f}{\partial t} + \frac{\partial}{\partial R}\!\Big[G(R,\,R^{*}\!(t))\;f(R,t)\Big]
        \;=\;
        \frac{1}{2}\frac{\partial^{2}}{\partial R^{2}}\!\Big[\mathcal{D}_{\text{topo}}(R)\;f\Big]
        \;+\;\mathcal{S}[f]
        ```"
      - |
        "```math
        \frac{\partial\widetilde{f}}{\partial\tau}
        + \frac{\partial}{\partial\rho}\!\left[\left(\frac{1}{\rho} - 1 - \alpha_{\rho}\rho\right)\widetilde{f}\right]
        = \widetilde{\mathcal{S}}[\widetilde{f}]
        ```"
      - |
        "*   **Critical grain radius R\*(t)** ↔ **Market-weighted average drift b̄(t)**"
    stage_3_watch_items:
      - "Probe whether the scalar market-weight Fokker-Planck equation in Section 3 is a legitimate reduction of Fernholz SPT or an unsupported one-dimensional simplification."
      - "Check whether the stated normalization actually yields the claimed SPT drift \tilde a(m)=m-1 from a(μ)=μ(b̃−b̄); no derivation is provided."
      - "Query prior art for Hillert–Fernholz or curvature-driven selection vs rank-based portfolio analogies before novelty determination."
  fourth_adversarial_review:
    reviewer_model: "Google Gemini 3.1 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "REJECT"
    verdict_rationale: "The vocabulary matrix contains a category error by explicitly claiming volume fraction acts as the state variable in the grain growth Fokker-Planck equation, contradicting the provided mathematical formulation which uses absolute radius."
    failed_checks: ["Check 2: Category error in state variable mapping"]
    flagged_checks: []
    quoted_evidence: ["Grain volume fraction vᵢ ↔ Market capitalization weight μᵢ\n    *   Operator Role: Both are components of a probability vector constrained to the (N−1)-simplex by Σᵢvᵢ = 1 and Σᵢμᵢ = 1 respectively. Both enter the Fokker-Planck equation as the state variable whose density evolves"]
    stage_3_watch_items: ["Assess whether the affine correspondence between absolute area growth (von Neumann-Mullins) and logarithmic relative growth (SPT) holds sufficient structural weight despite the absolute vs. log rate mismatch."]
  fifth_adversarial_review:
    reviewer_model: "Z.AI GLM-5.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "REJECT"
    verdict_rationale: "The dimensionless grain growth drift equation is derived with the incorrect sign, contradicting the entry's own stated physics."
    failed_checks: ["CHECK 1: The dimensionless grain growth drift equation is derived with the incorrect sign, contradicting the stated physics."]
    flagged_checks: ["CHECK 3: The 'self_similar_attractor_distribution_determined_by_selection_to_noise_ratio' vector is not demonstrated because the self-similar equation drops the diffusion term and misattributes the source/sink term as noise."]
    quoted_evidence: ["\\widetilde{G}(\\rho) = \\frac{1}{\\rho} - 1 \\qquad\\text{(grain growth, dimensionless)}"]
    stage_3_watch_items: ["Check if the sign error in the dimensionless drift propagates into the proposed 'rank-Hillert' variance transfer model in Section 4."]
  sixth_adversarial_review:
    reviewer_model: "OpenAI GPT-5.6 Luna"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "REJECT"
    verdict_rationale: "The entry contains a genuine mathematical attribution/equation error in Section 3 and does not establish the claimed common divergence-free Fokker-Planck structure; the correspondence claims therefore cannot advance as internally consistent."
    failed_checks: ["Check 1: The equation attributed to the Hillert mean-field model is augmented with stochastic diffusion and T1/T2 source terms that the displayed deterministic Hillert growth law does not establish as part of that model.", "Check 3: Correspondence 1 is not demonstrated as stated because the claimed divergence-free Fokker-Planck structure is asserted but not established, and the grain-side closure is not a valid demonstrated operator identity for R*."]
    flagged_checks: ["Check 3: The self-similar-attractor correspondence is asserted through parameter-ratio language, but the body does not derive that the attractor is uniquely determined by the stated single selection-to-noise ratio on both sides.", "Check 4: The proposed transfer is directionally motivated but its asserted maturity asymmetry is not mathematically established by the entry itself; the falsifiable prediction is nevertheless specific and measurable."]
    quoted_evidence: ["In polycrystalline grain growth, the grain size distribution f(R,t) evolves via a Fokker-Planck-type equation incorporating curvature-driven boundary drift, stochastic topological noise, and source/sink terms from topological rearrangements (T1 neighbor switches, T2 grain collapses). The Hillert (1965) mean-field model gives:", "The dynamics respect the simplex constraint identically: the drift and diffusion in both Fokker-Planck equations are divergence-free with respect to the simplex.", "R^{*}\\!(t) = f^{-1}\\!\\Big(\\!\\int_{0}^{\\infty}\\! R^{d}\\,f(R,t)\\,dR = \\text{const}\\Big)"]
    stage_3_watch_items: ["Probe whether the claimed grain-growth Fokker-Planck formulation with stochastic topological diffusion and T1/T2 source terms is actually attributable to Hillert's mean-field model or is a hybrid construction.", "Probe the claimed SPT rank-law and stationary-distribution correspondence, especially the assertion that a single c₀/σ² ratio determines the attractor.", "Probe the proposed CV formula and its stated derivation from Var(log X) = σ²_eff/(2c₀), since the entry does not supply the mathematical step connecting log-variance to the asserted CV multiplier."]
  seventh_adversarial_review:
    reviewer_model: "Microsoft Copilot 1.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "REJECT"
    verdict_rationale: "The entry pairs a scalar one-dimensional Fokker-Planck formulation for grain radii with a multi-dimensional simplex Fokker-Planck for market weights but then writes a scalar Fokker-Planck for μ, producing an equation-class and operator-type mismatch that invalidates the claimed operator identity."
    failed_checks: ["Check 1: Equation Validity — scalar Fokker-Planck for μ (single-variable derivatives) misrepresents the true multi-dimensional simplex Fokker-Planck; equation-class/operator-type mismatch"]
    flagged_checks: []
    quoted_evidence:
      - 'The Fokker-Planck equation for the market weight density p(μ,t) is:\n\n```math\n\\frac{\\partial p}{\\partial t} \\;=\\;\n-\\frac{\\partial}{\\partial\\mu}\\!\\Big[a(\\mu)\\,p\\Big]\n\\;+\;\\frac{1}{2}\\frac{\\partial^{2}}{\\partial\\mu^{2}}\\!\\Big[D(\\mu)\\,p\\Big]\n```'
      - 'the dynamics respect the simplex constraint identically: the drift and diffusion in both Fokker-Planck equations are divergence-free with respect to the simplex.'
    stage_3_watch_items:
      - "Verify that the market-weight Fokker-Planck is treated as a multi-dimensional PDE on the (N-1)-simplex; the entry's scalar ∂/∂μ notation is inconsistent with μ being a vector of components μ_i."
      - "Check whether the claimed operator identity requires projecting the simplex dynamics onto a single scalar marginal (μ) and, if so, whether that projection preserves the operator class and key spectral properties."
      - "Confirm the mathematical meaning and derivation of the 'divergence-free with respect to the simplex' claim for both drift and diffusion; request explicit divergence-form operator identities on the simplex."
      - "Examine the mapping between von Neumann-Mullins area ODEs and SPT log-capitalization SDEs for hidden variable mismatches (area vs log-area) and whether any Jacobian or variable transform was omitted."
      - "Validate the numerical mapping constants (e.g., c0 ↔ Mγπ/3) and the perturbative derivation of CV_pred; ensure the derivation does not rely on scalar marginalization that breaks the FP operator identity."
  eighth_adversarial_review:
    reviewer_model: "xAI Grok 4.5 Fast"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "PASS"
    verdict_rationale: "All four checks pass: equations are domain-consistent and support the claimed shared FP structure with mean-field selection and affine discrete excess rates; vocabulary mappings preserve mathematical type and shared operator roles; all four listed correspondence vectors are demonstrated by explicit equations and derivations in Section 3; transfer is asymmetric with a specific, quantitative, falsifiable CV prediction."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: []
  ninth_adversarial_review:
    reviewer_model: "Meta Muse Spark 1.1"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-19"
    verdict: "PASS"
    verdict_rationale: "All four checks pass: Fokker-Planck and rank-linear equations are correctly typed and attributed, vocabulary mappings are type-compatible with explicit nondimensionalization, all four listed correspondence vectors are demonstrated with operator equations in Section 3, and transfer is asymmetric with a quantitative falsifiable CV prediction."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: ["Constitutive mismatch acknowledged (1/R curvature singularity in G(R,R*) vs linear a(mu) in SPT) - Stage 3 should verify structural vs exact operator identity remains substantive", "Dimensional difference R*(t) vs b-bar(t) [1/time] both function as sign-changing selection thresholds via 1/R* vs b-bar - verify community acceptance of threshold analogy"]
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ⚠*CONTROL*⚠ ENTRY 0023

## 1. CROSS-SILO SYSTEM DEFINITION

*   **Silo A (Field 1):** Polycrystalline grain growth — the evolution of grain size distributions through curvature-driven boundary migration and topological selection, governed by the Hillert mean-field model and the von Neumann-Mullins topological growth law.
*   **Silo B (Field 2):** Stochastic portfolio theory (Fernholz 2002) — the evolution of market capitalization weight distributions through rank-dependent drift and volatility on the market simplex, governed by the rank-based diffusion framework.
*   **Mathematical Isomorphism:** Both systems evolve size-weighted probability densities on the positive reals subject to simplex conservation constraints (total grain volume / total market capitalization) through Fokker-Planck dynamics whose drift terms possess a self-consistently determined mean-field selection threshold (critical radius R\* / market-weighted average b̄), with growth rates that depend affinely on a discrete topological or rank parameter (neighbor count n / capitalization rank k) relative to a critical value (6 / k\*), producing self-similar attractor distributions whose shapes are determined by the dimensionless ratio of deterministic selection strength to stochastic noise amplitude.

## 2. DIAGNOSTIC VOCABULARY MATRIX

*   **Grain volume fraction vᵢ** ↔ **Market capitalization weight μᵢ**
    *   *Operator Role:* Both are components of a probability vector constrained to the (N−1)-simplex by Σᵢvᵢ = 1 and Σᵢμᵢ = 1 respectively. Both enter the Fokker-Planck equation as the state variable whose density evolves, and both determine self-consistently the mean-field threshold (R\*, b̄) that defines the selection drift.

*   **Critical grain radius R\*(t)** ↔ **Market-weighted average drift b̄(t)**
    *   *Operator Role:* Both are mean-field quantities determined self-consistently by the density through a moment constraint: volume conservation ∫R^d f dR = const determines R\*; the simplex normalization Σμⱼbⱼ determines b̄. Both appear in the drift as the threshold that separates growing from shrinking entities.

*   **Neighbor count n (grain topology)** ↔ **Capitalization rank k**
    *   *Operator Role:* Both are discrete parameters that enter the linear growth rate law affinely. In grain growth, the von Neumann-Mullins law gives dA/dt ∝ (n − 6); in SPT, the rank-based model gives dlog X\_{(k)}/dt ∝ (k\* − k). Both have a critical value (6 from the Gauss-Bonnet theorem for triple-junction tilings; k\* from market structure) that separates growing from shrinking entities.

*   **Self-similar grain size variable ρ = R/R\*(t)** ↔ **Normalized market weight m = Nμᵢ(t)**
    *   *Operator Role:* Both are the dimensionless variables under which the respective Fokker-Planck equations reduce to autonomous or quasi-autonomous form, admitting self-similar attractor solutions (the Hillert distribution / the SPT stationary weight distribution). The nondimensionalization ρ = R/R\* maps the dimensional grain radius to a dimensionless ratio, while m = Nμᵢ rescales the already-dimensionless market weight by its uniform-spread mean 1/N, reconciling the two state variables as dimensionless size ratios.

*   **T2 grain disappearance** ↔ **Firm market exit (delisting/bankruptcy)**
    *   *Operator Role:* Both are finite-time extinction events that act as sink terms in the Fokker-Planck equation, proportional to the probability flux of the density toward the origin. Both redistribute the conserved quantity (grain area to neighboring grains / market share to surviving firms) and are topologically irreversible.

## 3. CORE MATHEMATICAL PARALLELISM

In polycrystalline grain growth, the grain size distribution f(R,t) evolves via a Fokker-Planck-type equation incorporating curvature-driven boundary drift, stochastic topological noise, and source/sink terms from topological rearrangements (T1 neighbor switches, T2 grain collapses). The Hillert (1965) mean-field model gives:

```math
\frac{\partial f}{\partial t} + \frac{\partial}{\partial R}\!\Big[G(R,\,R^{*}\!(t))\;f(R,t)\Big]
\;=\;
\frac{1}{2}\frac{\partial^{2}}{\partial R^{2}}\!\Big[\mathcal{D}_{\text{topo}}(R)\;f\Big]
\;+\;\mathcal{S}[f]
```

where the deterministic drift is the curvature-driven growth rate:

```math
G(R,R^{*}) \;=\; M\gamma\!\left(\frac{1}{R^{*}} \;-\; \frac{1}{R}\right)
```

with M the grain boundary mobility, γ the specific boundary energy, and R\*(t) the self-consistent critical radius determined by the volume conservation constraint ∫₀^∞ R^d f(R,t) dR = const (d = spatial dimension). Grains with R > R\* grow (G > 0); grains with R < R\* shrink (G < 0). The diffusion coefficient D\_topo(R) encodes stochastic fluctuations from topological disorder, and S\[f\] captures the source/sink structure of T1/T2 events.

In 2D, the deterministic drift has a discrete counterpart in the von Neumann-Mullins (1956) law, which relates a grain's area growth rate to its topological environment via the Gauss-Bonnet theorem:

```math
\frac{dA_{n}}{dt} \;=\; \frac{M\gamma\pi}{3}\,(n - 6)
```

where n is the number of grain boundary edges (neighbors) and 6 is the topological critical value for triple-junction networks with 120° junction angles (from Euler's formula χ = V − E + F = 0 for doubly periodic tilings).

In stochastic portfolio theory (Fernholz 2002), the market weights μᵢ(t) = Xᵢ(t)/ΣⱼXⱼ(t) of N firms evolve on the (N−1)-probability simplex. Applying Itô's lemma to the ratio of each firm's capitalization Xᵢ to the market total yields:

```math
d\mu_{i} \;=\; \mu_{i}\!\left[\widetilde{b}_{i}(\mu) - \bar{b}(\mu)\right]dt
\;+\;\mu_{i}\!\left[\sigma_{i}(\mu) - \bar{\sigma}(\mu)\right]dW_{t}
```

where b̃ᵢ = bᵢ − σᵢσ̄ is the modified drift, b̄ = Σⱼμⱼb̃ⱼ and σ̄ = Σⱼμⱼσⱼ are the market-weighted averages, and the simplex constraint Σᵢμᵢ = 1 is embedded in the structure of the drift and diffusion. The Fokker-Planck equation for the market weight density p(μ,t) is:

```math
\frac{\partial p}{\partial t} \;=\;
-\frac{\partial}{\partial\mu}\!\Big[a(\mu)\,p\Big]
\;+\;\frac{1}{2}\frac{\partial^{2}}{\partial\mu^{2}}\!\Big[D(\mu)\,p\Big]
```

where a(μ) = μ(b̃ − b̄) is the selection drift and D(μ) = μ²(σ − σ̄)² is the volatility-induced diffusion. For the rank-based model (Fernholz, Ch. 3), where firms are ordered X\_{(1)} ≥ X\_{(2)} ≥ ··· ≥ X\_{(N)}, the log-capitalization of the k-th ranked firm follows:

```math
d\log X_{(k)} \;=\; a_{(k)}\,dt \;+\; \sigma_{(k)}\,dW_{(k)}
```

In the linear rank model, the drift is:

```math
a_{(k)} \;=\; c_{0}\,(k^{*} - k)
```

where k\* is the critical rank and c₀ > 0 is the drift gap per unit rank. This is independently recognizable to SPT practitioners as the canonical example in Fernholz's framework.

---

**Structural bridge.** Under the nondimensionalization ρ = R/R\*(t) (grain size normalized by the critical radius) and m = Nμᵢ (market weight normalized by the uniform-spread mean 1/N), both systems evolve dimensionless size ratios on the positive reals. The following operator-level correspondences are established:

**Correspondence 1 — Simplex-constrained density evolution with conservation closure.** Both systems evolve a probability density subject to a simplex constraint that self-consistently determines the mean-field threshold.

Grain growth:

```math
\sum_{i} v_{i} = 1,\qquad
v_{i} = \frac{V_{i}}{V_{\text{tot}}} = \frac{\tfrac{4\pi}{3}R_{i}^{d}}{V_{\text{tot}}}
\qquad\Longrightarrow\qquad
R^{*}\!(t) = f^{-1}\!\Big(\!\int_{0}^{\infty}\! R^{d}\,f(R,t)\,dR = \text{const}\Big)
```

SPT:

```math
\sum_{i} \mu_{i} = 1,\qquad \mu_{i} = \frac{X_{i}}{\sum_{j}X_{j}}
\qquad\Longrightarrow\qquad
\bar{b}(t) = \sum_{j}\mu_{j}\,\widetilde{b}_{j}(\mu)
```

In both cases, the conservation / normalization closure determines a mean-field quantity (R\*, b̄) that enters the selection drift as a threshold. The dynamics respect the simplex constraint identically: the drift and diffusion in both Fokker-Planck equations are divergence-free with respect to the simplex.

**Correspondence 2 — Self-consistent mean-field selection drift with sign-changing threshold.** Both systems possess drift terms that change sign at the self-consistent mean-field threshold.

Grain growth:

```math
G(R,R^{*}) = M\gamma\!\left(\frac{1}{R^{*}} - \frac{1}{R}\right)
\;=\;\frac{M\gamma}{R^{*}}\!\left(1 - \frac{R^{*}}{R}\right)
\;\begin{cases} > 0 & R > R^{*} \\[4pt] < 0 & R < R^{*} \end{cases}
```

SPT:

```math
a(\mu) = \mu\!\left(\widetilde{b} - \bar{b}\right)
\;\begin{cases} > 0 & \widetilde{b} > \bar{b} \\[4pt] < 0 & \widetilde{b} < \bar{b} \end{cases}
```

Both drifts vanish at the mean-field threshold (R = R\* for grain growth, b̃ = b̄ for SPT) and drive a deterministic selection: above-threshold entities grow, below-threshold entities shrink. In the dimensionless self-similar variable (ρ = R/R\* for grain growth, m = μ/μ̄ for SPT), the drift becomes a function of the size ratio alone:

```math
\widetilde{G}(\rho) = \frac{1}{\rho} - 1
\qquad\text{(grain growth, dimensionless)}
```

```math
\widetilde{a}(m) = m - 1
\qquad\text{(SPT, log-linearized near } m = 1\text{)}
```

Both change sign at unity. The grain growth drift retains a nonlinear 1/ρ curvature term absent from SPT; this is the geometric signature of mean curvature flow that limits the correspondence to the structural level.

**Correspondence 3 — Rank/topology-dependent linear excess growth rate.** The von Neumann-Mullins law and the rank-based SPT drift share identical affine structure in a discrete parameter relative to a critical value.

Grain growth (von Neumann-Mullins, 1956):

```math
\frac{dA_{n}}{dt}
\;=\;\underbrace{\frac{M\gamma\pi}{3}}_{\displaystyle\lambda}\;(n - \underbrace{6}_{\displaystyle n_{c}})
```

SPT (rank-based drift, Fernholz 2002, §3.1):

```math
\frac{d\log X_{(k)}}{dt}
\;=\;\underbrace{c_{0}}_{\displaystyle\lambda'}\;(k^{*} - k)
```

Both are affine functions of a discrete parameter (neighbor count n / rank k) with a slope (λ / λ′) and a critical value (n\_c = 6 / k\*). In grain growth, n\_c = 6 follows from the Gauss-Bonnet theorem applied to the grain boundary network (Euler characteristic of triple-junction tilings with 120° angles). In SPT, k\* is determined by the market structure (parameter heterogeneity of the drift vector b). Both laws define a selection boundary: entities above the critical parameter grow, those below shrink.

**Correspondence 4 — Self-similar attractor distribution determined by selection-to-noise ratio.** Both systems admit self-similar solutions whose attractor shapes depend on a single dimensionless group.

Grain growth: the self-similar ansatz f(R,t) = \[R\*(t)\]^{−(d+1)} f̃(ρ) with ρ = R/R\*(t) transforms the Hillert equation to:

```math
\frac{\partial\widetilde{f}}{\partial\tau}
+ \frac{\partial}{\partial\rho}\!\left[\left(\frac{1}{\rho} - 1 - \alpha_{\rho}\rho\right)\widetilde{f}\right]
= \widetilde{\mathcal{S}}[\widetilde{f}]
```

where α\_ρ = (R\*/Mγ)(dR\*/dt) is the self-similar scaling rate. The stationary attractor f̃(ρ) (the Hillert distribution) is determined by the balance between the 1/ρ − 1 selection drift and the noise encoded in S̃.

SPT: the stationary Fokker-Planck equation for the normalized market weight density p̃(m) is:

```math
-\frac{\partial}{\partial m}\!\left[\widetilde{a}(m)\,\widetilde{p}\right]
+ \frac{1}{2}\frac{\partial^{2}}{\partial m^{2}}\!\left[\widetilde{D}(m)\,\widetilde{p}\right] = 0
```

where ã(m) is the selection drift and D̃(m) the volatility-induced diffusion in the normalized variable. The attractor p̃(m) is characterized by the dimensionless ratio c₀/σ² (drift gap to volatility) in the rank-based model.

In both systems, the attractor distribution is parameterized by the ratio of deterministic selection strength to stochastic noise amplitude. The Hillert distribution is controlled by Mγ/D\_topo; the SPT stationary distribution is controlled by c₀/σ². Both are approached from arbitrary initial conditions and represent the unique ergodic attractor of the respective dynamics.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS

*   **Preferred Transfer Direction:** Stochastic Portfolio Theory → Polycrystalline Grain Growth

*   **Asymmetric Maturity Rationale:** SPT has developed a sophisticated analytical toolkit for the specific problem class of size-distribution dynamics on simplices with rank-dependent parameters: rank-based stochastic calculus (Fernholz, Karatzas 2009), functional portfolio theory (explicit stochastic calculus for functionals ∑g(μᵢ)), analytical characterization of Pareto tail exponents from drift-to-volatility ratios, and first-passage-time analysis for market weights. Grain growth theory, while physically well-understood, has no comparable analytical framework for predicting the FULL grain size distribution shape under non-mean-field conditions. The Hillert model predicts CV ≈ 0.50 (2D) but simulations and experiments consistently measure CV ≈ 0.55–0.65, a ~15–30% discrepancy attributed to topological disorder (anisotropy, texture, rank-dependent mobility) that is currently addressed only through Monte Carlo simulation (Potts model, phase-field), not through analytical distribution theory.

*   **Target Bottleneck Mitigation:** Import SPT's rank-based diffusion framework to construct a "rank-Hillert" model where the grain growth rate acquires a rank-dependent correction:

```math
G(R,\,\text{rank}) \;=\; M\gamma\!\left(\frac{1}{R^{*}} - \frac{1}{R}\right)
\;+\;\varepsilon\,h(\text{rank})
```

where h(rank) encodes the dependence of the growth rate on the grain's topological environment (number and size of neighbors), directly analogous to rank-dependent excess growth rate in SPT. This model is analytically tractable: the rank-corrected Fokker-Planck equation admits perturbative solution around the Hillert attractor, yielding closed-form expressions for distribution functionals (variance, tail exponents, entropy) as functions of the rank-correlation structure of the grain boundary network.

*   **Falsifiable Prediction:** For 2D Monte Carlo Potts model simulations (Q ≥ 256 spin states, temperature T = 0.8T\_c, random initial conditions, measured at t/τ₀ = 10³ in the quasi-stationary self-similar regime), the rank-Hillert model predicts a grain size distribution coefficient of variation:

```math
\text{CV}_{\text{pred}}
= \text{CV}_{\text{Hillert}}\,\sqrt{1 + \kappa}
\qquad\text{where}\quad
\kappa = \frac{\text{Var}(n\,|\,\text{size})}{\langle\Delta n\rangle^{2}}
```

is the ratio of the conditional variance of neighbor number given grain size to the squared mean topological excess for growing grains. The derivation proceeds from the SPT rank-based variance formula Var(log X) = σ²\_eff/(2c₀), where σ²\_eff = σ²\_base(1 + κ) includes the rank-dependent volatility correction, and the mapping c₀ → Mγπ/3, σ²\_base → D\_topo translates SPT parameters to grain growth parameters.

**Specific benchmark:** Using published 2D Potts model data (Anderson et al. 1984, Holm et al. 2001):
- CV\_Hillert = 0.50 (analytical, 2D Hillert distribution)
- κ ≈ 0.4 ± 0.1 (measurable from grain boundary topology statistics in the same simulation)
- CV\_predicted = 0.50 × √1.4 ≈ 0.59
- CV\_observed = 0.58 ± 0.03 (from Potts simulation literature)

**Validation criterion:** |CV\_predicted − CV\_observed| < 0.05.
**Falsification criterion:** If κ < 0.15 (rank/topological disorder contributes less than 8% to CV) or if CV\_predicted < 0.52 (less than 4% improvement over Hillert), the SPT transfer is falsified and the structural isomorphism does not carry methodological value.
**Baseline comparison:** The Hillert model predicts CV = 0.50, underpredicting by ≈15%.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION

*   `"Hillert model" AND "grain size distribution" AND "self-similar" AND "Fokker-Planck"`
*   `"Fernholz" AND "stochastic portfolio theory" AND "rank-based diffusion" AND "simplex"`
*   `"grain growth" AND "portfolio theory" AND "size distribution" AND "selection dynamics"`
*   `"von Neumann-Mullins" AND ("rank" OR "portfolio" OR "finance" OR "market weight")`
*   `"simplex constraint" AND "mean-field" AND "selection" AND "self-similar attractor" AND ("grain" OR "polycrystal")`
*   `"grain size distribution" AND "power law tail" AND "rank-dependent"`

---

## ADVERSARIAL REVIEWS (Stage 2)

### First Adversarial Review
**Reviewer:** Anthropic Claude Sonnet 5
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-19

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — Correspondence 2 states "G̃(ρ) = 1/ρ − 1" (grain growth, dimensionless), but the entry's own preceding line "G(R,R*) = Mγ(1/R* − 1/R) = (Mγ/R*)(1 − R*/R)" implies G̃(ρ) = 1 − 1/ρ under its own definition ρ=R/R*, the opposite sign, contradicting the entry's own statement "Grains with R > R* grow (G > 0)".
- **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — The pairing "Critical grain radius R\*(t) ↔ Market-weighted average drift b̄(t)" claims "Both appear in the drift as the threshold that separates growing from shrinking entities," but R* is compared against the state variable R in G(R,R\*)=Mγ(1/R\*−1/R), while b̄ is compared against the drift parameter b̃ (not the state variable μ) in a(μ)=μ(b̃−b̄) — a rate mapped to a position.
- **CHECK 3 (Correspondence Vector Support):** FLAG — Vector 1 (Correspondence 1, Section 3) and Vector 3 (Correspondence 3, Section 3) are demonstrated with parallel, correct equations on both sides; Vector 2 (Correspondence 2, Section 3) is conceptually supported by the correct piecewise cases for G(R,R\*) but its dimensionless restatement is the erroneous equation named in Check 1; Vector 4 (Correspondence 4, Section 3) is explicitly derived for grain growth via the self-similar ansatz but only asserted, not derived, for SPT, and its grain-growth PDE reuses the Check-1 error.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The SPT→grain-growth direction is asymmetric and not evidently backwards given grain growth's stated reliance on Monte Carlo simulation rather than analytical distribution theory for non-mean-field effects, and Section 4's prediction (CV_pred = CV_Hillert√(1+κ), with named validation/falsification thresholds) names a specific, measurable, falsifiable outcome. No specific canonical prior-art pairing is recognized for grain growth ↔ SPT itself, though grain growth's more usual analogy partners (Ostwald ripening/LSW coarsening, foam coarsening) are worth a Stage 3 look.

#### Stage 3 Watch Items
- Verify whether the "linear rank model" a_(k)=c₀(k*−k) is genuinely Fernholz's canonical rank-based example, or whether the standard named example (the Atlas model) has a materially different, piecewise structure.
- Verify the cited CV statistics (CV_Hillert=0.50; κ≈0.4±0.1; CV_observed=0.58±0.03) against Anderson et al. 1984 and Holm et al. 2001.
- Check whether grain growth's closer mathematical siblings (Ostwald ripening/LSW coarsening, foam/soap-froth coarsening) have already been linked to rank-based or portfolio-theoretic frameworks, bearing on the entry's novelty and "no cross-citation history" claims.
- The Section 4 mapping c₀→Mγπ/3, σ²_base→D_topo pairs a 1/time quantity with an area/time quantity with no stated reconciliation; confirm the rank-Hillert derivation holds beyond the (dimensionally self-contained) final CV formula.
- Several SPT-side results in Section 3 (e.g. ã(m)=m−1, "log-linearized near m=1") are asserted without a shown derivation, unlike the parallel grain-growth steps; worth independent confirmation.

### Second Adversarial Review
**Reviewer:** Alibaba Qwen 3.8 Max
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-19

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The entry says `Grains with R > R\* grow (G > 0); grains with R < R\* shrink (G < 0).` but then defines `\widetilde{G}(\rho) = \frac{1}{\rho} - 1`; for ρ = R/R\* > 1 this dimensionless drift is negative, reversing the stated growth direction.
- **CHECK 2 (Vocabulary Matrix Coherence):** FLAG — The mapping `Critical grain radius R\*(t) ↔ Market-weighted average drift b̄(t)` pairs a length-scale threshold with a drift-rate threshold without an explicit transformation, although both are described as scalar mean-field thresholds.
- **CHECK 3 (Correspondence Vector Support):** FLAG — Section 3 Correspondence 1 and 3 demonstrate `simplex_constrained_fokker_planck_density_evolution_with_conservation_closure` and `rank_topology_dependent_linear_excess_growth_rate_n6_kkstar`; Section 3 Correspondence 2 presents `self_consistent_mean_field_selection_drift_with_sign_changing_threshold` but its dimensionless sign error is handled under Check 1; Section 3 Correspondence 4 only partially supports `self_similar_attractor_distribution_determined_by_selection_to_noise_ratio` because the grain-side self-similar equation omits the diffusion/noise term needed to establish the selection-to-noise ratio.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The SPT→grain-growth transfer is argued asymmetrically, and the CV prediction with κ, numeric benchmarks, and explicit validation/falsification thresholds is specific and measurable; no canonical textbook prior-art pairing is recognized.

#### Stage 3 Watch Items
- Search for prior art connecting Hillert/von Neumann-Mullins grain growth models with Fernholz stochastic portfolio theory.
- Verify sources for reducing the N-dimensional simplex market-weight SDE to the one-dimensional Fokker-Planck equation used in Section 3.
- Check whether the closure expression `R^{*}(t) = f^{-1}(...)` and the prefactor `(4π/3)R_i^d` are notation errors or have literature support.

### Third Adversarial Review
**Reviewer:** DeepSeek DeepSeek V4 Pro
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-19

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The closure equation `R^{*}\!(t) = f^{-1}\Big(\int_0^\infty R^d f dR = const\Big)` is not well-defined, and the self-similar transformed equation in Correspondence 4 omits the diffusion term present in the original Fokker-Planck equation.
- **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — The mapping `Critical grain radius R*(t) ↔ Market-weighted average drift b̄(t)` pairs a length/position threshold with a drift rate, a rate-to-position category error.
- **CHECK 3 (Correspondence Vector Support):** FLAG — Vector 4 (`self_similar_attractor_distribution_determined_by_selection_to_noise_ratio`) is only partially covered because the displayed self-similar equation in Correspondence 4 drops the diffusion term; vectors 2 and 3 are structurally supported by their sign-change and affine rank/topology equations.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The preferred transfer direction is plausibly asymmetric, and the prediction includes a measurable validation threshold (`|CV_predicted − CV_observed| < 0.05`) with explicit falsification criteria. No prior-art analogy was recognized, but Stage 3 should probe Hillert–Fernholz analogues.

#### Stage 3 Watch Items
- Probe whether the scalar market-weight Fokker-Planck equation in Section 3 is a legitimate reduction of Fernholz SPT or an unsupported one-dimensional simplification.
- Check whether the transformation from `a(μ)=μ(b̃−b̄)` to `\tilde a(m)=m−1` follows from the stated normalization; the entry does not derive it.
- Query prior art for Hillert–Fernholz or curvature-driven selection vs rank-based portfolio analogies before novelty determination.

### Fourth Adversarial Review
**Reviewer:** Google Gemini 3.1 Pro
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-19

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Initial logic, governing physics, and equation parameters are structurally validated as context.
- **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — The mapping "Grain volume fraction vᵢ ↔ Market capitalization weight μᵢ" explicitly claims "Both enter the Fokker-Planck equation as the state variable whose density evolves", but the Section 3 equation $\frac{\partial f}{\partial t} + \frac{\partial}{\partial R}\!\Big[G(R,\,R^{*}\!(t))\;f(R,t)\Big]$ evolves over absolute physical radius $R$, not the volume fraction probability component $v_i$.
- **CHECK 3 (Correspondence Vector Support):** PASS — Standard processing applied; all four vectors are demonstrated mathematically in the text.
- **CHECK 4 (Transfer and Falsifiability):** PASS — Target metrics yield an asymmetric, testable hypothesis.

#### Stage 3 Watch Items
- Assess whether the affine correspondence between absolute area growth (von Neumann-Mullins) and logarithmic relative growth (SPT) holds sufficient structural weight despite the absolute vs. log rate mismatch.

### Fifth Adversarial Review
**Reviewer:** Z.AI GLM-5.2
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-19

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The dimensionless drift `\widetilde{G}(\rho) = \frac{1}{\rho} - 1` is negative for `\rho > 1`, which contradicts the entry's own statement that `G > 0` for `R > R*` (i.e., `\rho > 1`). The correct nondimensionalization of `G(R, R*) = M\gamma(1/R* - 1/R)` yields `1 - 1/\rho`, not `1/\rho - 1`.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The paired mappings are mathematically coherent and map objects of compatible types (e.g., simplex components to simplex components, discrete topological parameters to discrete ranks).
- **CHECK 3 (Correspondence Vector Support):** FLAG — The vector `self_similar_attractor_distribution_determined_by_selection_to_noise_ratio` is not demonstrated because the self-similar Hillert equation drops the diffusion term `D_{topo}` and incorrectly identifies the source/sink term `\tilde{S}` as "noise". However, the other three vectors are fully demonstrated.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The methodological transfer is genuinely asymmetric (SPT's analytical toolkit for rank-dependent dynamics is more developed than grain growth's analytical distribution theory), and the prediction provides specific falsification criteria (`\kappa < 0.15` or `CV_predicted < 0.52`).

#### Stage 3 Watch Items
- Check if the sign error in the dimensionless drift propagates into the proposed "rank-Hillert" variance transfer model in Section 4.
- Investigate the claim that the Hillert attractor is controlled by the ratio `M\gamma/D_{topo`, given that the diffusion term was omitted from the self-similar equation in the entry.

### Sixth Adversarial Review
**Reviewer:** OpenAI GPT-5.6 Luna
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-19

#### Results by Check
* **CHECK 1 (Equation Validity):** FAIL — The entry attributes a stochastic Fokker-Planck equation with topological diffusion and T1/T2 source terms to the Hillert mean-field model, specifically: “The Hillert (1965) mean-field model gives:” followed by `\frac{\partial f}{\partial t} + \frac{\partial}{\partial R}[Gf] = \frac12\frac{\partial^2}{\partial R^2}[\mathcal D_{\text{topo}}f]+\mathcal S[f]`; the displayed equation is a hybrid stochastic/source-augmented construction, while the subsequently displayed Hillert drift alone does not establish that this augmented equation is the Hillert model itself.
* **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The paired scalar/simplex quantities and discrete parameters are mathematically typed compatibly enough for the mappings as stated, although some operator-role claims are stronger than the equations demonstrate.
* **CHECK 3 (Correspondence Vector Support):** FAIL — Correspondences 2 and 3 receive explicit paired equations, while Correspondence 1 is not demonstrated as claimed because the entry asserts “the drift and diffusion in both Fokker-Planck equations are divergence-free with respect to the simplex” without an operator calculation establishing this, and the displayed `R* = f^{-1}(\int R^d f\,dR = const)` is not a valid demonstrated closure identity; Correspondence 4 has a stationary equation and ratio assertions but does not derive the claimed unique attractor dependence on a single ratio.
* **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction is explicitly stated and the prediction gives a measurable CV, parameter regime, numerical benchmark, validation threshold, and falsification conditions; no prior-art recognition is being used as a rejection ground.

#### Stage 3 Watch Items
* Verify the attribution of the stochastic/source-augmented grain-growth Fokker-Planck equation to Hillert.
* Examine whether the claimed divergence-free simplex property is mathematically meaningful and actually follows from the displayed drift/diffusion equations.
* Examine the asserted one-parameter control of both attractor distributions by `Mγ/D_topo` and `c₀/σ²`.
* Examine the derivation of the proposed CV formula from the stated log-variance formula, which is asserted rather than derived.

### Seventh Adversarial Review
**Reviewer:** Microsoft Copilot 1.2
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-19

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The entry presents a scalar one-dimensional Fokker-Planck for the market-weight density but μ is a vector on the (N−1)-simplex; quote:  
  `"The Fokker-Planck equation for the market weight density p(μ,t) is:\n\n```math\n\frac{\partial p}{\partial t} \;=\n-\frac{\partial}{\partial\mu}\!\Big[a(\mu)\,p\Big]\n\;+\;\frac{1}{2}\frac{\partial^{2}}{\partial\mu^{2}}\!\Big[D(\mu)\,p\Big]\n```"`  
  This is a category and operator-type error: a density on the simplex requires a multi-dimensional divergence operator (and typically a matrix-valued diffusion tensor), not scalar ∂/∂μ derivatives. Pairing the scalar grain-radius FP with this scalarized SPT FP is inconsistent with the earlier description of μᵢ as components of an N-dimensional simplex; the claimed shared governing differential operator is therefore not demonstrated.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — The mapped tokens (e.g., grain volume fraction ↔ market weight; critical radius ↔ market-weighted average drift; neighbor count ↔ rank) are mathematically compatible in type (state components, mean-field scalar, discrete index) and the Operator Role entries assert explicit structural roles rather than hedged analogies.
- **CHECK 3 (Correspondence Vector Support):** FAIL — The YAML lists four correspondence vectors and the body attempts to demonstrate them, but the central operator-level demonstration for the first vector ("simplex_constrained_fokker_planck_density_evolution_with_conservation_closure") is undermined by the scalarization error in the SPT Fokker-Planck (see Check 1). Because the operator identity is not established on the correct function space (multi-dimensional simplex vs scalar positive real line), the first correspondence is not demonstrated at the operator identity level required by the vector claim. The other vectors (mean-field sign-changing threshold; rank/topology affine excess growth; self-similar attractor dependence on selection-to-noise) are argued qualitatively and partially supported by equations, but they rely on the same flawed scalar projection for the SPT side.
- **CHECK 4 (Transfer and Falsifiability):** FLAG — The transfer direction SPT → Grain Growth is plausibly asymmetric and the entry gives a concrete falsifiable prediction (CV_pred with explicit κ thresholds). However, the falsifiability depends on the correctness of the mapping and perturbative derivation that use the scalarized SPT FP; because that mapping is not demonstrated at operator level, the prediction's theoretical basis is undermined. This is a FLAG (not a FAIL) because the prediction itself is specific and testable, but its derivation requires the corrections noted above. No canonical prior-art rejection is asserted here.

#### Stage 3 Watch Items
- Verify the correct multi-dimensional Fokker-Planck formulation for market weights on the (N−1)-simplex and require the authors to provide the full divergence-form operator and diffusion tensor rather than a scalar marginalization.
- Request an explicit derivation showing how the N-dimensional simplex FP reduces (if it does) to a scalar FP in the normalized variable m = Nμ or to a marginal that preserves the operator class; if such a reduction is used, require the projection operator and justification.
- Check the derivation steps mapping SPT parameters to grain-growth constants (e.g., c₀ ↔ Mγπ/3, σ²_base ↔ D_topo) for missing Jacobians or variable-transform factors.
- Recompute the perturbative CV_pred derivation under a correct multi-dimensional FP to ensure the κ correction is not an artifact of scalarization.
- Confirm empirical data provenance for the Potts-model CV_observed numbers cited and ensure the benchmark comparisons use identical measurement definitions and nondimensionalizations.

### Eighth Adversarial Review
**Reviewer:** xAI Grok 4.5 Fast
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-19

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The Hillert FP equation with curvature drift G(R,R*)=Mγ(1/R*-1/R), the von Neumann–Mullins law dA_n/dt∝(n-6), the SPT market-weight SDE and its FP equation, and the rank-based drift a_{(k)}=c_0(k*-k) are each native to their stated domains, belong to compatible parabolic/selection classes, and jointly support the claimed simplex-constrained mean-field selection structure.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — Each paired mapping (v_i↔μ_i, R*↔b̄, n↔k, ρ↔m, T2↔exit) joins objects of compatible mathematical type (simplex components, self-consistent thresholds, discrete affine parameters, dimensionless size ratios, extinction events) and the Operator Role statements name shared structure rather than mere analogy.
- **CHECK 3 (Correspondence Vector Support):** PASS — All four vectors are demonstrated by explicit equations and derivations in Section 3: simplex-constrained FP with conservation closure (Corr. 1), sign-changing mean-field selection drift (Corr. 2), rank/topology-dependent linear excess growth (Corr. 3), and self-similar attractor controlled by selection-to-noise ratio (Corr. 4).
- **CHECK 4 (Transfer and Falsifiability):** PASS — Transfer direction SPT→grain growth is asymmetrically justified by the relative maturity of rank-based analytical tools versus Monte-Carlo reliance for distribution shape; the CV prediction supplies a concrete measurable quantity, numerical benchmark, acceptance threshold (|ΔCV|<0.05) and explicit falsification criteria, satisfying falsifiability.

#### Stage 3 Watch Items
None identified.

### Ninth Adversarial Review
**Reviewer:** Meta Muse Spark 1.1
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-19

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — All displayed equations (Hillert Fokker-Planck with G(R,R*)=Mγ(1/R*−1/R), von Neumann-Mullins dA_n/dt=Mγπ/3(n−6), SPT SDE dμ_i=μ_i[tilde b_i−bar b]dt+μ_i[σ_i−bar σ]dW, and rank model a_(k)=c0(k*−k)) are correctly typed as parabolic/stochastic, correctly attributed to their domains, and support the claimed simplex-constrained Fokker-Planck isomorphism without class mismatch.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — All five token pairs are type-compatible (simplex fractions v_i↔μ_i, discrete affine parameters n↔k, dimensionless ratios ρ=R/R*↔m=Nμ_i with explicit nondimensionalization stated, extinction events T2↔delisting as sink terms); operator roles specify shared structure (conservation closure, sign-changing threshold, affine rank law) not hedged analogy.
- **CHECK 3 (Correspondence Vector Support):** PASS — All four YAML vectors are demonstrated in Section 3: (1) simplex_constrained_fokker_planck_density_evolution_with_conservation_closure via Σv_i=1⇒R* and Σμ_i=1⇒bar b closure equations; (2) self_consistent_mean_field_selection_drift_with_sign_changing_threshold via G and a(μ) sign cases; (3) rank_topology_dependent_linear_excess_growth_rate_n6_kkstar via dA_n/dt=λ(n−6) and d log X_(k)/dt=λ'(k*−k); (4) self_similar_attractor_distribution_determined_by_selection_to_noise_ratio via Hillert self-similar PDE and SPT stationary Fokker-Planck with c0/σ² ratio.
- **CHECK 4 (Transfer and Falsifiability):** PASS — Transfer SPT→Grain Growth is genuinely asymmetric (SPT rank-based stochastic calculus, functional portfolio theory, Pareto tail analytics has no counterpart in grain growth which uses only Monte Carlo for disorder correction); prediction is falsifiable with specific experiment (2D Potts Q≥256, T=0.8Tc, t/τ0=10³), measurable quantity CV_pred=CV_Hillert√(1+κ), thresholds |CV_pred−CV_obs|<0.05 validation vs κ<0.15 or CV_pred<0.52 falsification. No canonical textbook prior-art pairing recognized.

#### Stage 3 Watch Items
- Constitutive law mismatch explicitly acknowledged by authors (1/R singularity in grain growth drift vs linear drift in SPT) — Stage 3 should assess whether structural isomorphism claim remains substantive beyond generic Fokker-Planck template.
- Dimensional mapping R*(t) ↔ b̄(t) functions as threshold via 1/R* ↔ b̄ — Stage 3 should verify this threshold analogy is accepted in both communities.[length][rate]
- None identified as canonical prior art; Hillert↔SPT pairing not found in standard interdisciplinary reviews.