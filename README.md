# Supplementary materials

Supporting data for the manuscript:

**Knowledge-Guided Corrective Redispatch via Checked LLM Interpretation and Sensitivity-Aware Optimization**

The main experiment tables use the manuscript-version records from [efcda6f](https://github.com/a734402468-debug/knowledge-guided-corrective-redispatch-supplement/tree/efcda6fed40214d54a95a5a40dd2d30fd077cadc). The subsequent AC-valid audit is preserved in [f42498c](https://github.com/a734402468-debug/knowledge-guided-corrective-redispatch-supplement/commit/f42498c06852ca9c261bc5b792817e40791442df).

## Contents

| Path | Contents |
|---|---|
| `model_data/` | Cleaned IEEE 118-bus generator, load, load-bound, and branch-flow data |
| `prompts_and_schema/` | LLM prompt, input/output schemas, and checker rules |
| `experiment_data/llm_label_verification_clean/` | Data for the label-verification results |
| `experiment_data/feasibility_stress/` | Aggregate results for the 64-case feasibility study |
| `experiment_data/priority_preservation/` | Fixed-topology case records and reported summaries |
| `experiment_data/n1_stress/` | Manuscript N-1 results and separately identified archived metadata |
| `revision_analysis/` | Parameter, common-subset, first-to-final, representative-case, and runtime summaries |

## Metric conventions

- `Gate_1`--`Gate_4` in the archived labels correspond to Level 1--Level 4 in the manuscript.
- `baseline_2_hard_rule` is the archived method identifier for Baseline 2, the hard-constrained OPF comparator.
- `ezad_percent` and the priority activation shares use the first-round commanded redispatch and exclude G65 slack-bus balancing.
- Mean priority shares use AC-valid cases. Mean EZAD over all cases uses the complete 100-case set.
- The reported 96.9% label accuracy is the mean of the 90 per-output accuracies.

## Data limits

The full DIgSILENT PowerFactory project is not included. The N-1 folder distinguishes the manuscript's sampling description from the later archived manifest; the latter does not reproduce the original sampling pool.

The historical LHS seed and exact retained per-load multipliers were not preserved. The dispatch records support recomputation of the reported participation metrics. The feasibility-stress folder contains aggregate counts only.
