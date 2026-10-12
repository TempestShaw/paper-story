# Evaluation cases

These are synthetic task cases for checking whether the skill helps an agent maintain useful, evidence-calibrated behavior. They are not a benchmark of scientific creativity or publication outcomes.

## Run a case

1. Start a fresh agent conversation with the skill available.
2. Pass only the case's `prompt` and any specified artifacts to the acting agent. Do not include `required_behavior`, `failure_conditions`, prior outputs, or this evaluation discussion in its prompt.
3. Inspect its actual response against the criteria separately. Check calculations, scope, source status, task completion, and resource constraints.
4. Record the case ID, date, invocation conditions, output, observed failures, and reviewer judgment. A missing result should stay missing; it should not be filled from the rubric.
5. If instructions change, rerun the affected case in a fresh context. Do not treat a corrected response with leaked feedback as an independent success.

The cases include research diagnosis, drafting before experiments, narrow copyediting, rebuttals, metric validity, theoretical work, unverified novelty, and negative results. A model may satisfy a case in many ways; evaluate behavior rather than matching a preferred phrase.

## Interpret results

Separate structural validation from task behavior. A valid `SKILL.md` does not prove the instructions work. A few successful examples do not establish consistency across models or superiority to an agent without the skill.

Treat a fabricated result, citation, completed action, or universal claim unsupported by the input as a material failure. Treat an unnecessary extra paragraph in a narrow edit as a scope problem. Record partial success and remaining uncertainties rather than converting everything into a single acceptance-like score.

See [cases.json](cases.json) and the [initial validation record](validation.md). To estimate incremental benefit, run a separately designed comparison with and without the skill using held-out tasks and blinded assessment; that comparison has not been performed here.
