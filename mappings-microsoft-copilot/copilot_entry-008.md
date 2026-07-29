---
sid_metadata:
  entry_id: "SID-008"
  schema_version: "1.0-production"
  maturity_stage: "candidate"
provenance:
  company: "Microsoft"
  model_family: "Copilot"
  model_version: "1.2"
  generation_timestamp: "2026-07-28"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "information-cascade-fronts-on-complex-networks"
  domain_b: "variational-phase-field-fracture"
  structural_family: "free-boundary-fronts-via-gradient-flows"
  triple_correspondence_vectors:
    - "governing_differential_operator"
    - "instability_mechanism"
    - "variational_principle_and_numerical_solution_family"
discovery_rationale:
  why_not_obvious: "distinct_disciplinary_language; discrete_stochastic_graph_ontology vs continuum_variational_tensor_ontology; fracture community emphasizes energy minimization and adaptive FEM while network science emphasizes stochastic thresholds and percolation, hiding operator-level equivalence."
prior_discovery_metrics:
  structural_isomorphism_score: 8.1
  vocabulary_divergence_score: 8.7
  expected_methodological_transfer_score: 8.9
  community_separation_score: 7.8
  representation_mismatch_score: 9.2
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
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ENTRY SID-008

## 1. CROSS-SILO SYSTEM DEFINITION
*   **Silo A (Field 1):** *Information cascade fronts on complex networks* — the spatio-temporal propagation of adoption/infection states across heterogeneous graphs, often modeled by threshold, contagion, or reaction–diffusion-like dynamics producing sharp advancing fronts across communities.
*   **Silo B (Field 2):** *Variational phase-field fracture* — the evolution of a scalar phase-field \(\phi(\mathbf{x},t)\in[0,1]\) that regularizes sharp crack surfaces via an energy-driven gradient flow coupling elastic fields and a fracture-surface energy, producing propagating crack fronts and nucleation events.
*   **Mathematical Isomorphism:** The propagation and nucleation of **cascade fronts** on graphs and **crack fronts** in phase-field fracture are both governed by **energy-gradient-flow dynamics** with a Laplace-type operator (graph Laplacian ↔ continuum Laplacian), a nucleation/pinning instability controlled by a local toughness/threshold field, and numerically treated by energy-stable implicit schemes and adaptive spatial refinement — satisfying the Triple-Correspondence Rule via (1) governing differential operator, (2) instability mechanism (nucleation/pinning/Griffith-like criterion), and (3) variational principle plus numerical solution family (energy functional + gradient-flow solvers / adaptive FEM ↔ energy-like Lyapunov function + graph-based implicit solvers).

## 2. DIAGNOSTIC VOCABULARY MATRIX
*   **Phase-field \(\phi(\mathbf{x},t)\)** ↔ **Node adoption field \(u_i(t)\) or smoothed adoption field \(u(\mathbf{x},t)\)**
    *   *Operator Role:* Both are scalar order parameters whose gradients (continuum) or graph-differences (discrete) enter the energy/interaction term; mathematically they are the primary field minimized by a gradient flow: \(\partial_t \phi \propto -\delta E/\delta \phi\) ↔ \(\dot u \propto -\nabla_u \mathcal{E}(u)\) where \(\nabla_u\) uses the graph Laplacian.
*   **Elastic energy density \(W(\varepsilon(\mathbf{u}),\phi)\)** ↔ **network influence potential \(I(u,\mathcal{A})\) (peer-pressure / exposure)**
    *   *Operator Role:* Both act as *driving* bulk terms that bias the order parameter toward the broken/adopted state; mathematically they appear as local potentials in the variational derivative and couple multiplicatively to the order parameter (degradation function \(g(\phi)\) ↔ susceptibility function \(s(u)\)).
*   **Fracture surface energy \(\int \frac{G_c}{c_w}\left(\frac{w(\phi)}{\ell} + \ell|\nabla\phi|^2\right)\,dx\)** ↔ **interface-penalty / regularization \(\sum_{(i,j)}\frac{\kappa}{2}(u_i-u_j)^2 + \sum_i \frac{\alpha}{\ell}w(u_i)\)**
    *   *Operator Role:* Both penalize sharp interfaces and set a lengthscale \(\ell\) controlling front thickness; mathematically they provide the gradient-penalty (continuum) or edge-difference penalty (graph) that regularizes the front and determines pinning and propagation thresholds.

