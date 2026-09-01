# Frozen Operating-Point and Topology N-1 Stress Benchmark

This folder supports Tables 4-5, Figure 7, and the operating-point/topology stress analysis in Section 4.5.

## Benchmark composition

- 100 unique `(operating state, contingency)` pairs;
- 36 SOA-stressed, 34 NOA-stressed, and 30 system-wide stressed cases;
- exactly one line outage per pair;
- no duplicate `(operating state, contingency)` pairs;
- initial maximum line-loading range: 100.07%-148.98%.

All methods were evaluated on the same frozen 100-case set.

## Files

- `scenario_labels.json`: frozen case manifest with stress mode, disconnected line, overload information, and scenario-specific area roles.
- `scenario_summary.csv`: method-level outcomes and metrics by scenario.
- `dispatch_actions_long.csv`: generator-level redispatch actions.
- `label_activation_by_scenario.csv`: scenario-level priority activation shares.
- `source_manifest.csv`: provenance and source fields used to assemble the cleaned tables.
- `benchmark_audit.txt`: integrity checks and canonical benchmark audit.
- `stratified_results.csv`: convergence results stratified by stressed operating profile.

## Reproduction boundary

The archived manifest supports audit of the evaluated benchmark and the archived result tables support recomputation of reported aggregate metrics. The historical LHS random seed and exact retained per-load multipliers were not preserved, so exact regeneration of the original candidate-state pool is not possible. This benchmark is a controlled stress-test set rather than a statistical sample of natural operating-state occurrence.
