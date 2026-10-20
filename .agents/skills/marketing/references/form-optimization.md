# Form optimization

Load for field necessity, trust, validation and task completion. Inspect the
actual form/journey rather than treat every additional field as waste.

## Give each field a reason

Inventory label, type, required status, owner/use, sensitivity, validation,
default and later dependency. Keep fields required for eligibility, billing,
security or the promised action. Defer data useful only after success when the
actual owner permits it. Do not remove consent/authorization safeguards to make
a funnel shorter. Optional is not harmless when the field still feels mandatory.

Map the start: warm signed-in user, cold visitor, mobile keyboard, interrupted
flow, prior values. A multi-step form can clarify a complex task but can also
hide requirements. Choose grouping by decision and dependency; never prescribe
one step or a fixed field count.

## Inspect completion and recovery

- Labels explain expected input; placeholder-only guidance vanishes during typing.
- Required/optional status and format help should be evident before submit.
- Validation locates the field, explains correction and preserves safe input.
- Pending state prevents duplicate action without trapping failed requests.
- Server authority validates the real operation; client affordances are hints.
- Mobile controls, keyboard/focus order, long values and error announcements need
  actual UI proof through Frontend/Code, not a screenshot-only declaration.
- Explain cost, use of information and commitment at the point of concern using
  supported policy. Don't invent privacy/security assurances.

Example: a fictional request form needs work email for delivery but asks for
company size merely for future segmentation. Recommend deferring size only after
confirming it has no eligibility dependency. Separately retain entered fields
when the server rejects a malformed email; those are distinct hypotheses.

## Measure the task, not every keystroke

Existing step/field error and completion evidence can locate problems. Consider
abandonment, error recovery, qualified completion, duplicate attempts and harmful
submissions. Collection itself needs privacy and instrumentation authority;
do not log sensitive field values. Distinguish telemetry gaps from user refusal.

Deliver a concise field decision table, prioritized friction hypothesis,
requirements to retain and bounded UI/Development handoff. Use
[A/B testing](ab-testing.md) only for feasible uncertainty; fix reproducible
behavior failures directly under actual implementation authority. No form edit,
experiment or gain is implied by diagnosis.
