# Experiment map

Use one compact row per decision-changing test; add a protocol block where needed. A proposed experiment is PLANNED until actually run and inspected.

| Priority / experiment ID | Claim IDs and research question | Rival explanation | Intervention and control / comparator | Data split and independent unit | Metric and uncertainty | Budget | Outcome that weakens the claim | Figure / decision |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| P0 / E1 | [C1; answerable question] | [Specific rival] | [Matched comparison; variables held fixed] | [Train/dev/test; grouped separation; sampling unit] | [Definition; direction; aggregation; interval plan] | [Runs; compute; time; tuning] | [Qualitative or prespecified numerical condition] | [What this changes] |

## Protocol for [experiment ID]

- Setup/version: [Dataset, model, code, hardware/software where relevant.]
- Allocation and matching: [Randomization, paired samples, common seeds, budgets, blinding, or justified alternatives.]
- Train/development/test boundary: [What can influence fitting, tuning, rubric development, and final selection; never use final-test feedback for these.]
- Primary endpoint: [Metric, denominator, aggregation, direction, and intended interpretation.]
- Secondary/exploratory endpoints: [Label separately.]
- Uncertainty: [What varies; resampling/repetition unit; planned interval/test; assumptions.]
- Exclusions/failures: [Prespecified rules; failed runs/tool errors; attrition.]
- Possible outcomes: [What supports, narrows, refutes, or leaves the claim unresolved.]
- Resource cap and stopping decision: [Feasible budget and what happens when exhausted.]
- Artifacts to retain: [Configuration, logs, predictions, analysis, provenance.]
- Result/status: [PLANNED or exact artifact and observed outcome.]
