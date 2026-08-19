---
sid_metadata:
  entry_id: "CONTROL-SID-0005"
  schema_version: "2.0-control"
  maturity_stage: "adversarial-rejected"
provenance:
  company: "Microsoft"
  model_family: "Copilot"
  model_version: "1.2"
  generation_timestamp: "2026-08-17"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "elastohydrodynamic-lubrication-and-rough-surface-contact-tribology"
  domain_b: "semiconductor-device-transport-numerics"
  structural_family: "nonlinear-coupled-parabolic-elliptic-transport-with-free-boundary-and-contact-constraints"
  triple_correspondence_vectors:
    - "lubrication_reynolds_operator_vs_drift_diffusion_operator"
    - "film_thickness_elastic_coupling_vs_poisson_potential_coupling"
    - "contact_sealing_robin_like_boundary_vs_surface_recombination_robin_boundary"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language / incompatible_ontologies / historically_isolated_communities"
prior_discovery_metrics:
  structural_isomorphism_score: 8.2
  vocabulary_divergence_score: 8.7
  expected_methodological_transfer_score: 7.6
  community_separation_score: 8.9
  representation_mismatch_score: 8.5
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 7.0
    uncertainty: "±1.2"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "constitutive_law_mismatch"
  bibliometric_validation: "pending"
  first_adversarial_review:
    reviewer_model: "Anthropic Claude Sonnet 5"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "REJECT"
    verdict_rationale: "Check 1 fails on independent, internally-verifiable grounds: the Silo A steady-form equation in Section 3 does not follow from its own preceding equation (a sign error on the entrainment term), and the nondimensional group Pi is not actually dimensionless as claimed."
    failed_checks: ['Check 1: sign error in the Silo A steady-form Reynolds equation relative to its own preceding equation, plus a dimensional inconsistency in the Pi parameter and a sign inconsistency in the Poisson mobile-charge term']
    flagged_checks: ['Check 2: the h(x,t) vocabulary-matrix row header ambiguously pairs a field-type quantity (h) with rho, a source-type quantity, instead of phi']
    quoted_evidence:
      - '\frac{\partial h}{\partial t} + \frac{\partial}{\partial x}\left( -\frac{h^3}{12\eta}\frac{\partial p}{\partial x} + \frac{U h}{2} \right) = 0'
      - '\frac{\partial}{\partial x}\left( h^3(x,t)\frac{\partial p}{\partial x} \right) = 12\eta \frac{\partial h}{\partial t} - 6\eta U \frac{\partial h}{\partial x}.'
      - '\Pi = \frac{p_0 L^2}{\eta U h_0^3}'
      - '-\frac{\partial}{\partial x}\left(\epsilon\frac{\partial \phi}{\partial x}\right) = q(n-p)+\rho_{fixed}.'
      - 'J_n = -D_n\frac{\partial n}{\partial x} + \mu_n n \frac{\partial \phi}{\partial x}'
    stage_3_watch_items:
      - "If this entry is revised and resubmitted, verify the corrected forms of the flagged equations: the entrainment-term sign in the Silo A divergence equation, the dimensional consistency of Pi, and the mobile-charge sign in the Poisson equation."
      - "Confirm the intended h(x,t) vocabulary-matrix mapping is h-to-phi (field-to-field) and p-to-rho (source-to-source); the current row header text conflates phi and rho under a single mapping entry."
      - "No canonical source is recognized for the EHL-to-semiconductor-transport pairing specifically, but the broader free-boundary/complementarity-problem (variational inequality) literature already connects lubrication cavitation to other free-boundary problems such as obstacle problems and American option pricing; check whether a similar cross-domain solver-transfer argument already exists in the numerical-PDE or TCAD literature."
      - "The asymmetric-maturity claim (EHL active-set/complementarity solvers being more advanced than semiconductor TCAD for degenerate-coefficient free boundaries) is argued with specific technical detail but is not supported by citations in the entry; verify bibliometrically."
  second_adversarial_review:
    reviewer_model: "Alibaba Qwen 3.8 Max"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "REJECT"
    verdict_rationale: "The entry contains an algebraically inconsistent Reynolds equation and does not demonstrate the third listed correspondence vector, leaving fewer than three supported vectors."
    failed_checks:
      - "Check 1: The time-dependent Reynolds equation and the subsequent quasi-steady Reynolds operator have an inconsistent entrainment-term sign."
      - "Check 3: contact_sealing_robin_like_boundary_vs_surface_recombination_robin_boundary is only asserted through limits/analogous degeneracy, not demonstrated by an equation, operator identity, or derivation."
    flagged_checks:
      - "Check 2: The h(x,t) mapping to 'ρ(x,t) or Green's-kernel potential response' is type-ambiguous and inconsistent with the p↔φ and h^3↔μn identifications."
    quoted_evidence:
      - '\frac{\partial h}{\partial t} + \frac{\partial}{\partial x}\left( -\frac{h^3}{12\eta}\frac{\partial p}{\partial x} + \frac{U h}{2} \right) = 0 ... \frac{\partial}{\partial x}\left( h^3(x,t)\frac{\partial p}{\partial x} \right) = 12\eta \frac{\partial h}{\partial t} - 6\eta U \frac{\partial h}{\partial x}.'
      - 'The mapping is via the limit \(S\to0\) or \(S\to\infty\) and by treating regions with vanishing \(A\) as operator degeneracy analogous to cavitation.'
    stage_3_watch_items:
      - "Verify whether the intended Reynolds wedge term sign is convention-dependent or an algebraic error."
      - "Search for prior work connecting Reynolds lubrication operators, complementarity cavitation, and semiconductor drift-diffusion/Poisson contact models."
      - "Probe whether semiconductor device numerics already use active-set/variational-inequality or degenerate-mobility multigrid methods that would weaken the claimed asymmetry."
      - "Clarify whether h maps to carrier density, electrostatic potential, or charge density; the current source-field alignment is inconsistent."
      - "Reconcile the predicted ≤50% nonlinear-iteration count with the weaker ≥30% reduction falsification threshold."
  third_adversarial_review:
    reviewer_model: "DeepSeek DeepSeek V4 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "REJECT"
    verdict_rationale: "Rejected for a displayed Reynolds-equation sign error contradicting the entry's own continuity equation and for an asserted but underived boundary-correspondence vector."
    failed_checks:
      - "Check 1: Equation validity — Reynolds equation algebraically inconsistent with preceding continuity equation"
      - "Check 3: Correspondence Vector Support — contact/sealing Robin-like boundary vector is asserted, not derived"
    flagged_checks:
      - "Check 2: Vocabulary Matrix Coherence — film thickness row maps a response field to a source density or potential response ambiguously"
      - "Check 4: Transfer and Falsifiability — success and falsification thresholds leave a non-falsifying interval"
    quoted_evidence:
      - "\\frac{\\partial}{\\partial x}\\left( h^3(x,t)\\frac{\\partial p}{\\partial x} \\right) = 12\\eta \\frac{\\partial h}{\\partial t} - 6\\eta U \\frac{\\partial h}{\\partial x}."
      - "The mapping is via the limit \\(S\\to0\\) or \\(S\\to\\infty\\) and by treating regions with vanishing \\(A\\) as operator degeneracy analogous to cavitation."
    stage_3_watch_items:
      - "Probe whether the Reynolds/drift-diffusion operator analogy is already canonical in applied mathematics or semiconductor device numerics."
      - "Probe Vector 1: the drift-diffusion current contains \\(-D_n \\partial_x n\\), but the displayed equivalence matches only the drift flux \\(\\mu_n n \\partial_x \\phi\\)."
      - "Check the boundary/free-boundary mapping claim for prior art in variational inequality and Robin-limit reductions."
  fourth_adversarial_review:
    reviewer_model: "Google Gemini 3.1 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "REJECT"
    verdict_rationale: "The entry relies on mathematically contradictory variable mappings between the two domains and pairs fundamentally incompatible equation classes (domain-wide complementarity vs. fixed linear boundary conditions)."
    failed_checks:
      - "Check 1: Internal contradiction in variable mappings between Vector 1 and Vector 2, and an equation-class mismatch pairing a free-boundary inequality with a linear Robin condition."
      - "Check 2: Category error in the Vocabulary Matrix conflating a source charge density with the resulting potential field."
      - "Check 3: The boundary correspondence vector is listed but not validly demonstrated due to the equation-class mismatch."
    flagged_checks: []
    quoted_evidence:
      - "Under the identification\n   - \\(p \\leftrightarrow \\phi\\) (pressure ↔ electrochemical potential)"
      - "Thus the coupling is operator-equivalent: pressure→deformation kernel vs. charge→potential Green's kernel."
      - "Explicitly, the EHL unilateral constraint can be represented variationally (complementarity):\n\n```math\np\\ge0,\\quad \\mathcal{L}[p]\\le f,\\quad p(\\mathcal{L}[p]-f)=0,\n```\n\nwhile semiconductor surface recombination can be written as a Robin operator \\( \\mathcal{B}[\\phi]=S(\\phi-\\phi_{eq})\\)."
      - "**h(x,t) (film thickness; elastic convolution of p)** ↔ **\\(\\rho(x,t)\\) or Green's-kernel potential response (Poisson convolution of charge density)**"
    stage_3_watch_items:
      - "Verify whether applying EHL active-set complementarity solvers is actually appropriate for semiconductor drift-diffusion systems, given the lack of valid structural equivalence demonstrated here."
  fifth_adversarial_review:
    reviewer_model: "Xiaomi MiMo V2.5 Pro"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "FLAG"
    verdict_rationale: "Core operator-equivalence structure is mathematically sound, but the entry contains a sign error in the rearranged Reynolds equation, dimensionally incorrect nondimensional groups, and an internally conflicted vocabulary mapping for the film-thickness field."
    failed_checks: []
    flagged_checks:
      - "Check 1: Sign error in rearranged Reynolds equation source term"
      - "Check 1: Both claimed dimensionless similarity parameters are dimensional"
      - "Check 2: Ambiguous h ↔ ρ/or-φ mapping creates tension with p ↔ φ mapping"
    quoted_evidence:
      - "∂/∂x(h³ ∂p/∂x) = 12η ∂h/∂t − 6ηU ∂h/∂x — The entry's own first equation is ∂h/∂t + ∂/∂x(−h³/(12η) ∂p/∂x + Uh/2) = 0; algebraic rearrangement yields +6ηU ∂h/∂x on the right-hand side, not −6ηU ∂h/∂x. The sign on the Couette source term is wrong."
      - "Π = p₀L²/(ηUh₀³) — Claimed as a 'nondimensional group' and 'Dimensionless similarity parameter.' Dimensional analysis: [p₀L²] = [kg·m/s²], [ηUh₀³] = [kg·m³/s²], giving Π dimensions of 1/m², not dimensionless."
      - "Γ = μ_n n₀ L²/D_n — Claimed as a 'nondimensional group.' Using the Einstein relation D_n = μ_n V_T, this reduces to n₀L²/V_T with dimensions of 1/(V·m) (for 3D carrier density), not dimensionless. The correct dimensionless Debye-ratio group would be (L/λ_D)² = q²n₀L²/(εkT)."
      - "h(x,t) (film thickness; elastic convolution of p) ↔ ρ(x,t) or Green's-kernel potential response (Poisson convolution of charge density) — The 'or' is unresolved. Mapping 1 identifies p ↔ φ (pressure ↔ potential), yet the convolutional structure in point 2 of Section 3 identifies source (p) ↔ source (ρ) and response (h) ↔ response (φ). The vocabulary matrix does not reconcile these two levels of correspondence."
    stage_3_watch_items:
      - "The EHL-to-semiconductor operator correspondence (degenerate divergence-form + convolutional elliptic coupling) is not a canonical textbook analogy I recognize. Verify whether this pairing has appeared in published interdisciplinary work on computational PDE transfer, operator preconditioning, or numerical methods for degenerate problems."
      - "The sign error and dimensional errors appear to be generation artifacts rather than conceptual misunderstandings; the structural argument in Section 3 points 1–3 is internally consistent once the sign and nondimensionalization are corrected. Human reviewer should assess whether these errors invalidate the claimed limit-matching argument."
  sixth_adversarial_review:
    reviewer_model: "Z.AI GLM-5.2"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "REJECT"
    verdict_rationale: "The two displayed EHL equations are mutually inconsistent in the sign of the Couette/entrainment term — a convention-independent internal error — and the claimed operator equivalence additionally conflates a governing operator with a drift-flux divergence."
    failed_checks:
      - "Check 1: Sign inconsistency between the two displayed EHL Reynolds equations — the continuity form implies +6ηU∂h/∂x while the 'steady or quasi-steady' form writes −6ηU∂h/∂x, so the two equations are incompatible under the entry's own definition of U as entrainment speed."
    flagged_checks:
      - "Check 1: The claimed operator equivalence pairs the Reynolds operator ∂_x(h³∂_x p) (governing operator for p) with the drift-flux divergence ∂_x(μ_n n ∂_x φ), which is a transport term in the continuity equation for n rather than the principal operator for φ (the principal operator for φ is the Poisson operator ∂_x(ε∂_x φ)); the quasi-Fermi/electrochemical-potential reformulation that would establish role-equivalence is named but not displayed."
      - "Check 2: The vocabulary pairing p↔φ is inconsistent with the convolutional parallel demonstrated in Vector 2, which pairs source↔source (p↔charge density) and field↔field (h↔φ); Section 2's 'h ↔ ρ or Green's-kernel potential response' hedges this unresolved role conflict."
    quoted_evidence:
      - "EHL continuity form: '\\frac{\\partial h}{\\partial t} + \\frac{\\partial}{\\partial x}\\left( -\\frac{h^3}{12\\eta}\\frac{\\partial p}{\\partial x} + \\frac{U h}{2} \\right) = 0' — expanding (U, η constant) gives ∂_x(h³∂_x p) = 12η∂_t h + 6ηU∂_x h."
      - "EHL steady/quasi-steady form: '\\frac{\\partial}{\\partial x}\\left( h^3(x,t)\\frac{\\partial p}{\\partial x} \\right) = 12\\eta \\frac{\\partial h}{\\partial t} - 6\\eta U \\frac{\\partial h}{\\partial x}.' — the Couette term carries the opposite sign relative to the continuity form above; the two equations cannot both hold under the same entrainment speed U, and the squeeze/Couette relative sign is convention-independent (standard Reynolds derivation yields same-sign, +/+)."
      - "Operator-equivalence claim: 'the principal second-order elliptic/parabolic operators coincide in divergence form: ∂_x(A ∂_x ψ), A_EHL=h^3/(12η), A_SC=μ_n n' — but A_SC=μ_n n premultiplies ∂_x φ inside the electron continuity equation, whose unknown is n; φ is not the variable governed by this operator."
    stage_3_watch_items:
      - "Verify whether a Reynolds-lubrication ↔ semiconductor drift-diffusion/Poisson operator equivalence has been published in the tribology or TCAD literature; the convolutional-coupling parallel (elastic kernel ↔ Poisson Green's function) is a generic linear-response observation and may not be novel."
      - "Probe whether the quasi-Fermi/electrochemical-potential reformulation (J_n = μ_n n ∇φ_n, continuity becoming a nonlinear divergence operator for φ_n) is what the generating model intended for Vector 1; the displayed standard (n, φ) formulation does not itself establish the p↔φ operator identity."
      - "Confirm the sign convention of the Reynolds Couette/entrainment term against the entry's single definition of U as 'entrainment speed'; the internal +6ηU vs −6ηU discrepancy should be resolved before any re-submission."
      - "Check whether the claimed asymmetric transfer (EHL active-set/complementarity solvers → semiconductor DD-Poisson with mobility collapse) has prior art in TCAD numerics for degenerate-mobility or 2D-material contact problems."
  seventh_adversarial_review:
    reviewer_model: "OpenAI GPT-5.6 Luna"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "REJECT"
    verdict_rationale: "The entry contains a concrete sign error in its derived Reynolds operator equation and a category-error alternative in the vocabulary mapping."
    failed_checks: ["Check 1: The displayed steady/quasi-steady Reynolds equation has the wrong sign on the entrainment term.", "Check 2: The mapping h(x,t) ↔ rho(x,t) maps film thickness, a response field, to charge density, a source field, without a stated transformation."]
    flagged_checks: []
    quoted_evidence: ['In Section 3, the entry states: "\frac{\partial}{\partial x}\left( h^3(x,t)\frac{\partial p}{\partial x} \right) = 12\eta \frac{\partial h}{\partial t} - 6\eta U \frac{\partial h}{\partial x}." Expanding the immediately preceding displayed continuity equation gives the entrainment contribution with a plus sign on the right-hand side, so the displayed derived equation has the wrong sign.', 'In Section 2, the entry states: "h(x,t) (film thickness; elastic convolution of p) ↔ \rho(x,t) or Green''s-kernel potential response (Poisson convolution of charge density)". The h ↔ rho alternative maps a film-thickness response/deformation field to charge density, which is a source field in the Poisson equation; no transformation is supplied that makes those objects the same mathematical type.']
    stage_3_watch_items: []
  eighth_adversarial_review:
    reviewer_model: "xAI Grok 4.5 Fast"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "FLAG"
    verdict_rationale: "Core operator and convolutional correspondences are supported by matching divergence-form and linear elliptic kernel structures, but the boundary-constraint vector relies on an incomplete limit mapping that is only partially demonstrated, and the vocabulary entry for film thickness versus density/potential response mixes object types."
    failed_checks: []
    flagged_checks: ["Check 2: Vocabulary Matrix Coherence — film-thickness mapping mixes scalar field with density/potential response", "Check 3: Correspondence Vector Support — contact_sealing_robin_like_boundary_vs_surface_recombination_robin_boundary only partially demonstrated via limits"]
    quoted_evidence: []
    stage_3_watch_items: ["Verify whether the unilateral free-boundary complementarity in EHL is rigorously equivalent (beyond heuristic limit) to Robin surface-recombination conditions under the stated S\to0/∞ limits", "Confirm that the h ↔ ρ/Green’s-kernel identification is intended as source-to-field map rather than direct field-to-field, given the explicit type mismatch in the matrix"]
  ninth_adversarial_review:
    reviewer_model: "Meta Muse Spark 1.1"
    protocol_version: "2.0-production"
    review_timestamp: "2026-08-18"
    verdict: "PASS"
    verdict_rationale: "All three correspondence vectors are demonstrated with compatible nonlinear parabolic-elliptic divergence operators, symmetric convolution kernels, and complementarity-to-Robin boundary mapping, with a quantitatively falsifiable transfer prediction."
    failed_checks: []
    flagged_checks: []
    quoted_evidence: []
    stage_3_watch_items: []
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ⚠*CONTROL*⚠ ENTRY 0005

