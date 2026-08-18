---
sid_metadata:
  entry_id: "CONTROL-SID-0015"
  schema_version: "2.0-control"
  maturity_stage: "candidate"
provenance:
  company: "DeepSeek"
  model_family: "DeepSeek"
  model_version: "V4 Pro"
  generation_timestamp: "2026-08-17"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "nematic-liquid-crystal-director-dynamics"
  domain_b: "neural-field-pattern-formation"
  structural_family: "nonconvex-gradient-flow-pattern-formation"
  triple_correspondence_vectors:
    - "shared_nonconvex_lyapunov_gradient_descent"
    - "shared_typeI_finite_wavenumber_bifurcation_threshold"
    - "shared_boundary_quantized_mode_spectrum"
discovery_rationale:
  why_not_obvious: "incompatible_ontologies_and_distinct_disciplinary_language"
prior_discovery_metrics:
  structural_isomorphism_score: 8.2
  vocabulary_divergence_score: 9.1
  expected_methodological_transfer_score: 7.8
  community_separation_score: 9.4
  representation_mismatch_score: 7.5
  expected_transfer_effort: "high"
  novelty_prior:
    estimate: 8.4
    uncertainty: "±1.0"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "constitutive_law_mismatch_between_nonlocal_synaptic_kernel_and_local_nematic_elasticity"
  bibliometric_validation: "pending"
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ⚠*CONTROL*⚠ ENTRY 0015

## 1. CROSS-SILO SYSTEM DEFINITION
*   **Silo A (Field 1):** Quasi-two-dimensional nematic liquid-crystal director relaxation in the one-constant Frank-Oseen limit, driven by an external electric field and exhibiting the Fréedericksz transition and director pattern formation.
*   **Silo B (Field 2):** Amari-type neural field pattern formation on a homogeneous periodic domain, exhibiting Turing-like pattern selection through nonlocal excitatory/inhibitory synaptic coupling.
*   **Mathematical Isomorphism:** Both are nonconvex dissipative gradient flows (`shared_nonconvex_lyapunov_gradient_descent`) whose boundary-quantized linear spectra undergo a finite-wavenumber instability when a dimensionless control parameter crosses zero (`shared_typeI_finite_wavenumber_bifurcation_threshold`); the explicit long-wavelength continuum limit of the neural synaptic integral operator produces the same second-order spatial operator family as the nematic Laplacian, providing the required scale bridge.

## 2. DIAGNOSTIC VOCABULARY MATRIX
*   θ(x,t) ↔ u(x,t)
    *   *Operator Role:* Scalar order-parameter fields. θ is the planar director angle obtained from the unit-vector director n=(cosθ,sinθ) after restriction to a single plane; u is the dimensionless neural activity field. Both appear as the argument of a nonconvex free-energy/Lyapunov functional and both are real scalar fields in the restricted models used here.
*   Frank-Oseen free energy F[θ] ↔ neural Lyapunov functional L[u]
    *   *Operator Role:* Nonconvex functionals whose first variation supplies the dissipative driving force: γ∂_tθ=−δF/δθ versus τ∂_tu=−(1/f′(u))δL/δu. Both are non-increasing along dynamics.
*   electric-field dimensionless control Π_A ↔ synaptic-gain dimensionless control Π_B
    *   *Operator Role:* Scalar bifurcation parameters defined by Π_A=ε0ΔεE²d²/(Kπ²)−1 and Π_B=f′(u0)max_k \hat w(k)−1. Both cross zero at the pattern-onset threshold.
*   strong-anchoring boundary modes nπ/d ↔ periodic Fourier modes 2πm/L
    *   *Operator Role:* Discrete spectral mode labels in the linearized operator. Dirichlet anchoring selects nπ/d; periodic neural-field boundary conditions select 2πm/L.

## 3. CORE MATHEMATICAL PARALLELISM

In a planar nematic cell of thickness d with strong planar anchoring, let θ(x,t) be the director angle. The one-constant Frank-Oseen free energy with an electric field along x is

```math
F[\theta]=\int_0^d\left[\frac{K}{2}(\partial_x\theta)^2-\frac{\epsilon_0\Delta\epsilon E^2}{2}\sin^2\theta\right]dx
```

Overdamped Ericksen-Leslie relaxation is

```math
\gamma\frac{\partial\theta}{\partial t}=-\frac{\delta F}{\delta\theta}
=K\partial_x^2\theta+\epsilon_0\Delta\epsilon E^2\sin\theta\cos\theta
```

with θ(0)=θ(d)=0. Linearizing around θ=0 gives

```math
\gamma\frac{\partial\theta}{\partial t}
=K\partial_x^2\theta+\epsilon_0\Delta\epsilon E^2\theta
```

The discrete modes are

```math
\theta_n(x,t)=a_n(t)\sin(k_nx),\quad k_n=\frac{n\pi}{d}
```

```math
\gamma\dot a_n=[\epsilon_0\Delta\epsilon E^2-Kk_n^2]a_n
```

The threshold is

```math
E_c^2=\frac{K}{\epsilon_0\Delta\epsilon}\left(\frac{\pi}{d}\right)^2
```

and the dimensionless control parameter is

```math
\Pi_A=\frac{\epsilon_0\Delta\epsilon E^2 d^2}{K\pi^2}-1
```

On the neural-field side, the Amari equation on a periodic domain x∈[-L,L] is

```math
\tau\frac{\partial u(x,t)}{\partial t}=-u(x,t)+\int_{-L}^{L}w(x-y)f(u(y,t))dy+I
```

with even kernel w and sigmoid f, f′>0. For symmetric w the Lyapunov functional is

