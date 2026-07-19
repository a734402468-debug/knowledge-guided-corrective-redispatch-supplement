# Prompts and Schema

This folder contains the prompt and schema files used to document the checked
priority-labeling interface.

## Files

- `Prompt.txt`: English prompt for guideline-based priority-label generation.
- `priority_label_input_schema.json`: JSON Schema for the input payload.
- `priority_label_output_schema.json`: JSON Schema for the LLM output.
- `checker_rules.md`: Deterministic runtime checks that complement the static JSON Schema.

## Important note

The static JSON Schema checks syntax, required fields, and allowed enum values.
Input-dependent properties such as complete generator coverage and uniqueness of
`resource_id` are verified by the deterministic checker described in
`checker_rules.md`.
