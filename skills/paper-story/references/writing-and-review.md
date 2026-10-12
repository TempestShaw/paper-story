# Writing and reviewing a defensible argument

Use this guide to turn the evidence ledger into readable manuscript text. Adapt the structure to the discipline and contribution type. Keep argument repair and copyediting distinct.

## Start with the reader's unresolved question

State the consequential problem in its actual setting. Explain what current knowledge or practice cannot establish, using the closest relevant sources. Identify the observation or idea that changes the question. Then explain why the chosen analysis or method addresses it and what the evidence permits the reader to conclude.

Avoid reconstructing the project's chronology. A list of modules is not a contribution statement; explain the claim each module helps test or achieve. Do not exaggerate the weakness of prior work to create a gap. Credit the strongest relevant predecessor and state exactly what remains different.

For a replication, state the claim and conditions being checked. For a negative result, explain the expectation being tested and the scope of the null or adverse finding. For a theory paper, prioritize definitions, theorem statements, assumptions, proof ideas, and consequences. No form requires a new architecture or a SOTA table.

## Calibrate the claim

| Available support | Appropriate formulation | Overreach to repair |
| --- | --- | --- |
| A selected failure example | “We exhibit a failure under [conditions].” | “Current systems generally fail.” |
| A sampled descriptive study | “We observe [pattern] in [population/protocol].” | “This establishes the cause.” |
| Fair comparative evaluation | “A improves [metric] over [comparators] under [budget].” | “A is universally superior.” |
| A mechanism still being tested | “We hypothesize [mechanism] and test [prediction].” | “We identify the root cause.” |
| A supported causal estimate | “Under [identification conditions], changing X affects Y in [setting].” | “X explains every observed failure.” |
| A valid bounded theorem | “Under assumptions A–C, we prove P.” | “Our theorem guarantees real-world performance.” |
| An unvalidated proxy improvement | “The method improves [proxy]; relevance to [outcome] remains to be tested.” | “The method improves human outcomes.” |

Do not remove a limitation merely because it weakens a hook. A precise boundary often explains why the result is useful.

## Build an abstract

Fit the target length and actual paper type. Include the question and setting, the gap, the specific contribution, the strongest available evidence, and the main implication or boundary. Compress background before compressing the central result.

When results are unavailable, still produce the requested draft. Write a proposal abstract or use an explicit placeholder such as `[RESULT NEEDED: held-out task-success difference and interval]`. Do not replace absent results with “extensive experiments demonstrate” or invented numbers. Keep a separate, short note listing unresolved facts; do not bury placeholders in a polished passage.

For user-reported results, preserve their values and mark provenance in the accompanying notes. Do not silently promote them to checked facts. When a rate changes from 60% to 66%, state six percentage points or 10% relative improvement; use the intended quantity consistently.

## Build an introduction and contribution list

Organize paragraphs by their role in the argument rather than a fixed count:

1. Establish a concrete problem and why its solution matters.
2. Identify the unresolved limitation of the closest work in the relevant regime.
3. Introduce the insight, hypothesis, or question; distinguish which one it is.
4. Explain the approach and why it addresses that issue.
5. State the contributions, available evidence, and scope.

Make each contribution independently checkable. “We identify [phenomenon] in [protocol],” “we introduce [specific construction],” and “we establish [bounded property]” are different claims with different evidence burdens. Avoid splitting one idea into several near-identical contribution bullets. Mention numerical gains only with a named metric, comparison, setting, and evidence status.

Audit title and opening paragraph for broader claims than the body supports. Remove generic claims such as “first,” “universal,” “fundamental,” or “solves” unless their exact scope is substantiated. A neutral title can communicate a strong result without a manufactured paradox.

## Connect figures and experiments

Give each main figure a reader question and claim ID before deciding its visual form. Use diagrams for architecture or hypothesized mechanisms, curves for a controlled relationship, and tables for exact comparisons. Clearly distinguish a conceptual schematic from measured evidence.

Captions should state the setting, comparison, metric direction and units, aggregation, uncertainty definition where present, and bounded takeaway. Include failure regions and comparison budgets where material. Do not use a cherry-picked qualitative example as evidence of prevalence or general superiority.

In results prose, separate observation from interpretation: identify the measured contrast, quantify its uncertainty where available, assess the competing explanation, and delimit the conclusion. A failed mechanism test can coexist with a useful engineering improvement; preserve that distinction.

## Review with localized objections

Begin with a faithful account of the contribution and the strongest evidence. Raise an objection only when you can identify its target and consequence. Use “the manuscript does not report X” when information is missing; do not infer “the authors did not do X.”

Prioritize a concern affecting the central conclusion over a cosmetic omission. Check relevant dimensions: distinction from closest work, support for the core claim, causal identification, measurement validity, fair comparison, generalization, cost, reproducibility, and clarity. Avoid prescribing an experiment that cannot change any substantive conclusion.

For each concern, give the smallest repair and an honest fallback claim. A prose clarification, reanalysis, sensitivity check, new experiment, and narrower conclusion are different remedies. Do not invent numerical acceptance probabilities or pretend to speak for a real program committee.

## Respond to reviewers

Quote or accurately summarize each actual concern. Answer it directly before giving context. Cite the relevant section, table, or new artifact, then state the manuscript change. Separate existing evidence, completed new work, and proposed work. If the concern is correct, acknowledge it and adjust the claim.

Do not imply a proposed experiment was performed or that a manuscript was edited when only suggested wording exists. Do not promise infeasible work to deflect criticism. Where a reviewer requests an unfair comparison, explain the mismatch and offer a comparison that addresses the underlying question.

Check venue rules about rebuttal length, additional results, anonymity, and AI assistance against current primary sources before applying them. The skill supplies reasoning guidance, not an authoritative venue policy.