## 1. CROSS-SILO SYSTEM DEFINITION
*   **Silo A (Field 1):** *Elastohydrodynamic lubrication (EHL) of rough-surface contacts* — thin viscous lubricant film flow in a converging-diverging contact, governed by the Reynolds lubrication equation coupled to elastic deformation of the contacting solids (film-thickness equation), with mixed boundary conditions where contact (film rupture/sealing) imposes nonlinear constraints.
*   **Silo B (Field 2):** *Semiconductor device transport numerics (drift-diffusion + Poisson with surface recombination and Schottky/contact regions)* — carrier transport described by coupled drift-diffusion equations for electron/hole densities, self-consistently coupled to Poisson's equation for electrostatic potential, with boundary/interface conditions modeling recombination, injection, and insulating/sealing regions.
*   **Mathematical Isomorphism:** Under the lubrication long-wave limit and standard nondimensionalizations, the Reynolds lubrication operator for pressure coupled to an elastic convolutional film-thickness relation is operator-equivalent to a nonlinear drift-diffusion operator for carrier fluxes coupled to Poisson potential via a linear elliptic Green's-kernel relation, and contact/sealing conditions map to Robin-like surface recombination/injection boundary conditions; this equivalence holds after identifying pressure ↔ electrochemical potential, film-thickness convolutional elasticity ↔ Poisson Green's-kernel potential response, and viscous flux divergence ↔ divergence of drift-diffusion current, provided both systems are expressed in the same parabolic-elliptic operator class and appropriate nondimensional groups (Reynolds number analog and Debye length ratio) are taken in the quasi-steady thin-film / quasi-neutral limits.

