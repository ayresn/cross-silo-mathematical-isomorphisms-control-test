---
type: "methodological-protocol"
utility: "large-language-model-structural-isomorphism-discovery"
target_architecture: "model-agnostic-deep-learning-systems"
reproducibility: "protocol-guided-candidate-generation"
schema_version: "1.0-control"
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

CRITICAL STRUCTURAL DISCOVERY CONSTRAINTS:
1. The Triple-Correspondence Rule: The structural mapping must explicitly enumerate at least THREE independent correspondences drawn from: governing differential operator, boundary conditions, conserved quantities, instability mechanisms, symmetry groups, variational principles, dimensionless similarity parameters, or numerical solution families.
2. Asymmetric Methodological Transfer: Prioritize candidates where a highly mature source field possesses substantially more developed computational, analytical, or experimental methodology than the target field, offering an immediate opportunity to break an operational bottleneck.
3. Representation Mismatch: Favor pairings that bridge entirely mismatched foundational ontologies (e.g., matching physical continuum mechanics tensors directly onto discrete stochastic probability graphs) that nonetheless evolve under identical mathematical structures.

STRUCTURE & FORMATTING:
Output your entire response as raw Markdown in exactly two parts, in this order: (1) the candidate entry matching the format in Sections 1-5 below, and (2) the README directory-entry snippet matching Section 6 below, preceded by the separator line specified in Section 6. Do not include conversational preambles or postscripts beyond that separator. You MUST wrap all display equations inside standard fenced math code blocks using the triple-backtick language tag "math" (e.g., ````math ... ````).

ENTRY NUMBERING RULE:
Every entry has exactly one 3-digit number, scoped to the generating model's own directory (Claude's entries are numbered independently of Gemini's, GPT's, etc., each starting at 001). This single number is reused verbatim everywhere it appears below: `sid_metadata.entry_id` (as "SID-NNN"), the "ENTRY NNN" heading, and both places it appears in the Section 6 filename/link. These are not separate counters. You have no visibility into the actual current count for this model's directory from within this session — insert your best guess as a placeholder (e.g., 001 if unknown), and note for the maintainer that it must be verified or renumbered against the real current state of that directory before committing.

### METADATA AND STRUCTURAL BLUEPRINT:

---
sid_metadata:
  entry_id: "SID-[Entry Number per the Entry Numbering Rule above, e.g., 001]"
  schema_version: "1.0-control"
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
    - "[Enumerate component 1, e.g., governing_differential_operator]"
    - "[Enumerate component 2, e.g., instability_mechanism]"
    - "[Enumerate component 3, e.g., numerical_solution_family]"
discovery_rationale:
  why_not_obvious: "[e.g., distinct_disciplinary_language / incompatible_ontologies / historically_isolated_communities]"
prior_discovery_metrics:
  # NOTE: All scores below are model-generated self-assessments produced at generation time.
  # They reflect the generating model's internal pattern-matching confidence, not externally
  # validated measurements. They should be used as triage-ranking signals for human reviewers
  # deciding which entries to prioritize for Stage 2 bibliometric validation — not as evidence
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

# INTERDISCIPLINARY STRUCTURAL MAPPING: ⚠*CONTROL*⚠ ENTRY [Same Entry Number as sid_metadata.entry_id above, e.g., 001]

## 1. CROSS-SILO SYSTEM DEFINITION
*   **Silo A (Field 1):** [Specific technical sub-discipline and core phenomenon observed].
*   **Silo B (Field 2):** [Specific technical sub-discipline and core phenomenon observed].
*   **Mathematical Isomorphism:** [A dense, 1-sentence technical explanation of the exact shared mathematical, thermodynamic, or topological law governing both systems, explicitly referencing the selected triple-correspondence vectors].

## 2. DIAGNOSTIC VOCABULARY MATRIX
*   [Silo A Jargon Token] ↔ [Silo B Jargon Token]
    *   *Operator Role:* [Explain the exact mathematical reason and functional equivalent role these terms share under the operator].
*   [Silo A Jargon Token] ↔ [Silo B Jargon Token]
    *   *Operator Role:* [Explain the exact mathematical reason and functional equivalent role these terms share under the operator].

## 3. CORE MATHEMATICAL PARALLELISM
[Provide a 1-paragraph explanation of how Silo A models its phenomenon, including its primary equation wrapped in a fenced math block. For example:
```math
\frac{dX}{dt} = f(X, Y, t)
```
Then, provide a 1-paragraph explanation of how Silo B models its phenomenon using its respective named equation wrapped in a fenced math block. Explain how these curves map onto each other in latent space topology.]

## 4. ASYMMETRIC METHODOLOGICAL TRANSFER & SCIENTIFIC HYPOTHESIS
*   **Preferred Transfer Direction:** [Source Field/Silo] → [Target Field/Silo]
*   **Asymmetric Maturity Rationale:** [Detail exactly why the chosen source field possesses a significantly more mature computational, analytical, or experimental toolkit than the target domain].
*   **Target Bottleneck Mitigation:** [State a testable, peer-review-quality hypothesis detailing how importing the source field's algorithms explicitly resolves a persistent operational bottleneck in the target domain].
*   **Falsifiable Prediction:** [Specify at least one distinct, empirically observable prediction or benchmark outcome that would mathematically differ from the current domain state of the art].

## 5. RELEVANT ACADEMIC SEARCH STRINGS FOR VERIFICATION
*   `"Exact Jargon Phrase from Silo A" AND "Core Equation Name A" AND "Secondary Concept A"`
*   `"Exact Jargon Phrase from Silo B" AND "Core Equation Name B" AND "Secondary Concept B"`

## 6. README DIRECTORY ENTRY
Immediately after Section 5, output the separator line `--- END ENTRY / BEGIN DIRECTORY SNIPPET ---`, then output the following four-line snippet. This snippet is for the maintainer to paste into the matching company subsection of README.md's CORE DATASET DIRECTORY — it does not belong in the entry file itself.

*   **[<model_version-slug>_entry-[Same Entry Number as sid_metadata.entry_id above, e.g., 001]](mappings-<company-slug>-<model_family-slug>/<model_version-slug>_entry-[same number].md)** — `Stage 1 / pending`
    *   *System Synthesis:* [A short, evocative 3-6 word Title Case phrase capturing the discovery, in the style of existing entries such as "Resonant Destabilization of Crystalline Plaque" — do not simply restate the Mathematical Isomorphism sentence from Section 1]
    *   *Domains:* [Domain A, Title Case] & [Domain B, Title Case]
    *   *Isomorphism:* [Named equation/method from Silo A] mapped to [Named equation/method from Silo B]

Constraints on this snippet:
*   The entry number here must be numerically identical to this entry's own `sid_metadata.entry_id` and to the "ENTRY NNN" heading above — see the Entry Numbering Rule.
*   The filename slug must exactly match this entry's own `provenance.model_version` field so the directory link resolves correctly.
*   The directory path must exactly match `mappings-[provenance.company]-[provenance.model_family]/`, lowercased and hyphenated.
*   The status tag is always `Stage 1 / pending` for a newly generated entry — never mark it as validated here.
*   *Domains* and *Isomorphism* must reuse the same domain names and named methods already established in this entry's own YAML and Section 3 — do not introduce new terminology that doesn't appear elsewhere in the entry.
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
