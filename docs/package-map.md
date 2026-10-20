# Package map

Find the skill, procedure or reference for your task. The package contains
**ten skills**, **four engineering procedures** and **42 supporting references**.
The tables explain what each file helps with and when to load it.

This human reference is outside the installed instruction context. The
[README](../README.md) owns installation/use. An installed task starts from its selected skill,
reads the host's own instructions, and follows only relevant support links.

## Complete skeleton

The tables below enumerate every canonical instruction file and its trigger.
Paths are relative to the package root; links lead to the actual file.

| Surface | Files and installation job |
| --- | --- |
| Root | [README.md](../README.md) for installation/use; [AGENTS.md](../AGENTS.md) for package maintenance only; [LICENSE](../LICENSE); `.gitignore` for local scratch |
| Canonical content | `.agents/skills/<owner>/SKILL.md` plus every reference listed below; `.agents/workflows/` contains the four procedures |
| Codex actors | [.codex/agents/code-agent.toml](../.codex/agents/code-agent.toml), [.codex/agents/review-agent.toml](../.codex/agents/review-agent.toml) |
| Claude actors | [.claude/agents/code-agent.md](../.claude/agents/code-agent.md), [.claude/agents/review-agent.md](../.claude/agents/review-agent.md) |
| Claude skill discovery | Ten real links `.claude/skills/{code-agent,development,frontend,lead-agent,marketing,product,review-agent,seo,taste,writing}` to their matching `../../.agents/skills/<name>` directory |
| Shared project instructions | Real `CLAUDE.md -> AGENTS.md`; the package maintenance file must not replace a host application's instructions |
| Human design reference | This file; optional to copy, never mandatory preload |
| Transient evidence | Ignored `tmp/`; not installed or published as canonical instruction content |

