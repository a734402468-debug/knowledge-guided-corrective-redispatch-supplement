# Fixed-topology priority-preservation study

This folder supports Figure 6 and Section 4.4.

## Files

- `scenario_summary.csv`: method outcomes and scenario metrics.
- `dispatch_actions_long.csv`: generator-level first-round redispatch actions.
- `label_activation_by_scenario.csv`: priority activation shares by scenario.
- `source_manifest.csv`: source-file hashes.

Priority shares exclude G65, the slack generator; the raw dispatch file retains its records. Cases without an AC-valid dispatch remain in the tables and appear as gray cells in Figure 6.