## 2. DIAGNOSTIC VOCABULARY MATRIX
*   **p(x,t) (lubrication pressure)** ↔ **\(\phi(x,t)\) (electrostatic / electrochemical potential)**  
    *   *Operator Role:* Both enter a second-order elliptic/parabolic divergence operator: pressure appears in the Reynolds operator \(\nabla\cdot\big(h^3\nabla p\big)\) (parabolic in time when film-thickness evolves) while potential enters drift term \(\nabla\cdot\big(\mu n \nabla \phi\big)\) inside continuity equations; both are scalar fields solved from divergence-form PDEs. Nondimensionalization: scale \(p\) by \(p_0\), \(\phi\) by thermal voltage \(V_T\) or characteristic potential \(\Phi_0\); identify mobility-like factor \(h^3\) ↔ carrier-mobility \(\mu n\).
*   **h(x,t) (film thickness; elastic convolution of p)** ↔ **\(\rho(x,t)\) or Green's-kernel potential response (Poisson convolution of charge density)**  
    *   *Operator Role:* In EHL, \(h = h_0 + \mathcal{K}*p\) where \(\mathcal{K}\) is an elastic kernel (Hertz/half-space kernel). In semiconductors, potential \(\phi\) satisfies \(-\nabla\cdot(\epsilon\nabla\phi)=q(n-p)+\rho_{fixed}\) with solution \(\phi=\mathcal{G}*(q(n-p)+\rho_{fixed})\). Both are linear elliptic convolutional couplings mapping a source (pressure or charge) to a field (deformation or potential).
