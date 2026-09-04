# Fixed-topology priority-preservation study

This folder supports Figure 6 and Section 4.4.

## Files

- `aggregate_summary.csv`: values reported for the three methods.
- `scenario_summary.csv`: AC-valid outcomes and scenario-level metrics.
- `label_activation_by_scenario.csv`: priority activation shares by scenario.

Each method contains 100 cases. `is_success` records the final all-line AC validation outcome. EZAD and the priority shares are computed from the first-round commanded redispatch after excluding G65 slack-bus balancing. Under the frozen rule realization used in this study, External-area directions are Level 1; therefore `ezad_percent` equals the Level 1 commanded share. Cases without an AC-valid dispatch remain in the case tables and appear as gray cells in Figure 6.
