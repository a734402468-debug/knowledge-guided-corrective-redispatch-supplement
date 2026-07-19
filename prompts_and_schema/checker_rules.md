# Deterministic Checker Notes

The JSON Schema files define the syntactic and enum-level output contract. The
runtime checker additionally verifies constraints that depend on the input
candidate set and therefore cannot be fully enforced by a static JSON Schema.

## Runtime checks

1. Parseability
   - The LLM response must be a single valid JSON object.

2. Schema validity
   - The response must pass `priority_label_output_schema.json`.
   - No additional fields are accepted.

3. Allowed values
   - Zone roles must be one of `Source`, `Sink`, `Local`, and `External`.
   - Priority labels must be one of `Gate_1`, `Gate_2`, `Gate_3`, and `Gate_4`.

4. Required generator coverage
   - Every generator in the input `generators_info` must appear exactly once in
     `resource_actions`.
   - Missing, duplicated, or unknown `resource_id` values are rejected.

5. Direction consistency
   - Every accepted generator must include both an upward label and a downward label.

6. Prohibited numerical or physical fields
   - Outputs containing redispatch magnitudes, OPF coefficients, PTDF values,
     generator limits, line-flow values, or algebraic network constraints are rejected.

7. No automatic completion
   - Missing resource labels are not filled by fallback rules. The output is
     rejected or regenerated.

## Notes

`External` generators are not omitted. They are included in `resource_actions`
and assigned `Gate_1` in both directions, preserving them as emergency-backup
candidates rather than removing them from the OPF candidate set.