*   **Sealing/contact region (h→0, cavitation) ↔ Schottky/insulating contact region (carrier-blocking or high recombination)**  
    *   *Operator Role:* Both impose mixed boundary constraints that switch operator regimes: in EHL cavitation imposes unilateral inequality \(p\ge0\) with free-boundary where \(p=0\) (film rupture), while in semiconductor contacts a surface recombination velocity or Schottky barrier imposes Robin-type flux conditions \(J\cdot n = S(\phi - \phi_{eq})\) that can effectively block current (analogous to sealing). The mapping requires explicit transformation of inequality constraints to high-rate Robin limits.

## 3. CORE MATHEMATICAL PARALLELISM
**Silo A (EHL) primary model (thin-film Reynolds + elastic coupling, quasi-steady film evolution):**

EHL lubrication for a Newtonian lubricant in thin-film approximation with time-dependent film thickness \(h(x,t)\) and pressure \(p(x,t)\) is commonly written (1D for clarity; extension to 2D is straightforward) as the Reynolds-type continuity for film mass (or pressure Poisson-like operator when steady):

```math
\frac{\partial h}{\partial t} + \frac{\partial}{\partial x}\left( -\frac{h^3}{12\eta}\frac{\partial p}{\partial x} + \frac{U h}{2} \right) = 0
```

