# LLM Label-Verification Data

This folder provides compact verification data for the LLM-assisted priority-labeling module.

## Files

- `table3_label_verification_summary.csv`: aggregate results reported in the revised manuscript's Table 3.
- `real_operating_input_label_results.csv`: detailed results for scenario-derived operating inputs.
- `equivalent_wording_variant_results.csv`: results for equivalent-guideline-wording tests.
- `label_mismatch_cases.csv`: checker-rejected or reference-mismatched cases for audit.
- `repeatability_summary.csv`: repeated-call consistency and whole-output exactness.
- `llm_verification_column_dictionary.csv`: column definitions.

## Interpretation

Checker acceptance and semantic label agreement are reported separately. A checker-accepted output can still contain a mismatch relative to the frozen guideline-derived rule table. The prompt, schemas, and deterministic checker rules are provided in `prompts_and_schema/`.
