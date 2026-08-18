---
sid_metadata:
  entry_id: "CONTROL-SID-0003"
  schema_version: "2.0-control"
  maturity_stage: "candidate"
provenance:
  company: "Meta"
  model_family: "Muse"
  model_version: "Spark 1.1"
  generation_timestamp: "2026-08-17"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "autothermal-reactive-transport-in-porous-catalysts"
  domain_b: "nonlinear-optics"
  structural_family: "cusp_bifurcation_parabolic_activator_inhibitor_systems"
  triple_correspondence_vectors:
    - "shared_parabolic_activator_inhibitor_operator_pair"
    - "shared_cusp_catastrophe_S_shaped_steady_state_normal_form"
    - "shared_finite_wavenumber_modulational_instability_dispersion_threshold"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language / incompatible_ontologies / representation_mismatch_real_vs_complex_envelope / historically_isolated_communities"
prior_discovery_metrics:
  structural_isomorphism_score: 8.4
  vocabulary_divergence_score: 8.9
  expected_methodological_transfer_score: 8.3
  community_separation_score: 9.1
  representation_mismatch_score: 8.6
  expected_transfer_effort: "medium"
  novelty_prior:
    estimate: 8.1
    uncertainty: "±1.0"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "very_high"
  constitutive_equivalence_confidence: "medium"
  primary_failure_risk: "constitutive_law_mismatch"
  bibliometric_validation: "pending"
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ⚠*CONTROL*⚠ ENTRY 0003

## 1. CROSS-SILO SYSTEM DEFINITION
* **Silo A (Field 1):** Autothermal reactive transport in porous catalysts – transient formation of hotspots, ignition-extinction multiplicity and moving reaction fronts in a porous pellet where exothermic Arrhenius kinetics couples to heat and mass diffusion with Lewis number Le ≠1.
* **Silo B (Field 2):** Thermo-optic nonlinear cavity optics – transverse pattern formation and dissipative Kerr cavity soliton bistability in a high-Q microresonator where instantaneous Kerr self-focusing couples to slow thermal refractive-index shift.
* **Mathematical Isomorphism:** After nondimensionalization to slab/transverse geometry and transformation $(u,\theta)\leftrightarrow(I=|\psi|^2/I_0,\Theta=(dn/dT)T_{th}/n_2I_0)$ mapping two real scalars on $L^2(\Omega)$, both systems reduce to the same two-component parabolic activator-inhibitor operator $\partial_\tau U = D\nabla^2U+F(U;\mu)$ with $D=\mathrm{diag}(1,Le^{-1})$ vs $\mathrm{diag}(1,\Gamma^{-1})$, whose homogeneous nullcline is S-shaped with cusp catastrophe and whose linearization yields identical finite-$q$ modulational instability dispersion structure, equivalence holding up to constitutive difference $\exp(\theta)$ vs polynomial $|\psi|^2$ sharing same singularity class.

## 2. DIAGNOSTIC VOCABULARY MATRIX
* **fractional concentration $u=c/c_s$ ↔ normalized intracavity intensity $I=|\psi|^2/I_*$**
    * *Operator Role:* Real scalar activator field $u,I\in\mathbb{R}^+_0$ on $L^2(\Omega)$ entering parabolic operator $L_a=\partial_\tau -\nabla^2$ as $L_a u = -\phi^2 f(u,\theta)$ vs $L_a I = \mathrm{Re}[\psi^*\cdot (\partial_\tau\psi -i\nabla^2\psi)]$ after phase averaging. Complex-to-real mismatch reconciled by explicit transformation $I=|\psi|^2$, $I_*=1/(n_2 L_{cav})$ and restriction to stationary phase $\partial_\tau\arg\psi=0$.
