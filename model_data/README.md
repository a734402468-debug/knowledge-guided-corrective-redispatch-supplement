# Supplementary Network Data

This folder contains cleaned network data exported from the DIgSILENT PowerFactory model used in the IEEE 118-bus case study.

## Files

- `generators_original.csv`: generator active-power settings and regulation limits.
- `loads_nominal.csv`: nominal active-power load settings.
- `load_bounds_30pct.csv`: per-load bounds corresponding to the stated +/-30% stress range.
- `branch_active_power_flows.csv`: exported branch active-power flows and line-loading values.
- `network_data_column_dictionary.csv`: column definitions.

The load bounds are defined by:

```text
p_min_mw = 0.7 * p_nominal_mw
p_max_mw = 1.3 * p_nominal_mw
```

## Scope

These cleaned tables document the model quantities used by the case study but are not a replacement for the complete proprietary PowerFactory project. The bounds specify the admissible stress range; they are not the exact retained per-load multipliers of the historical frozen N-1 operating states.
