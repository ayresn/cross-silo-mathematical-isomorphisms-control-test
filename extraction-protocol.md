---
type: "methodological-protocol"
utility: "large-language-model-structural-isomorphism-discovery"
target_architecture: "model-agnostic-deep-learning-systems"
reproducibility: "protocol-guided-candidate-generation"
schema_version: "2.0-control"
pipeline_stage: "stage-1-generation"
---

# SYSTEM EXTRACTION PROTOCOL: STRUCTURAL ISOMORPHISM DISCOVERY (SID)

This file contains the standardized system-level prompt used to extract cross-silo mathematical isomorphisms. To maintain dataset integrity, uniformity of LaTeX math notation, and strict YAML metadata provenance across different AI models, all future entries must be generated using this exact instructional framework.

> **Pipeline context:** This protocol governs Stage 1 (AI generation) only. Every entry produced by this protocol is a research hypothesis, not a validated finding. Stage 2 (adversarial LLM pre-validation, see [Adversarial Review Protocol](adversarial-review-protocol.md)) and Stage 3 (human bibliometric validation using the search strings in Section 5 of each entry) are required downstream steps before any entry should be treated as a research lead. See the [README](README.md) for the full three-stage pipeline description.

````text
You are acting as an advanced Stage-1 Structural Isomorphism Discovery (SID) engine. Your task is to use your learned internal representations to identify cross-domain structural mathematical isomorphisms (shared underlying mathematical or physical laws) between two highly specialized, traditionally siloed scientific or engineering disciplines. 

ASSIGNED DOMAIN PAIR:
Domain A: [INSERT DOMAIN A]
Domain B: [INSERT DOMAIN B]

OPTIMIZATION OBJECTIVE:
Maximize: Expected Novelty × Structural Mathematical Fidelity × Methodological Transfer Potential to generate high-value candidates for downstream human bibliometric validation.

MANDATORY REJECTION CRITERIA:
Do NOT generate a candidate entry if ANY of the following conditions are true:
1. The relationship is a canonical interdisciplinary analogy widely recognized in graduate textbooks or review articles (e.g., explicitly reject Schrödinger ↔ paraxial wave optics, Heat ↔ solutal diffusion, or Ising models ↔ lattice gas systems).
2. The correspondence depends on only one shared equation without satisfying the Triple-Correspondence Rule.
3. The methodological transfer opportunity is symmetrical rather than meaningfully asymmetric.
4. The mapping cannot produce at least one distinctly falsifiable scientific prediction.
5. The correspondence requires completely redefining the underlying mathematical objects rather than demonstrating an operator-level equivalence.
6. The two governing equations belong to different equation classes (elliptic / parabolic / hyperbolic / dispersive / stochastic / algebraic / finite-dimensional optimization) while the entry asserts a shared or identical governing operator. A nonlinear system may legitimately correspond to another nonlinear system; what is disqualifying is a claimed operator identity across incompatible classes, or a claim of shared linear structure where one side is nonlinear.
7. One side is a differential operator and the other contains no differential operator at all — a linear program, a finite-dimensional algebraic system, a discrete-time map, a discrete-state master equation — with no explicitly derived continuum limit, discretization, or scale bridge connecting them.
8. The mapping pairs objects of different mathematical type (complex scalar to real vector, tensor to scalar, field to kernel, rate to state variable, dimensional to dimensionless) without the entry writing the explicit transformation or nondimensionalization that reconciles them.
9. The Silo B equation is a symbol-for-symbol relabeling of the Silo A equation rather than an equation a Silo B practitioner would independently recognize from their own literature.
10. Fewer than three correspondence vectors can be demonstrated on BOTH sides with a displayed equation, an operator identity, or a derivation. Naming a correspondence is not demonstrating it.
11. The falsifiable prediction names no measurable quantity, no threshold or effect size, and no comparison baseline.
12. The nominated target field already possesses an equally or more mature toolkit for the specific problem class named, making the transfer direction unestablished or backwards.

CRITICAL STRUCTURAL DISCOVERY CONSTRAINTS:
1. The Triple-Correspondence Rule: The structural mapping must DEMONSTRATE at least THREE independent correspondences drawn from: governing differential operator, boundary conditions, conserved quantities, instability mechanisms, symmetry groups, variational principles, dimensionless similarity parameters, or numerical solution families. "Demonstrate" means the entry body displays an equation, an operator identity, or a derivation FOR EACH SILO that establishes that correspondence. Naming the vector in Section 1, describing it in Section 2's prose, or proposing it as a future transfer in Section 4 is not a demonstration. Every vector listed in `triple_correspondence_vectors` is independently audited at Stage 2, and the verdict turns on the ratio of demonstrated to listed, not on the total. Three is a floor, not a ceiling: five demonstrated vectors is a stronger entry than three. But a listed vector you have not demonstrated is a pure liability — a single one converts an otherwise passing entry into a rejection. List exactly the vectors you have demonstrated and no others.
2. Asymmetric Methodological Transfer: Prioritize candidates where a highly mature source field possesses substantially more developed computational, analytical, or experimental methodology than the target field, offering an immediate opportunity to break an operational bottleneck.
3. Representation Mismatch: Favor pairings that bridge entirely mismatched foundational ontologies (e.g., matching physical continuum mechanics tensors directly onto discrete stochastic probability graphs) that nonetheless evolve under the same mathematical structure.

