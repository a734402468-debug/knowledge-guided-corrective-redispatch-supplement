# Supplementary Materials for Guideline-Aware Corrective OPF

This repository provides supplementary materials for the manuscript:

**Guideline-Aware Corrective OPF in Power Systems: An LLM-Assisted Framework with Checked Interpretation and Sensitivity-Aware Mapping**

The repository documents the checked guideline-to-OPF interface, the IEEE 118-bus case-study data, archived scenario-level results, and the compact analyses added during manuscript revision.

## Repository structure

| Path | Contents | Manuscript mapping |
|---|---|---|
| `model_data/` | Cleaned IEEE 118-bus generator, load, load-bound, and branch-flow data | Simulation setup |
| `prompts_and_schema/` | LLM prompt, input/output schemas, and deterministic checker rules | Checked priority-labeling interface |
| `experiment_data/llm_label_verification_clean/` | Label-verification, mismatch, wording-variant, and repeatability data | Table 3 and Section 4.2 |
| `experiment_data/feasibility_stress/` | Frozen aggregate convergence counts for the 64-case hard-rule feasibility study | Figure 5 and Section 4.3 |
| `experiment_data/priority_preservation/` | Scenario-level and generator-level fixed-topology results | Figure 6 and Section 4.4 |
| `experiment_data/n1_stress/` | Frozen N-1 manifest, scenario summaries, dispatch actions, benchmark audit, and stratified results | Tables 4-5, Figure 7, and Section 4.5 |
| `revision_analysis/` | Parameter sensitivity, first-to-final comparison, representative cases, common-subset comparison, and runtime summaries | Tables 2, 6, and 7 and associated revision text |

## Reproducibility scope

The archived files support:

- audit of the evaluated benchmark composition;
- recomputation of the reported aggregate metrics from archived scenario-level results where those results are available;
- inspection of generator-level redispatch actions for the priority-preservation and N-1 studies;
- verification of the compact sensitivity, paired-subset, first-to-final, and runtime summaries added during revision.

The repository does **not** contain the complete DIgSILENT PowerFactory project. The historical random seed and the exact retained per-load multipliers for the frozen N-1 candidate-state pool were not preserved; therefore, exact regeneration of that historical LHS candidate pool is not possible. The N-1 results should be interpreted as a controlled comparison on the same frozen 100-case benchmark, not as an estimate of the natural probability of operating-state occurrence.

The feasibility-stress folder contains the published aggregate counts. The original per-case feasibility-stress dispatch archive is not included and is not represented here as scenario-level raw data.

## Benchmark integrity

The frozen N-1 benchmark contains 100 unique `(operating state, contingency)` pairs under three stressed operating profiles:

- 36 SOA-stressed cases;
- 34 NOA-stressed cases;
- 30 system-wide stressed cases.

Each pair contains one line outage. The initial maximum line-loading range is 100.07%-148.98%. All compared methods use the same frozen cases, physical model, candidate-resource definition before method-specific enforcement, physical constraints, validation criterion, and stopping conditions.

## Interpretation boundary

Checker acceptance establishes structural completeness, coverage, prohibited-field compliance, and runtime admissibility. It is not equivalent to semantic agreement with the frozen guideline-derived reference labels. The LLM remains an interpretation component; numerical penalties, redispatch values, physical constraints, and AC-valid acceptance are handled deterministically downstream.
