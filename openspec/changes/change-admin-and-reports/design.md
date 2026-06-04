## Context

This change covers the governance layer for the AI programming community. The platform uses publish-first article visibility, so administrator tools and report workflows are required to handle problematic articles, comments, users, and tags after content is already public.

## Goals / Non-Goals

**Goals:**
- Provide administrator-only management for reports, articles, comments, users, and tags.
- Support article/comment reports from authenticated users.
- Support first article takedown, author edit/republish, and second-report deletion behavior.
- Support user ban/unban and comment deletion.
- Record moderation decisions for auditability.

**Non-Goals:**
- No publication pre-review workflow.
- No complex admin permission hierarchy beyond administrator access.
- No private messaging governance in v1.
- No automated ML moderation.

## Decisions

### Use admin-only protected routes and procedures

Admin features will be exposed only through administrator-protected routes and tRPC procedures. Authorization checks must happen server-side, not only in UI rendering.

### Keep report handling state explicit

Reports use explicit states: pending, handled, and ignored. Handling records store actor, time, target, and decision so future audits can distinguish valid moderation from ignored or abusive reports.

### Model publish-first article governance as state transitions

Articles move between public, taken-down, and deleted states. A first takedown hides the article publicly but keeps it editable by the author. If the same republished article is reported again after the prior takedown, the article is deleted and no longer editable.

### Keep tag management in admin scope

Tag merge, rename, disable, and normalization live in the admin backend because tag quality directly affects recommendation and search behavior.

## Risks / Trade-offs

- Malicious repeated reports can delete republished articles → Mitigation: record report and deletion history for administrator audit.
- Admin actions can hide or delete important content → Mitigation: require admin authorization and persist moderation action records.
- Tag merges can affect many articles → Mitigation: perform merge through a dedicated operation that rewrites associations consistently.
- Banned users may still have existing content → Mitigation: ban blocks login/actions but does not automatically delete historical content.

## Migration Plan

Add report, moderation action, ban, and tag management fields/models through Prisma migrations. Seed an administrator account before enabling admin routes.

## Open Questions

- The exact number of reports required for the first takedown is not finalized.