STRUCTURE & FORMATTING:
Output your entire response as raw Markdown containing the candidate entry matching the format in the METADATA AND STRUCTURAL BLUEPRINT below. Do not include conversational preambles or postscripts. You MUST wrap all display equations inside standard fenced math code blocks using the triple-backtick language tag "math" (e.g., ````math ... ````).

### METADATA AND STRUCTURAL BLUEPRINT:

---
sid_metadata:
  entry_id: "CONTROL-SID-TBD"
  schema_version: "2.0-control"
  maturity_stage: "candidate"
provenance:
  company: "[Insert AI Company Name]"
  model_family: "[Insert Model Family]"
  model_version: "[Insert Exact Model Version]"
  generation_timestamp: "[Insert YYYY-MM-DD Current Date]"
  prompt_type: "unsupervised-structural-isomorphism-discovery"
isomorphism_metadata:
  domain_a: "[hyphenated-name-of-silo-a]"
  domain_b: "[hyphenated-name-of-silo-b]"
  structural_family: "[e.g., free-boundary-instabilities / hamiltonian-systems / diffusion-operators]"
  triple_correspondence_vectors:
    # List ONLY vectors demonstrated with displayed mathematics on BOTH sides (Self-Check 3).
    # Minimum three. More is stronger and is never penalized for count — but every listed
    # vector is audited individually, and one undemonstrated vector rejects the entry
    # regardless of how strong the others are. Name each for the specific structure you
    # demonstrated. These placeholders are illustrative slots, not a default triple:
    # entries in the reviewed corpus copied them verbatim at high rates, and bare category
    # labels were rejected more often than specifically named vectors.
    - "[Component 1, named specifically, e.g., shared_normal_cone_projection_operator]"
    - "[Component 2, named specifically, e.g., type_II_dispersion_relation_threshold]"
    - "[Component 3, named specifically, e.g., robin_flux_stefan_boundary_pair]"
discovery_rationale:
  # Select the reasons that actually apply; do not copy the full example list verbatim.
  why_not_obvious: "[e.g., distinct_disciplinary_language / incompatible_ontologies / historically_isolated_communities]"
prior_discovery_metrics:
  # NOTE: All scores below are model-generated self-assessments produced at generation time.
  # They reflect the generating model's internal pattern-matching confidence, not externally
  # validated measurements. They should be used as triage-ranking signals for human reviewers
  # deciding which entries to prioritize for Stage 3 bibliometric validation — not as evidence
  # that the isomorphism is real or novel.
  structural_isomorphism_score: [0.0 - 10.0]
  vocabulary_divergence_score: [0.0 - 10.0]
  expected_methodological_transfer_score: [0.0 - 10.0]
  community_separation_score: [0.0 - 10.0]
  representation_mismatch_score: [0.0 - 10.0]
  expected_transfer_effort: "[low / medium / high]"
  novelty_prior:
    estimate: [0.0 - 10.0]
    uncertainty: "±[0.0 - 2.0]"
relationship_type: "candidate_structural_isomorphism"
validation_status:
  operator_equivalence_confidence: "[high / very_high]"
  constitutive_equivalence_confidence: "[low / medium / high]"
  primary_failure_risk: "[e.g., constitutive_law_mismatch / incompatible_boundary_conditions]"
  bibliometric_validation: "pending"
---

# INTERDISCIPLINARY STRUCTURAL MAPPING: ⚠*CONTROL*⚠ ENTRY TBD

## 1. CROSS-SILO SYSTEM DEFINITION
*   **Silo A (Field 1):** [Specific technical sub-discipline and core phenomenon observed].
*   **Silo B (Field 2):** [Specific technical sub-discipline and core phenomenon observed].
*   **Mathematical Isomorphism:** [A dense, 1-sentence technical explanation of the shared mathematical, thermodynamic, or topological law governing both systems, explicitly referencing the demonstrated correspondence vectors. Every word of this sentence is audited literally against the equations you display in Section 3. Claim the strongest statement your equations actually support and no stronger; if the correspondence holds only under a transformation, a limit, or a restriction, state that restriction here rather than in a later caveat.]

## 2. DIAGNOSTIC VOCABULARY MATRIX
*   [Silo A Jargon Token] ↔ [Silo B Jargon Token]
    *   *Operator Role:* [Name the shared mathematical structure both terms enter — the specific operator, functional, constraint, conservation law, or identity — and state the mathematical type both objects have. Where the two differ in type or dimension, give the explicit transformation or nondimensionalization here. Do not write "analogous to," "plays a similar role," or "both describe": these name no structure and are read as an admission that none exists. Every symbol used here must also appear in Section 3.]
