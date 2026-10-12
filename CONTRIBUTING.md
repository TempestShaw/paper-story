# Contributing

Improve how the skill handles real research decisions. Useful contributions include a minimal example of overclaiming, a missing evidence check, a clearer experimental decision, a new contribution type, or a shorter instruction with the same behavior.

## Propose a change

1. Describe the research task and the observable problem.
2. Provide a public or fictional input. Remove private manuscripts, personal data, credentials, and unpublished results unless their release is authorized.
3. Show the current behavior and the behavior the evidence actually justifies.
4. Keep changes to the smallest relevant instruction or reference. Link detailed guidance from `SKILL.md` rather than expanding the main file indefinitely.
5. Add or update a case in `evals/cases.json` when behavior changes.

Keep the English and Traditional Chinese README aligned for changes to installation, modes, or limitations. The agent-facing instructions remain in English, with responses following the user's requested language.

## Verify

- Validate the skill against the [Agent Skills specification](https://agentskills.io/specification), including directory name, required frontmatter, and relative resources.
- Check local Markdown links and JSON syntax.
- Exercise the changed behavior in a fresh agent conversation with only the skill and the input case. Evaluate it against the case criteria separately; do not leak the rubric to the acting agent.
- Record which cases were run, limitations, and any failures. A clean format check is not a behavioral evaluation.

Avoid adding invented results, unsupported novelty or award claims, claims of higher acceptance rates, or prompts that force all work into one narrative mold. Cite primary sources for external factual claims and retain the provenance distinction between inspiration and evidence.

Contributions are made under the repository's MIT license. Preserve attribution to third-party sources without importing material whose redistribution rights are unclear.
