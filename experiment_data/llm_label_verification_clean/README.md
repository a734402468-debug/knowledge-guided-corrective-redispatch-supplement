# LLM Label-Verification Data

This folder provides compact verification data for the LLM-assisted priority-labeling module.

## Files

- `table2_label_verification_summary.csv`: aggregate results used for the paper's LLM label-verification table.
- `real_operating_input_label_results.csv`: detailed results for real operating metadata inputs.
- `equivalent_wording_variant_results.csv`: results for equivalent-guideline-wording tests.
- `label_mismatch_cases.csv`: rejected or mismatched cases for audit.
- `llm_verification_column_dictionary.csv`: column definitions.


## Notes

These files are intended to support the reported label-generation reliability results
without uploading a large number of raw LLM logs. The prompt, output template/schema,
and deterministic checker rules are provided separately in `prompts_and_schema/`.
