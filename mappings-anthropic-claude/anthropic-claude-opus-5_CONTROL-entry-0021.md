---
sid_metadata:
  entry_id: "CONTROL-SID-0021"
  schema_version: "2.0-control"
  maturity_stage: "candidate"
provenance:
  company: "Anthropic"
  model_family: "Claude"
  model_version: "Opus 5"
  generation_timestamp: "2026-08-17"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "single-pass-free-electron-laser-physics"
  domain_b: "closed-cyclic-queueing-network-theory"
  structural_family: "periodic-transport-with-constant-torque-trapping-and-conserved-population"
  triple_correspondence_vectors:
    - "periodic_divergence_form_transport_operator_with_conserved_zero_mode"
    - "constant_torque_pendulum_separatrix_and_shared_adiabaticity_criterion"
    - "moving_bucket_retention_factor_and_its_shared_variational_optimum"
    - "bounded_concave_cycle_flux_ceiling"
    - "phase_normalization_gauge_group_with_gauge_invariant_flux_observable"
discovery_rationale:
  why_not_obvious: "incompatible_ontologies / distinct_disciplinary_language / historically_isolated_communities / the_shared_object_appears_only_after_a_density_dependent_scaling_limit_on_one_side_and_a_co_moving_frame_reduction_on_the_other"
prior_discovery_metrics:
  # NOTE: All scores below are model-generated self-assessments produced at generation time.
  # They reflect the generating model's internal pattern-matching confidence, not externally
  # validated measurements. They should be used as triage-ranking signals for human reviewers
  # deciding which entries to prioritize for Stage 3 bibliometric validation — not as evidence
  # that the isomorphism is real or novel.
  structural_isomorphism_score: 8.1
  vocabulary_divergence_score: 9.2
  expected_methodological_transfer_score: 7.4
  community_separation_score: 9.0
  representation_mismatch_score: 8.6
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 7.0
    uncertainty: "±1.6"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "overdamped_relaxation_collapses_the_second_order_bucket_to_first_order_adler_phase_locking_voiding_the_retention_factor"
  bibliometric_validation: "pending"
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ⚠*CONTROL*⚠ ENTRY 0021

## 1. CROSS-SILO SYSTEM DEFINITION

*   **Silo A (Field 1):** Single-pass high-gain FEL physics, post-saturation **tapered-undulator energy extraction** — electrons trapped in a ponderomotive bucket whose resonant phase is held fixed by a longitudinally varying undulator parameter $K(z)$, with efficiency limited by progressive detrapping as the bucket shrinks.
*   **Silo B (Field 2):** Closed cyclic queueing network theory, **capacity-profile scheduling on a CONWIP loop** — $N$ jobs circulating over $M$ stations under a fixed total service-capacity budget, where a spatially non-uniform, *traveling* capacity profile locks a fraction of the job population to itself and pumps it around the loop faster than the uniform-capacity drift.
*   **Mathematical Isomorphism:** After the density-dependent (Kurtz) scaling and the $M\to\infty$ continuum limit, both systems are divergence-form transport processes on $S^1$ with a conserved zero mode, whose characteristics in the frame co-moving with a prescribed traveling drive obey the *same* constant-torque pendulum $\ddot\psi=-\Omega^2(\sin\psi-s)$ — hence the same separatrix and trapping condition $|s|\le 1$, the same adiabaticity criterion $|\dot\Omega|\ll\Omega^2$, the same moving-bucket retention factor $\alpha(s)=(1-s)/(1+s)$ and therefore the same variational optimum $s^\star=\sqrt2-1$ for the extracted product $s\,\alpha(s)$, the same bounded-concave cycle-flux ceiling, and the same one-parameter phase/normalization gauge group with a gauge-invariant flux observable; the correspondence holds **only** for a prescribed, adiabatically slowly varying drive amplitude and **only** in the underdamped regime $\Omega\tau\gg1$, and it does **not** extend to SASE start-up, where the FEL drive is dynamical and self-consistent while the queueing capacity profile remains exogenous.

## 2. DIAGNOSTIC VOCABULARY MATRIX