where \(h(x,t)=h_0(x)+\int K(x-x')\,p(x',t)\,dx'\) encodes elastic deformation via kernel \(K\) (half-space or layered elasticity), \(\eta\) is viscosity, and \(U\) is entrainment speed. In steady or quasi-steady regimes the dominant operator is

```math
\frac{\partial}{\partial x}\left( h^3(x,t)\frac{\partial p}{\partial x} \right) = 12\eta \frac{\partial h}{\partial t} - 6\eta U \frac{\partial h}{\partial x}.
```

Contact/cavitation constraint:

```math
p(x,t) \ge 0,\quad p(x,t)=0\ \text{on cavitated regions},\quad \int_{contact} p\,dx = F_{\text{load}}.
```

**Silo B (Semiconductor drift-diffusion + Poisson):**

Carrier continuity for electrons (1D) coupled to Poisson:

```math
\frac{\partial n}{\partial t} + \frac{\partial J_n}{\partial x} = G - R(n,p),
```

with electron current

```math
J_n = -D_n\frac{\partial n}{\partial x} + \mu_n n \frac{\partial \phi}{\partial x},
```

and Poisson

```math
-\frac{\partial}{\partial x}\left(\epsilon\frac{\partial \phi}{\partial x}\right) = q(n-p)+\rho_{fixed}.
```

In quasi-neutral or drift-dominated thin-layer limits, combining continuity and current gives a divergence-form operator for the potential-like quantity (electrochemical potential) analogous to the Reynolds divergence operator.

**Bridging the operators (explicit correspondence and limits):**

1. **Operator form equivalence (Vector 1):** Compare the divergence-form flux in EHL \(\partial_x\big(h^3\partial_x p\big)\) with the divergence of drift flux \(\partial_x\big(\mu_n n \partial_x \phi\big)\). Under the identification
   - \(p \leftrightarrow \phi\) (pressure ↔ electrochemical potential),
   - \(h^3/(12\eta) \leftrightarrow \mu_n n\) (effective mobility-like prefactor),
   the principal second-order elliptic/parabolic operators coincide in divergence form:

```math
\partial_x\big( A(x,t)\,\partial_x \psi(x,t)\big),\quad A_{\text{EHL}}=h^3/(12\eta),\quad A_{\text{SC}}=\mu_n n.
```

2. **Convolutional coupling (Vector 2):** In EHL the film thickness depends linearly on pressure via an elastic kernel:

```math
h(x,t)=h_0(x)+\int K(x-x')\,p(x',t)\,dx'.
```

In semiconductor electrostatics, Poisson inversion yields potential as convolution with Green's function \(\mathcal{G}\):

```math
\phi(x,t)=\int \mathcal{G}(x-x')\big(q(n(x',t)-p(x',t))+\rho_{fixed}(x')\big)\,dx'.
```

Both are linear elliptic maps \( \text{source} \mapsto \text{field} \) with kernels \(K\) and \(\mathcal{G}\) that are symmetric, positive-definite (under standard elasticity and dielectric assumptions), and admit spectral representations. Thus the coupling is operator-equivalent: pressure→deformation kernel vs. charge→potential Green's kernel.

3. **Boundary / inequality mapping (Vector 3):** Cavitation/contact in EHL imposes unilateral constraint \(p\ge0\) with free boundary where \(p=0\). In semiconductor contacts, a high surface recombination velocity \(S\) or insulating barrier imposes a Robin boundary condition:

```math
J_n\cdot n = S\big(\phi - \phi_{eq}\big).
```

In the limit \(S\to\infty\) (strong recombination) or \(S\to0\) (blocking), the Robin condition approaches Dirichlet or Neumann extremes, which can be mapped to the EHL free-boundary by interpreting cavitation as a region where the effective mobility \(A(x,t)\) collapses (e.g., \(h\to0\Rightarrow A\to0\)), producing a switch in operator regime. Explicitly, the EHL unilateral constraint can be represented variationally (complementarity):

```math
p\ge0,\quad \mathcal{L}[p]\le f,\quad p(\mathcal{L}[p]-f)=0,
```

while semiconductor surface recombination can be written as a Robin operator \( \mathcal{B}[\phi]=S(\phi-\phi_{eq})\). The mapping is via the limit \(S\to0\) or \(S\to\infty\) and by treating regions with vanishing \(A\) as operator degeneracy analogous to cavitation.

**Dimensionless similarity parameter identification:** define nondimensional groups

```math
\text{EHL: }\Lambda = \frac{h_0}{L},\quad \Pi = \frac{p_0 L^2}{\eta U h_0^3}
```

```math
\text{SC: }\lambda_D/L,\quad \Gamma = \frac{\mu_n n_0 L^2}{D_n}
```

Quasi-neutral or thin-layer limits correspond to \(\lambda_D/L \ll 1\) (Poisson response fast) analogous to EHL steady-film limit \(\Pi\gg1\) where pressure field dominates film evolution; matching these limits yields the operator-class equivalence used above.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
*   **Preferred Transfer Direction:** *EHL/tribology → Semiconductor device numerics*
*   **Asymmetric Maturity Rationale:** The EHL/tribology community has developed robust numerical solvers for strongly nonlinear Reynolds-type divergence operators coupled to convolutional elastic kernels and unilateral contact constraints: specialized multigrid-preconditioned Newton-Krylov solvers, complementarity/variational inequality formulations for cavitation (e.g., penalty and active-set methods), and fast spectral convolution techniques for half-space elasticity kernels. Semiconductor device simulation has mature drift-diffusion solvers but typically treats Poisson–drift-diffusion coupling with different preconditioning strategies and often struggles with sharp free-boundary-like switching at metal-semiconductor interfaces, nanoscale insulating gaps, and mixed Robin/inequality conditions in emerging 2D-material heterostructures. The EHL toolkit is therefore asymmetric: it offers numerics tailored to divergence-form operators with degenerate mobility prefactors and free-boundary complementarity that are directly applicable to semiconductor problems with strong mobility collapse or insulating gaps.
*   **Target Bottleneck Mitigation:** Hypothesis: importing EHL active-set complementarity solvers and spectral elastic-kernel convolution accelerators into semiconductor drift-diffusion–Poisson solvers will reduce iteration counts and improve robustness when simulating devices with spatially localized mobility collapse (e.g., oxide pinholes, nanoscale vacuum gaps, or phase-change regions) and when enforcing mixed Robin/inequality contact models. Concretely, replacing standard Newton–Raphson linearization with an active-set Newton–Krylov preconditioned by a multigrid that respects the degenerate \(A(x)\) structure will halve the number of global nonlinear iterations on benchmark problems with sharp mobility contrasts.
*   **Falsifiable Prediction:** On a defined benchmark — a 2D semiconductor device with a nanoscale insulating gap region of width \(w=5\) nm embedded in a \(L=1\ \mu\)m device, with mobility collapse factor \(A_{\min}/A_{\max}=10^{-6}\), and with surface recombination velocity \(S\) varying between \(10^{-2}\) and \(10^{6}\ \text{m/s}\) — implement two solvers:
  - **Baseline:** standard drift-diffusion–Poisson Newton–Raphson with ILU-preconditioned GMRES (state-of-the-art baseline).
  - **Transferred:** EHL-inspired active-set Newton–Krylov with multigrid preconditioner and spectral convolution for Poisson inversion.
  
  **Prediction:** For \(A_{\min}/A_{\max}\le10^{-6}\) and \(S\ge10^{4}\ \text{m/s}\), the transferred solver will achieve convergence in **≤50%** of the nonlinear iterations and **≤60%** of wall-clock time compared to Baseline on the same mesh and tolerance \( \| \text{residual} \|_2 < 10^{-8}\). Observation that the transferred solver does not reduce nonlinear iterations by at least 30% or fails to converge more often than Baseline falsifies the hypothesis. All numeric thresholds derive from the operator degeneracy \(A\) and boundary parameter \(S\) defined above and the residual tolerance is consistent with the PDE norms shown in Section 3.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
*   `"Reynolds equation" AND "elastic kernel" AND "complementarity cavitation active set"`
*   `"drift-diffusion Poisson" AND "Robin boundary" AND "surface recombination velocity"`
*   `"lubrication h^3 gradient p" AND "drift diffusion mobility n gradient phi" AND "operator equivalence"`

---

## ADVERSARIAL REVIEWS (Stage 2)

### First Adversarial Review
**Reviewer:** Anthropic Claude Sonnet 5
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The Silo A steady-form equation "∂/∂x(h³∂p/∂x) = 12η∂h/∂t − 6ηU∂h/∂x" has a sign error relative to the preceding time-dependent equation "∂h/∂t + ∂/∂x(−h³/(12η)∂p/∂x + Uh/2) = 0" (expanding the latter correctly gives +6ηU∂h/∂x, not −6ηU∂h/∂x); the claimed nondimensional group "Π = p₀L²/(ηUh₀³)" carries units of m⁻² rather than being dimensionless; and the Poisson equation's mobile-charge term "q(n−p)" is sign-inverted relative to the drift-current convention used in the same section's Jₙ equation "Jₙ = −Dₙ∂n/∂x + μₙn∂φ/∂x" (holes carry +q and electrons −q, so the source term should read q(p−n)).
- **CHECK 2 (Vocabulary Matrix Coherence):** FLAG — In Section 2, the mapping header "h(x,t) (film thickness; elastic convolution of p) ↔ ρ(x,t) or Green's-kernel potential response (Poisson convolution of charge density)" ambiguously pairs the field-type quantity h with ρ, the source-type quantity that is actually charge density (the counterpart of pressure p, not of h); the accompanying Operator Role text correctly treats h and φ as the field-to-field pair, but the row header itself conflates φ and ρ.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed vectors are demonstrated with explicit equations: Vector 1 (lubrication_reynolds_operator_vs_drift_diffusion_operator) via the divergence-operator comparison in "Bridging the operators" point 1; Vector 2 (film_thickness_elastic_coupling_vs_poisson_potential_coupling) via the explicit convolution integrals in point 2; Vector 3 (contact_sealing_robin_like_boundary_vs_surface_recombination_robin_boundary) via the complementarity system and Robin operator in point 3.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction is argued with specific, non-generic solver detail (active-set Newton-Krylov and spectral elastic-kernel convolution vs. standard Newton-Raphson/ILU-GMRES) rather than reversible generic language, and the prediction names concrete measurable thresholds (≤50% nonlinear iterations, ≤60% wall-clock time, falsified below a 30% reduction or worse reliability than baseline); no specific canonical prior-art source is recognized for this exact domain pairing, though the broader free-boundary/variational-inequality literature connecting lubrication cavitation to other free-boundary problems is a related family worth Stage 3 attention.

#### Stage 3 Watch Items
- If this entry is revised and resubmitted, verify the corrected forms of the flagged equations: the entrainment-term sign in the Silo A divergence equation, the dimensional consistency of Π, and the mobile-charge sign in the Poisson equation.
- Confirm the intended h(x,t) vocabulary-matrix mapping is h↔φ (field-to-field) and p↔ρ (source-to-source); the current row header text conflates φ and ρ under a single mapping entry.
- No canonical source is recognized for the EHL↔semiconductor-transport pairing specifically, but the broader free-boundary/complementarity-problem (variational inequality) literature — which already connects lubrication cavitation to other free-boundary problems such as obstacle problems and American option pricing — is a related family; check whether a similar cross-domain solver-transfer argument already exists in the numerical-PDE or TCAD literature.
- The asymmetric-maturity claim (EHL active-set/complementarity solvers being more advanced than semiconductor TCAD for degenerate-coefficient free boundaries) is argued with specific technical detail but is not supported by citations in the entry; verify bibliometrically.

### Second Adversarial Review
**Reviewer:** Alibaba Qwen 3.8 Max
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — the entry gives `\frac{\partial h}{\partial t} + \frac{\partial}{\partial x}\left( -\frac{h^3}{12\eta}\frac{\partial p}{\partial x} + \frac{U h}{2} \right) = 0` but then gives `\frac{\partial}{\partial x}\left( h^3(x,t)\frac{\partial p}{\partial x} \right) = 12\eta \frac{\partial h}{\partial t} - 6\eta U \frac{\partial h}{\partial x}`; algebraically the first displayed equation implies a `+6\eta U \partial h/\partial x` term, so the entrainment sign is inconsistent.
- **CHECK 2 (Vocabulary Matrix Coherence):** FLAG — Section 2 maps `h(x,t) (film thickness; elastic convolution of p)` to `ρ(x,t) or Green's-kernel potential response (Poisson convolution of charge density)`, which conflates a film-thickness field with a charge-density/potential-response object and is not consistently aligned with Section 1's `p ↔ φ` and `h^3 ↔ μ n` identifications.
- **CHECK 3 (Correspondence Vector Support):** FAIL — Vectors 1 and 2 are presented with equations in Section 3 items 1 and 2, but Vector 3 (`contact_sealing_robin_like_boundary_vs_surface_recombination_robin_boundary`) is not demonstrated: Section 3 item 3 only states that the mapping is via limits and an analogous degenerate mobility, without deriving an EHL Robin-like condition or an operator identity from the EHL complementarity condition; because this vector is needed to reach three, fewer than three vectors are demonstrated.
- **CHECK 4 (Transfer and Falsifiability):** PASS — the EHL-to-semiconductor direction is argued with specific solver-toolkit asymmetry, and the benchmark prediction names measurable iteration-count/time thresholds and a falsification condition; no canonical textbook prior art is recognized from memory, but Stage 3 should probe related prior art.

#### Stage 3 Watch Items
- Verify whether the intended Reynolds wedge-term sign is convention-dependent or an algebraic error.
- Search for prior work connecting Reynolds lubrication operators, complementarity cavitation, and semiconductor drift-diffusion/Poisson contact models.
- Probe whether semiconductor device numerics already use active-set/variational-inequality or degenerate-mobility multigrid methods that would weaken the claimed asymmetry.
- Clarify whether `h` maps to carrier density, electrostatic potential, or charge density; the current source-field alignment is inconsistent.
- Reconcile the predicted ≤50% nonlinear-iteration count with the weaker ≥30% reduction falsification threshold.

### Third Adversarial Review
**Reviewer:** DeepSeek DeepSeek V4 Pro
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The displayed equation \(\frac{\partial}{\partial x}\left( h^3(x,t)\frac{\partial p}{\partial x} \right) = 12\eta \frac{\partial h}{\partial t} - 6\eta U \frac{\partial h}{\partial x}\) is algebraically inconsistent with the preceding continuity equation \(\frac{\partial h}{\partial t} + \frac{\partial}{\partial x}\left( -\frac{h^3}{12\eta}\frac{\partial p}{\partial x} + \frac{U h}{2} \right)=0\), which yields \(+6\eta U \frac{\partial h}{\partial x}\), not \(-6\eta U \frac{\partial h}{\partial x}\).
- **CHECK 2 (Vocabulary Matrix Coherence):** FLAG — The row \(h(x,t) \leftrightarrow \rho(x,t)\) or Green's-kernel potential response maps a response field to a source density in the first branch; the operator-role text and Section 3 later use \(h \leftrightarrow \phi\), so the matrix is ambiguous rather than category-definite.
- **CHECK 3 (Correspondence Vector Support):** FAIL — Vectors 1 and 2 are supported in Section 3 at the operator and convolutional-coupling levels, but the third vector `contact_sealing_robin_like_boundary_vs_surface_recombination_robin_boundary` is asserted by analogy rather than derived: the body states the Robin limit "can be mapped" to the EHL free-boundary by interpreting mobility collapse, with no operator identity connecting the complementarity condition to the Robin operator.
- **CHECK 4 (Transfer and Falsifiability):** FLAG — The transfer direction is plausibly asymmetric and the prediction is specific, but the success threshold (≤50% iterations) and falsification threshold (at least 30% reduction) create a 30–50% band where the numerical claim is false but not falsified by the stated criterion.

#### Stage 3 Watch Items
- Confirm whether the Reynolds/drift-diffusion operator analogy is already canonical in applied mathematics or semiconductor device numerics; the entry should be checked against textbooks/reviews before novelty is credited.
- Probe Vector 1: the drift-diffusion current contains \(-D_n \partial_x n\), but the displayed equivalence matches only the drift flux \(\mu_n n \partial_x \phi\). Stage 3 should determine whether this omitted diffusion term weakens the claimed isomorphism.
- Check the boundary/free-boundary mapping claim for prior art in variational inequality and Robin-limit reductions.

### Fourth Adversarial Review
**Reviewer:** Google Gemini 3.1 Pro
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The text presents a mathematical contradiction by mapping pressure \(p\) to potential \(\phi\) to align the divergence operators ("Under the identification... \(p \leftrightarrow \phi\)"), but subsequently maps pressure to charge to align the convolutions ("pressure→deformation kernel vs. charge→potential Green's kernel"), forcing \(p\) to be simultaneously treated as field and source. Additionally, it pairs a domain-wide free-boundary inequality ("\(p\ge0,\quad \mathcal{L}[p]\le f,\quad p(\mathcal{L}[p]-f)=0\)") with a linear fixed-boundary condition ("Robin operator \( \mathcal{B}[\phi]=S(\phi-\phi_{eq})\)"), which is a disqualifying equation-class mismatch.
- **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — The mapping "**h(x,t) (film thickness; elastic convolution of p)** ↔ **\(\rho(x,t)\) or Green's-kernel potential response (Poisson convolution of charge density)**" contains a category error. It conflates the source variable (\(\rho\), charge density) with the resulting field variable ("Green's-kernel potential response"), failing to establish a coherent, compatible mathematical type.
- **CHECK 3 (Correspondence Vector Support):** FAIL — The vector `contact_sealing_robin_like_boundary_vs_surface_recombination_robin_boundary` is listed but not demonstrated; Section 3 attempts to support it by mapping a variational inequality to a Robin condition, which establishes no shared mathematical structure. Vectors 1 and 2 are mutually contradictory.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction is asymmetric (proposing EHL complementarity solvers for SC numerics) and the prediction provides specific, falsifiable metrics (e.g., convergence in "≤50% of the nonlinear iterations").

#### Stage 3 Watch Items
- Verify whether applying EHL active-set complementarity solvers is actually appropriate for semiconductor drift-diffusion systems, given the lack of valid structural equivalence demonstrated here.

### Fifth Adversarial Review
**Reviewer:** Xiaomi MiMo V2.5 Pro
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** FLAG — The core Reynolds, drift-diffusion, and Poisson equations are correctly stated and belong to the same parabolic-elliptic coupled operator class. However, the rearranged Reynolds equation has a sign error on the Couette source term: the entry's first equation `∂h/∂t + ∂/∂x(−h³/(12η) ∂p/∂x + Uh/2) = 0` rearranges to `∂/∂x(h³ ∂p/∂x) = 12η ∂h/∂t + 6ηU ∂h/∂x` (plus sign), not the entry's stated `12η ∂h/∂t − 6ηU ∂h/∂x`. Additionally, both claimed dimensionless similarity parameters are dimensional: Π = p₀L²/(ηUh₀³) has dimensions of 1/m², and Γ = μ_n n₀L²/D_n has dimensions of 1/(V·m), despite being labeled as "nondimensional groups." Neither error affects the core divergence-form operator equivalence or the convolutional coupling claim, which remain mathematically valid.
- **CHECK 2 (Vocabulary Matrix Coherence):** FLAG — Mapping 1 identifies p ↔ φ (pressure ↔ electrochemical potential), but Mapping 2 uses an unresolved "or": h ↔ "ρ(x,t) or Green's-kernel potential response." The convolutional structure argued in Section 3 point 2 implies the natural field-level correspondence is p ↔ ρ (sources) and h ↔ φ (responses), which conflicts with Mapping 1. The operator-level claim — both systems feature a linear elliptic convolution mapping source to field via a symmetric positive-definite kernel — is mathematically sound, but the vocabulary matrix does not reconcile the two levels of correspondence. No category error from the prohibited list applies; both terms are scalar fields.
- **CHECK 3 (Correspondence Vector Support):** PASS — All three listed vectors are demonstrated with explicit equations in Section 3: (1) divergence-form operator ∂_x(A∂_xψ) equivalence with A_EHL = h³/(12η) and A_SC = μ_n n, (2) convolutional coupling h = h₀ + K*p versus φ = G*ρ with symmetric positive-definite kernels, and (3) cavitation complementarity (p ≥ 0, variational inequality) versus Robin surface recombination (J·n = S(φ−φ_eq)) linked through operator degeneracy limits.
- **CHECK 4 (Transfer and Falsifiability):** PASS — The transfer direction (EHL complementarity solvers → semiconductor device numerics) is genuinely asymmetric: EHL has mature active-set and penalty methods for degenerate divergence operators with unilateral constraints, while semiconductor solvers typically lack these tools for sharp mobility-collapse regions. The prediction is specific and falsifiable: on a defined 2D benchmark (w = 5 nm gap, A_min/A_max = 10⁻⁶, S varying 10⁻²–10⁶ m/s), the transferred solver should achieve ≤50% of baseline nonlinear iterations and ≤60% of wall-clock time, with falsification if iteration reduction is <30% or convergence fails more often than baseline. No canonical prior-art pairing recognized for this specific domain combination.

#### Stage 3 Watch Items
- Verify whether the EHL-complementarity-to-semiconductor-device-numerics pairing has appeared in published computational methods literature (operator preconditioning, numerical PDE transfer, degenerate-problem solvers).
- The sign error and dimensional errors are likely generation artifacts; the human reviewer should assess whether correcting them would alter the limit-matching argument that establishes the operator-class equivalence regime.
- The ambiguous h ↔ ρ/or-φ vocabulary mapping suggests the entry may benefit from restructuring the correspondence as a two-level mapping (transport-operator level vs. elliptic-coupling level) rather than a flat field-by-field table.

### Sixth Adversarial Review
**Reviewer:** Z.AI GLM-5.2
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** FAIL — The two displayed EHL equations are mutually inconsistent: the continuity form `∂h/∂t + ∂/∂x(-h³/(12η) ∂p/∂x + Uh/2) = 0` expands (U, η constant) to `∂_x(h³ ∂_x p) = 12η ∂_t h + 6ηU ∂_x h`, but the immediately following "steady or quasi-steady" form `∂/∂x(h³ ∂p/∂x) = 12η ∂h/∂t − 6ηU ∂h/∂x` writes the Couette/entrainment term with the opposite sign; under the entry's own single definition of U as entrainment speed both cannot hold, and the squeeze-vs-Couette relative sign is fixed (same-sign) by the standard continuity-plus-flux derivation, so the second equation is a wrong equation rather than a convention choice. A secondary FLAG on this check: the asserted "operator equivalence" treats `∂_x(μ_n n ∂_x φ)` as the principal operator for φ, when in the displayed drift-diffusion system it is a drift term inside the continuity equation for n; the principal operator for φ is the Poisson operator `∂_x(ε ∂_x φ)`, and the quasi-Fermi reformulation that would legitimize the identification is only named ("combining continuity and current gives a divergence-form operator for the potential-like quantity"), never displayed.
- **CHECK 2 (Vocabulary Matrix Coherence):** FLAG — The matrix pairing `p ↔ φ` (Section 2, mapping 1) conflicts with the convolutional parallel demonstrated in Vector 2, which pairs source↔source and field↔field: `h = h_0 + ∫K p` (source p → field h) parallels `φ = ∫G(q(n−p)+ρ_fixed)` (source charge → field φ), implying `p ↔ ρ` and `h ↔ φ`, not `p ↔ φ`; Section 2's hedged "h ↔ ρ or Green's-kernel potential response" reflects this unresolved role conflict. Both tokens are scalar fields (no type error), so this is a FLAG rather than a category-error FAIL.
- **CHECK 3 (Correspondence Vector Support):** PASS — Each listed vector has supporting body text: Vector 1 (lubrication_reynolds_operator_vs_drift_diffusion_operator) displays both divergence-form operators and an explicit A_EHL/A_SC identification (its operator-role defect is captured under Check 1); Vector 2 (film_thickness_elastic_coupling_vs_poisson_potential_coupling) displays `h = h_0 + ∫K p` and `φ = ∫G ρ`; Vector 3 (contact_sealing_robin_like_boundary_vs_surface_recombination_robin_boundary) displays both the EHL complementarity form `p≥0, L[p]≤f, p(L[p]−f)=0` and the semiconductor Robin condition `J_n·n = S(φ−φ_eq)`.
- **CHECK 4 (Transfer and Falsifiability):** PASS — Asymmetry is specific and defensible: the EHL community's active-set/complementarity and spectral-kernel-convolution machinery for degenerate-mobility divergence operators with free boundaries is a genuine specialty not standard in TCAD DD-Poisson preconditioning, and the named "less mature" target niche (mixed Robin/inequality contacts with mobility collapse in 2D-material heterostructures) is plausible; the direction is not backwards. Falsifiability is satisfied: Section 4 names a concrete benchmark (2D device, w = 5 nm gap, A_min/A_max = 10⁻⁶, S ∈ [10⁻², 10⁶] m/s), measurable outcomes (nonlinear iteration count ≤ 50%, wall-clock ≤ 60% of baseline at ‖residual‖₂ < 10⁻⁸), and a falsification threshold (no ≥ 30% iteration reduction or more frequent non-convergence). No canonical textbook prior-art pairing (à la Schrödinger↔paraxial optics or Black-Scholes↔heat) is recognized for this EHL↔DD-Poisson coupling; the convolutional-coupling observation is generic linear response, not a named analogy.

#### Stage 3 Watch Items
- Verify whether a Reynolds-lubrication ↔ semiconductor drift-diffusion/Poisson operator equivalence has been published in the tribology or TCAD literature; the elastic-kernel ↔ Poisson-Green's-function parallel is generic linear response and may not be novel.
- Probe whether the generating model intended the quasi-Fermi/electrochemical-potential reformulation (J_n = μ_n n ∇φ_n) for Vector 1; the displayed standard (n, φ) formulation does not itself establish the p↔φ operator identity.
- Confirm the sign convention of the Reynolds Couette/entrainment term against the entry's single definition of U as "entrainment speed"; the internal +6ηU vs −6ηU discrepancy must be resolved before re-submission.
- Check whether the claimed asymmetric transfer (EHL active-set/complementarity solvers → DD-Poisson with mobility collapse) has prior art in TCAD numerics for degenerate-mobility or 2D-material contact problems.
- Resolve the Section 2 vs Vector 2 role conflict: is the intended correspondence `p↔n, h↔φ` (primary unknown ↔ primary unknown, convolutional output ↔ convolutional output), which would make the convolutional parallel in Vector 2 internally consistent and contradict the Section 2 matrix?

### Seventh Adversarial Review
**Reviewer:** OpenAI GPT-5.6 Luna
**Protocol:** v2.0
**Verdict:** REJECT
**Review Date:** 2026-08-18

#### Results by Check
* **CHECK 1 (Equation Validity):** FAIL — Section 3 gives `\frac{\partial}{\partial x}\left( h^3(x,t)\frac{\partial p}{\partial x} \right) = 12\eta \frac{\partial h}{\partial t} - 6\eta U \frac{\partial h}{\partial x}`, but expanding the immediately preceding Reynolds continuity equation yields a **plus** sign for the (6\eta U,\partial_x h) term on the right-hand side.
* **CHECK 2 (Vocabulary Matrix Coherence):** FAIL — The Section 2 mapping `h(x,t) (film thickness; elastic convolution of p) ↔ \rho(x,t) or Green's-kernel potential response (Poisson convolution of charge density)` includes the category-error mapping (h\leftrightarrow\rho): h is a response/deformation field whereas (\rho) is the Poisson source charge density, and no transformation is stated to identify them.
* **CHECK 3 (Correspondence Vector Support):** PASS — Vector 1 is supported by the divergence-form operator comparison in Section 3, Vector 2 by the paired elastic-kernel and Poisson-Green-function equations, and Vector 3 by the cavitation/complementarity and Robin-boundary equations in Section 3.
* **CHECK 4 (Transfer and Falsifiability):** PASS — The stated transfer direction is explicitly EHL/tribology → semiconductor numerics, and the prediction specifies measurable iteration-count and wall-clock thresholds with explicit benchmark parameters and falsification criteria.

#### Stage 3 Watch Items
None identified.

### Eighth Adversarial Review
**Reviewer:** xAI Grok 4.5 Fast
**Protocol:** v2.0
**Verdict:** FLAG
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — The displayed Reynolds operator \(\partial_x(h^3\partial_x p)\) and the drift term \(\partial_x(\mu_n n\partial_x\phi)\) are both second-order divergence-form operators of matching elliptic/parabolic class under the stated identifications and quasi-steady limits; the elastic convolution and Poisson Green’s-kernel equations are both linear elliptic integral operators of the same type.
- **CHECK 2 (Vocabulary Matrix Coherence):** FLAG — The pairing “h(x,t) (film thickness; elastic convolution of p) ↔ ρ(x,t) or Green’s-kernel potential response (Poisson convolution of charge density)” mixes a geometric scalar field with a charge-density source / potential response; while the subsequent Operator Role text correctly identifies both as linear convolutional maps, the token-level objects are not of identical mathematical type.
- **CHECK 3 (Correspondence Vector Support):** FLAG — Vectors “lubrication_reynolds_operator_vs_drift_diffusion_operator” and “film_thickness_elastic_coupling_vs_poisson_potential_coupling” are fully demonstrated by explicit operator identities and kernel equations in Section 3; the third vector “contact_sealing_robin_like_boundary_vs_surface_recombination_robin_boundary” is only partially demonstrated—the body shows a unilateral free-boundary complementarity on one side and a Robin condition on the other, linked solely by informal S\to0/∞ limits and mobility collapse, without a shared variational or operator identity.
- **CHECK 4 (Transfer and Falsifiability):** PASS — Transfer direction is asymmetric (EHL free-boundary/complementarity and spectral-kernel tooling toward semiconductor mobility-collapse and mixed-contact problems); the prediction supplies concrete measurable thresholds (≤50 % nonlinear iterations, ≤60 % wall-clock time, residual <10^{-8}, specific A_min/A_max and S ranges) that can falsify the claim.

#### Stage 3 Watch Items
- Verify whether the unilateral free-boundary complementarity in EHL is rigorously equivalent (beyond heuristic limit) to Robin surface-recombination conditions under the stated S→0/∞ limits.
- Confirm that the h ↔ ρ/Green’s-kernel identification is intended as source-to-field map rather than direct field-to-field, given the explicit type mismatch in the matrix.

### Ninth Adversarial Review
**Reviewer:** Meta Muse Spark 1.1
**Protocol:** v2.0
**Verdict:** PASS
**Review Date:** 2026-08-18

#### Results by Check
- **CHECK 1 (Equation Validity):** PASS — Section 3 displays standard Reynolds equation ∂h/∂t + ∂x(-h^3/12η ∂x p + Uh/2)=0 with h=h0+K*p and standard drift-diffusion continuity ∂t n + ∂x Jn = G-R, Jn=-Dn∂x n + μn n ∂x φ, Poisson -∂x(ε∂x φ)=q(n-p)+ρ, both second-order divergence-form parabolic-elliptic with solution-dependent mobilities A_EHL=h^3/12η and A_SC=μn n, no class mismatch.
- **CHECK 2 (Vocabulary Matrix Coherence):** PASS — p(x,t)↔φ(x,t) both scalar fields in divergence operator ∇·(A∇ψ); h=K*p ↔ φ=G*(charge) both linear elliptic convolution maps with symmetric positive-definite kernels; sealing/contact region (h→0, p≥0 free boundary) ↔ Schottky/insulating contact region both mixed-regime boundary constraints, each Operator Role specifies shared structure (divergence form, kernel map, Robin/complementarity with degenerate A limit), not hedged analogy.
- **CHECK 3 (Correspondence Vector Support):** PASS — lubrication_reynolds_operator_vs_drift_diffusion_operator demonstrated in Section 3.1 via ∂x(A∂x ψ) identity; film_thickness_elastic_coupling_vs_poisson_potential_coupling demonstrated in Section 3.2 via h(x,t)=h0+∫K p and φ(x)=∫G(q(n-p)+ρ_fixed); contact_sealing_robin_like_boundary_vs_surface_recombination_robin_boundary demonstrated in Section 3.3 via p≥0 complementarity p(L-f)=0 and Robin J·n=S(φ-φ_eq) with S→∞/0 and A→0 degeneracy limit.[p]
- **CHECK 4 (Transfer and Falsifiability):** PASS — Asymmetry EHL→semiconductor justified by multigrid-preconditioned Newton-Krylov active-set complementarity and fast spectral convolution for degenerate A and free-boundary cavitation, claimed absent in drift-diffusion solvers for nanoscale insulating gaps; falsifiability provides specific benchmark (w=5nm, L=1μm, A_min/A_max=10^-6, S∈[10^-2,10^6] m/s, residual norm <1e-8) and thresholds (≤50% nonlinear iterations, ≤60% wall-clock, falsified if <30% reduction); no canonical textbook prior-art pairing recognized, advisory none.

#### Stage 3 Watch Items
- None identified. Bibliometric check should verify novelty of EHL complementarity solvers applied to semiconductor mobility-collapse and Robin/inequality contacts, but pairing is not a standard graduate-textbook analogy.