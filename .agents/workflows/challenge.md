# Challenge

Independently challenge the assigned plan before consequential implementation.
[Review Agent](../skills/review-agent/SKILL.md) inspects read-only; Lead records
its assessment, dispositions findings and resolves material decisions. Read the
role first: no writes or scratch, checks, runtime/browser/provider execution or
delegation. A challenge verdict is not implementation authority.

## Inspect the plan against the original request

Read the human request, accepted choices, intended output, plan, relevant source
and supplied evidence. Identify actual acceptance/reject cases and where the
assignment stops. A review-only entry does not need another proposal, tracker,
hash ritual or fixed artifact template. Request only missing essentials.

First ask whether the plan omits required behavior, adds unrequested behavior or
misunderstands the user's rule. Trace a representative path from actual input
to output and a material rejected case. A neat task list does not establish a
coherent result, and a technically sound solution can solve the wrong problem.

## Challenge in this order

1. **Question the requirement.** Which human rule, observed failure, supported
   contract or necessary dependency requires it? Distinguish accepted decisions
   from assumptions and implementation conveniences. Do not reopen a locked
   choice without a concrete contradiction or safety consequence.
2. **Delete unnecessary work.** If a step, state, interface, service, artifact or
   reviewer disappears, can the requested result remain correct, safe and provable?
   If yes, remove it from the current task. Existing uncertainty can justify a
   small investigation; it cannot justify speculative implementation.
3. **Simplify the retained solution.** Can the existing owner or installed library
   do it? Can truth be derived instead of stored twice? Does an extra abstraction,
   flag, queue or provider solve an actual constraint, or only make the plan look
   extensible? Name the simpler mechanism and its actual tradeoff.
4. **Attack relevant failure boundaries.** Select the applicable questions from
   [Engineering checks](../skills/development/references/engineering-checks.md)
   and the host's domain owners. Test the plan against a specific forbidden action,
   stale/concurrent input, failed operation or compatibility boundary where it
   matters. Do not run a mandatory all-domain tour or design a competing system.
5. **Attack the proof.** Name a way the planned check could pass while the desired
   behavior remains broken. Does it reach the real owner and observe the required
   output, rejection or durable state? Use [Testing](../skills/development/references/testing.md)
   when the answer is uncertain. Missing runtime evidence is distinct from a
   contradictory design; Review requests the smallest authorized Code-run check.
6. **Challenge delivery cost.** Are assignments independent? Is integration owned?
   Does the plan repeat completed research, demand huge packets for tiny changes,
   or make the user manage routine execution? Retain only process that changes a
   decision, prevents a meaningful failure or preserves needed continuity.

For a CLI, examine exit code and stdout/stderr, not just successful execution.
For a library, consider supported callers and its error contract. For file work,
consider output contents and overwrite/partial-write behavior. The actual host
chooses the relevant path; none requires a database or browser by default.
Frontend retains the visual agreement contract for unsettled UI.

## Admit findings by consequence, not possibility

A required revision needs a concrete contract conflict, demonstrated omission
or material unhandled boundary with a credible trigger and consequence. Avoid
hypothetical redesigns, preferences and claims that every nearby weakness blocks
this change. Apply the defer test: can the requested outcome still be correct,
safe and proved without this work? If yes, it is not a current-task blocker.
A touched helper does not admit its whole pre-existing failure model.

For each required finding return the source/location, violated requirement,
trigger, consequence and smallest plan correction or missing evidence. Separate
contradiction, assumption and proof gap. Optional advice stays visibly optional.
Return a concise conversation assessment:

- **plan-supported:** the inspected design addresses the requested outcome and
  relevant risks; this does not claim implemented behavior was tested;
- **required-revision:** name the decisions or omissions that must change;
- **not-verified:** essential source or contract evidence is missing, with the
  smallest input needed to decide.

## Resolve and stop or continue

Lead records the independent report and dispositions. Same-contract corrections
and cleanup remain inside the assignment; material new intent/design returns to
the human with recommendation, reason, tradeoff and one decision. Unrelated work
is dropped or separated within actual authority. Review rechecks the changed
plan and affected assumptions, not a complete new investigation without cause.

For full delivery, a supported plan plus continuing human authority permits
[Implementation](implementation.md). For challenge-only work, finish with the
assessment and next action. Neither an independent verdict nor an assistant's
record permits implementation, publication or proof execution by itself.