*   **Ponderomotive phase $\psi$** ↔ **Co-moving loop phase $\psi=2\pi(x-vt)+\tfrac{\pi}{2}$**
    *   *Operator Role:* Both are the angle coordinate of the divergence-form transport operator $\partial_t+\partial_\psi(\,\cdot\,u)$ on $S^1$, and both are the argument of the constant-torque pendulum of §3. Type on both sides: real, dimensionless, $\psi\in\mathbb{R}/2\pi\mathbb{Z}$. Type bridge: Silo A's $\psi$ is intrinsically continuous; Silo B's is a *station index* $i\in\mathbb{Z}/M\mathbb{Z}$ made continuous by the Kurtz scaling $x=i/M\in S^1$ displayed in §3, then boosted into the frame of the traveling capacity wave, $\xi=x-vt$.
*   **Bunching factor $b=\langle e^{-i\psi}\rangle$** ↔ **First loop harmonic $\hat q_1=\oint q(x,t)\,e^{-2\pi i x}dx$**
    *   *Operator Role:* Both are the $k=1$ Fourier coefficient of a normalized density on $S^1$, i.e. the order parameter conjugate to the drive in each system's flux integral. Type on both sides: complex scalar with $|b|,|\hat q_1|\le 1$ after normalization by the zero mode. Type bridge: under $\psi=2\pi x+\pi/2$ and $q\mapsto q/\!\oint q$, the two definitions coincide symbol-for-symbol; modulus is the imbalance amplitude, argument is the angular location of the cluster.
*   **Scaled energy deviation $p=(\gamma-\gamma_r)/(\rho\gamma_r)$** ↔ **Normalized job slip rate $\hat p=\dot\psi/\Omega$**
    *   *Operator Role:* Both are the momentum conjugate to $\psi$ in the pendulum Hamiltonian $H=\tfrac12\hat p^2-\cos\psi-s\psi$ and the drift velocity in the transport operator, $u=\partial H/\partial \hat p$. Type on both sides: real, dimensionless. Type bridge: Silo A's $p$ is already dimensionless through division by the Pierce parameter $\rho$; Silo B's $\dot\psi$ carries units of inverse time and is nondimensionalized by the trapped-mode frequency $\Omega=\sqrt{2\pi\bar\mu\hat c\cos\psi_r/\tau}$ derived in §3.
*   **Resonant phase $\psi_r$ / taper rate $\sin\psi_r$** ↔ **Normalized wave-speed mismatch $s=(v-\bar\mu)/(\bar\mu\hat c)$**
    *   *Operator Role:* Both are the constant-torque coefficient in $\ddot\psi=-\Omega^2(\sin\psi-s)$, i.e. the single parameter that fixes the separatrix topology and the retention factor $\alpha$. Type on both sides: real, dimensionless, confined to $[-1,1]$ for a bucket to exist. Type bridge: Silo A's is already dimensionless ($\sin$ of an angle); Silo B's is a velocity ratio, nondimensionalized by the product of the mean service rate $\bar\mu$ and the relative capacity-modulation amplitude $\hat c$.
*   **Undulator taper $dK/dz$** ↔ **Capacity-wave speed $v$**
    *   *Operator Role:* Both are the externally imposed control that translates the operating point along the propagation coordinate, i.e. the parameter whose *position dependence* breaks the one-parameter gauge group of §3 and thereby converts a gauge freedom into an actuator. Type on both sides: real. Type bridge: $dK/dz$ has units $\mathrm{m}^{-1}$ and enters only through the dimensionless combination $\sin\psi_r$ via the resonance condition; $v$ has units of loop-fractions per unit time and enters only through $s$.
*   **Radiation phase $\arg A$** ↔ **Visit-ratio normalization $\alpha_{\rm gauge}$ in $r\mapsto\alpha_{\rm gauge}r$**
    *   *Operator Role:* Both parameterize a one-parameter group acting freely on the state description while leaving every measurable flux invariant; the physical observables $|A|$ and $X_i=r_iG(N-1)/G(N)$ are precisely the gauge-invariant combinations. Type on both sides: real parameter of a $U(1)$-like (respectively $\mathbb{R}_{>0}$) group action; the two groups are non-isomorphic as groups, so the correspondence claimed is at the level of *free action with a gauge-invariant flux*, not group isomorphism.
