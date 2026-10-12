# Argument archetypes and evidence requirements

Treat these patterns as optional heuristics for making a contribution legible. They are neither exhaustive categories nor causal predictors of acceptance. Selected successful papers cannot establish that adopting a pattern improves acceptance. Negative results, replications, careful measurements, and incremental contributions can stand on their own.

Choose **one primary archetype and at most one secondary archetype**, or choose none. Add a secondary only when it supports the same central claim with adequate evidence. Do not assemble several weak stories into an apparently strong one.

Before drafting, fill the argument skeleton, identify the strongest plausible alternative explanation, and specify what result would change the claim. Separate evidence already obtained from proposed experiments. Treat the requirements below as starting points: the design must match the actual estimand, domain, and scope.

## Contents

- [1. Diagnose a mechanism before proposing a remedy](#1-diagnose-a-mechanism-before-proposing-a-remedy)
- [2. Test a consequential default assumption](#2-test-a-consequential-default-assumption)
- [3. Use theory to explain empirical behavior](#3-use-theory-to-explain-empirical-behavior)
- [4. Build a benchmark that reveals meaningful failures](#4-build-a-benchmark-that-reveals-meaningful-failures)
- [5. Establish real-world or social consequences](#5-establish-real-world-or-social-consequences)
- [6. Offer a useful unifying abstraction](#6-offer-a-useful-unifying-abstraction)
- [Select and revise the argument](#select-and-revise-the-argument)

## 1. Diagnose a mechanism before proposing a remedy

- **When justified:** Use when a recurring failure has a testable mechanism, and explaining that mechanism materially changes which remedy should work. A performance gain alone does not identify a root cause.

- **Argument skeleton:** “[Failure] arises through [mechanism] under [conditions]; intervening on [mechanism] changes [outcome], motivating [remedy] within [scope].”

- **Minimum evidence:** Measure the proposed mechanism separately from the outcome. Manipulate it with appropriate controls, test a competing explanation, and account for changes in data, capacity, compute, and tuning. Check the direction and strength of the predicted response. Empirical causal claims require interventions or a defensible identification strategy with explicit confound controls and assumptions.

- **Decisive falsification or alternative:** The outcome remains unchanged after a successful manipulation, a different mechanism predicts the response equally well, or an intervention changes an uncontrolled factor that explains the benefit. Distinguish a failed manipulation from evidence against the hypothesis.

- **Useful figure:** Plot intervention strength against mechanism measurements and outcomes, with uncertainty and control conditions.

- **Common overclaim:** Calling one contributing factor “the fundamental cause,” or treating an ablation as complete causal identification.

- **Downgrade path:** Report a reproducible failure pattern and an associated factor. Present the mechanism as a working hypothesis; evaluate the remedy's practical utility as a separate claim.

## 2. Test a consequential default assumption

- **When justified:** Use when a documented assumption influences current methods or evaluation, and relaxing it produces a meaningful, testable difference. Establish that the assumption is actually used in the relevant setting; do not manufacture a consensus to overturn.

- **Argument skeleton:** “[Assumption] is unnecessary or unreliable for [task] in [regime], because [controlled evidence] supports [qualified replacement].”

- **Minimum evidence:** Cite the assumption accurately from primary sources. Define its scope and the consequence of rejecting it. Compare strong implementations under matched information, resources, and tuning opportunities. For a negative claim, use sensitivity or power analysis to show which effect sizes the experiment could detect; an inconclusive result is not equivalence.

- **Decisive falsification or alternative:** The finding disappears after fair tuning, depends on a changed objective, or results from information available only to the challenger. A strong counterexample can refute a universal claim without establishing how commonly the alternative works.

- **Useful figure:** Show both approaches across the variable that marks the assumption's boundary, including crossover and failure regions.

- **Common overclaim:** “The field is wrong,” when the evidence identifies a restricted exception or an implementation weakness.

- **Downgrade path:** State a boundary condition, counterexample, replication discrepancy, or competitive alternative. Remove contrarian language if no consequential default has been established.

## 3. Use theory to explain empirical behavior

- **When justified:** Use when a formal model yields informative predictions about an observed phenomenon, clarifies a mechanism, or identifies conditions for success and failure. A theorem added for appearance provides no explanatory contribution.

- **Argument skeleton:** “Under [assumptions], [model or result] predicts [observable behavior], which [tests] support within [regime] and bound outside it.”

- **Minimum evidence:** State assumptions, quantities, proof obligations, and the mapping from mathematical objects to measurements. Verify proof correctness and whether the result is nonvacuous at relevant scales. Test predictions beyond observations used to formulate or fit the explanation, and compare with a simpler competing model. Separate formal guarantees from empirical support for their applicability.

- **Decisive falsification or alternative:** A discriminating prediction fails where the assumptions hold, the proposed mapping cannot be measured, or a simpler model predicts equally well. Failure outside the theorem's assumptions limits applicability; it does not by itself disprove the theorem.

- **Useful figure:** Overlay predicted and observed behavior with uncertainty, parameter provenance, and regions where assumptions hold or fail.

- **Common overclaim:** Presenting a stylized proof as an explanation of a full system without validating the connecting assumptions.

- **Downgrade path:** Offer a restricted theorem, descriptive model, or mechanistic conjecture. Remove unsupported explanatory claims rather than decorating an empirical result with theory.

## 4. Build a benchmark that reveals meaningful failures

- **When justified:** Use when existing evaluations miss a clearly defined capability, risk, or operating condition, and a new measurement can distinguish relevant behavior. Difficulty alone does not establish a useful construct.

- **Argument skeleton:** “Existing evaluations undermeasure [construct]; [benchmark] measures [operational definition] and reveals [failure] across [evaluated systems and conditions].”

- **Minimum evidence:** Justify construct validity, task selection, population coverage, annotation quality, and scoring. Document provenance, contamination checks, train/test separation, and development decisions. Include strong baselines, relevant human or reference performance, uncertainty, and subgroup or difficulty analyses. Test whether scores respond to the intended capability rather than shortcuts, formatting, or irrelevant burdens. Use a held-out confirmation set when failures guided construction.

- **Decisive falsification or alternative:** Ambiguous labels, leakage, unrealistic sampling, excessive linguistic complexity, or arbitrary scoring explain the ranking. A shortcut method succeeds without the target capability, or valid solutions receive low scores.

- **Useful figure:** Pair a capability-by-system results matrix with uncertainty and representative scored examples showing what each failure category means.

- **Common overclaim:** Treating benchmark failure as inability in general, or claiming real-world relevance from synthetic difficulty alone.

- **Downgrade path:** Present a diagnostic collection, stress test, or exploratory dataset with explicit coverage limits. Preserve useful observations while withholding broad rankings or capability claims.

## 5. Establish real-world or social consequences

- **When justified:** Use when the research changes an outcome relevant to identifiable people or institutions, and the link from technical behavior to that outcome can be examined. Significance depends on evidence about consequences, not on adding an impact paragraph.

- **Argument skeleton:** “For [population] in [setting], [intervention or observed practice] changes or is associated with [relevant outcome] by [supported magnitude], subject to [costs and limits].”

- **Minimum evidence:** Define stakeholders, setting, comparator, outcome, and time horizon. Distinguish direct outcomes from proxies. Assess heterogeneity, error costs, feasibility, and distribution of benefits and burdens. Support causal language with an intervention or credible identification and confound controls. State selection, attrition, measurement, and transportability assumptions; simulation or laboratory evidence does not establish deployment impact.

- **Decisive falsification or alternative:** A proxy improves while the intended outcome does not, adoption or workflow costs erase benefits, a subgroup bears substantial harm, or selection and concurrent changes explain the association.

- **Useful figure:** Show outcomes and costs against the relevant comparator, disaggregated where justified, with uncertainty and the actual observation horizon.

- **Common overclaim:** Claiming societal benefit from accuracy gains, stakeholder consultation, or an untested deployment scenario.

- **Downgrade path:** Report technical feasibility, laboratory efficacy, stakeholder evidence, or an observed association. Describe anticipated impact as a hypothesis and name the field evidence still needed.

## 6. Offer a useful unifying abstraction

- **When justified:** Use when a common representation explains previously separate methods, reduces meaningful complexity, or generates testable predictions and designs. Renaming shared notation is insufficient.

- **Argument skeleton:** “[Abstraction] recovers [prior cases] through [explicit mapping] and enables [new prediction, simplification, or capability] under [conditions].”

- **Minimum evidence:** Derive the mappings and identify exceptions, lost information, and required assumptions. Show what the abstraction makes easier to explain, implement, analyze, or predict. Compare with existing organizing frameworks. If claiming simplicity, define its unit: assumptions, parameters, components, runtime, or description length. Evaluate downstream tradeoffs and account for complexity shifted into preprocessing, tuning, or infrastructure.

- **Decisive falsification or alternative:** Important cases require arbitrary special handling, the abstraction loses distinctions necessary for prediction, or apparent simplicity merely relocates effort. Check whether an established framework gives the same insight with fewer assumptions.

- **Useful figure:** Map prior cases into the common representation, marking exact correspondences, approximations, exceptions, and a new consequence that can be tested.

- **Common overclaim:** “A universal framework” based on a few favorable examples, or “simpler” based only on fewer displayed equations.

- **Downgrade path:** Offer a taxonomy, restricted equivalence, conceptual perspective, or implementation simplification. Keep the mappings useful while narrowing claims of unification and generality.

## Select and revise the argument

Choose the pattern whose decisive evidence is strongest, not whose title sounds most ambitious. Put missing evidence into the experiment plan rather than the abstract. If results contradict the initial story, update the claim and preserve the contradiction in the report. A narrow result with a clear boundary can be the complete contribution.
