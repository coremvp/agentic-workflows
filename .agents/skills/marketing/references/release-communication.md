# Release communication

Load to turn actual changes into a supported user-facing update. A commit list
is raw input; the artifact needs a reader and truthful availability.

## Trace changes to their user effect

For each candidate inspect the source/release record, affected actor, prior
behavior, current behavior, state/permission limits and available evidence.
Group by user task, not file touched. Record whether the change is internal,
disabled, preview-only, eligible beta or generally available. Product/source
owners resolve conflicts; do not infer rollout from merge status.

| Source fact | Useful communication | Misleading shortcut |
| --- | --- | --- |
| Input survives failed validation | Correct the field without re-entering safe details | “Forms never fail” |
| Feature available to opted-in workspaces | Beta, eligibility and known limits | “Everyone can use it today” |
| Refactor changes no user behavior | Omit unless it answers a real technical concern | Invent a speed/security improvement |
| Captured fixture demo | Label what the capture demonstrates | Present it as customer adoption |
| Flag still disabled | Draft/hold with activation dependency | Call it shipped because code merged |

Choose the selected audience's consequence. A bug fix may be worth leading with
when it blocked work; a minor visual adjustment need not get equal prominence.
An accurate beta is valid communication, not something to hide categorically.

## Produce a useful update

Lead with what users can now do or what frustrating behavior changed. Include
eligibility, action/setup, inspectable proof and limitations where they affect
the decision. Prefer the relevant existing guide to another explanation page.
Use a digest for distinct small improvements and a focused announcement for a
single consequential result. Avoid unsupported dates, uptime, superiority,
performance numbers and invented testimonials.

Flag changed instructions, API behavior, migration/recovery and search/page
ownership for Documentation/Writing, Development or SEO as appropriate. A
proposed handoff does not complete those changes. Use [launch readiness](launch-readiness.md)
when an announced action still depends on release checks.

Gate only a demonstrated dependency of the selected audience and promised action.
A known mobile trial-form defect, for example, need not block an existing admin's
invitation resend or an eligible workspace's CSV beta when those paths don't use
that form. Keep an unrelated defect as a separate note/backlog item rather than
inventing an engineering prerequisite. If evidence shows the announced path does
depend on it, route that dependency through [launch readiness](launch-readiness.md).

Return the draft plus a compact source-to-claim map and explicit holds/limits.
Production checks remain Code-owned, and distribution remains separately
human-authorized. The communication can be complete as a local draft while
availability proof or response is pending.