*   **Saturation power $P_{\rm sat}\simeq\rho P_{\rm beam}$** ↔ **Throughput ceiling $X_\infty=\min_i \mu_i/r_i$**
    *   *Operator Role:* Both are the value at which a bounded concave flux function on the cycle attains its maximum, i.e. $\sup$ of the constitutive flux law that closes the transport operator. Type on both sides: real, units of power / jobs per unit time; both become dimensionless after division by the corresponding uncoupled ceiling ($P_{\rm beam}$, $\bar\mu$), giving the efficiency $\eta$ and the utilization respectively.

## 3. CORE MATHEMATICAL PARALLELISM

**Silo A.** The 1-D high-gain FEL is modeled by the Bonifacio–Pellegrini–Narducci system in the universal scaling $\bar z = 2k_w\rho z$, with $\rho$ the Pierce parameter and $A$ the scaled complex radiation envelope:

```math
\rho=\left[\frac{1}{16}\,\frac{K^{2}[JJ]^{2}}{\gamma_r^{3}}\,\frac{\omega_p^{2}}{c^{2}k_w^{2}}\right]^{1/3},
\qquad
\frac{d\psi_j}{d\bar z}=p_j,\quad
\frac{dp_j}{d\bar z}=-\!\left(Ae^{i\psi_j}+{\rm c.c.}\right),\quad
\frac{dA}{d\bar z}=\big\langle e^{-i\psi}\big\rangle\equiv b .
```

Its kinetic form is a Vlasov equation on the phase cylinder $S^1\times\mathbb R$, and integrating over $p$ gives a divergence-form continuity equation in $\psi$ with the electron number as the conserved zero mode:

```math
\partial_{\bar z} f + p\,\partial_\psi f-\big(Ae^{i\psi}+{\rm c.c.}\big)\partial_p f=0
\;\;\Longrightarrow\;\;
\partial_{\bar z} n+\partial_\psi\!\big(n\,u\big)=0,\qquad
\frac{d}{d\bar z}\oint_{S^1} n\,d\psi=0 .
```

The system also carries the exact drive/reservoir invariant, obtained directly from the three equations above:

```math
\frac{d}{d\bar z}\Big(|A|^{2}+\langle p\rangle\Big)
=\Big(A^{*}\langle e^{-i\psi}\rangle+A\langle e^{i\psi}\rangle\Big)
-\Big(A\langle e^{i\psi}\rangle+A^{*}\langle e^{-i\psi}\rangle\Big)=0 .
```

**Silo B.** A closed cyclic queueing network of $M$ stations and $N$ jobs is a finite closed migration process with generator

```math
(\mathcal A f)(\mathbf n)=\sum_{i=1}^{M}\mu_i(n_i)\big[f(\mathbf n-\mathbf e_i+\mathbf e_{i+1})-f(\mathbf n)\big],
\qquad \sum_i n_i=N,\quad i\in\mathbb Z/M\mathbb Z,
```

whose stationary law is Gordon–Newell product form,
$\pi(\mathbf n)=G(N)^{-1}\prod_i x_i^{\,n_i}/\beta_i(n_i)$ with $x_i=r_i/\mu_i$, $\mathbf r=\mathbf r P$.
Under the density-dependent (Kurtz) scaling $n_i=Mq_i$, $\mu_i(n)=M\mu_i\phi(n/M)$, the CTMC converges to the fluid model on the station ring, and a Taylor expansion in the lattice spacing $1/M$ supplies the explicit scale bridge to a continuum operator ($x=i/M$, $\tilde t=\mu t/M$):

```math
\dot q_i=\mu\big[\phi(q_{i-1})-\phi(q_i)\big]
\;\;\xrightarrow[\;M\to\infty\;]{\;q_i=q(i/M)\;}\;\;
\partial_{\tilde t}q+\partial_x\phi(q)=\frac{1}{2M}\,\partial_x^{2}\phi(q)+O(M^{-2}),
\qquad
\frac{d}{d\tilde t}\oint_{S^1}q\,dx=0 .
```

