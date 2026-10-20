# Agentic Workflows

Reusable skills and workflows for developing and marketing your application with
your existing coding agent. Start with **Development** or **Marketing**, describe
the result you want, and load the methods relevant to that task.

The package supplies instructions, references and thin Codex/Claude Code actor
definitions. You supply the client, account, model access and application tools.
It has no hosted team, application runtime, installer or background updater.
Native definitions and format checks do not establish reliable task delivery.

## What you get

| Skill | Responsibility |
| --- | --- |
| `development` | Discover the host, choose effort, implement, verify and coordinate source review |
| `lead-agent` | Main-conversation scope, decisions, assignments and continuation |
| `code-agent` | Produce/integrate code, prose and media; execute all checks and accepted fixes |
| `review-agent` | Independently inspect plans, source and supplied evidence read-only |
| `product` | Establish the user outcome, alternatives, business rules and supported value |
| `frontend` | Inspect visual references, agree unsettled direction, build usable accessible UI |
| `marketing` | Research an audience, choose an argument/channel, distribute under authority and learn |
| `writing` | Shape a source-grounded draft or edit for its reader, voice and medium |
| `seo` | Diagnose search/discovery problems and choose the smallest supported correction |
| `taste` | Develop judgment from inspected work and preserve real contextual feedback |

Four engineering procedures live in `.agents/workflows`: **Proposal**,
**Challenge**, **Implementation** and **AI Code Review**. Their outputs differ;
selecting one phase stops at that phase. Ordinary content uses its own relevant
owners. The [package map](docs/package-map.md) lists every entry, procedure,
reference and conditional trigger. The [source reference](REFERENCE.md) connects
our methods to primary guidance and research. Both documents are optional human
reference material, outside the installed instruction context.

## Install into an existing repository

Clone the package, then open your application's repository in your coding tool:

```sh
git clone https://github.com/coremvp/agentic-workflows.git
```

Use a reviewed source commit; prefer a tagged release when available. Give your
agent the source checkout path and this request:

```text
Install Agentic Workflows from the source checkout I provide into this
repository. Read its README installation contract and inspect my existing
instructions, skills and native actors. Show the exact file plan and any
conflicts. Preserve my configuration, custom instructions and learned Taste
feedback. Install only this package after I resolve material conflicts;
do not change application code or call paid providers.
```

The installation plan identifies the source commit, target repository and selected
client(s). Read the source's `.agents/skills/lead-agent/SKILL.md` and
`.agents/skills/code-agent/SKILL.md` for actor boundaries; do not spawn a native
actor while its target role files are missing. No new account is needed.

The literal file plan, also the manual fallback:

1. Copy all ten `.agents/skills/<name>` directories with their complete support
   files, and the four `.agents/workflows/*.md` procedures. Preserve the relative
   layout. Copy `LICENSE` to `AGENTIC_WORKFLOWS_LICENSE` in the host root and
   record the component scope in the host's existing README/notices: these ten
   directories, four procedures, selected native Code/Review definitions and
   derived discovery links. The package's root `AGENTS.md` is maintenance context;
   it must not replace the application's instructions. `docs/` is optional human
   reference, not an agent preload or an application requirement.
2. For Codex, copy the two `.codex/agents/*.toml` definitions. Preserve existing
   client/global settings, models, approval/sandbox policy and concurrency. For
   Claude Code, copy the two `.claude/agents/*.md` definitions and create each
   `.claude/skills/<name>` symlink to `../../.agents/skills/<name>`. Code inherits
   the client's defaults. Claude Review lists only Read/Grep/Glob and preloads
   its role through `skills`; Code preloads its own role the same way.
3. Merge the routing text below into the host's existing instructions. If there
   is no `AGENTS.md`, create a minimal routing file with no invented app facts.
   This checkout's `CLAUDE.md` is a real relative symlink to `AGENTS.md`. Create
   that link in the host only if `CLAUDE.md` is absent; preserve a correct link.
   If another file/link exists, surface its content/target and agree how to keep
   its custom instructions before any replacement. Current Claude guidance also
   supports native `AGENTS.md` loading and imports, with settings/version caveats;
   those modes are not equivalent to this package's chosen symlink layout.
4. Surface any skill, actor, instruction-file or nonempty-directory collision
   before writing it. The user decides material replacements. Do not overwrite
   host configuration, domain/runtime rules or learned Taste entries. In
   particular, `taste/references/project-judgment.md` becomes project-owned after
   installation; merge an intentional update without resetting that history to
   the empty distribution template.
5. Record source commit and local adaptations in the host README. Check copied
   Markdown paths/anchors, canonical and Claude alias references, native formats
   and actual symlink targets. Verify Git records each real link as mode `120000`;
   a regular text file containing a target is not a symlink. Report static checks
   separately from client discovery and actual delegated work.

Suggested routing text to merge into host instructions:

```text
For an authorized engineering outcome, load .agents/skills/development/SKILL.md.
For marketing, load .agents/skills/marketing/SKILL.md; ordinary content uses
its relevant owners rather than the four engineering phases by default.
Lead stays in the main conversation; Code produces and executes checks;
independent Review reads source/evidence without writes or execution.
Choose effort from the actual uncertainty and consequence. Clear bounded
work with an established approach skips a fresh Proposal/Challenge cycle.
Load Taste for consequential creative choices or useful real feedback.
Read this repository's own application/domain instructions first.
```

If the OS/checkout cannot preserve links, use documented derived copies under
`.claude/skills` from the canonical directories. Refresh those copies on updates;
do not maintain a second independent corpus. The Claude actors still need their
matching role skills discoverable for preload. Report this installation mode and
its checks explicitly.

## Use it