```math
L[u]=-\frac12\iint w(x-y)f(u(x))f(u(y))\,dx\,dy+\int \Phi(u(x))\,dx
```

```math
\Phi'(u)=u f'(u)
```

Then

```math
\frac{\delta L}{\delta u}=f'(u)[u-w*f]
```

```math
\tau\frac{\partial u}{\partial t}=-\frac{1}{f'(u)}\frac{\delta L}{\delta u}
```

so dL/dt≤0. The homogeneous state u0 satisfies u0=W0 f(u0)+I, W0=∫w. Linearizing with u=u0+εv e^{λt+ikx} gives

```math
\tau\lambda(k)=-1+f'(u_0)\hat w(k)
```

where \hat w(k)=∫w(r)e^{-ikr}dr. Discrete periodic modes k_m=2πm/L give

```math
u(x,t)=\sum_m \hat u_m(t)e^{ik_m x}
```

```math
\tau\dot{\hat u}_m=[-1+f'(u_0)\hat w(k_m)]\hat u_m
```

The threshold is

```math
f'(u_0)\max_k\hat w(k)=1
```

and the dimensionless control parameter is

```math
\Pi_B=f'(u_0)\max_k\hat w(k)-1
```

The boundary-quantized spectra are termwise corresponding:

```math
k_n^{(A)}=\frac{n\pi}{d}
\quad\leftrightarrow\quad
k_m^{(B)}=\frac{2\pi m}{L}
```

and the linearized growth laws are scalar:

```math
\gamma \lambda_n^{(A)}=\epsilon_0\Delta\epsilon E^2-K(k_n^{(A)})^2
```

```math
\tau \lambda_m^{(B)}=-1+f'(u_0)\hat w(k_m^{(B)})
```

Thus both instabilities set in when the first discrete mode crosses zero.

Because the neural operator is nonlocal while the nematic operator is local, an explicit scale bridge is required. For short-range kernels,

```math
\int w(x-y)f(u(y))dy
=W_0 f(u)+\frac{W_2}{2}\partial_x^2 f(u)+O(\partial_x^4)
```

```math
W_0=\int w(r)dr,\quad W_2=\int r^2 w(r)dr
```

Linearizing f about u0 gives

```math
\tau\partial_t v =(\mu W_0-1)v+\frac{\mu W_2}{2}\partial_x^2 v,\quad \mu=f'(u_0)
```

which is the same second-order operator family as the nematic linearization:

```math
\partial_t\theta=\frac{K}{\gamma}\partial_x^2\theta+\frac{\epsilon_0\Delta\epsilon E^2}{\gamma}\theta
```

with coefficient map

```math
\frac{K}{\gamma}\leftrightarrow\frac{\mu W_2}{2\tau},\qquad
\frac{\epsilon_0\Delta\epsilon E^2}{\gamma}\leftrightarrow\frac{\mu W_0-1}{\tau}
```

This bridge is valid only in the low-wavenumber continuum limit and does not assert exact equality of the full nonlocal neural operator and the local nematic operator.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
*   **Preferred Transfer Direction:** nematic-liquid-crystal-director-dynamics → neural-field-pattern-formation
*   **Asymmetric Maturity Rationale:** The nematic community has mature, energy-stable discretizations for nonconvex Frank-Oseen and Landau-de Gennes gradient flows (convex splitting, scalar auxiliary variable methods, deflated continuation for multiple stationary states). The neural-field community has strong analytical methods for bump construction and linear Turing analysis, but its standard numerical toolkit for Amari equations is dominated by explicit Euler or fixed-point iteration, which does not preserve the nonlocal Lyapunov functional and imposes step-size restrictions. Energy-stable discretizations for symmetric-kernel Amari gradient flows are not a standard neural-field tool.
*   **Target Bottleneck Mitigation:** Transfer the nematic convex-splitting recipe to the neural Lyapunov functional L[u]. Split L into convex and concave parts in the firing-rate variable v=f(u), treat the convex part implicitly and the concave part explicitly. This yields an unconditionally gradient-stable time integrator for symmetric-kernel Amari fields, eliminating spurious pattern drift and allowing timesteps far beyond the explicit stability limit.
*   **Falsifiable Prediction:** For a one-dimensional Amari field on x∈[-20,20] with periodic boundaries, zero input I=0, kernel

```math
w(x)=2g(x;1)-g(x;2),\qquad
g(x;\sigma)=\frac{1}{\sqrt{2\pi\sigma^2}}e^{-x^2/(2\sigma^2)}
```

and sigmoid f(u)=1/(1+e^{-4u}), the homogeneous state has f′(0)=1 and the most unstable Fourier mode has

```math
k_c^2=\frac{2}{3}\ln2,\qquad
\hat w(k_c)=2^{2/3}-2^{-4/3}\approx1.1906
```

so τλ(k_c)=0.1906>0. The imported energy-stable scheme with timestep Δt=10τ must keep the discrete Lyapunov functional L_h non-increasing to within 10^{-12} over 1000 steps. The baseline explicit Euler scheme at the same timestep has amplification factor

```math
1+10\tau\lambda(k_c)=2.906
```

for the most unstable mode and therefore diverges or violates L_h monotonicity by more than 0.1. Falsification: if the energy-stable scheme's L_h increases by more than 10^{-12} in any step, or if explicit Euler remains bounded and monotone at Δt=10τ, the transfer hypothesis is rejected.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
*   `"Ericksen-Leslie" AND "Fréedericksz transition" AND "energy-stable" AND "gradient flow"`
*   `"Amari neural field" AND "Lyapunov functional" AND "Turing instability" AND "nonlocal"`
*   `"nematic liquid crystal" AND "neural field" AND "gradient flow" AND "finite-wavenumber instability"`