**Vector 1 — periodic divergence-form transport operator with conserved zero mode.** The two boxed transport equations are the same operator: first-order advection in divergence form on $S^1$ with periodic closure, so the constant function is a null direction and the total population is rigidly conserved ($\oint n\,d\psi$ and $\oint q\,dx = N/M$). On Silo A the conservation is Liouville's theorem; on Silo B it is the telescoping of the cyclic flux $\sum_i[\phi(q_{i-1})-\phi(q_i)]=0$, i.e. cut-independence of the loop flow. Linearizing the Silo B operator about $\bar q$ with $q=\bar q+\epsilon e^{2\pi ikx+\lambda\tilde t}$ gives the ring spectrum

```math
\lambda(k)=-2\pi i k\,\phi'(\bar q)-\frac{(2\pi k)^{2}}{2M}\phi'(\bar q),
\qquad
\gamma_1\equiv|\mathrm{Re}\,\lambda(1)|_{t}=\frac{2\pi^{2}\mu\,\phi'(\bar q)}{M^{2}},
\qquad
T_{\rm relax}=\frac{M^{2}}{2\pi^{2}\mu\,\phi'(\bar q)} .
```

**Vector 2 — constant-torque pendulum separatrix and shared adiabaticity criterion.** Write $A=|A|e^{i\varphi_A}$ and absorb $\varphi_A$ into $\psi$. With a taper that holds the resonance condition $\lambda_r=(\lambda_w/2\gamma_r^{2})(1+K^{2}/2)$ satisfied while the resonant electron decelerates,

```math
\frac{2}{\gamma_r}\frac{d\gamma_r}{dz}=\frac{d}{dz}\ln\!\Big(1+\frac{K^{2}}{2}\Big),
\qquad
\frac{d\gamma_r}{dz}=-\frac{eK[JJ]E_0}{2\gamma_r mc^{2}}\sin\psi_r ,
```

the trapped-electron dynamics reduce to the pendulum with constant torque

```math
\boxed{\;\frac{d^{2}\psi}{d\bar z^{2}}=-\,\omega_s^{2}\big(\sin\psi-\sin\psi_r\big)\;},
\qquad \omega_s^{2}=2|A|\cos\psi_r .
```

On the Silo B side, take a closed loop with finite buffers, for which the fluid model is the standard relaxation (second-order production-flow) system rather than the kinematic-wave limit: job speed relaxes to the local equilibrium speed $U$ with time constant $\tau$, $\ddot x=\tau^{-1}[U(x,t)-\dot x]$. Impose the traveling capacity profile of fixed budget $\oint\mu\,dx=\bar\mu$,

```math
\mu(x,t)=\bar\mu\big[1+\hat c\cos\!\big(2\pi(x-vt)\big)\big],
```

and pass to the co-moving frame $\xi=x-vt$, $\psi=2\pi\xi+\pi/2$:

```math
\boxed{\;\frac{d^{2}\psi}{dt^{2}}+\frac{1}{\tau}\frac{d\psi}{dt}=-\,\Omega^{2}\big(\sin\psi-s\big)\;},
\qquad
\Omega^{2}=\frac{2\pi\bar\mu\hat c\,\cos\psi_r}{\tau},
\qquad
s=\frac{v-\bar\mu}{\bar\mu\,\hat c} .
```

The two boxed equations are the same operator under $(\bar z\leftrightarrow t,\;\omega_s\leftrightarrow\Omega,\;\sin\psi_r\leftrightarrow s)$, **up to the dissipative term $\tau^{-1}\dot\psi$, which has no FEL counterpart.** The correspondence is therefore restricted to the underdamped regime $\Omega\tau=\sqrt{2\pi\bar\mu\hat c\,\tau\cos\psi_r}\gg1$, i.e. $\tau\gg(2\pi\bar\mu\hat c)^{-1}$; outside it the bucket degenerates to first-order Adler locking and everything below fails. Both sides then share the same separatrix, existing iff

