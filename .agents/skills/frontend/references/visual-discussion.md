# Visual discussion before implementation

For an unsettled frontend design or redesign, establish the surface's purpose,
the user's decision, useful information, format, hierarchy and intended interaction
before application implementation. Discuss the direction visibly with the user.

Inspect exact relevant pages/sections/interactions. Show actual screenshots in the
conversation, or exact local image paths where the client cannot display images;
identify each source and explain what to adapt: hierarchy, density,
type, layout, visual weight, interaction or motion. Links and names alone are
insufficient. [UI references](ui-references.md) helps discovery; existing approved
application UI is the first reference. Component galleries provide visual grammar,
not the product's information design.

Show the current application where relevant and a rendered proposed mockup the
user can judge. Label reference, current application and proposal separately.
Use deterministic HTML/TSX/SVG for mockups; disclose illustrative data and unwired
controls. Include relevant desktop and mobile views. Material motion needs an
interactive preview as well as useful stills. A prototype does not authorize an
application change. Keep mockups, render scripts and captures in the assigned
scratch root; a temporary application route or component is an application edit.
Do not create one as a workaround for missing preview tools. State the actual
render/capture limit and the smallest useful fallback.

Recommend one considered direction or a small comparison with a clear tradeoff.
Every chart, table, feed, metric and substantial figure needs a distinct job:
name the question, source, units/comparison and resulting decision where useful.
Remove repeated information unless another format adds meaningful drilldown.
Avoid default stat-card compositions without a demonstrated user need; meaningful
metric cards remain valid. Do not invent activity, geography, revenue or provider
truth for a signature visual.

When a direction is rejected, reconsider information and composition before
producing another cosmetic variation. Record actual accepted decisions. Once a
direction is accepted and implementation is authorized, continue bounded work
and small fixes without repeated approval or another full case study. Tiny fixes
within established approved UI do not require this full discussion. The user's
explicit instructions and prior accepted decisions remain authority.

After agreement write the task-specific implementation contract in the ignored
task record using Frontend's fields; do not store it in this reference. Then
compare the real app's rendered result. Preserve authentication, billing, data access, semantic/keyboard
behavior and supported loading/empty/error states. Neither a mockup nor a static
source check establishes that the application works.
