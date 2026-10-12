# Sources and provenance

Checked on 2026-10-11. This file distinguishes inspiration, selected bibliographic checks, and methodological reading. It is not a systematic review or a causal study of paper acceptance.

## Inspiration

This skill was inspired by user-supplied text titled **“Story Is All You Need：扒透35篇顶会最佳/杰出论文的叙事密码，我们找到了六大范式”**, attributed in that text to **人工智能学社**. Its original publication URL and date were not independently verified. The title's “35” describes the supplied article's selection; this repository does not claim to have audited every paper or every technical summary.

The article motivated six lenses: mechanism diagnosis, revising assumptions, explanatory theory, diagnostic evaluation, real-world impact, and unification. The instructions, decision rules, templates, and fictional examples here are an original operational synthesis. The article text, screenshots, paper figures, and comments are not redistributed.

Treat a selected set of award winners as examples for reflection. It does not establish how prevalent these lenses are among all submissions, whether they caused awards, or whether using them changes acceptance probability. Those questions require an appropriate comparative design, explicit coding, and attention to selection effects. Do not repeat unverified submission-volume or reviewer-time claims as facts.

## Selected award records

These records support the award labels below. They do not validate every technical description in the supplied article or establish a reason for the award beyond what the official source actually says.

| Article shorthand | Bibliographic clarification | Verified award | Primary record |
| --- | --- | --- | --- |
| D4RT | Efficiently Reconstructing Dynamic Scenes One D4RT at a Time | CVPR 2026 Best Paper | [CVPR announcement](https://cvpr.thecvf.com/Conferences/2026/News/Best_Papers) |
| Transformers are Succinct | Transformers are Inherently Succinct | ICLR 2026 Outstanding Paper | [ICLR announcement](https://blog.iclr.cc/2026/04/23/announcing-the-iclr-2026-outstanding-papers/) |
| LLMs Get Lost | LLMs Get Lost In Multi-Turn Conversation | ICLR 2026 Outstanding Paper | [ICLR announcement](https://blog.iclr.cc/2026/04/23/announcing-the-iclr-2026-outstanding-papers/) |
| Lychee-FD | A method name; the official title begins “Hierarchical Acoustic-Semantic Modeling” | ACL 2026 Outstanding Paper | [ACL awards list](https://2026.aclweb.org/program/best_papers/) |
| STEER | A method name; the official title begins “Rethinking Entropy Interventions in RLVR” | ACL 2026 Outstanding Paper | [ACL awards list](https://2026.aclweb.org/program/best_papers/) |
| GeoRA | GeoRA: Geometry-Aware Low-Rank Adaptation for RLVR | ACL 2026 Outstanding Paper | [ACL awards list](https://2026.aclweb.org/program/best_papers/) |

The ACL list contains three main best-paper entries and eighteen Outstanding entries: 21 in those categories, counted from the official page. It also includes theme, resource, social-impact, demonstration, and student-workshop categories. Thus “21” is not an exhaustive count of all ACL award categories. The source article also selects particular categories at other conferences; do not advertise its selection as an exhaustive awards catalog.

## Research-reporting foundations

| Source | Why consult it | Limit |
| --- | --- | --- |
| [NeurIPS Paper Checklist](https://neurips.cc/public/guides/PaperChecklist) | Check alignment of claims with demonstrated scope, assumptions, limitations, reproducibility details, and statistical reporting. | Verify the current target venue's requirements separately. |
| [Pineau et al., 2021, Improving Reproducibility in Machine Learning Research](https://jmlr.org/papers/v22/20-303.html) | A primary report on the NeurIPS reproducibility program and its approach to improving experimental transparency. | It is not an evaluation of this skill. |
| [Dodge et al., 2019, Show Your Work: Improved Reporting of Experimental Results](https://aclanthology.org/D19-1224/) | Consider model selection and hyperparameter-search budgets when interpreting comparisons. | Match the resource policy to the actual research question. |

The six-lens taxonomy and this workflow are editorial and methodological heuristics. Their utility must be checked on actual research tasks. No publication, citation, or award outcome is promised.

## Packaging and installation references

- [Agent Skills specification](https://agentskills.io/specification): required metadata, folder naming, optional resources, and progressive loading.
- [Skills CLI](https://github.com/vercel-labs/skills): repository discovery and installation using `npx skills add` with a named skill. Client support and installation behavior can change; consult its current documentation.

## Attribution and reuse

The repository's MIT license covers its original files. Linked articles, papers, conference pages, and software retain their respective rights and licenses. Cite their original sources when discussing their findings; this file does not replace reading a paper or confer rights to reproduce its figures.
