# Operating-point and topology N-1 stress benchmark

This folder supports Tables 4--5, Figure 7, and Section 4.5.

## Benchmark

- 100 unique operating-state--contingency pairs;
- 36 SOA-stressed, 34 NOA-stressed, and 30 system-wide stressed cases;
- one line outage per pair;
- initial maximum line loading: 100.07%--148.98%.

## Files

- `scenario_labels.json`: frozen case manifest.
- `scenario_summary.csv`: method outcomes and scenario metrics.
- `dispatch_actions_long.csv`: generator-level first-round redispatch actions.
- `label_activation_by_scenario.csv`: priority activation shares by scenario.
- `source_manifest.csv`: source-file hashes.
- `benchmark_audit.txt`: benchmark checks.
- `stratified_results.csv`: AC-valid rates by stressed operating profile.

Priority shares exclude G65, the slack generator; the raw dispatch file retains its records. The historical LHS seed and exact retained per-load multipliers were not preserved, so the original candidate-state pool cannot be regenerated exactly.