```math
|\sin\psi_r|\le 1 \quad\Longleftrightarrow\quad |s|\le1
\quad\Longleftrightarrow\quad \bar\mu(1-\hat c)\le v\le\bar\mu(1+\hat c),
```

and, because in each case the control parameters are ramped along the propagation coordinate, both admit the identical adiabatic-invariance condition on the trapped action $J=\oint \hat p\,d\psi$:

```math
\left|\frac{1}{\omega_s^{2}}\frac{d\omega_s}{d\bar z}\right|\ll1
\qquad\text{and}\qquad
\left|\frac{1}{\Omega^{2}}\frac{d\Omega}{dt}\right|\ll1 .
```

**Vector 3 — moving-bucket retention factor and its shared variational optimum.** For the constant-torque pendulum the bucket area, and hence the trapped fraction $f_t$, is the separatrix action

```math
J(\psi_r)=\oint_{\rm sep}\hat p\,d\psi
=\sqrt2\!\!\int_{\psi_1}^{\psi_2}\!\!\Big[\cos\psi-\cos\psi_2+(\psi-\psi_2)\sin\psi_r\Big]^{1/2}d\psi
\;\simeq\;J(0)\,\alpha(\psi_r),
```

```math
\alpha(s)=\frac{1-s}{1+s},\qquad s=\sin\psi_r\ \ (\text{Silo A}),\qquad s=\frac{v-\bar\mu}{\bar\mu\hat c}\ \ (\text{Silo B}).
```

Because $J$ depends on the torque only through $s$, the *same* function governs both. The quantity each field wants to maximize is the product of retained population and per-unit transport rate. In Silo A the extraction efficiency over a fixed undulator length is $\eta\propto f_t\times|\Delta\gamma_r/\gamma_r|\propto \alpha(s)\,s$. In Silo B the wave-pumped flux is $\Delta X=f_t\,(v-\bar\mu)=\bar\mu\hat c\,\alpha(s)\,s$. Maximizing the common objective:

```math
\frac{d}{ds}\left[\frac{s(1-s)}{1+s}\right]=\frac{1-2s-s^{2}}{(1+s)^{2}}=0
\;\Longrightarrow\;
s^{\star}=\sqrt2-1\approx0.4142,
\qquad
\big[s\,\alpha(s)\big]_{\max}=3-2\sqrt2\approx0.1716 .
```

Silo A reading: $\psi_r^\star\approx24.5^\circ$, consistent with the empirically favored $20^\circ\!-\!40^\circ$ taper window. Silo B reading: $v^{\star}=\bar\mu\big[1+\hat c(\sqrt2-1)\big]$ and $\Delta X_{\max}=(3-2\sqrt2)\,\bar\mu\hat c$.

**Vector 4 — bounded concave cycle-flux ceiling.** The transport operator is closed on each side by a bounded concave constitutive flux, and the cycle ceiling is the minimum of that flux around the loop. Silo A: $|b|=|\langle e^{-i\psi}\rangle|\le1$ with equality only for a delta-bunched beam, so with $|A|^{2}+\langle p\rangle$ conserved and $p$ bounded by the bucket half-height $\Delta p=2\sqrt{2|A|}$,

```math
\frac{d|A|^{2}}{d\bar z}=2\,{\rm Re}\big(A^{*}b\big)\le2|A|,
\qquad
|A|_{\rm sat}=O(1)\;\Longrightarrow\;\eta_{\rm sat}\simeq\rho,\quad P_{\rm sat}\simeq\rho\,P_{\rm beam},
\quad L_g=\frac{\lambda_w}{4\pi\sqrt3\,\rho}.
```

Silo B: for FCFS single-server stations $\phi(q)=\min(q,1)$, concave and bounded, so

```math
X(N)=\frac{G(N-1)}{G(N)}\ \xrightarrow[N\to\infty]{}\ X_\infty=\min_i\frac{\mu_i}{r_i},
\qquad
\partial_{\mu_j}X_\infty=\frac{1}{r_j}\,\mathbf 1\!\left\{\frac{\mu_j}{r_j}=\min_i\frac{\mu_i}{r_i}\right\}.
```