* **Frank-Kamenetskii temperature $\theta = E_a(T-T_s)/R T_s^2$ ↔ thermo-optic detuning $\Theta=(dn/dT)T_{th}/(n_2 I_*)$**
    * *Operator Role:* Real scalar thermal inhibitor field $\theta,\Theta\in\mathbb{R}$ obeying $L_{th}=Le^{-1}\partial_\tau -\nabla^2 +Bi$ vs $\Gamma^{-1}\partial_\tau -\nabla_\perp^2 +\ell^{-2}$ with source $\propto$ activator $+\beta\phi^2 f$ vs $+\eta I$, both entering activator nullcline as $\exp(\theta/(1+\theta/\gamma))$ vs $(\theta_0-I-\Theta)$.
* **Thiele modulus squared $\phi^2=R_p^2k(T_s)/D_e$ ↔ normalized pump $F^2=|E_{in}|^2$**
    * *Operator Role:* Dimensionless bifurcation parameter $\mu$ scaling autocatalytic production in $\partial_\tau U = D\nabla^2U +\mu g(U)$ where $g_A=u\exp(\theta)$ vs $g_B=(1+\kappa_{th})I$, both appear as coefficient of nonlinear source in energy/Helmholtz balance.
* **Robin Biot number $Bi=hR_p/k_e$ ↔ cavity mirror coupling $\kappa = \mathcal{T}/2L$**
    * *Operator Role:* Coefficient in boundary operator $B(U)=\mathbf{n}\cdot\nabla U +Bi\,U=0$ on $\partial\Omega$ for heat/mass Danckwerts flux vs impedance-mismatched mirror $ \mathbf{n}\cdot\nabla_\perp\psi + (\kappa+i\delta)\psi=0$, same Sturm-Liouville type with $Bi,\kappa\in\mathbb{R}^+$.

## 3. CORE MATHEMATICAL PARALLELISM

Silo A models a porous catalyst slab/cylinder with coupled mass and energy balances. Transient nondimensional form for infinite slab $\xi=r/R_p\in$, $\tau=tD_e/R_p^2$, Lewis number $Le=\alpha/D_e$, Prater $\beta=(-\Delta H)D_ec_s\gamma/(k_eT_s)$, $\gamma=E_a/RT_s$:[0][1]

```math
\varepsilon_c\frac{\partial u}{\partial\tau}= \nabla^2 u -\phi^2 u \exp\left(\frac{\theta}{1+\theta/\gamma}\right)
\]
```math
\frac{1}{Le}\frac{\partial\theta}{\partial\tau}= \nabla^2\theta +\beta\phi^2 u \exp\left(\frac{\theta}{1+\theta/\gamma}\right) -Bi\,\theta|_{\partial\Omega}
\]
```math
B_A(u,\theta): \mathbf{n}\cdot\nabla u + Bi_m u =0,\; \mathbf{n}\cdot\nabla\theta + Bi_h\theta =0 \;\text{on }\partial\Omega
```

with $\phi^2$ Thiele modulus. This is a two-component parabolic reaction-diffusion system with exponential Arrhenius nonlinearity, elliptic steady limit.

Silo B models a driven Kerr cavity with thermal refraction, transverse version of Lugiato-Lefever with heat (Chembo & Menyuk PRA 2013; Yu et al. Optica 2021), recognizable to nonlinear optics. Complex envelope $\psi$, real thermal shift $\Theta$, photon lifetime $\tau_{ph}$, thermal time $\tau_{th}$, $\Gamma=\tau_{ph}/\tau_{th}\ll1$, diffraction length $a$, pump detuning $\theta_0$, pump $F$:

```math
\frac{\partial\psi}{\partial\tau}=-(1+i\theta_0)\psi + i\nabla_\perp^2\psi + i\left(|\psi|^2+\Theta\right)\psi +F
\]
```math
\frac{1}{\Gamma}\frac{\partial\Theta}{\partial\tau}= \nabla_\perp^2\Theta -\ell^{-2}\Theta +\eta |\psi|^2
\]
```math
B_B(\psi,\Theta): \mathbf{n}\cdot\nabla_\perp\psi +\kappa\psi =0,\; \mathbf{n}\cdot\nabla_\perp\Theta +Bi_{th}\Theta=0
```

