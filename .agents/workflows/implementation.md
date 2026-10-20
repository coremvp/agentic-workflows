# Implementation

[Code Agent](../skills/code-agent/SKILL.md) produces and integrates the authorized
change, fixes admitted findings and alone executes checks. Lead owns scope,
material decisions and continuation. Use this procedure for a direct bounded
instruction, accepted design or concrete review fix; do not manufacture another
planning cycle.

## Admit the actual assignment

Read the exact human authority, owned object, host instructions, source and
relevant branch/base/head/dirty state. Name the observable result, write roots,
locked choices, acceptance/reject cases, dependencies and finish boundary.

- `initial`: build the directly requested bounded change or accepted plan.
- `review_fix`: close Lead-admitted in-scope findings under continuing authority;
  read their invariant, target and closure need before editing.

A question or review verdict is read-only without actual implementation
permission. Do not ask again for authority that continues inside the same
contract. Return material unknown scope, design or permission to Lead with a
recommendation, reason and tradeoff; continue independent admitted work.

## Work through the actual owner

Inspect the entry, behavior, side effects and consumers before changing them.
Reuse the installed compatible library and host pattern. For uncertain APIs,
consult relevant current first-party guidance rather than guess. Load only the
host domain owners and [Engineering checks](../skills/development/references/engineering-checks.md)
sections triggered by this change.

For a bug, follow [Debugging](../skills/development/references/debugging.md):
establish expected/observed behavior, obtain the smallest authorized reproduction,
isolate a falsifiable cause and fix that cause. Do not stack speculative fixes,
suppress an error or widen a timeout merely to make the symptom disappear.
Known concrete corrections do not need a new debugging report.

Make the smallest complete change. Follow direct callers, public types, imports,
validation, authority, state readers and instructions that rely on the changed
contract. A new field, response or state is incomplete if the real consumer still
uses the old meaning. Keep error and recovery behavior intentional; do not turn
failed work into sample or optimistic success.

Integrate in dependency order. Independent tasks may proceed in parallel only
with disjoint ownership; shared files have one writer. Preserve and accommodate
others' edits. Inspect shared callers before changing a primitive. Preserve
accepted UI through [Frontend](../skills/frontend/SKILL.md), including visual
agreement for an unsettled direction; a mockup is not application implementation.

Necessary same-contract work and cleanup continue. Drop unrelated defects;
return material new scope or design before mutation. A touched helper does not
admit its entire historical failure model. In `review_fix`, each edit must close
an admitted finding or a directly required sibling under the same contract.

## Verify the promised behavior

Inventory the host's owning tests and existing E2E or command scenarios. Use
[Testing](../skills/development/references/testing.md) to map acceptance and
material rejected outcomes to the smallest complete proof. Run focused checks;
a test count, build or formatting pass is not evidence of the whole result.

For a bug, show that the relevant failure is exercised and the correction fixes
it. Where a failure's ownership is uncertain, compare appropriate unchanged
baseline/current target evidence before attributing it to this task. Add a
meaningful regression when it protects the behavior; do not add tests that merely
copy wording, decorative counts, arbitrary geometry or illustrative values.

Before manual browser/provider proof, use the matching existing scenario if it
can assert the result. Follow documented host commands and permissions, start
only necessary dependencies and close task-owned helpers. Do not stop another
owner's runtime. Begin host-bound diagnostics through approved host execution;
a sandbox error does not diagnose host health or justify a shared restart.
Never read secret files directly or print credentials. Authorized host commands
may consume their documented configuration without exposing its values.

Observe the actual output at the required boundary: CLI output/exit, public
consumer behavior, generated contents, computation result, worker effect, or web
response and durable reader as applicable. Record inputs, command and outcome,
source target, relevant environment and limitations. Distinguish real runtime,
source inspection, seeded, replayed, mocked and manual evidence. Required skipped
proof is `not_run`; it does not become a successful result. A mockup is not the
app, row inspection is not a lifecycle replay and a provider mock is not a
provider action.

Reuse valid proof when tested files and inputs have not changed. Rerun checks
invalidated by a correction; commit, push or a record edit alone does not make
unchanged evidence stale. A failed check starts bounded diagnosis, not permission
to alter unrelated code, CI gates or infrastructure.

## Hand off and finish the selected phase

Return changes, integration state, source-bound evidence and limits to Lead for
the existing record when needed. Supply [readable review inputs](../skills/code-agent/SKILL.md#supply-a-readable-review-packet)
without mandatory expanded ledgers for small work. Do not adjudicate findings
or approve yourself.

For a complete meaningful behavior change, independent [AI Code Review](ai-code-review.md)
inspects the result when supported. Code fixes only admitted findings under
continuing authority and refreshes changed source and invalidated proof; Review
closes them. Disclose unavailable independent review as self-review or not run.
For implementation-only work, report the phase and review not run, then stop.

Complete the assigned normal-hook commits and shipping boundary. Do not infer
push, publication, deployment, destructive operations, paid calls or production
authority. State exactly what is saved, committed, pushed, merged or deployed,
and any required output still unsupported.
