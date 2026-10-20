---
name: frontend
description: Shape and implement useful visual or interactive interfaces through inspected references, rendered proposals, existing components and accessible responsive behavior.
---

# Frontend

This is the canonical visual owner. Inspect the actual application, its local
instructions, installed framework/libraries and touched feature. Reuse existing
components and theme; inspect shared callers before changing a primitive. A
reference is not permission to install a UI library or upgrade the stack.

For unsettled design or redesign, read [Visual discussion](references/visual-discussion.md)
before application implementation: show inspected reference pictures, the current
surface and a rendered proposal for real human agreement. [UI references](references/ui-references.md)
helps discovery; each task still inspects relevant examples. Load [Taste](../taste/SKILL.md)
for consequential composition, character and applicable project learning.
Small fixes within an accepted direction do not need another full case study.

## Preserve actual state and interaction owners

Trace the actual live-data, preview and presentation owners; preserve their
boundaries. Keep server clients/secrets out of browser code. Session/cache keys
must not mix actors/accounts. UI capability flags are hints; the server rechecks
protected actions. Never turn an API error into sample success.

For changed interactions, name the source of truth, pending state, successful
result and recovery. Refresh or invalidate the relevant data after a change;
preserve safe input when validation or a request fails. Prevent duplicate actions
without trapping the user after failure. An optimistic update needs the host's
actual rollback/reconciliation behavior rather than an invented success state.

Where async work can overlap, inspect the race: a slow earlier search must not
replace a newer query, a response for a closed detail view must not populate a
different item, and changing actor/account must not retain another context's
result. Use established request, cancellation and state conventions; do not add
a new state library for a local fix. Select the race that the feature can actually
encounter, rather than impose a concurrency tour on static content.

## Make hierarchy and composition useful

Inspect the rendered application and preserve accepted styling unless the brief
changes it. Identify the primary decision/action, necessary context and secondary
detail. Give each section a distinct information job; charts/metrics need an
actual source, meaningful comparison and honest units. Reuse the host's real
component, token and layout conventions rather than a universal palette, type
scale, spacing system, density or framework.

For a consequential composition, compare the current render and references:

- Typography: use existing roles to distinguish heading, label, body and numeric
  information. Judge line length, wrapping and emphasis at actual size; a larger
  headline alone cannot repair unclear information order.
- Hierarchy: make the main decision easy to locate, place related evidence near
  it and reveal secondary detail when useful. Remove competing emphasis and
  repeated summaries before adding decoration.
- Spacing: group related controls and separate distinct tasks through the host's
  rhythm, alignment and containment. Inspect long labels and real values before
  fixing dimensions; do not polish one ideal screenshot at the expense of use.

Use semantic headings and native or established accessible controls, persistent
field labels, meaningful errors and visible focus. Keyboard order should follow
the interaction. For dialogs, menus, drawers and replaced content, inspect focus
entry, containment where appropriate, escape/dismissal and return. Do not rely
on color alone to communicate a consequential state. Use the host's relevant
accessibility guidance and component APIs.

After agreement, retain a bounded implementation contract in Lead's task record:
section/information order, states, interactions, reused components, responsive
behavior and acceptance. Implement the accepted direction and compare the real
render with the proposal. Task decisions do not become permanent skill rules.

Inspect relevant desktop/mobile widths, narrow containment, long/error content
and pending/empty states. For changed controls, check keyboard/focus, invalid
input, recovery and duplicate/pending behavior; for async changes, check the
relevant stale-response path. Confirm that responsive ordering preserves meaning
and actions remain reachable, with horizontal scrolling only where justified.
Select checks for the actual change, including zoom or reduced motion when they
matter. Use the host's matching existing browser/E2E proof before a manual fallback;
record why a fallback is needed and the actual tool.
Use the in-app browser when available. Screenshots show presentation, not
persistence or authorization. Avoid arbitrary pixel/decorative-count assertions.
Read installed/current first-party framework guidance when rendering, caching,
metadata or other version-dependent semantics matter.
