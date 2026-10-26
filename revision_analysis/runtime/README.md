# Prototype Runtime Breakdown

`timing_summary.csv` contains the archived prototype timing summaries.

LLM inference is separate from downstream physical execution. PowerFactory-side execution includes worker-side setup, parameter updates, and iterative physical calculation; core SLP-AC computation is a component within that total. Transport/service overhead is the measured HTTP round-trip minus worker-side execution and should not be interpreted as pure network latency.

The timing results characterize a look-ahead security-assessment and operator decision-support prototype, not a subsecond control implementation.
