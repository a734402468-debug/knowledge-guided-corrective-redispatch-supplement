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
| `experiment_data/priority_preservation/` | Fixed-topology scenario and dispatch records |
| `experiment_data/n1_stress/` | Frozen N-1 benchmark and results |
| `revision_analysis/` | Parameter, common-subset, first-to-final, representative-case, and runtime summaries |

## Metric conventions

- `Gate_1`--`Gate_4` in the JSON records correspond to Level 1--Level 4 in the manuscript.
- Priority activation shares exclude G65, the slack generator. The raw `dispatch_actions_long.csv` files retain the G65 records.
- Average priority shares use AC-valid cases unless a file states another denominator.

## Data limits

The full DIgSILENT PowerFactory project is not included. The frozen N-1 benchmark contains 100 unique operating-state--contingency pairs: 36 SOA-stressed, 34 NOA-stressed, and 30 system-wide stressed cases. Each pair contains one line outage.

The historical LHS seed and the exact retained per-load multipliers were not preserved, so the original candidate-state pool cannot be regenerated exactly. The archived files support audit and recomputation on the frozen benchmark. The feasibility-stress folder contains aggregate counts only.