Both are the statement that a bounded concave flux on a closed cycle caps transport at $\min$ over the cycle, with a subgradient that collapses to zero once the local operating point leaves the binding set — the shared diminishing-returns law behind both detrapping and bottleneck migration. *Where it stops:* the FEL flux $|b(|A|)|$ rises and then **falls** past saturation (phase-space overshoot), whereas $\min(q,1)$ is monotone-then-flat; the correspondence covers the ascending and binding branches only.

**Vector 5 — phase/normalization gauge group with gauge-invariant flux observable.** The FEL system admits the exact free action

```math
\psi\mapsto\psi+\psi_0,\quad A\mapsto Ae^{-i\psi_0}
\;\Longrightarrow\;\text{equations invariant},\quad |A|\ \text{invariant},\ \arg A\ \text{pure gauge}.
```

The Gordon–Newell system admits the exact free action generated by the non-uniqueness of $\mathbf r=\mathbf r P$:

```math
r_i\mapsto\alpha_{\rm gauge}r_i\;\Rightarrow\;x_i\mapsto\alpha_{\rm gauge}x_i,\quad
G(N)\mapsto\alpha_{\rm gauge}^{N}G(N),\quad
\pi(\mathbf n)\ \text{invariant},\quad
X_i=r_i\frac{G(N-1)}{G(N)}\ \text{invariant}.
```

In both, the group acts freely on the representation, the physical flux is the invariant, and the *control primitive is obtained by making the group parameter depend on the propagation coordinate*: $\psi_0\to\nu\bar z$ maps the resonant FEL equations onto the detuned ones (verified by substituting $p\to p+\nu$, $\psi\to\psi+\nu\bar z$, $A\to Ae^{-i\nu\bar z}$, which reproduces $dA/d\bar z-i\nu A=b$), and $\alpha_{\rm gauge}\to\alpha_{\rm gauge}(x,t)$ is exactly the traveling capacity profile $\mu(x,t)$ above. The two groups are $U(1)$ and $\mathbb R_{>0}$ and are not isomorphic; what is shared is the free action with a gauge-invariant flux and the *breaking-as-actuation* construction.

**Where the whole correspondence stops.** In the FEL, $A$ is a dynamical variable satisfying $dA/d\bar z=b$, so drive and reservoir exchange a conserved quantity; the SASE start-up regime, the cubic dispersion relation $(\mu-\delta)^{2}\mu=1$, and the shot-noise initial condition have **no counterpart** in the exogenously scheduled capacity profile and are explicitly excluded. Everything above is stated in the KMR regime, where $|A|$ is treated as prescribed and adiabatically slowly varying.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS

*   **Preferred Transfer Direction:** Single-pass FEL physics (tapered-undulator theory) → Closed cyclic queueing network theory (capacity scheduling)

*   **Asymmetric Maturity Rationale:** For this exact operator class — a constant-torque pendulum whose torque is a designed function of the propagation coordinate, with a shrinking adiabatic invariant — the FEL community has forty years of dedicated apparatus: Kroll–Morton–Rosenbluth resonant-phase taper theory; adiabatic-invariant-preserving taper laws; explicit trapped-fraction accounting; prebunching and pre-taper sections engineered to raise $f_t$ before the torque is applied; particle-in-cell solvers (GENESIS, GINGER, PUFFIN) with the taper profile in the optimization loop; adjoint and evolutionary taper-profile optimization; and direct experimental measurement of the $(\,\text{taper rate},f_t,\eta\,)$ triple at LCLS, FLASH, SACLA and the European XFEL. Closed cyclic queueing theory is *strongly* mature at a different set of problems: exact steady-state product-form analysis (Gordon–Newell, BCMP), Buzen convolution and Mean Value Analysis, saddle-point asymptotics of normalizing constants, heavy-traffic and fluid limit theorems, infinitesimal perturbation analysis and likelihood-ratio gradient estimation, and convex-programming **static** capacity allocation under a budget — for which it needs nothing from physics. The narrow missing capability is different from all of these: it is the treatment of a **deliberately non-stationary, spatially traveling capacity profile as a design primitive**, together with the invariant-based accounting that goes with it. The nonstationary-queueing toolkit (pointwise stationary approximation, modified offered load, SIPP) consists of *approximations for a given exogenous modulation*; none of them supplies a trapping condition, an adiabatic invariant, a retention factor, or an optimal modulation speed, and the regime where the modulation timescale is comparable to the loop's own relaxation time is the acknowledged weak point of exactly those methods.

