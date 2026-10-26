# LLM Label-Verification Data

This folder provides compact verification data for the LLM-assisted priority-labeling module.

## Files

- `table2_label_verification_summary.csv`: aggregate results reported in Table 2.
- `real_operating_input_label_results.csv`: detailed results for scenario-derived operating inputs.
- `equivalent_wording_variant_results.csv`: results for equivalent-guideline-wording tests.
- `label_mismatch_cases.csv`: checker-rejected or reference-mismatched cases for audit.
- `repeatability_summary.csv`: repeated-call consistency and whole-output exactness.
- `llm_verification_column_dictionary.csv`: column definitions.

## Interpretation

The reported 96.9% is the arithmetic mean of `gate_label_accuracy` over the 90 outputs. Outputs receive equal weight; this is not a micro-average over all generator-direction labels. Missing generator labels count as errors in the per-output accuracy.

Checker acceptance and semantic label agreement are reported separately. A checker-accepted output can still contain a mismatch relative to the frozen guideline-derived rule table. The prompt, schemas, and deterministic checker rules are provided in `prompts_and_schema/`.
