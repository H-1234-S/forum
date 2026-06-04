## Context

This change covers public search for the AI programming community. Search complements homepage recommendations by allowing users to intentionally find articles and authors.

## Goals / Non-Goals

**Goals:**
- Allow visitors to search public articles by title, summary, body, and tags.
- Allow visitors to search public users by nickname and bio.
- Display article results and user results as distinct sections.

**Non-Goals:**
- No dedicated external search engine in v1.
- No semantic/vector search in v1.
- No advanced filters unless added by a later change.
- No searching private or hidden content.

## Decisions

### Keep v1 search database-backed

Search should use the existing PostgreSQL/Prisma persistence layer in v1 to avoid operating external search infrastructure before the core platform is stable.

### Search only public surfaces

Article search returns public articles only. User search returns public profile information only.

### Group results by type

The search page separates article and user results so users can quickly distinguish content from author profiles.

## Risks / Trade-offs

- Database-backed text search may be less powerful than a dedicated search engine → Mitigation: keep v1 scope simple and preserve fields needed for future search upgrades.
- Searching article body can be slower on large datasets → Mitigation: add appropriate indexes or limit ranking complexity during implementation.

## Migration Plan

Add indexes needed for article and user search fields during implementation.

## Open Questions

- Exact search ranking formula can be tuned during implementation.
