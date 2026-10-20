# Testing and proof selection

Read when choosing verification, adding a regression, assessing a coverage claim
or attributing a failure. The goal is evidence of the requested behavior, not the
largest suite or most elaborate harness. Code executes; Review inspects supplied
source and output. The host's commands and permission boundaries remain binding.

## Start with the claim a check must establish

For each important acceptance or rejection case, identify the actual owner,
input/start state and observable result. Then choose the smallest check that
reaches it. Several criteria may share one check. Do not make a proof table or
new test file mandatory when a short explanation and existing check suffice.

Ask: if the implementation were still wrong, could this assertion pass? A test
that asserts its own mock return, successful HTTP status without the promised
effect, or existence of an element without its action can give false confidence.
Inspect the activated code and asserted output before calling it coverage.

| Claim | Useful proof boundary | Common false success |
| --- | --- | --- |
| Validation or pure business rule | Real validator/function with relevant valid and rejected inputs | Test reconstructs the rule rather than importing its owner |
| Durable write and reader meaning | Actual persistence owner and real consumer with meaningful state | Mock repository echoes the requested value; reset only covers defaults |
| Protected action | Actual authorization path with eligible and denied/foreign-state inputs | Hidden button or fabricated allowed identity without the enforcement path |
| CLI contract | Actual command input, stdout/stderr and exit status | Process launches or prints a success phrase despite failed work |
| Library compatibility | Supported consumer uses public exports/types and expected errors/results | Internal helper passes while the public entry or error contract changed |
| File transformation | Actual output contents and relevant existing-file/error behavior | File exists but is empty, partial, misplaced or destructive |
| Pure computation | Real function and specified relationships/boundary inputs | A few agreeable sample values miss the defining relation or numeric boundary |
| Worker/event lifecycle | Actual handler/state/effect at relevant duplicate, failure or cancellation | Mock callback called once without testing delivery or terminal behavior |
| Rendered interaction | Existing browser/interaction scenario through the real state owner | Screenshot/preview looks correct but controls or data path are unwired |
| Provider behavior | Authorized provider path with verified outcome and declared environment | Mock, seeded row or redirect is presented as a completed external action |

Select only actual claims. A library calculation does not need a database or
browser. A route unit test can legitimately prove parsing/error mapping without
proving persistence; describe the limited claim rather than discard useful tests.

## Reuse the host's verification structure

Inspect owning unit/integration tests and existing command/E2E scenarios before
adding or manually recreating one. Prefer:

- a focused unit check for a deterministic isolated rule;
- integration through the real boundary when persistence, authorization,
  serialization or another subsystem interaction is the claim;
- a matching existing E2E/browser/command scenario when the assembled path matters;
- bounded manual/external proof when automation cannot establish the result,
  stating why and what remains unverified.

These are choices, not four mandatory layers. Mocks control a dependency to
inspect a narrower owner; they do not prove that dependency. Real database
constraints/transactions may differ from an in-memory substitute. Keep a replay,
seeded account, fixture preview and live path visibly distinct.

For a regression, choose the smallest input that exercises the actual defect
and a meaningful reject or boundary case. Where practical, show that the new
assertion fails for the defect and passes for the correction. Protect the named
invariant, not the implementation's exact shape, prose formatting, decorative
counts, arbitrary pixel geometry or incidental example values. Do not introduce
a test solely to mirror a reversible point edit.

A useful local check does not automatically belong in CI. Follow the host's
existing placement policy; changing workflow gates, retries, runners or timeouts
requires its own authority. Do not install a new fixture/eval project to validate
an instruction package or call an example real delivery.

## Diagnose a failing check before assigning ownership

Record the actual failure and which owner ran. Distinguish product failure,
assertion/fixture mismatch, environment/configuration, unavailable dependency and
tool/sandbox failure. None authorizes changing a gate just to make it green.

If the change's ownership is unclear, compare relevant evidence against the
unchanged baseline and current target. Consider target-branch movement: a failure
already present on current main is not automatically caused by this patch, and
a target fix may mean updating the branch is enough. Run baseline comparisons
only where they answer that ambiguity; do not repeat all suites on every ref.
Unavailable baseline evidence stays unknown. Use [Debugging](debugging.md) for
an actual unresolved failure.

Use the host's documented commands and environment policy. A configuration
listing or example can reveal names without exposing secrets. Authorized tooling
may load required configuration internally; do not inspect secret files or print
values to diagnose it. A sandbox connection failure does not establish host
service health; use the approved host path before making that claim.

## Bind evidence to what actually ran

Return the command/check, inputs/start state, actual owner and output, source
revision or working tree, relevant environment and evidence location. Make a
failing exit or required skip explicit; a required `not_run` check remains a
completion gap unless the human changes the contract. Do not hide failure behind
a count of unrelated passing checks.

Use precise descriptions: source inspection, real local/runtime, fixture-backed,
helper-seeded, replayed, mocked or manual. A source reading can support a source
conclusion; it does not prove runtime behavior. A row shows stored state, not
that a lifecycle replay or provider action happened. Actual audience response
needs real exposure; it is outside technical test claims.

Keep a source binding proportionate. A stable committed target can use its
revision and readable diff; ambiguous dirty/moving content needs an immutable
snapshot, diff or hash sufficient to identify the reviewed tree. Avoid mandatory
hash manifests for a tiny stable artifact. Review must be able to inspect the
relevant source and outputs with file reads alone.

## Reuse proof until an input changes

Name what invalidates a result: changed tested code, dependency/runtime input,
configuration, data/start state or a concrete discrepancy discovered in review.
A commit, push, PR-body or ignored-record edit alone is not an invalidator.
After fixes, rerun affected checks and broaden only when the new change or
failure warrants it. Do not reopen expensive browser/provider proof merely to
leave a tab visible or repeat a claim.

Close task-owned helpers when their proof is finished. Deliver what ran and did
not, the supported claims and remaining gap. Green checks and source review are
evidence for the assigned scope, not proof that every application concern works.
