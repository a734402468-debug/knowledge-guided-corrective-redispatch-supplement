# Supplementary materials

Supporting data for the manuscript:

**Guideline-Aware Corrective OPF in Power Systems: An LLM-Assisted Framework with Checked Interpretation and Sensitivity-Aware Mapping**

## Contents

| Path | Contents |
|---|---|
| `model_data/` | Cleaned IEEE 118-bus generator, load, load-bound, and branch-flow data |
| `prompts_and_schema/` | LLM prompt, input/output schemas, and checker rules |
| `experiment_data/llm_label_verification_clean/` | Data for the label-verification results |
| `experiment_data/feasibility_stress/` | Aggregate results for the 64-case feasibility study |
| `experiment_data/priority_preservation/` | Fixed-topology case records and reported summaries |
| `experiment_data/n1_stress/` | Frozen N-1 case manifest, case records, and reported summaries |
| `revision_analysis/` | Parameter, common-subset, first-to-final, representative-case, and runtime summaries |

## Metric conventions

- `Gate_1`--`Gate_4` in the archived labels correspond to Level 1--Level 4 in the manuscript.
- `baseline_2_hard_rule` is the archived method identifier for Baseline 2, the hard-constrained OPF comparator.
- `ezad_percent` and the priority activation shares use the first-round commanded redispatch and exclude G65 slack-bus balancing.
- Mean priority shares use AC-valid cases. Mean EZAD over all cases uses the complete 100-case set.

## Data limits

The full DIgSILENT PowerFactory project is not included. The frozen N-1 benchmark contains 100 unique operating-state--contingency pairs: 36 SOA-stressed, 34 NOA-stressed, and 30 system-wide stressed cases. Each pair contains one line outage.

The historical LHS seed and the exact retained per-load multipliers were not preserved, so the original candidate-state pool cannot be regenerated exactly. The files support inspection and recomputation of the reported metrics on the retained cases. The feasibility-stress folder contains aggregate counts only.
