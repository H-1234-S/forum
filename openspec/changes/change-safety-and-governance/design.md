## Context

This change covers baseline safety and abuse-prevention controls for the AI programming community. The platform uses publish-first moderation, so v1 needs lightweight safeguards before and after user-generated content becomes public.

## Goals / Non-Goals

**Goals:**
- Rate limit high-risk actions such as publishing, comments/replies, reports, and repeated interactions.
- Replace configured sensitive words with `***` before public display.
- Validate avatar and article images by file type, size, and count.

**Non-Goals:**
- No pre-publication manual review queue in v1.
- No advanced anti-spam ML system in v1.
- No external image moderation provider in v1.
- No destructive moderation automation beyond explicitly specified governance rules.

## Decisions

### Use lightweight rate limits at action boundaries

Rate limits should protect mutation endpoints that can create spam or abuse, especially publishing, commenting, reporting, and repeated interactions.

### Replace sensitive words before public display

Configured sensitive words are replaced with `***` in submitted article and comment text before content appears publicly.

### Centralize image validation

Avatar and article image uploads should share validation logic where possible while enforcing target-specific limits such as article image count.

## Risks / Trade-offs

- Simple sensitive-word replacement can miss variants → Mitigation: keep the dictionary configurable and allow future improvements.
- Rate limits can frustrate legitimate active users → Mitigation: tune limits during implementation and keep error messages clear.
- Local image validation does not detect harmful image content → Mitigation: v1 validates type/size/count and relies on report/admin flows for content governance.

## Migration Plan

Add storage for configurable sensitive words and any rate-limit state needed beyond in-memory development behavior during implementation.

## Open Questions

- Exact v1 rate-limit windows and thresholds can be finalized during implementation.
