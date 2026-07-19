# Supplementary Network Data

This folder provides cleaned network data exported from the DIgSILENT PowerFactory model used in the IEEE 118-bus case study.

## Source setting

The network topology is illustrated in the manuscript. The files here provide the numerical generator, load, load-bound, and branch-flow data used as supplementary evidence.

## Files

- `generators_original.csv`: original generator active-power settings and active-power limits.
- `loads_nominal.csv`: nominal active-power load settings.
- `load_bounds_30pct.csv`: load perturbation bounds used for the +/-30% operating-point stress cases.
- `branch_active_power_flows.csv`: branch active-power flow and line-loading values exported after load-flow calculation.
- `network_data_column_dictionary.csv`: column definitions.


## Load bounds

The load bounds are generated from the nominal load as

```text
p_min_mw = 0.7 * p_nominal_mw
p_max_mw = 1.3 * p_nominal_mw
```

## Notes

PowerFactory internal object paths are omitted from the cleaned tables. Original raw exports can be regenerated using the accompanying export script if needed.
