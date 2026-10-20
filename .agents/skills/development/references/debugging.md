# Debugging

Read for an actual reported or observed failure, including a failing relevant
check. Diagnose the cause before changing behavior. This reference does not
authorize new application work, runtime access or provider operations. Code alone
runs reproduction and diagnostics; Review reads recorded evidence.

## Establish the failure, not a theory

Record the expected behavior from the human or host contract, actual output,
smallest known input/start state and affected version/environment. Distinguish
what was observed from a report or interpretation. Preserve the meaningful error
and safe context; do not copy secrets, tokens, personal data or sensitive payloads
into logs, screenshots, source examples or handoffs.

Reproduce through the smallest actual owner within authority. Follow the request,
command, function, event or file operation to its output. Use an existing relevant
scenario rather than building a new demo. A bug report does not require a full
application stack when a function or command reproduces it.

If reproduction is unavailable, narrow the missing input or environment and state
what source inspection can still establish. Do not claim reproduced, demand
unrelated setup or silently use production. A sandbox failure establishes that
path failed; it does not diagnose the host. Follow approved host execution before
reporting host health, and never restart shared services from that assumption.

## Locate where correct input becomes incorrect output

Read the actual error and owning source. Compare with the nearest working path:
another supported input, known-good state, direct consumer, host pattern or
relevant baseline. Change one meaningful condition at a time when isolating cause.
Inspect recent differences only where they can explain the observed transition;
a recent commit is a lead, not proof of fault.

Trace the value and decision through the relevant boundaries. Which input reached
the owner? Which validation/default applied? Which actor/state selected the branch?
What effect or result actually occurred, and what did its consumer report? The
first place expected and observed behavior diverge is more useful than the last
error message.

For a worker or external effect, consider duplicate delivery, ordering and partial
success only when the symptom suggests them. For a CLI, compare stdout/stderr and
exit with actual operation success. For a library or computation, compare public
contract and boundary inputs. Select [Engineering checks](engineering-checks.md)
only for implicated risks; do not turn diagnosis into a whole-app review.

## Use a falsifiable hypothesis

State the suspected cause, evidence supporting it, a plausible competing
explanation and the smallest check that would distinguish them. Predict the
result before running the check. For example, a stale display can come from an
incorrect write, stale read or presentation mapping; inspecting the real writer
and reader distinguishes them before adding a refresh or cache bypass.

Code runs the bounded check, records the observation and updates the explanation.
An observation that contradicts the theory should change the theory. Do not pile
on cache clearing, retries, timeouts or broad refactors to see whether something
helps. If a probe needs new authority, return that exact need through Lead and
continue source investigation that remains in scope.

Add temporary instrumentation only where it can answer the question, inside
assigned roots and without secret-bearing output. Remove task-only instrumentation
when finished unless retained diagnostics have a justified host-owned purpose.
Do not mute a meaningful error or substitute fake success to obtain a green run.

## Fix the cause and preserve the contract

Make the smallest correction at the real owner. Check direct callers and siblings
that share the same violated invariant; avoid treating every adjacent weakness
as part of the bug. Preserve accepted behavior, error contracts and useful
recovery. A new architecture, permission rule or data model is a material change
for Lead/human decision, not a side effect of debugging.

Use [Testing](testing.md) to show the actual failing case is exercised, the fix
satisfies it and relevant accepted/rejected behavior survives. Add the smallest
useful regression when warranted. Passing a broader build without the failing
path is not closure. If ownership is disputed, compare appropriate baseline
and current evidence before declaring the patch responsible.

If successive attempts yield no new observation, stop speculative mutation.
Summarize what is known, hypotheses excluded, the remaining uncertainty and the
smallest discriminating input/check or human decision. This is a bounded evidence
request, not an automatic retry quota, model escalation or permission expansion.

## Return a useful diagnosis

Give Lead the trigger, expected/actual result, source-grounded cause, correction,
proof and limits. Keep it short when the cause is clear; do not require another
artifact for every bug. Preserve enough evidence in the existing task record
when the work may resume. Label a mitigation, source-supported hypothesis and
verified fix differently. A necessary unrun check remains unverified.