Native definitions inherit client defaults. Claude Review has only
Read/Grep/Glob; Codex Review follows a behavioral read-only contract and inherits
the parent's effective permissions. See the README's
[native limits](../README.md#native-discovery-and-permission-limits).

### Ten entry skills

| Skill and file | Responsibility | Load when |
| --- | --- | --- |
| [Development](../.agents/skills/development/SKILL.md) | Host discovery, phase routing and real-owner proof; choose direct/design-bearing/selected-phase effort before procedure; concrete risk/testing/debugging routes | Authorized engineering outcome or selected engineering phase |
| [Lead](../.agents/skills/lead-agent/SKILL.md) | Main conversation, material decisions, bounded assignments and one useful continuation record; proportional handoffs and exact resume state | Coordination, decision, scope or continuity is needed |
| [Code](../.agents/skills/code-agent/SKILL.md) | Authorized code/prose/media production and integration; sole check execution; scratch and factual-claim boundaries; readable evidence scaled to target | Production, checks or accepted fixes are assigned |
| [Review](../.agents/skills/review-agent/SKILL.md) | Independent read-only investigation and closure; source-bound remedies and actual acceptance verdict; no writes, execution or delegation | Independent assessment is selected |
| [Product](../.agents/skills/product/SKILL.md) | Actual user outcome/business truth; alternatives, switching forces, evidence and bounded recommendation | Outcome, value, rights or business direction is consequential |
| [Frontend](../.agents/skills/frontend/SKILL.md) | Inspected visual references, rendered unsettled direction, real agreement and accepted momentum; interaction/accessibility depth | Visual/UI work, selected interaction or consequential visual choice |
| [Marketing](../.agents/skills/marketing/SKILL.md) | Audience/job/argument/proof/channel/learning; acquisition, attempt, first-value and continued-use diagnosis before tactics | Customer research, communication, launch, campaign or distribution decision |
| [Writing](../.agents/skills/writing/SKILL.md) | Reader/medium/source/voice; select blank brief, voiced draft or point edit; deliver the promise and revise the consequential weakness | Prose production or assessment |
| [SEO](../.agents/skills/seo/SKILL.md) | Intent/canonical ownership/discoverability; ordered symptom/evidence/layer/correction/verification method | Search or crawler-facing behavior is material |
| [Taste](../.agents/skills/taste/SKILL.md) | Observe/compare/critique/revise; derive contextual voice/visual judgment; preserve latest accepted direction and real feedback | Consequential creative judgment or useful actual feedback |

### Four engineering procedures

| Procedure and file | Output and method |
| --- | --- |
| [Proposal](../.agents/workflows/proposal.md) | Real problem, success/rejection criteria, actual owner/source, compatible primary guidance, meaningful alternatives, reason for new moving parts and proof plan |
| [Challenge](../.agents/workflows/challenge.md) | Independent attack on requirements, deletion/simplification, ownership/failures, false-success proof and material unresolved choices; Lead resolves findings |
| [Implementation](../.agents/workflows/implementation.md) | Bounded accepted change integrated through actual callers/contracts, debugging when relevant, meaningful real-owner checks and resumable handoff |
| [AI Code Review](../.agents/workflows/ai-code-review.md) | Missing/extra/misunderstood behavior pass, source trace, conditional risk investigation, severity/evidence findings, admitted fixes and focused closure |

Clear bounded work skips fresh Proposal/Challenge. A selected phase stops at its
output. Ordinary content does not inherit these engineering procedures. These
routes preserve actual authority and independent Review without prescribing a
large packet or new actor for every mechanical edit.

## All supporting references

Each reference belongs to the skill named below. Load the guides relevant to
the current decision; an ordinary task does not need the entire library.

### Development: four references

| Final reference | Use | Conditional trigger |
| --- | --- | --- |
| [content-systems.md](../.agents/skills/development/references/content-systems.md) | author/model/permissions/preview/publish/cache/search trace, provider choice, migrations and publication truth | Technical CMS, editorial model, preview or publishing integration |
| [engineering-checks.md](../.agents/skills/development/references/engineering-checks.md) | relevant boundary/failure questions across authority, data, runtime, compatibility, config and UI; concrete non-web paths | A changed behavior crosses a consequential technical boundary |
| [testing.md](../.agents/skills/development/references/testing.md) | acceptance/rejection to smallest actual owner, false-success checks, baseline attribution, honest mocks/skips and invalidators | Select or assess meaningful proof |
| [debugging.md](../.agents/skills/development/references/debugging.md) | observed/expected, competing hypotheses, working comparison, discriminating evidence and root-cause fix | An actual supplied failure needs diagnosis/fix |

### Frontend: two references

| Final reference | Use | Conditional trigger |
| --- | --- | --- |
| [ui-references.md](../.agents/skills/frontend/references/ui-references.md) | discover examples by navigation/form/list/table/dashboard/chart/onboarding/landing problem; inspect the mechanism | Need useful visual/interaction reference discovery |
| [visual-discussion.md](../.agents/skills/frontend/references/visual-discussion.md) | actual pictures/current/proposal, distinct information jobs, real choice, rejection and accepted momentum; scratch/image fallback | Visual direction is unsettled or disputed |

### Marketing: fifteen references

| Final reference | Use | Conditional trigger |
| --- | --- | --- |
| [ab-testing.md](../.agents/skills/marketing/references/ab-testing.md) | feasibility, exposure/allocation/outcome, guardrails, power limits and alternatives | A real experiment decision is justified |
| [channel-strategy.md](../.agents/skills/marketing/references/channel-strategy.md) | audience encounter, awareness, evidence, account access and effort | Choose where/how a supported argument reaches a reader |
| [content-promotion.md](../.agents/skills/marketing/references/content-promotion.md) | distinct encounter jobs, useful sequencing, proof reuse and attribution limits | Distribute an existing supported asset |
| [content-strategy.md](../.agents/skills/marketing/references/content-strategy.md) | existing canonical answer versus justified new work; reader contribution, evidence and effort priority | Select or order content work |
| [conversion.md](../.agents/skills/marketing/references/conversion.md) | eligible attempts/durable completion; distinguish visitor, comprehension, trust, failure and value problems | Diagnose a specific conversion/value gap |
| [customer-research.md](../.agents/skills/marketing/references/customer-research.md) | episodes/context, deduplication, contrary evidence, interpretation and decision | Understand a customer problem or test a consequential assumption |
| [form-optimization.md](../.agents/skills/marketing/references/form-optimization.md) | field necessity/sensitivity, validation/recovery, server authority, mobile/focus and actual completion | A form is the consequential user path |
| [interviews-and-surveys.md](../.agents/skills/marketing/references/interviews-and-surveys.md) | behavioral recruiting, non-leading questions, disconfirmation and sample limits | Design or interpret interviews/surveys |
| [launch-readiness.md](../.agents/skills/marketing/references/launch-readiness.md) | dependencies of the actual promised path, owners/evidence/holds and recovery | The request asks readiness for a specific launch promise |
| [launch.md](../.agents/skills/marketing/references/launch.md) | availability, eligibility, user effect, proportionate release form and encounter | Plan a launch or release communication |
| [release-communication.md](../.agents/skills/marketing/references/release-communication.md) | change-to-effect translation, audience/starting state, beta/disabled distinctions, source-bound promises | Explain a delivered or planned release |
| [research-sources.md](../.agents/skills/marketing/references/research-sources.md) | source choice by uncertainty, access/currentness, untrusted-source treatment and limits | Need external evidence for a marketing decision |
| [social-media-specs.md](../.agents/skills/marketing/references/social-media-specs.md) | current account/surface constraints, crop/playback/caption checks rather than frozen limits | Produce or inspect a social asset |
| [social-research.md](../.agents/skills/marketing/references/social-research.md) | inspect comparable work and responses, include weaker examples, separate mechanism from causal claims | Study social work for a consequential choice |
| [x-algorithm.md](../.agents/skills/marketing/references/x-algorithm.md) | pinned primary ranking/filtering/prediction/diversity mechanics and coefficient limits | X distribution mechanics matter to the actual decision |

### Product: one reference

| Final reference | Use | Conditional trigger |
| --- | --- | --- |
| [positioning.md](../.agents/skills/product/references/positioning.md) | buying situation, current workaround/alternatives, switching forces, supported mechanism, objection/proof and next action | Positioning, value or switching choice |

### SEO: seven references

| Final reference | Use | Conditional trigger |
| --- | --- | --- |
| [audit.md](../.agents/skills/seo/references/audit.md) | source/raw HTML/text/DOM/search-data limits; diagnose failing discovery layer and smallest correction | Investigate a search/discovery symptom |
| [international-seo.md](../.agents/skills/seo/references/international-seo.md) | locale graph, canonical/hreflang/sitemap/origin consistency and useful translation | Multiple locales/regions are actually served |
| [local-pages-and-measurement.md](../.agents/skills/seo/references/local-pages-and-measurement.md) | real distinct local page job, doorway risks and stage-specific measurement | Local landing pages or measurement |
| [local-profiles-and-citations.md](../.agents/skills/seo/references/local-profiles-and-citations.md) | actual business eligibility, identity/privacy, duplicates and current provider rules | A real business profile/citation problem |
| [local-seo.md](../.agents/skills/seo/references/local-seo.md) | separate local-business eligibility from useful organic answers; select relevant support | A local search request |
| [search-opportunities.md](../.agents/skills/seo/references/search-opportunities.md) | query/page evidence, actual intent/overlap, existing owner versus new page, bounded priority | Choose a justified search/content opportunity |
| [title-tags.md](../.agents/skills/seo/references/title-tags.md) | diagnose page/query/title mismatch, descriptive title and presentation-width limits | A title change is the supported correction |

### Taste: three references

| Final reference | Use | Conditional trigger |
| --- | --- | --- |
| [creative-direction.md](../.agents/skills/taste/references/creative-direction.md) | composition/sequence/voice/rhythm, production feasibility and actual inspected medium | Consequential creative direction or craft mismatch |
| [project-judgment.md](../.agents/skills/taste/references/project-judgment.md) | Project-owned lessons: host-owned observations/preferences/hypotheses, context/exceptions/current-direction precedence | Retrieve or curate relevant real feedback; preserve host entries on update |
| [studies.md](../.agents/skills/taste/references/studies.md) | observation versus interpretation, compare/critique/revise, feedback and revision triggers; pending write when unauthorized | Reference study or real consequential feedback |

### Writing: ten references

| Final reference | Use | Conditional trigger |
| --- | --- | --- |
| [carousels.md](../.agents/skills/writing/references/carousels.md) | advancing argument, delivered promise/count, readable actual-size sequence | A carousel is requested |
| [content-refresh.md](../.agents/skills/writing/references/content-refresh.md) | keep/refresh/rewrite decision, useful URL/anchor/voice preservation, current truth | Maintain a dated existing answer |
| [content-types.md](../.agents/skills/writing/references/content-types.md) | docs/article/social/script starting state, reader task, medium and evidence | Select the artifact's actual mode |
| [copywriting-frameworks.md](../.agents/skills/writing/references/copywriting-frameworks.md) | choose structure for the missing reader decision, fulfill promise, provide early/progressive value | Argument structure is unsettled |
| [copywriting.md](../.agents/skills/writing/references/copywriting.md) | reason to care, supported mechanism/proof, objection, commitment and character | Write a supported persuasive argument |
| [editing.md](../.agents/skills/writing/references/editing.md) | diagnose truth/value/argument/order/specificity/voice/action; revise consequential weaknesses | Revise an existing draft |
| [language-and-rhythm.md](../.agents/skills/writing/references/language-and-rhythm.md) | concrete thought, causal connection, attribution and purposeful pacing | Expression/rhythm obscures the thought |
| [repurposing.md](../.agents/skills/writing/references/repurposing.md) | claim/proof/limits transfer, rebuild for medium, avoid all-platform bundles | Adapt existing supported work |
| [short-form-video.md](../.agents/skills/writing/references/short-form-video.md) | visible proof beats, truthful capture plan, production-useful script and actual playback limits | Short video script/storyboard/production |
| [social-posts.md](../.agents/skills/writing/references/social-posts.md) | supported idea, delivered hook, advancing thread, real voice/channel limits | A social post/thread is requested |

## Host types and concrete proof boundaries

Development discovers the actual input, behavior owner, observable output and
side effects first. Engineering checks/testing/debugging supply the methods;
the host's existing domain instructions remain authoritative. The following are
conditional paths, not a tour every task must perform.

| Host/output | Trace and meaningful failure/compatibility evidence |
| --- | --- |
| Web UI | User action through actual state/server owner to visible outcome; permitted/forbidden states, input failure, focus/keyboard, responsive behavior and stale requests when relevant. A screenshot proves presentation only. |
| API/service | Caller/input validation through business/authority owner to response and side effect; unauthorized/invalid/repeated requests, contract/errors and downstream failure when relevant. |
| Worker/event | Event/claim through work/commit/ack; actual retry/concurrency/idempotency/terminal owner, duplicate delivery, partial failure, cancellation/shutdown and bounded resource use when present. |
| CLI | Argument/stdin/environment precedence through command to stdout/stderr, exit status and filesystem/process effects; malformed input, dry-run, working directory and supported shell/platform/package behavior. |
| Library/SDK | Public exports/types and caller contract through return/error/effect; supported old/new callers, import/build targets, dependency constraints and meaningful failure paths. |
| File transformation/artifact | Input/encoding/schema through transform/write to actual reopened output; malformed/partial input, existing-file collision, atomicity/recovery and format/layout requirements when material. |
| Pure computation | Input domain and assumptions through calculation to result/error; independent expected cases or known invariants, boundaries, precision/units, determinism and resource bounds relevant to the request. No invented persistence/browser path. |

| Concern | Load/inspect only when | Smallest useful owner/evidence |
| --- | --- | --- |
| Authorization/secrets | Actors, access or privileged config affect the change | Host authority boundary, permitted/forbidden paths and redacted configuration metadata |
| Tenant isolation | The host has real tenant/resource partitioning | Scoping writer/query and negative cross-tenant cases |
| Persisted truth | A durable state or derived reader changes | Actual writer/default/final reader; transitions and stale/absent states |
| Migrations | Stored shape/history changes | Host migration/repair/compatibility owner; representative history and recovery |
| Concurrency/retries/idempotency | Work may overlap, repeat or partially complete | Claim/commit/ack/terminal owner; duplicate/race/failure evidence |
| Compatibility/errors | Consumers or public interface may break | Affected callers, exports/protocols/formats, invalid input and supported versions |
| Config/deployment | Startup/build/environment/release behavior changes | Existing host commands/config layering and real deploy boundary when authorized |
| Accessibility | User interaction/presentation changes | Actual keyboard/focus/semantic/responsive owner and rendered interaction |
| Documentation | A setup/command/contract/user promise changes | Owning source, literal guide and actual starting state |

No stack-specific auth, billing, database, framework, deployment, provider or
operational commands are installed as universal rules. A missing consequential
owner/source/tool is an explicit evidence gap; Lead obtains the smallest material
decision and Code continues unaffected work. Paid calls, credentials, production,
publishing and application mutations retain their applicable authorization.
Regulatory, specialist security, scientific or platform-specific assurance needs
the host's real standard/expertise; this package makes no universal certification
or completeness claim.

## Troubleshooting and instruction owners

Use these pointers when discovery, coordination or review breaks down. They
identify where the relevant guidance lives; instructions do not guarantee that
a client or model will follow them.

| Problem | Where to look |
| --- | --- |
| Workflow links fail from Claude aliases | Development/Code/Review canonical procedure links; native Claude adapters direct search to `.agents/`; README installation checks lexical aliases |
| Another installed skill shadows host Taste | README verifies actual loaded base/path and uses explicit canonical reads; Taste preserves host-specific judgment |
| Lead next action is stale or a new record restarts planning | Lead and Development continuation/resume instructions compare current tree/decisions with the existing record |
| Code is told to own Lead's record | Code returns evidence; Lead owns the existing continuation record |
| A fix introduces an unsupported fact/actor/permission | Writing's substantive claim check; Code factual-output contract; Review source-bound remedy and closure criteria |
| Review approves an acknowledged acceptance failure | Review role and AI Code Review acceptance, verdict and revalidation contract |
| Backup/script/proof escapes assigned scratch | Code's exact assigned scratch-root rule, including temporary files |
| Mock evidence is called real persistence/authority | Development testing plus Implementation evidence categories and actual-owner proof |
| CTA omits starting prerequisites or names the wrong actor | Writing content-types/copywriting, Marketing release communication and source-bound claim check |
| Tiny work receives heavy packet/hash/ledger ceremony | Development effort route, Lead proportional record, Code/Review proportional readable handoff; Challenge deletes unnecessary mandatory steps |
| Visual reference cannot be read or mockup becomes an app route | Frontend visual discussion scratch/image fallback and actual agreement boundary |
| Taste lesson cannot be written under current authority | Taste studies keeps a pending proposal in the existing record and requests the needed decision |
| Format/native listing is presented as reliable delivery | README native-discovery and permission limits; Code/Review truthful run/not-run reports |