After splitting $\psi=\sqrt{I}e^{i\phi}$ and adiabatically eliminating $\phi$ for stationary patterns, $(I,\Theta)$ obeys same structure as $(u,\theta)$ with $D_B=\mathrm{diag}(a, \Gamma^{-1})$ and polynomial nonlinearity $i|\psi|^2\psi$. Variable identification $U_A=[u,\theta]^T\leftrightarrow U_B=[I,\Theta]^T$ via $I=|\psi|^2$, $\Theta=(dn/dT)T_{th}/(n_2I_*)$, $Le^{-1}\leftrightarrow\Gamma^{-1}$, $\beta\phi^2\leftrightarrow\eta$, $Bi\leftrightarrow\ell^{-2}$.

Correspondence 1 – shared parabolic activator-inhibitor operator – demonstrated above: both are $\partial_\tau U = D\nabla^2U+F(U)$ with $D$ diagonal positive, $F$ nonlinear autocatalytic, class parabolic nonlinear.

Correspondence 2 – shared cusp catastrophe S-shaped steady state. Homogeneous $\nabla^2=0$, $\partial_\tau=0$ nullclines:

Silo A: Frank-Kamenetskii balance with external loss coefficient $S_h$, $u_s\approx1$ for diffusion-limited exterior:

```math
G_A(\theta_s)=\delta \exp\left(\frac{\theta_s}{1+\theta_s/\gamma}\right)-S_h\theta_s =0,\quad \delta\equiv\beta\phi^2
\]
```math
\frac{dG_A}{d\theta_s}=0,\; \frac{d^2G_A}{d\theta_s^2}=0 \;\Rightarrow\; \text{cusp at }\delta_c\approx3.32\text{ (slab)},\; \theta_{s,c}=1
```

Silo B: Homogeneous LLE + thermal steady $\Theta_s=\kappa_{th}I_s$, $\kappa_{th}=\eta\ell^2$:

```math
F^2 = I_s\left[1+(\theta_0-(1+\kappa_{th})I_s)^2\right]\equiv H_B(I_s)
\]
```math
G_B(I_s)=H_B(I_s)-F^2=0,\; \frac{dG_B}{dI_s}=0,\; \frac{d^2G_B}{dI_s^2}=0 \Rightarrow \text{cusp at }\theta_{0,c}=\sqrt{3}(1+\kappa_{th}),\; I_{s,c}=\frac{2\theta_{0,c}}{3(1+\kappa_{th})^2}
```

Both $G_{A,B}=0$ are cubic-equivalent S-shaped hysteresis with cusp normal form $x^3+ax+b=0$, Taylor expansion of exponential $\exp(\theta)\approx1+\theta+\theta^2/2+\theta^3/6$ yields same singularity class.

Correspondence 3 – finite-wavenumber modulational/filamentation instability. Linearize $U=U_s+\hat{U}e^{\lambda\tau+iq\cdot x}$:

Silo A dispersion Jacobian $J_A=\partial F_A/\partial U|_{s}$:

```math
\det\left(J_A - q^2 D_A -\lambda I_2\right)=0,\quad J_A=\phi^2 e^{\theta_s}\begin{pmatrix}-1 & -\frac{u_s}{(1+\theta_s/\gamma)^2}\\ \beta & \frac{\beta u_s}{(1+\theta_s/\gamma)^2}\end{pmatrix}-\begin{pmatrix}0&0\\0&Bi\end{pmatrix}
\]
```math
\lambda_{A\pm}(q)=\frac{1}{2}\left(\mathrm{tr}M_q \pm\sqrt{\mathrm{tr}M_q^2-4\det M_q}\right),\; M_q=J_A-q^2D_A,\; Re\lambda_{A+}>0 \text{ for } q_c^2\approx \beta\phi^2 e^{\theta_s}/2
```

Silo B Bogoliubov + thermal:

```math
\lambda_{B\pm}(q)=-1\pm\sqrt{I_s^2-\left(\theta_0-2I_s-\Theta_s-q^2\right)^2}-\frac{\Gamma\eta q^2}{q^2+\ell^{-2}}
\]
```math
Re\lambda_{B+}(q)>0 \iff I_s>1 \text{ and } |q-q_c|\approx0,\; q_c^2=\theta_0-2I_s-\Theta_s
```

