# Social media specs

Load when a requested social artifact must satisfy text, attachment, media or
account-specific constraints. This is a lookup method, not a frozen universal
limits table; features vary by account, publishing surface and version.

## Verify the constraint that matters

Identify platform, account tier/type when relevant, post/story/thread/carousel/
video format, client/API surface and actual production tools. Use current
first-party help/developer documentation or observed editor constraints. Record
source/date, applicable surface, limit/unit and exception. A third-party summary
can point to evidence but cannot establish an applicable current limit.

| Constraint | What to inspect |
| --- | --- |
| Text | Counting rules, links, Unicode, long-form eligibility, thread behavior |
| Images | Dimensions/aspect/crop, attachment count, accessible description |
| Video | Container/codec, size/duration/aspect, captions/audio, upload surface |
| Carousel/document | Supported type/page behavior, crop and readable viewing size |
| Links/previews | Destination, metadata, preview timing and thumbnail truth |
| API/scheduler | Account access, permissions and difference from native composer |

If unavailable, say which limit is unverified. Produce a conservative draft or
ask one material format/account decision; do not fabricate a current number.
A supplied source excerpt can be used within its date/scope, without claiming
live verification.

## Validate the produced artifact through Code

Code checks actual length/media encoding/dimensions/crop/playback when the tools
and assets exist. A script can specify an intended duration, but playback is
required to establish timing. Respect readability and safe composition across
the applicable view instead of filling every allowed pixel/character.

Return the relevant verified constraints, artifact implications and missing
checks. Loading this guide never posts, connects accounts, installs a scheduler
or gives spending authority. Platform mechanics do not replace audience judgment;
[channel strategy](channel-strategy.md) owns why the format belongs.
