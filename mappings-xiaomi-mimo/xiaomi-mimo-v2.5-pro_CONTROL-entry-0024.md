---
sid_metadata:
  entry_id: "CONTROL-SID-0024"
  schema_version: "2.0-control"
  maturity_stage: "candidate"
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