# AI Code Review

Independently inspect the requested result and Code's evidence, then revalidate
admitted fixes. [Review Agent](../skills/review-agent/SKILL.md) owns read-only
assessment. Lead owns scope, dispositions and the record; Code owns fixes and all
checks. Read Review's role first: no file/scratch writes, execution, runtime,
browser/provider proof or delegation.

## Establish the exact target

Read the human contract, accepted choices, intended output and important reject
cases. Inspect the actual changed source, supplied diff and relevant base/head
or working-tree binding from [Code's inputs](../skills/code-agent/SKILL.md#supply-a-readable-review-packet).
Read new files as well as modifications. Load relevant host/domain instructions.
Review-only work does not require a new proposal, tracker or full ceremony.

Do not assume a commit identifies dirty content or that an old diff is the target.
If a target, direct consumer or essential evidence is missing, ask Lead for the
smallest Code-supplied input. When comparing a branch, distinguish its changes
from target-branch movement before reporting missing code or regressions.
Read supplied outputs; do not run Git or commands to reconstruct evidence.

## Review the result before polishing the implementation

1. **Missing:** Does each requested behavior and material rejected outcome have
   an implementation owner? Are integration, failures or instructions omitted?
2. **Extra:** Did the change add capabilities, dependencies, state or redesign
   beyond the accepted result? Is that addition required for correctness?
3. **Misunderstood:** Does the implementation use the right actor, object, scope,
   state and definition of success? A passing test of the wrong rule is still wrong.

Compare against the human contract, not the implementer's summary. Do not invent
new acceptance or reopen an accepted choice without concrete contradictory source.
Separate absent behavior from missing proof of behavior.

## Trace concrete paths and select relevant risks

Follow the changed entry through validation and authority, behavior/side effects,
output and direct consumers. Follow an important success and rejection/failure
path where applicable. For a CLI, inspect actual exit/stdout/stderr behavior; for
a library, supported callers and errors; for files, contents and overwrite rules;
for a worker, claim/side effect/acknowledgment and retry outcome. Do not assume a
web/database architecture.

Read related code when it can change the conclusion: a helper's caller, a schema
constraint, a cache reader or an error mapper. Diff-only inspection can miss the
actual contract. Conversely, touching a helper does not make its entire old
failure model part of this review.

Select triggered sections of [Engineering checks](../skills/development/references/engineering-checks.md)
and the host's relevant owners. Inspect how the specific change behaves at that
boundary, not whether the patch contains reassuring words. For example, an access
change needs actor/resource scope and a denied path; a new stored value needs its
writer/default and real reader; a retry needs a bound and terminal consequence.
No change owes a tour of every domain.

## Inspect what the evidence actually proves

Map recorded Code checks to acceptance and meaningful rejection cases. Use
[Testing](../skills/development/references/testing.md) to identify a false-success
path: could these assertions pass with the defective implementation? Read the
assertion, activated owner, inputs, recorded output and limits when relevant.
Build/package/mocked output cannot establish application persistence, permission
checks, provider action or runtime cancellation by itself.

Keep source reasoning, recorded reproduction, coverage gap and speculation
separate. A concrete source defect need not be claimed as reproduced. Missing
proof is not a reproduced bug; request the smallest Code-run check and expected
result. Reuse still-valid evidence for unchanged source/inputs. Do not require
reruns merely because a commit, push or handoff changed.

## Report actionable findings

A finding needs the exact path/line or artifact location, violated requirement,
trigger/input, user/system consequence, supporting source/evidence and smallest
correction or closure proof. Do not give a generic warning where a concrete
failure can be traced. Check your suggested remedy against source too: new
qualifiers in a fix can create a different factual defect.

Prioritize by consequence under a credible trigger, not by how much code changed:

| Severity | Use when |
| --- | --- |
| Critical | A credible path permits severe unauthorized access, irreversible data loss or broad failure requiring immediate attention. Name the affected boundary and evidence; the label grants no production action. |
| High | A supported important path is broken, unsafe or materially incompatible, with no acceptable existing recovery. |
| Medium | A real scoped failure, incorrect result or required proof gap affects the accepted outcome and needs correction before claiming it complete. |
| Low | A limited defect has a small consequence. State whether it actually fails acceptance; optional style stays a recommendation, not a defect. |

Keep severity distinct from confidence. A possibility without a source-grounded
trigger is an investigation question, not a critical finding. Apply the defer
test against the original outcome: if it remains correct, safe and provable
without the work, do not make it a current-task blocker. Identify material
baseline issues only within scope; do not widen the task into a competing redesign.

Return findings ordered by consequence and one assessment:

- **supported:** inspected source and supplied evidence support the assigned
  scope; state limits and any optional recommendations;
- **requires-correction:** name unmet acceptance or concrete in-scope defects;
- **not-verified:** required source or proof cannot support the conclusion, with
  the smallest missing input/check.

If there are no findings, say so; still state coverage and unverified boundaries.
For a source-only assignment, report source conclusions without claiming runtime
verification. An acknowledged acceptance failure cannot be called Approved.
Lead's finding dispositions and a human waiver remain separate from Review's
independent assessment.

## Revalidate accepted closure without restarting discovery

Lead sends admitted corrections to Code under continuing human authority. Code
returns the changed target and invalidated checks through
[Implementation](implementation.md) in `review_fix` mode. Review inspects each
accepted finding's correction, affected direct paths and newly introduced facts
or failures against the exact current source and evidence.

Return closed, still open or not verified per admitted finding with the reason.
Do not restart a full audit unless a concrete new contradiction invalidates its
scope. Missing proof returns through Lead as a bounded Code request. Review
returns reports in the conversation and writes no artifacts.

For complete delivery, Lead finishes after integration, required proof and
accepted closure or names the unresolved boundary. Review-only work stops with
the requested assessment. A verdict does not authorize implementation, merge,
publication or distribution. Distinguish independent Review from self-review and
phase completion from full delivery.
