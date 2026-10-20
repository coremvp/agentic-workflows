# Sources and best practices

The sources behind Agentic Workflows, the practices they inform, and the package
owners that apply them. **Last source review: 19 October 2026.**

Use this when maintaining the package. It is optional reference material, outside
the normal task preload. [README](README.md) owns installation/use; the
[package map](docs/package-map.md) lists every skill, procedure and support file.
Working instructions remain with their actual owners. The full case study and
private execution records remain local.

Official requirements, provider recommendations, empirical findings and our own
working choices have different authority. These sources do not certify this
package, grant permission or establish reliable delivery on every application.

## Contents

- [Practices worth retaining](#practices-worth-retaining)
- [Official guidance](#official-guidance)
- [Additional compiled guidance](#additional-compiled-guidance)
- [Inspected implementations](#inspected-implementations)
- [Search and distribution sources](#search-and-distribution-sources)
- [Empirical evidence](#empirical-evidence)
- [Maintaining the package](#maintaining-the-package)

## Practices worth retaining

| Practice | Actual package owner |
| --- | --- |
| Capture expertise, real corrections and host facts the model lacks; avoid generic expert personas. | The relevant domain skill and its conditional support |
| Describe a coherent job and activation boundary. Distinguish explicit, implicit and adjacent requests. | Each skill description; [Development](.agents/skills/development/SKILL.md) and [Marketing](.agents/skills/marketing/SKILL.md) routing |
| Keep entries focused, directly link deeper material and explain when to load it. | Each skill’s reference links; the package map records the full catalog |
| Match strictness to fragility. Use clear inputs, outputs, defaults and recovery; retain judgment where several approaches are valid. | Domain support and actual host rules |
| Add scripts/assets only when repeatability or quality justifies them. A source link does not prove an asset was inspected. | [Code](.agents/skills/code-agent/SKILL.md), production owner and [Taste](.agents/skills/taste/SKILL.md) |
| Inspect unfamiliar instructions, scripts, dependencies and network destinations before installation. Preserve host configuration. | [Installation contract](README.md#install-into-an-existing-repository) |
| Establish outcome/current behavior, alternatives, boundaries and meaningful proof before consequential design. | [Proposal](.agents/workflows/proposal.md) |
| Question requirements, delete/simplify, challenge missing/extra/misunderstood outcomes and false-success checks. | [Challenge](.agents/workflows/challenge.md) |
| Diagnose actual failure with competing hypotheses and a discriminating check; integrate through real callers/contracts. | [Debugging](.agents/skills/development/references/debugging.md) and [Implementation](.agents/workflows/implementation.md) |
| Check acceptance and rejection at the smallest actual owner. Distinguish source, mocked, replayed, runtime and audience evidence. | [Testing](.agents/skills/development/references/testing.md) and [engineering checks](.agents/skills/development/references/engineering-checks.md) |
| Independently inspect source/evidence, source-check proposed remedies and close admitted fixes without an unrelated audit. | [Review](.agents/skills/review-agent/SKILL.md) and [AI Code Review](.agents/workflows/ai-code-review.md) |
| Scale coordination, records and review to the task; stop at the requested phase. Questions include a recommendation, reason, tradeoff and one decision. | [Lead](.agents/skills/lead-agent/SKILL.md) and Development |
| Ground business truth in actual capability and customer evidence; compare current workarounds and switching forces. | [Product](.agents/skills/product/SKILL.md) and [positioning](.agents/skills/product/references/positioning.md) |
| Turn audience situations and competing interpretations into a bounded argument, channel and next decision. | Marketing and [customer research](.agents/skills/marketing/references/customer-research.md) |
| Distinguish a new brief, voiced draft and point edit. Deliver reader value early and preserve factual qualifiers and useful character. | [Writing](.agents/skills/writing/SKILL.md) |
| Diagnose access/indexability/canonical ownership/intent before tactics; deliberately select existing versus new content. | [SEO](.agents/skills/seo/SKILL.md) and [audit](.agents/skills/seo/references/audit.md) |
| Inspect reference pictures and render unsettled direction before app implementation; proceed within accepted direction afterward. | [Frontend](.agents/skills/frontend/SKILL.md) and [UI references](.agents/skills/frontend/references/ui-references.md) |
| Separate observation, interpretation, preference and audience evidence. Retain real feedback with context, exceptions and revision conditions. | Taste and [feedback method](.agents/skills/taste/references/studies.md#learn-from-actual-response) |
| Revisit model-dependent scaffolding. Preserve useful depth while deleting obsolete or redundant instructions. | Each existing owner; no automatic new skill or workflow |

Lead/Code/read-only Review is our working arrangement, not a prescribed provider
roster. Clear bounded work skips unnecessary phases. Human authority remains
separate from a plan or verdict; installing instructions does not authorize an
application exercise or expand the host’s permissions.

## Official guidance

Live documents were retrieved on the date above. Articles, code and papers retain
the dates or exact revision links below. Suggested line counts, scenario counts
and example metrics are authoring aids, not certification or measured results
for this package.

| Source | Retrieval/version treatment | Use in this assessment |
| --- | --- | --- |
| [Anthropic skill authoring](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/best-practices) | Live, retrieved 2026-10-19 | Specificity, structure, references and iteration |
| [Complete Guide for Claude](https://resources.anthropic.com/hubfs/The-Complete-Guide-to-Building-Skill-for-Claude.pdf) | 33-page PDF; distribution chapter says January 2026 | Use cases and separate activation/function/performance checks; dated advice flagged |
| [Updated Skill Creator](https://claude.com/resources/articles/improving-skill-creator-test-measure-and-refine-agent-skills) | Published 2026-03-03 | Capability vs preference, revision and model progress |
| [Anthropic Skill Creator source](https://github.com/anthropics/skills/blob/dbd4588f9e1033efb41dad4bef2f7947c8993d44/skills/skill-creator/SKILL.md) | `dbd4588f9e1033efb41dad4bef2f7947c8993d44`, commit dated 2026-10-09 | Actual authoring implementation; qualitative judgment and optional machinery |
| [Agent Skills engineering](https://www.anthropic.com/engineering/equipping-agents-for-the-real-world-with-agent-skills) | Published 2025-10-16; open-standard update 2025-12-18 | Dynamic resources and trust review |
| [Context engineering](https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents) | Published 2025-09-29 | Relevant context and continuity |
| [Building effective agents](https://www.anthropic.com/engineering/building-effective-agents) | Published 2024-12-19 | Conditional architecture patterns, not client schema |
| [Multi-agent research](https://www.anthropic.com/engineering/multi-agent-research-system) | Published 2025-06-13 | Assignments, independence and cost |
| [Long-running agents](https://www.anthropic.com/engineering/effective-harnesses-for-long-running-agents) | Published 2025-11-26 | Incremental progress and recoverable state |
| [Application harness design](https://www.anthropic.com/engineering/harness-design-long-running-apps) | Published 2026-03-24 | Evaluator limitations and removing obsolete scaffolding |
| [Demystifying evals](https://www.anthropic.com/engineering/demystifying-evals-for-ai-agents) | Published 2026-01-09 | Inspect transcripts and check graders against actual intended outcomes |
| [Claude best practices](https://code.claude.com/docs/en/best-practices), [skills](https://code.claude.com/docs/en/skills), [subagents](https://code.claude.com/docs/en/sub-agents), [memory](https://code.claude.com/docs/en/memory) | Live, retrieved 2026-10-19 | Planning proportionality, discovery, context, tools and instructions |
| [OpenAI Build Skills](https://learn.chatgpt.com/docs/build-skills) | Live, retrieved 2026-10-19 through official Docs MCP | Format, discovery, activation, resources and distribution |
| [OpenAI AGENTS.md](https://learn.chatgpt.com/docs/agent-configuration/agents-md), [subagents](https://learn.chatgpt.com/docs/agent-configuration/subagents) | Live, retrieved 2026-10-19 through official Docs MCP | Instruction hierarchy and actual permission inheritance |
| [Rethinking skills and prompts](https://developers.openai.com/blog/rethinking-skills-and-prompts-for-gpt-6-astra) | Published 2026-09-11 | Precise triggers, fewer mandatory reads and model-dependent scaffolding |
| [Testing skills systematically](https://developers.openai.com/blog/eval-skills) | Published 2026-01-22 | Outcome/process/style/effort distinction; older example paths qualified |
| [Harness-aware evaluation](https://developers.openai.com/cookbook/examples/partners/harness_aware_plugin_evals/harness_aware_plugin_evals) | Cookbook dated 2026-09-23 | Why lower-level tests do not establish product-harness behavior |
| [OpenAI Skill Creator source](https://github.com/openai/skills/blob/49f948faa9258a0c61caceaf225e179651397431/skills/.system/skill-creator/SKILL.md) | `49f948faa9258a0c61caceaf225e179651397431`, commit dated 2026-06-24 | Resources, duplicate guidance and optional metadata |
| [OpenAI harness engineering](https://openai.com/index/harness-engineering/) | Published 2026-02-11 | Inspectable feedback and explicitly limited application account |
| [Agent Skills specification](https://agentskills.io/specification), [authoring guidance](https://agentskills.io/skill-creation/best-practices), [output evaluation](https://agentskills.io/skill-creation/evaluating-skills) | Live, retrieved 2026-10-19 | Portable contract, coherent scope and real-task feedback |

Important current distinctions:

- Anthropic’s inspected creator encourages stronger trigger language to reduce
  missed activation; OpenAI warns broad triggers can load irrelevant skills.
  Diagnose the actual failure before widening or narrowing a description.
- The January guide’s limitation on Skill Creator evaluations was superseded by
  the March update. Old authoring examples are not current client schemas.
- Codex custom actors inherit effective parent permissions; per-agent sandbox or
  approval fields cannot create separate isolation. Our Review restriction there
  is behavioral. Claude Review’s Read/Grep/Glob list restricts exposed tools.
- Claude supports native AGENTS.md from v2.1.277 with precedence/settings caveats,
  imports and symlinks. Our chosen real CLAUDE.md symlink remains deliberate.
- Native actor configuration and loaded skills differ. Explicitly assign task
  and domain context; verify selected canonical paths when names collide.
- The supported installation is the complete ten-skill/four-procedure bundle.
  Cross-owner links prevent treating arbitrary folders as independent packages.
- Optional UI metadata and provider distribution machinery are not prerequisites
  here. Preserve the approved minimal package and the host’s actual settings.

## Additional compiled guidance

These sources were inspected during the broader study and remain useful for
their bounded topics. They introduce no runtime or installation dependencies.

| Primary source | Contribution and limit |
| --- | --- |
| [Writing effective tools for agents](https://www.anthropic.com/engineering/writing-tools-for-agents) | Clear non-overlapping responsibilities, compact useful outputs and realistic verification; no requirement to add tools here. |
| [Iterating development workflows with Codex](https://developers.openai.com/cookbook/examples/codex/iterating-development-workflows-with-codex) | Capture reusable decisions and frequent work; example goal/prompt/log layouts are optional. |
| [Execution plans](https://developers.openai.com/cookbook/articles/codex_exec_plans), archived | Historical milestone/resume ideas, not current client configuration or a mandatory artifact tree. |
| [Session memory](https://developers.openai.com/cookbook/examples/agents_sdk/session_memory) and [context personalization](https://developers.openai.com/cookbook/examples/agents_sdk/context_personalization) | Relevant decisions and contextual preferences; no required SDK, vector store or memory service. |

## Inspected implementations

Pinned source methods inform our own coherent implementation. They do not establish
verified customer outcomes, competitor rankings or private execution behavior.

| Source and inspected revision | Mechanism worth adapting | What we deliberately do not inherit |
| --- | --- | --- |
| [Superpowers](https://github.com/obra/superpowers/tree/bb92a77741419a4ab5f06e711a283343f1ada0c3): planning, systematic debugging, implementation/review prompts, receiving review and verification | Explicit outputs/interfaces/dependencies; a falsifiable debugging hypothesis and discriminating check; missing/extra/misunderstood requirements before quality | Compulsory worktrees, artifact forests, model escalation, fixed iteration quotas and proving unchanged work again for each completion message |
| [Spec Kit](https://github.com/github/spec-kit/tree/c6a4c18f1d01a8bec241c618eb6dfea952508744): plan/analyze/clarify/tasks/implement/checklist templates | Trace a requirement to implementation and proof; expose ambiguity, contradictions and ordering; research a material uncertainty | Mandatory IDs, intermediate document count, question quotas or a full phase structure for a small clear task |
| [REA](https://github.com/morluto/rea/tree/b0b485abff802b79d238dd24a9fa4abd0713d3ee): reverse-engineering entry, evidence workflows and recovery guidance | Discover the real target/tools; distinguish observation, inference and unknowns; constrain the final conclusion to the original question | Specialized engines, binary artifacts, automatic MCP installation and broad environment diagnosis for ordinary source work |
| [Corey’s marketing skills](https://github.com/coreyhaines31/marketingskills/tree/365b412152b9542499ca1439426f7fc3cc92bb65): product marketing/voice, customer research, CRO/forms, onboarding, writing/editing, content strategy, SEO | Turn actual situations into marketing decisions; identify switching forces and journey stage; derive voice from observable material; diagnose a draft before rewriting | A compulsory context database, fixed sample confidence/variants/scores, universal copy rules, paid-tool defaults or unsupported uplift statistics |
| [Illyism SEO skills](https://github.com/Illyism/seo-skills/tree/a47acc9d28ceebe5d4845cda29113a6c07781bca): SEO autopilot and blog refresher | Actual state → bounded priority → authorized correction → verification → later measurement; keep/modify/new before making a page | Daily whole-site rituals, automatic articles/merges, simulated ranking evidence, word-count targets or cosmetic freshness |
| [AgentsKit public demo](https://agentskit.co/demo) and [site](https://agentskit.co/) | Make the request, important decisions, work and finished result understandable without operating a specialist catalog | Claims about private installed instructions, routing or reliable autonomy: those were not inspected or executed |
| [X algorithm](https://github.com/xai-org/x-algorithm/tree/862a1235ca4d743cc48211309ebbbcc1a5a540a3): README, value-model adapter, scoring and parameters | Preserve useful specialist depth with a source pin and limits; distinguish filtering/ranking mechanics from a content recommendation | Turning coefficients into raw engagement exchange rates, guaranteed posting recipes or a promise of reach |

Keep outside authors out of the skill architecture. Source reputation, copied
catalogs and renamed files do not establish ownership or quality. Understand the
mechanism, adapt it to the actual job and take responsibility for the result.

## Search and distribution sources

| Primary source | Contribution and boundary |
| --- | --- |
| [Google: helpful content](https://developers.google.com/search/docs/fundamentals/creating-helpful-content) | Original useful contribution; no preferred word count or cosmetic freshness as a substitute for value. |
| [Google: title links](https://developers.google.com/search/docs/appearance/title-link) | Descriptive page-relevant titles; no guaranteed fixed character limit. |
| [Google: AI features](https://developers.google.com/search/docs/appearance/ai-features) | Established useful-content and technical discovery fundamentals; no invented separate AI-ranking ritual. |

Marketing’s source-bound [X algorithm reference](.agents/skills/marketing/references/x-algorithm.md)
is covered by the pinned implementation study above. Ranking coefficients do not
establish posting recipes, raw engagement exchange rates or guaranteed reach.

## Empirical evidence

Primary reports were inspected at these exact versions. Their experiments were
not reproduced; peer-review status was not independently established. None tested
this package. Different interventions, tasks, selection rules and baselines
prevent a pooled skills-uplift estimate. Efficiency, compliance and correctness
answer different questions.

### Repository context

| Primary study | Design and finding | Interpretation limit |
| --- | --- | --- |
| [Gloaguen et al., Evaluating AGENTS.md, v3](https://arxiv.org/html/2602.11988v3), 29 Sep 2026; first submitted 12 Feb | Four model/client configurations; 300 SWE-bench Lite and 138 CTXbench Python tasks. Generated files did not significantly improve resolution; mean inference cost increased about 20%/23%. Developer files gained 2.4 percentage points, not significant (`p=.21`). | This is session-level repository guidance. One completion per condition, Python-only, partly generated task material. Removing other docs changed the result, so “context never helps” is untenable. |
| [Lulla et al., On the Impact of AGENTS.md Files on the Efficiency of AI Coding Agents, v2](https://arxiv.org/html/2601.20404v2), 30 Mar 2026; first submitted 28 Jan | Codex/GPT-5.2-Codex, 124 small historical PR tasks across ten repos. Median runtime fell 28.64%; median output tokens fell 16.58%. | Comprehensive functional correctness was explicitly outside scope. Manual plausibility checks are not gold-test correctness. Median total tokens slightly increased. This is efficiency evidence, not equal-quality proof. |
| [Khatri, Do Context Files Help Coding Agents?, v1](https://arxiv.org/html/2607.27250v1), 28 Jul 2026 | 17 tasks, three Python repos, Claude/Codex and 288 evaluated runs. Compared none, always-loaded instructions and selective wiki retrieval; hidden tests found no detected correctness effect. | Only 15–17 task clusters; descriptive equivalence bounds were not powered equivalence tests. Selective content and injection channels differed. This cannot establish that all three approaches are equally good. |

### Conditional skills

| Primary study | Design and finding | Interpretation limit |
| --- | --- | --- |
| [Li et al., SkillsBench, v4](https://arxiv.org/html/2602.12670v4), 14 Jun 2026; first submitted 13 Feb | 87 tasks, eight domains, 18 model/harness configurations, matched conditions and three trials. Curated skills improved mean pass rate from 33.9% to 50.5%, a 16.6-point gain. | Quality-selected skills and exclusion of tasks without measurable skill separation make this an optimistic, skill-sensitive inventory. No length-matched control. Per-task skill-count/length groups are not randomized ablations. It establishes no universal three-skill cap. |
| [Han et al., SWE-Skills-Bench, v1](https://arxiv.org/html/2603.15401v1), 16 Mar 2026 | 49 relevant SWE skills, 565 requirement-driven tasks on pinned repos, Claude Code/Haiku 4.5. Pass rate increased 89.8% to 91.0%; mean tokens rose 10.5%. | Twenty-four skills already scored 100% in both conditions. Requirements/verifiers were generated; one configuration and no repeated-run uncertainty intervals in the inspected text. Its high baseline leaves much less improvement headroom than SkillsBench. |
| [Wang et al., Agent Skill Evolution, v1](https://arxiv.org/html/2610.04832v1), 4 Oct 2026 | 2,608 revision pairs; executable subset of 80 tasks/57 repos and four agents. Updated rules increased required-action compliance by 23 points across four agents; pooled blind human correctness increased 10 points across three judged agents. | Mechanically checkable changed directives were selected. The Sonnet correctness confidence interval crossed zero. On-demand loading retained 51% of the action gain, not 51% of correctness. Carrying an old body cost about 50% more episode tokens. Permission/prohibition rules were underrepresented. |
| [Jiang et al., Demystifying Agent Skills, v1](https://arxiv.org/html/2608.14036v1), 14 Aug 2026 | Skills and workflow memory distilled from prior trajectories; 8,135 normalized records, with 528 matched triples for the cited comparison. Skills scored 61.9%, workflow memory 55.9%, raw execution 59.1%. | The 6.06-point gain is versus workflow memory. Versus raw execution, 2.84 points had a confidence interval crossing zero. Larger retrieval pools reduced measured use precision without a corresponding general success collapse. This is not an installed-catalog limit. |

Resource findings remain mixed. Plausible navigation or redundancy explanations
do not establish why studies differ. A valid skill, discovery, relevant loading,
a followed instruction, a correct result and acceptable cost are separate evidence.

## Maintaining the package

1. Keep working instructions in the nearest existing owner. This document owns
   source rationale rather than another copy of the contract.
2. Pin inspected code/paper versions and date live documentation. Recheck material
   client facts before changing an adapter.
3. Distinguish requirements, recommendations, observed behavior and our policy.
   Flag superseded advice instead of silently treating it as current.
4. Preserve useful specialized depth with explicit load triggers. Remove duplicated
   or obsolete content for a reason, rather than a file-count target.
5. Improve from actual authorized work: intended result, important rejection cases,
   corrections and effort. Subjective judgment is not actual customer response.
6. Preserve host configuration, domain truth and learned Taste during intentional
   source updates. Copying files alone does not establish integration parity.

This reference introduces no new runtime, agent, workflow, evaluation suite or
publication authority. Package instructions and host constraints remain the
working contract.
