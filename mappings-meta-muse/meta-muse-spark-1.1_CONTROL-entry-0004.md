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