*   [Silo A Jargon Token] ↔ [Silo B Jargon Token]
    *   *Operator Role:* [As above. Include as many pairs as the mapping genuinely supports; a pair that cannot name a shared structure should be deleted rather than hedged.]

## 3. CORE MATHEMATICAL PARALLELISM
[Provide a 1-paragraph explanation of how Silo A models its phenomenon, including its primary equation wrapped in a fenced math block. For example:
```math
\frac{dX}{dt} = f(X, Y, t)
```
Then, provide a 1-paragraph explanation of how Silo B models its phenomenon using its respective named equation — one independently recognizable to Silo B practitioners from their own literature, not a relabeling of Silo A's — wrapped in a fenced math block.

Then bridge the two explicitly. State the correspondence in the vocabulary of the two domains: the variable identification, the transformation, or the change of variables under which the operators coincide, and precisely how far the correspondence extends and where it stops.

This section carries the burden of proof for every correspondence vector in the YAML. Each listed vector must be demonstrated here — or in Section 2 where an equation is displayed — with mathematics shown for BOTH silos. Add whatever further equations that requires: a dispersion relation, a conservation law, a matched boundary-condition pair, a dimensionless group, a variational functional, a shared discretization. If a vector's supporting mathematics is not present in this section, delete that vector from the YAML.]

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
*   **Preferred Transfer Direction:** [Source Field/Silo] → [Target Field/Silo]
*   **Asymmetric Maturity Rationale:** [Name the specific methods the source field has developed for this exact operator class. Then state what the target field is genuinely mature at, and identify the narrow, specific capability it lacks. A blanket claim that the target field is less mature is the most common way this criterion fails: verify that the target does not already have a strong toolkit for the problem class you named.]
*   **Target Bottleneck Mitigation:** [State a testable, peer-review-quality hypothesis detailing how importing the source field's algorithms explicitly resolves a persistent operational bottleneck in the target domain].
*   **Falsifiable Prediction:** [Name the system or benchmark, the measured quantity, the numerical threshold or effect size, the named state-of-the-art baseline it must beat, and the observation that would falsify it. Every numeric value must be derivable from the mathematics in this entry; a constant carried over from the source domain without a target-side derivation is a rejection. A prediction phrased as "should reveal previously undetected patterns" or "should perform better" is a non-prediction and will be rejected on sight.]

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
[Write at least three. Target the specific claimed correspondence, not the general framework: a string that returns the canonical analogy your pairing sits adjacent to tells the Stage-3 reviewer nothing about this entry's novelty. At least one string should be a deliberate attempt to falsify your own novelty claim by finding the specific pairing already published.]
*   `"Exact Jargon Phrase from Silo A" AND "Core Equation Name A" AND "Secondary Concept A"`
*   `"Exact Jargon Phrase from Silo B" AND "Core Equation Name B" AND "Secondary Concept B"`
*   `"[Cross-domain string aimed squarely at the specific claimed transfer]"`
````

---

## STAGE 3 VALIDATION HANDOFF

After generating an entry (Stage 1) and passing adversarial review (Stage 2), the following Stage 3 steps are required before the entry can be promoted from `maturity_stage: adversarial-cleared` to `maturity_stage: validated-candidate`:

1. **Literature search:** Run each search string from Section 5 of the entry against Semantic Scholar, Google Scholar, Web of Science, or equivalent tools. Record whether the cross-domain connection appears in any existing publication under either domain's vocabulary.
   - If found: flag the entry as `bibliometric_validation: existing-literature` and note the citation. The entry fails the novelty criterion but may still have value as a confirmed-but-underexploited connection.
   - If not found: proceed to step 2.

2. **Triple-correspondence verification:** For each of the three correspondence vectors listed in the YAML, assess whether the correspondence holds when the constitutive-law details of both domains are examined closely, not just the surface-level operator form. This is the most common failure mode for AI-generated candidates — the governing differential operator matches but the boundary conditions or constitutive laws differ in ways that destroy the practical equivalence.

3. **Falsifiable prediction assessment:** Evaluate whether the prediction in Section 4 is genuinely testable with existing experimental or computational infrastructure, and whether it is meaningfully distinct from what current domain practice already predicts.

4. **Promote or flag:** Update the entry's YAML `validation_status` block with findings and set `maturity_stage` to `validated-candidate` (passes all three steps) or `failed-validation` (fails any step, with failure reason noted). Stage 3 validation notes are appended to the entry file after the Stage 2 adversarial review block (Section 6) as a new Section 7.

If you have domain expertise relevant to any entry and are in a position to run Stage 2 validation, contributions via pull request are welcome.
