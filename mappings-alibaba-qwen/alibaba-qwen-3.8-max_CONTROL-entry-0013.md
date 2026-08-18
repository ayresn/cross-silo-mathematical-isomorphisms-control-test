---
sid_metadata:
  entry_id: "CONTROL-SID-0013"
  schema_version: "2.0-control"
  maturity_stage: "candidate"
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