## Context

This change covers the article capability for the AI programming community. Articles are the primary public content unit and must support technical text, images, tags, SEO details, view counts, and publish-first governance.

## Goals / Non-Goals

**Goals:**
- Allow authenticated users to publish technical articles with text, summary, tags, and images.
- Publish articles publicly immediately without pre-review.
- Allow authors to edit and delete their own articles.
- Support takedown, author edit/republish, and second-report deletion states.
- Provide SEO-friendly article detail pages with image carousel, view count, author info, and related articles.

**Non-Goals:**
- No categories in v1; articles use tags only.
- No drafts in v1.
- No columns, paid resources, courses, or Q&A.
- No pre-publication review.

## Decisions

### Treat tags as required article metadata

Articles require 1-5 tags because tags support search, related article recommendations, and future personalized recommendations. Categories are intentionally excluded from v1.

### Store images locally in v1

Article images use local filesystem storage with persisted metadata. Each article supports up to 9 images, each no larger than 5MB and limited to JPG, PNG, or WebP.

### Publish immediately, then govern through status

New articles become public immediately. Moderation uses status transitions rather than approval queues. Taken-down articles are hidden from public surfaces but remain editable by authors. Deleted articles are not editable or publicly visible.

### Keep article detail SEO-friendly

Article detail pages should be addressable public routes with metadata derived from title and summary. Taken-down or deleted articles must not appear in public detail pages.

## Risks / Trade-offs

- Publish-first content can expose problematic material → Mitigation: upload validation, sensitive-word replacement, reporting, and admin takedown/delete flows.
- Local storage does not scale horizontally → Mitigation: centralize upload logic and store metadata so later object storage migration is straightforward.
- No drafts can frustrate authors → Mitigation: keep v1 scope small and revisit drafts after core publishing works.
- Second-report deletion can be abused → Mitigation: preserve report and status history for auditability.

## Migration Plan

Add article, article image, article status/history, and view-count persistence through Prisma migrations. Upload directories must be configured before enabling image uploads.

## Open Questions

- Duplicate-view protection rules can be finalized during implementation.
