# Fixed-topology priority-preservation study

This folder supports Figure 6 and Section 4.4.

## Files

- `aggregate_summary.csv`: values reported for the three methods.
- `scenario_summary.csv`: AC-valid outcomes and scenario-level metrics.
- `label_activation_by_scenario.csv`: priority activation shares by scenario.
- `dispatch_actions_long.csv`: manuscript-version generator-level dispatch records, including G65.

Each method contains 100 cases. The manuscript-version AC-valid counts are 82, 54, and 88 for Baseline 1, Baseline 2, and the proposed method. `is_success` records the validation outcome in that version: convergence and monitored line loadings below 100.1%. EZAD and the priority shares use the first-round commanded redispatch, excluding G65 slack-bus balancing. External-area directions are Level 1; therefore `ezad_percent` equals the Level 1 commanded share. Cases without an AC-valid dispatch remain in the tables and appear as gray cells in Figure 6.
