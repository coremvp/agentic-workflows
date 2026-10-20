# X algorithm

Load when X distribution mechanics materially affect a recommendation. Keep
mechanism, source configuration, observed response and hypotheses separate.
Research snapshot: 14 October 2026, official repository revision
`17c96bf346df3d62b90f1bb01830d432dba74485`. Recheck current primary source before a
new source-dependent recommendation; don't treat this snapshot as live telemetry.

## What the published implementation establishes

The [official repository](https://github.com/xai-org/x-algorithm) describes retrieval
from followed and other accounts, prediction-based ranking and separate visibility
filtering. Viewer context influences predictions. Blocks/mutes, labels and
eligibility can affect visibility independently of ranking; diversity and
selection stages also matter. Not reaching a reader is not automatically a weak
hook or one missing engagement type.

The [published parameters](https://github.com/xai-org/x-algorithm/blob/17c96bf346df3d62b90f1bb01830d432dba74485/home-mixer/params/param.rs)
and [value model](https://github.com/xai-org/x-algorithm/blob/17c96bf346df3d62b90f1bb01830d432dba74485/home-mixer/scorers/value_model.rs)
include scoring weights. The source's August 2026 clarification says weights
scale predicted actions/continuous values, not raw engagement counts. Saying
weights are wholly withheld is stale. A coefficient ratio does not mean one
report cancels a fixed number of likes. Published defaults do not establish
every live experiment or account's outcome.

## Pipeline, signal categories and diversity

Read the pinned [scoring implementation](https://github.com/xai-org/x-algorithm/blob/17c96bf346df3d62b90f1bb01830d432dba74485/xai-value-model/scoring.rs)
with the parameters/value model rather than treating a coefficient as a posting
recipe. Candidates are retrieved and hydrated, filtered for eligibility, scored,
adjusted/reranked and selected; visibility decisions can remove a selected item.
A high predicted score cannot make an ineligible item visible.

| Prediction family | Examples / interpretation |
| --- | --- |
| Engagement | Likely reaction, reply, repost, quote or share |
| Click | Likely post/profile/link interaction or media opening |
| Attention | Dwell and video continuation; some outputs are continuous values |
| Author interest | Likely follow behavior |
| Negative response | Likely not-interested, mute, block, report or insufficient attention |

These are viewer-specific predictions, not totals a creator can exchange.
The published pipeline description includes repeated-author decay to a floor.
Treat author-diversity configuration as a scoped mechanism, not a claim that
every scoring call enables it: the pinned value-model adapter disables its own
author-diversity option. Check the actual adjustment/call path and experiment
configuration before asserting an effect. Other adjustments/reranking can change order;
repeated-author decay isn't a clock enforcing a public posting interval.

Original diagnostic example: three useful posts by one fictional founder may
compete for the same viewer's limited encounter, while another viewer sees none
because retrieval/context differs. Study distinct reader jobs and actual exposure
before blaming one word in the hook. The source suggests possible mechanisms;
it does not establish that spacing posts an hour apart fixes this situation.

## Translate mechanisms into questions

| Observation | Inspect before recommending |
| --- | --- |
| Low reach | Relevant audience/context, exposure, eligibility, sample/window |
| Impressions without useful response | Whether promise/proof fits encountered readers |
| Different formats perform differently | Topic, audience, capture, distribution and measurement confounds |
| Repeated posts disappoint | Distinct reader jobs, saturation/context, not an invented timing rule |
| Negative response | Artifact/context and actual objections rather than engagement bait |

A useful hypothesis is to make the task and proof recognizable to the intended
reader. It is not “ask for replies because replies guarantee reach.” Don't
infer fixed posting intervals, hook word counts, video seconds or causal reach
improvements from implementation. Avoid coordinated manipulation or misleading
claims in pursuit of a ranking signal.

## Recommend a bounded study or artifact

Read [channel strategy](channel-strategy.md) for fit and
[social research](social-research.md) for artifact comparison. Use the supplied
source date and actual response scope. Distinguish a plausible mechanism from
observed audience effect. Recommend one relevant content change or evidence
question and a useful outcome beyond impressions. Writing owns expression;
posting, account diagnosis/access and monitoring require their own authority.