Both exhibit $\lambda(q)$ with maximum at $q_c\neq0$ giving hotspot filamentation vs optical filamentation, threshold $I_s>1$ maps to Frank-Kamenetskii $\delta>\delta_{fil}$.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
* **Preferred Transfer Direction:** autothermal-reactive-transport-in-porous-catalysts → nonlinear-optics
* **Asymmetric Maturity Rationale:** Porous catalyst community possesses 40-year mature singularity-theoretic continuation toolkit: pseudo-arclength Keller continuation with adaptive mesh, detection of isola/mushroom/hysteresis loops, isola variety unfolding, and large Le stiffness handling via LOCA/AUTO97, specifically for exponential Arrhenius coupled to Robin boundaries. Nonlinear optics community, while mature at pure LLE Newton shooting and split-step propagation for Kerr combs, lacks robust automated isola tracking for two-time-scale $\Gamma\sim10^{-3}$ thermo-optic LLE where thermal branch causes disconnected isolas missed by forward detuning scans.
* **Target Bottleneck Mitigation:** Importing Balakotaiah-Luss singularity classification and LOCA's bordered augmented Jacobian isola-continuation algorithm into pyLLE/LLEtools will systematically track disconnected steady-state branches of thermo-optic cavity solitons as $\phi^2\leftrightarrow F^2$ varies, resolving operational bottleneck where thermal nonlinearity is treated as perturbative drift and isolated high-power soliton branches are overlooked in microresonator stability maps.
* **Falsifiable Prediction:** For a Si3N4 microring $FSR=100$ GHz, $Q=1.2\times10^6$, $\tau_{ph}=1.2$ ns, $\tau_{th}=0.6\mu s$ ($\Gamma=0.002$, $\ell=1.5$, $\eta=0.8$, $\kappa_{th}=0.35$), at fixed pump $F^2=4.5$ (200 mW in waveguide), catalyst-derived continuation predicts an isolated closed loop (isola) of single dissipative Kerr soliton solutions at normalized detuning $\theta_0\in[4.2,4.8]$ with intracavity temperature rise $\Delta T=19\pm3$ K, intracavity power $I_{isola}=1.18\pm0.05\times I_{main}$, comb transmitted power $P_{comb}=+17\pm2$% above main-branch soliton at same $\theta_0$, separated from main S-branch by unstable gap $\Delta\theta_{gap}>0.30$ measured in cold-cavity linewidths. Baseline for comparison is standard LLEtools single-parameter Newton continuation without thermal history, which predicts continuous branch with no isola and <2% power variation. Falsification: systematic slow forward/backward detuning scans at 0.2 kHz rate over $\theta_0\in[0,6]$ on three nominally identical rings showing no isolated branch within $\pm0.5$ in $\theta_0$ of prediction with power contrast >10%, and bordered continuation refinement to tolerance $10^{-8}$ shows isola diameter shrinking to <0.01 in $F^2$-$\theta_0$ plane for all $\eta\in[0.4,1.2]$, merging with main branch.

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
* `"Frank-Kamenetskii parameter" AND "Thiele modulus" AND "isola" AND "porous catalyst"`
* `"Lugiato Lefever" AND "thermal" AND "bistability" AND "isola" AND "microresonator"`
* `"autothermal reactor" AND "optical bistability" AND "cusp catastrophe" AND "thermo-optic"`
* `"thermal LLE" AND "Balakotaiah singularity" AND "pseudo arclength continuation" AND "cavity soliton" AND NOT "Schrödinger paraxial"`