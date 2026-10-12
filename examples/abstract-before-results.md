# Worked example: drafting before experiments finish

**Fictional teaching example.** This is an authored example, not a claim that an experiment was run. The skill should still produce useful text when results are missing.

## Input

> Draft an abstract for a request scheduler that groups jobs by predicted service time. We will compare latency and fairness with first-come-first-served and a deadline scheduler on synthetic workloads and an anonymized trace. Experiments have not run. Our hypothesis is that grouping reduces queueing, but fairness might deteriorate with heavy-tailed arrivals.

## Draft

Request schedulers must balance responsiveness with equitable service across heterogeneous workloads. We propose grouping requests by predicted service time to examine whether this structure reduces queueing without unacceptable fairness costs. We plan to compare the scheduler with first-come-first-served and a deadline-based alternative on synthetic workloads and an anonymized trace, measuring latency, per-group waiting time, and sensitivity to heavy-tailed arrivals. [RESULT NEEDED: matched-load comparisons, uncertainty, and observed fairness tradeoffs.] The study will characterize the operating conditions under which service-time grouping is useful and identify regimes in which prediction error or unequal waiting costs limit its applicability.

## Why this wording is appropriate

It distinguishes implementation and hypothesis from an unexecuted evaluation. It names the comparators, outcomes, and potential failure regime. It leaves the result visibly unresolved and avoids claiming completed validation, novelty, or superiority.