In Codex, start with `Use $development ...` or `Use $marketing ...`. In Claude
Code use `/development ...` or `/marketing ...`. Name the outcome and constraints;
the package discovers the host's architecture and tools instead of imposing a
framework, database, provider or deployment model.

Effort follows the task:

- **Clear bounded work:** the goal, acceptance, owner and established approach
  are known. Code makes the change and runs focused proof. Skip fresh external
  research, Proposal and Challenge unless a material unknown appears. Mechanical
  edits do not require a new actor merely because the package is installed;
  meaningful behavior changes retain appropriate independent review when
  supported. A small handoff contains source/target, intended result, actual
  checks/limits and next action in the conversation or existing record.
- **Design-bearing work:** resolve consequential ambiguity or competing
  approaches through focused research, Proposal and independent Challenge.
  Code implements the accepted contract, Review inspects source/evidence, Code
  fixes admitted findings and Review closes them. An already accepted design
  skips repeated planning.
- **A selected phase:** finish the requested proposal, challenge,
  implementation or review phase and stop there.

A multi-step, delegated or interrupted task uses one ignored continuation record
when needed. An expanded packet, hash ledger and full review repetition are not
requirements for every small change. A moving/dirty target still needs enough
source binding for independent Review to know what it inspected.

For unsettled frontend direction, inspect references and a rendered proposal
before application implementation. The user agrees the direction; bounded
accepted work then continues. Taste lessons retain context, source, exceptions
and revision conditions; they do not train the model or impose a universal style.

Publishing, outreach, spending, provider setup and production retain separate
authority. Installing instructions does not authorize an application exercise.

### Native discovery and permission limits

Codex uses repository `.agents/skills`; Claude uses `.claude/skills`. The supplied
native names are `code-agent` and `review-agent`; Lead remains in the main
conversation. Loading a skill does not itself start a subagent. Claude's `skills`
field preloads the role; assigned domains remain explicit reads because ordinary
non-fork subagents do not inherit the parent's loaded skills/history.

Verify the actual skill base/path shown by your client. A personal, ancestor or
other installed skill with the same name may be selected in a particular
configuration; a matching name alone does not prove this repository's file was
loaded. Read the canonical `.agents/skills/<name>/SKILL.md` explicitly when
selection is unclear. Use canonical `.agents/` paths for search: Glob/Grep may
not traverse Claude's symlink aliases even when direct reads work.

Claude Review exposes Read/Grep/Glob only. Codex custom agents inherit the
parent's effective sandbox and approval policy: `sandbox_mode` and
`approval_policy` in a custom agent file do not override those settings. The
Codex Review definition therefore states a behavioral read-only/no-execution
contract, without claiming independent permission isolation. Do not change the
parent's settings or universally disable shell access to simulate isolation;
a host may use its shell as the available source reader. Missing proof returns
to Code through Lead. Review never runs checks or writes scratch.

The included definitions and source checks do not establish compatibility with
every client version or configuration, or reliable task delivery. After
installation, start a fresh session in your coding tool:

1. Inspect skill/actor discovery and the actual canonical paths. For Claude,
   inspect `/skills`, `/agents` and `/memory`; confirm both role preloads and
   Review's tool list. For Codex, inspect the available skills/actors and
   inherited effective settings using that client's current controls.
2. Ask Lead to assign one bounded **read-only assessment of existing source** to
   Review with the canonical role and applicable domain paths. Confirm its report
   identifies source/evidence limits and requests missing execution from Code.
   A listing proves discovery; this assessment checks one actor interaction.
3. On package source or an already selected real task, request one phase only
   and confirm it stops there. If an existing interrupted task has a continuation
   record, resume from its accepted decisions and actual current source rather
   than repeat planning. Do not manufacture an app mutation to test this.
4. Use the package for your next real authorized task, with normal task-specific
   proof. Do not invent an application change as installation validation.

If delegation is unavailable, explicitly load canonical roles and disclose
sequential self-review. One conversation changing roles is not independent
review. Other Agent Skills clients may read the files, but their native actor
discovery and permission behavior are not verified by this package.

## Update intentionally

Compare the recorded installed commit with the new reviewed source. Plan changes
to package-owned paths, surface customized-file conflicts and preserve host
AGENTS/CLAUDE/configuration, domain contracts and learned Taste. Refresh derived
Claude copies when used. Recheck references and changed native definitions;
reuse prior proof only when its tested content and inputs remain unchanged.

## Conditional depth

Entry points route to practical support when its decision matters. Development
covers engineering risks, proof selection, debugging and technical content
systems. Marketing retains research, conversion/forms/testing, content, launches,
channels, social constraints and X algorithm mechanics. Writing covers reader
promise, voice, editing and medium-specific production. SEO covers layered
diagnosis, intent, titles, international and local search. Product owns outcome
and positioning; Frontend owns visual/UI decisions; Taste preserves contextual
judgment. No task preloads the whole reference library.

## License and contributions

The package is [MIT licensed](LICENSE). Its license does not cover proprietary
application files or other repositories. For installation changes, follow
[Update intentionally](#update-intentionally); installed copies do not update
automatically.

Prefer contributions tied to a concrete failure or decision in the nearest owner.
Contribute only material you may distribute under this package's license. Remove
private feedback, secrets, account records and application source you cannot
share. The package contains no telemetry that uploads project data.

Client references: [Agent Skills](https://agentskills.io/specification),
[Codex skills](https://learn.chatgpt.com/docs/build-skills),
[Codex subagents](https://learn.chatgpt.com/docs/agent-configuration/subagents),
[Claude skills](https://code.claude.com/docs/en/skills),
[Claude project instructions](https://code.claude.com/docs/en/memory#agentsmd),
[Claude subagents](https://code.claude.com/docs/en/sub-agents).