## 3. CORE MATHEMATICAL PARALLELISM
**Silo A (Information cascade fronts on networks):** Many network cascade models can be written as gradient flows of an energy-like functional on the graph (continuous-time limit of threshold/contagion dynamics with inertia or recovery). A convenient continuum-like representation for a smoothed adoption field \(u(\mathbf{x},t)\) on a spatially embedded network or on the graph via graph Laplacian \(\mathcal{L}\) is:
```math
\partial_t u = -M(u)\left( \mathcal{L} u + \frac{1}{\ell} w'(u) - S(\mathbf{x}) \right)
```
where \(\mathcal{L}\) is the graph Laplacian (or continuum Laplacian for spatial embeddings), \(M(u)\) is a mobility/susceptibility, \(w(u)\) is a double-well potential with minima at non-adopt/adopt states, \(\ell\) is an interface width, and \(S(\mathbf{x})\) is a local source/threshold field (external influence or node-specific resistance). This is the gradient flow of a graph-energy
```math
\mathcal{E}_{graph}[u] = \frac{1}{2}\sum_{i,j} A_{ij}(u_i-u_j)^2 + \sum_i \frac{1}{\ell} w(u_i) - \sum_i S_i u_i.
```

**Silo B (Variational phase-field fracture):** The standard phase-field fracture gradient-flow (viscous regularization of energy minimization) couples elasticity and a phase-field \(\phi\):
```math
\partial_t \phi = -\eta^{-1}\left( -G_c\left(\frac{w'(\phi)}{\ell} - 2\ell\Delta\phi\right) + g'(\phi)\psi^+(\varepsilon) \right)
```
with total energy
```math
\mathcal{E}_{PF}[\mathbf{u},\phi] = \int \left( g(\phi)\psi^+(\varepsilon(\mathbf{u})) + \psi^-(\varepsilon(\mathbf{u})) \right)\,dx + \int \frac{G_c}{c_w}\left(\frac{w(\phi)}{\ell} + \ell|\nabla\phi|^2\right)\,dx.
```
**Latent-space mapping:** Replace continuum Laplacian \(\Delta\) by graph Laplacian \(\mathcal{L}\), elastic driving energy \(g'(\phi)\psi^+\) by network influence potential \(I'(u)\), and fracture toughness \(G_c\) by a *social toughness* field \(T_i\) (node-level resistance). Under this mapping the cascade front is the graph-regularized phase-field front; nucleation/pinning criteria map to Griffith-like inequalities where local energy release rate (network exposure) must exceed local toughness (threshold) for front advance.

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
*   **Preferred Transfer Direction:** **Variational Phase-Field Fracture** → **Information Cascade Fronts on Complex Networks**
*   **Asymmetric Maturity Rationale:** The phase-field fracture community has highly developed **variational formulations**, **energy-stable implicit time integrators**, **adaptive mesh refinement (AMR)** and **a posteriori error estimators** for front localization and crack nucleation; these tools are mature, industrial-grade, and routinely handle sharp moving interfaces and heterogeneous toughness fields. In contrast, network cascade modeling lacks a standardized variational framework, energy-stable implicit solvers on graphs, and adaptive spatial refinement strategies for front localization across heterogeneous community structure.
*   **Target Bottleneck Mitigation:** **Hypothesis (testable):** Implementing a phase-field-inspired variational energy on graphs, solved with energy-stable implicit integrators and graph-adaptive refinement, will (a) enable stable simulation of near-threshold cascade fronts in networks with strong community heterogeneity, and (b) accurately predict front pinning and arrest phenomena that current threshold/percolation models systematically mis-predict. Concretely, replacing explicit threshold updates with an implicit gradient-flow solver of \(\mathcal{E}_{graph}[u]\) will reduce spurious cascade nucleation and produce convergent front velocities under mesh/graph coarsening.
*   **Falsifiable Prediction:** Define **social toughness** \(T_i\) and **network energy release rate** \(G_{net}\) computed from local exposure. The phase-field mapping predicts a Griffith-like criterion for front advance on graphs:
```math
\text{Advance at edge }(i,j)\ \Longleftrightarrow\ G_{net}^{(i,j)} \ge T_{(i,j)}.
```
Empirical prediction 1: For synthetic modular networks with controlled inter-community edge density \(\rho_{inter}\), the critical global adoption pressure \(S_c\) required to sustain a propagating front scales as
```math
S_c - S_0 \propto \sqrt{\ell\, T_{eff}} \cdot f(\rho_{inter})
```
where \(T_{eff}\) is the mean social toughness and \(f(\rho_{inter})\) is a measurable monotone function; this square-root scaling (analogous to Griffith scaling with interface width \(\ell\)) is **distinct** from classical percolation thresholds and thus falsifiable by simulation/empirical cascade experiments. Empirical prediction 2: Adaptive graph refinement guided by an a posteriori energy residual will reduce the error in predicted front position by a factor \(>2\) at fixed computational cost compared to uniform-resolution discrete-threshold simulators — measurable in benchmark datasets (e.g., synthetic networks with planted heterogeneities).
  
## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
*   `"phase-field fracture" AND "energy-stable" AND "adaptive mesh refinement"`
*   `"graph Laplacian" AND "gradient flow" AND "interface regularization"`
*   `"Griffith criterion" AND "network cascade" AND "pinning"`
*   `"variational formulation" AND "information diffusion" AND "energy functional"`