*   **Target Bottleneck Mitigation:** Hypothesis — the persistent bottleneck-migration problem in closed cyclic networks (every static reallocation of a fixed capacity budget merely relocates the binding constraint, per the subgradient collapse in Vector 4) is not a limit of allocation but a limit of *stationarity*. Importing KMR taper design predicts that a traveling capacity profile of zero mean, moving at $v$ inside the trapping window $\bar\mu(1\pm\hat c)$, phase-locks a fraction $\alpha(s)$ of the job population and pumps it, yielding a throughput channel unavailable to any static allocation at the same budget, with the optimal schedule fixed analytically at $s^\star=\sqrt2-1$ rather than found by simulation search. The FEL trapped-fraction/pre-bunching apparatus transfers directly as a prescription for *pre-clustering* the loop population before the wave is switched on.

*   **Falsifiable Prediction:** Benchmark: a closed cyclic CONWIP loop, $M=32$ stations, $N=16$ jobs ($\bar q=0.5$), FCFS single-server stations with $\bar\mu=1$, finite buffers giving relaxation constant $\tau=5$ (so $\Omega\tau\approx2.9>1$, underdamped condition satisfied), total capacity budget held fixed at $\oint\mu\,dx=\bar\mu$, modulation amplitude $\hat c=0.3$; calibration timescale $T_{\rm relax}=M^{2}/(2\pi^{2}\mu\phi')=1024/2\pi^{2}\approx51.9$ from Vector 1. Measured quantity: time-averaged loop throughput $\bar X(v)$ at a designated reference station, by discrete-event simulation. Baseline: the static balanced Gordon–Newell/MVA allocation $\mu_i\propto r_i$ at the same budget, which is the state of the art for closed-network capacity assignment. Predictions: (i) $\bar X(v)/\bar X_{\rm static}-1$ attains its maximum at $v^{\star}/\bar\mu=1+\hat c(\sqrt2-1)=1.124$; (ii) the peak relative gain equals $(3-2\sqrt2)\hat c=0.0515$, i.e. $5.15\%$, to within the untrapped back-reaction, and must exceed $0.05\hat c=1.5\%$; (iii) **no gain whatever** for $v/\bar\mu\notin[1-\hat c,1+\hat c]=[0.7,1.3]$, since no bucket exists there — in particular the static non-uniform profile $v=0$ gives $|s|=1/\hat c=3.3>1$ and must show zero gain. Falsified if the argmax lies outside $v/\bar\mu\in[1+0.35\hat c,\,1+0.48\hat c]=[1.105,1.144]$; or if peak gain $<1.5\%$; or if statistically significant gain appears outside the trapping window; or if the gain fails to vanish as $\tau$ is reduced below $(2\pi\bar\mu\hat c)^{-1}\approx0.53$, where the pendulum becomes overdamped and $\alpha(s)$ must be replaced by the Adler locking range.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION

*   `"resonant phase" AND "Kroll-Morton-Rosenbluth" AND "trapped fraction" AND "tapered undulator" AND "bucket area"`
*   `"closed cyclic queueing network" AND ("Gordon-Newell" OR "CONWIP") AND "time-varying service capacity" AND ("traveling wave" OR "moving bottleneck")`
*   `("free-electron laser" OR "tapered undulator") AND ("closed queueing network" OR "Gordon-Newell" OR "CONWIP" OR "mean value analysis")`  ← deliberate novelty-falsification string: a hit here retires the entry
*   `"moving bucket" AND "(1 - sin psi_s)/(1 + sin psi_s)" AND ("production line" OR "supply chain" OR "job shop")`
*   `"adiabatic invariant" AND "phase locking" AND "capacity modulation" AND "closed loop production" NOT "traffic flow"`