# Content systems

Load for a technical editorial/CMS requirement. Inspect the actual application,
content owners, manifests/versions and publishing path before proposing a provider.
A request for content support doesn't imply a new CMS or runtime.

## Trace the existing path

Map author → content model/storage → validation/permissions → preview/publish →
reader/cache/search. Identify how drafts differ from public truth and who can
create, review, publish and recover. File-based content, an existing admin UI or
a current provider may already satisfy the requirement.

Compare the requested editor's actual needs: nontechnical editing, scheduling,
collaboration, preview, locale ownership, structured reuse and rollback. Inspect
existing workflow friction rather than choose the fashionable stack. Source and
provider support must match the installed version; verify current first-party
API guidance for requested integration.

## Design only necessary contracts

| Boundary | Decision / failure case |
| --- | --- |
| Model | Stable identity/slug, type, locale, required content, links/assets; avoid arbitrary schemas |
| Editorial authority | Who edits/approves/publishes; draft access isn't public access |
| Preview | Scoped authorization, expired/revoked access, private assets; no secret in browser output |
| Publish | Durable supported state and failure recovery; a click isn't completion |
| Cache/search | Actual invalidation and public inventory; draft never leaks through cache |
| Webhook | Signature/raw-body and idempotency when provider requires them; bounded retries/failures |
| Migration | Existing URLs/anchors/assets/history, staged validation and rollback ownership |

For a fictional file-based site whose only requirement is draft preview, reuse
its existing draft reader/authorization if sufficient. Don't install a headless
CMS because the task says “editorial.” If a provider genuinely earns its place,
justify tradeoffs and migration burden before implementation.

## Hand off a bounded implementation

Product decides consequential capability/rights, SEO canonical/indexability and
Writing editorial expression; technical source owners govern runtime. Use the
existing Development phase and Code proof for an authorized app change. No tokens,
provider accounts, app mutation or paid calls from loading a reference.

Return architecture facts, smallest recommendation, models/permissions/draft-
public/cache/failure boundaries, migration need and meaningful verification.
A plan is not integrated publishing proof; say which path/check didn't run.
