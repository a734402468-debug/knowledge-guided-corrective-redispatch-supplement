# Operating-point and topology N-1 stress benchmark

This folder supports Tables 4--5, Figure 7, and Section 4.5.

## Benchmark

- 100 unique operating-state--contingency pairs;
- 36 SOA-stressed, 34 NOA-stressed, and 30 system-wide stressed cases;
- one line outage per pair;
- initial maximum line loading: 100.07%--148.98%.

## Files

- `scenario_labels.json`: frozen case manifest.
- `aggregate_summary.csv`: values reported for the three methods.
- `scenario_summary.csv`: AC-valid outcomes and scenario-level metrics.
- `label_activation_by_scenario.csv`: priority activation shares by scenario.
- `benchmark_audit.txt`: benchmark checks.
- `stratified_results.csv`: AC-valid rates by stressed operating profile.

Each method contains the same 100 retained cases. `ezad_percent` is computed from the External-area generator sets specified by `zone_roles` in `scenario_labels.json`. EZAD and the priority shares use the first-round commanded redispatch and exclude G65 slack-bus balancing. The historical LHS seed and exact retained per-load multipliers were not preserved, so the original candidate-state pool cannot be regenerated exactly.
