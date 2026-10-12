# Worked example: a promising improvement with an unresolved mechanism

**Fictional teaching example.** The project, counts, and budgets below are invented for illustration. They are not experimental results from the maintainer or a published paper. This is an authored example of the intended reasoning, separate from the validation runs.

## Input

> Use Paper Story in diagnose mode. A document-transformation agent succeeds on 91/100 simple tasks and 52/100 compound tasks. Our new version succeeds on 92/100 and 78/100 respectively. It adds named intermediate artifacts and a validator, and uses three times the inference tokens. There is only one training seed. We want to claim that ambiguous intermediate references are the root cause of compound-task failures. We can afford six evaluation runs over two days.

## Diagnosis

The current result is a **reported improvement for the combined intervention**. It does not identify which change caused the difference. Ambiguous references remain a plausible mechanism to test. The compound-task difference is 26 percentage points in this sample; one training seed and uninspected logs leave important uncertainty.

| Claim | Status | Current support | Main gap |
| --- | --- | --- | --- |
| The combined version improves compound-task success in this sample. | REPORTED | User-supplied counts: 52/100 versus 78/100. | Inspect per-task outcomes, failure handling, and evaluation comparability. |
| Ambiguous references cause the failures. | HYPOTHESIS | The intervention includes named intermediates. | Validator and token-budget changes are competing explanations. |
| The benefit transfers to new task families. | UNKNOWN | No supplied evidence. | An independently held-out family evaluation. |

**Provisional framing:** Investigate the reliability of intermediate-artifact handling under a controlled evaluation. A root-cause narrative would become justified only after evidence separates reference ambiguity from the competing explanations. Novelty requires a separate literature check.

## Six-run evaluation plan

First inspect the existing logs and freeze an unused confirmation set grouped by source document or task family. Use the same items, evaluator, decoding policy, and a declared token budget for paired comparisons. Treat this as an inference-stage diagnostic plan; it does not measure training-seed variability.

| Run | Configuration | Decision it informs |
| --- | --- | --- |
| 1 | Baseline at the original token budget | Anchor the original behavior under the new evaluation. |
| 2 | Baseline at the larger token budget | Test extra compute as an explanation. |
| 3 | Named artifacts only, at the larger budget | Isolate the representation change relative to run 2. |
| 4 | Validator only, at the larger budget | Isolate validation relative to run 2. |
| 5 | Named artifacts plus validator, at the larger budget | Estimate the combined intervention and its interaction. |
| 6 | Run 5 with a semantics-preserving change of intermediate names/ordering, at the same budget | Test sensitivity to presentation and possible naming shortcuts. |

Before running, define task success, valid-reference rate, error categories, cost, and how tool failures count. Have a small blinded manual audit check that the evaluator scores the intended task. Analyze paired task outcomes with uncertainty at the dependency-group level when feasible; do not claim that an item-level interval captures training variation.

If run 2 largely removes the improvement, weaken the representation explanation. If run 4 matches run 5, validation is a serious rival. If run 3 improves reference validity but not task success, keep those outcomes separate. If the sixth run fails, investigate presentation sensitivity; it alone does not prove the original mechanism. Treat apparent differences with insufficient precision as unresolved.

## Current defensible thesis

> Preliminary reported results motivate a controlled study of how intermediate-artifact representations and validation affect compound document-transformation tasks under matched inference budgets.

The next decision-changing action is a budget-matched baseline plus separated intervention comparison. A stronger title should wait for the result of that comparison.
