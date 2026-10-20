---
name: development
description: Deliver an authorized feature, bug fix or interface improvement by understanding the actual application, choosing a proportionate approach, integrating the change and verifying it with independent review where needed.
---

# Development

Start with the outcome the user wants. Discover how their application works and
choose the smallest route that can deliver it. The founder should not select
specialists, manage dependencies or repeatedly tell the agent to continue.

[Lead](../lead-agent/SKILL.md) stays in the main conversation and owns scope,
material decisions and delivery. [Code](../code-agent/SKILL.md) produces,
integrates, fixes and alone executes checks. [Review](../review-agent/SKILL.md)
independently inspects assigned plans, source and evidence without executing or
writing. Load the procedure for the selected phase, not every procedure at entry.

## Choose effort before phases

| Situation | Route |
| --- | --- |
| The outcome, owner and established approach are clear; no material boundary needs redesign | Code makes the bounded change and runs focused proof. Use source review appropriate to its consequence; do not require fresh research, Proposal or Challenge. |
| The outcome is unclear, material approaches compete, or the change introduces consequential rights, state, dependencies or lifecycle decisions | Lead plans the unresolved decisions, researches the uncertainty and obtains independent Challenge before implementation. Reuse accepted work rather than plan it again. |
| The user asks for one phase or an explanation | Complete that request and stop there. A question or review does not authorize a build. |

A mechanical correction does not need another actor merely because agents are
available. For a meaningful complete behavior change, use separate independent
Review when supported. If delegation is unavailable, perform the needed work in
explicit Code/review roles and disclose self-review. Switching roles in one
conversation never establishes independent review.

| Phase | Owner | Procedure |
| --- | --- | --- |
| Define the change and choose an approach | Lead | [Proposal](../../../.agents/workflows/proposal.md) |
| Challenge material assumptions and unnecessary work | Review; Lead resolves decisions | [Challenge](../../../.agents/workflows/challenge.md) |
| Implement, integrate and verify | Code | [Implementation](../../../.agents/workflows/implementation.md) |
| Inspect source, evidence and accepted-finding closure | Review; Code fixes admitted findings | [AI Code Review](../../../.agents/workflows/ai-code-review.md) |

The design-bearing route is plan -> independent challenge -> resolve material
choices -> implement and check -> independent source review -> admitted fixes
and invalidated checks -> closure -> deliver. Direct work skips completed or
unnecessary phases. Continuing human authority applies inside the same contract;
material new scope or design returns to the user. Never invent a feature,
redesign or evaluation to demonstrate this package.

## Understand the actual host

Read the request, host AGENTS/README and local instructions, relevant source,
manifests, lockfile and existing checks. Establish the affected person or caller,
current behavior, intended output, important rejected outcomes and stop boundary.
Infer established facts before asking; material unknowns use Lead's recommendation,
reason, tradeoff and one-decision contract.

Find the actual entry, behavior owner, side effects and consumers. An HTTP route
is one possible entry; a CLI command, exported function, file transformation or
worker is another. A pure calculation may have no persistence, server or browser.
Use the host-path questions in [Engineering checks](references/engineering-checks.md)
when a technical boundary matters; select applicable sections instead of filling
an all-domain checklist.

Reuse existing owners and installed libraries. Follow the selected lockfile and
package-manager policy. For an uncertain integration or version-dependent API,
inspect compatible current first-party guidance before inventing an approach.
Compare meaningful alternatives only where the decision is unsettled; routine
use of an established pattern needs no new research report.

Load [Product](../product/SKILL.md) for consequential business choices,
[Frontend](../frontend/SKILL.md) for UI and [Writing](../writing/SKILL.md) for prose.
Discover backend, data, identity, billing, runtime and other technical owners
from the host. This package assumes no framework, database, entitlement model or
application paths. A missing domain skill means inspect the real implementation
and requirements, not create an adapter or assert generic assurance.

Ordinary audience, content and communication work uses [Marketing](../marketing/SKILL.md)
and its relevant owners without this engineering cycle. Frontend alone owns
conditional reference pictures, rendered proposals and human visual agreement.
Accepted small UI fixes do not repeat that discussion.

## Load depth for an actual decision

| Trigger | Read |
| --- | --- |
| A changed trust, data, interface, runtime, configuration, UI or documentation boundary | [Engineering checks](references/engineering-checks.md), only the applicable sections and host owners |
| Choosing proof, interpreting test coverage, adding a regression or assigning a failure to this change | [Testing](references/testing.md) |
| Diagnosing an actual reported or observed failure | [Debugging](references/debugging.md) |
| A technical CMS, editorial model, preview or publishing requirement | [Content systems](references/content-systems.md) |

These references supply methods, not mandatory extra phases or permission to run
anything. A mock or build cannot establish durable data, permissions, a provider
action or completed application delivery.

## Coordinate, resume and finish

Use the two native Code/Review definitions where supported. There is no native
Lead. Preserve client models, permissions and concurrency limits. Assign bounded
independent work only when it helps; dependent tasks wait for their actual input.
Do not parallelize edits to one shared owner.

A small bounded task needs its intended result, source target, checks/limits and
next action in the conversation or existing record. For multi-step, delegated
or interruptible work, Lead maintains one ignored continuation record with only
applicable decisions, assignments, findings and source-bound evidence. Update the
next action at phase boundaries. On resume, find that record; Code reports the
current revision, dirty state and relevant diff; Lead reconciles changes and
resumes the first incomplete step. Do not restart accepted planning or reuse
proof invalidated by a changed input.

If native roles or discovery links are unavailable, explicitly read canonical
role and domain files into available agents. Disclose the limitation. Code alone
operates task-owned runtimes, browsers and checks; Lead reads the returned evidence.
Deliver the requested phase or outcome with Review's actual disposition, material
limits and exact saved, committed, pushed, merged or deployed state.
