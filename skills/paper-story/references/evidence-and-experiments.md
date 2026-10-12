# Evidence and experiment design

Turn a proposed paper story into bounded claims, inspectable support, and experiments that distinguish explanations. Start from the decision each experiment should change. Prefer a small decisive comparison to scores with unclear implications.

## Contents

- [Keep a claim ledger](#keep-a-claim-ledger)
- [Match claims to evidence](#match-claims-to-evidence)
- [Design a discriminating experiment](#design-a-discriminating-experiment)
- [Make comparisons fair](#make-comparisons-fair)
- [Protect evaluation independence](#protect-evaluation-independence)
- [Validate benchmarks and metrics](#validate-benchmarks-and-metrics)
- [Quantify uncertainty and report precisely](#quantify-uncertainty-and-report-precisely)
- [Revise the story after results](#revise-the-story-after-results)

## Keep a claim ledger

Record each assertion, its population/task/model/budget scope, evidence status, artifact location, unresolved gap, and next action. Separate observations, explanations, and plans. Preserve qualifiers in the title, abstract, figure captions, and conclusion.

| Status | Apply when |
| --- | --- |
| VERIFIED | You inspected an underlying artifact that supports the bounded assertion; identify the file, run, table, passage, or proof. |
| REPORTED | A user or secondary source states the assertion, but you have not checked the underlying artifact. |
| HYPOTHESIS | An explanation or prediction remains untested or insufficiently distinguished from alternatives. |
| PLANNED | An experiment or analysis is specified but has not produced inspected results. |
| CONTRADICTED | Inspected evidence conflicts with the assertion within its stated scope. |
| UNKNOWN | Available information does not establish support or contradiction. |

Never let a status replace scope. Verifying a table does not establish its methodology, reproduce its numbers, or extend its result beyond the evaluated setting. Record those checks separately. Retain both supporting and conflicting evidence when outcomes differ across conditions.

## Match claims to evidence

| Claim type | Necessary support and boundary |
| --- | --- |
| Descriptive: “X occurs” | Inspect examples or measurements with a defined sampling process, unit, denominator, and exclusions. A selected example establishes existence, not prevalence. |
| Comparative: “A improves on B” | Compare relevant methods under a specified evaluation and resource policy; inspect effect sizes and uncertainty. Bound the claim to tested comparators and conditions. |
| Causal: “X causes Y” | Specify the intervention and causal quantity; use randomization or justify identification assumptions, confounding controls, and alternative explanations. Correlation alone leaves mechanism hypothetical. |
| Theoretical: “Under assumptions A, property P holds” | State definitions, quantifiers, assumptions, and complete argument or proof. Inspect dependencies and edge cases. Numerical illustrations do not establish a theorem. |
| Generalization: “The result transfers” | Evaluate independently held-out populations, sources, times, or task families relevant to the claim. Explain their relationship to training and the remaining coverage boundary. |
| Practical: “The method is useful” | Measure relevant end-to-end utility, cost, latency, reliability, and failure consequences against a realistic alternative. A proxy score alone does not establish deployment value. |

For a compound claim, satisfy every component or split it into independently qualified assertions. Treat novelty as a separate literature question, not an implication of high scores.

## Design a discriminating experiment

Write an experiment card before allocating substantial compute:

| Field | Required decision |
| --- | --- |
| Claim and rival | State the exact hypothesis and strongest plausible alternative explanation. |
| Intervention and control | Identify what changes and what remains comparable; include a negative control where informative. |
| Measurement and comparator | Define the outcome, evaluation protocol, reference method, and meaningful effect size. |
| Split and sample | Name the data source, grouping unit, train/dev/test role, and planned sample or run count. |
| Budget | Cap training, tuning, inference, annotation, and wall-clock cost; define stopping rules before seeing outcomes. |
| Falsifier | State which observation would weaken the claim and which result would remain inconclusive. |
| Figure | Sketch the axes, conditions, units, uncertainty, and expected contrasting patterns without inventing results. |

Rank candidates by their ability to separate explanations, feasibility, and importance to the main claim. Check data and metric sanity cheaply; run a diagnostic pilot; spend remaining budget on the strongest unresolved comparison. Mark pilot-driven choices as exploratory and reserve independent confirmation where feasible. If resources cannot separate the hypotheses, narrow the claim and record the ambiguity.

Fictional example: a retrieval method appears more accurate because it receives longer input. Compare it with a token-matched control using irrelevant retrieved passages, keep the evaluation items and decoding policy fixed, and plot paired accuracy differences alongside input tokens. If both retrieval conditions improve similarly, useful retrieved content is not yet established as the explanation.

## Make comparisons fair

Include a simple sanity baseline and the strongest feasible relevant comparator. Verify implementation, checkpoint, preprocessing, and evaluation compatibility. Provide comparable tuning opportunities under a declared policy; disclose borrowed results and protocol differences instead of silently mixing them.

Choose the resource question explicitly: matched data, parameter count, training compute, inference compute, latency, or total cost answer different questions. Report hardware, precision, batch size, context length, search or sampling budget, and tuning costs when they affect the comparison. Use quality-versus-cost curves when no single budget match is informative. Explain unavailable baselines and resulting limits.

Treat ablations as interventions on a specified system. Removing a component can change capacity, optimization, data exposure, or compute. Retune fairly where appropriate, inspect interactions, and avoid declaring a component universally necessary from one removal. An ablation can establish a contribution within the tested configuration while leaving its mechanism unresolved.

## Protect evaluation independence

Define train, development, and final test roles before adapting the method. Split by the dependency unit: person, document, repository, source, template, task family, or time, as appropriate. Audit duplicates and near-duplicates, shared derivations, answer contamination, and preprocessing fitted using held-out data. A random row split may preserve these dependencies.

Track every use of evaluation feedback: prompt revisions, reward construction, example selection, hyperparameter search, filtering, checkpoint choice, and manual error analysis can make a nominal test set part of development. Reclassify repeatedly consulted data and obtain an independent final test when needed. Disclose contamination uncertainty for opaque pretraining corpora.

Sharing raw input tasks between supervised fine-tuning and reinforcement-learning training can be permissible. Document shared tasks, targets, and feedback, and keep final testing independent. Do not allow test labels, rewards, outputs, or test-informed adaptation to enter training; distinguish transfer to new tasks from reuse of a training pool.

## Validate benchmarks and metrics

Connect benchmark coverage to the intended construct and population. Inspect task representativeness, annotation quality, ambiguity, difficulty, saturation, shortcuts, and selection effects. Document exclusions and failed cases. Multiple similar benchmarks do not automatically establish broad transfer.

Check metric code against hand-worked cases and known correct, incorrect, empty, malformed, and adversarial outputs. Test whether formatting, verbosity, answer copying, or irrelevant content can inflate scores. State aggregation, weighting, missing-output handling, and direction of improvement.

When a proxy evaluates subjective quality, calibrate it on a modest, diverse, blindly assessed human sample using a clear rubric. Inspect disagreements and subgroup errors; report agreement and sampling limits. Use deterministic checks, domain validators, or small manual audits where suitable. Expensive LLM judges are optional; if used, validate their rubric, order sensitivity, repeatability, and agreement with humans. Distinguish evaluator agreement from probabilistic calibration when reporting either.

## Quantify uncertainty and report precisely

Identify the independent sampling unit and source of variation. Separate variation across test items, training seeds, dataset splits, and repeated measurements. Log seeds, attempted and completed runs, failures, selection rules, and exact configurations. Many correlated outputs from one run do not become independent training replicates.

For matched methods on the same items, splits, or seeds, analyze paired differences when that pairing is meaningful. Resample or model at the dependency unit; use grouped or hierarchical methods when required. Report the effect size and interval for the comparison, not an inference from overlapping separate error bars.

Label standard deviation as dispersion across specified observations. Label a confidence interval with its confidence level, estimand, calculation method, and assumptions. Do not substitute SD for a confidence interval or imply that an item-level interval captures training variability. With one run, say so; with few runs, expose the observations and uncertainty limits. Do not manufacture significance, intervals, variance, or missing repetitions. Treat insufficient precision as inconclusive rather than proof of equivalence.

State units and denominators: examples versus users, per-query versus aggregate cost, seconds versus milliseconds, percentage points versus relative percent. Give counts behind rates and disclose exclusions, averaging weights, rounding, and missing values. Preserve exact artifact provenance for every reported number.

## Revise the story after results

Compare the observation with the predeclared falsifier. Check instrumentation before interpreting surprises, then retain valid negative outcomes. Narrow, replace, or withdraw claims contradicted by evidence; distinguish failure of the method from failure of the proposed explanation. Update the ledger, experiment priorities, figures, abstract, and limitations together. Never repair a weak result by silently changing the metric, subset, comparator, or hypothesis.

Further reading: [NeurIPS Paper Checklist](https://neurips.cc/public/guides/PaperChecklist). Consult it as methodological reading; verify any venue-specific requirements separately.
