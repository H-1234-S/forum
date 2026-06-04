## Context

This change covers user-facing identity and social graph features for the AI programming community. Profiles and follows make articles attributable, allow readers to discover authors, and provide durable signals for recommendation.

## Goals / Non-Goals

**Goals:**
- Provide public profile pages.
- Provide an authenticated personal center.
- Allow profile editing for avatar, nickname, and bio.
- Allow follow and unfollow relationships.
- Provide a favorites page for collected articles.

**Non-Goals:**
- No private messaging in v1.
- No badges, levels, points, or enterprise verification in v1.
- No complex social graph recommendation model in v1.

## Decisions

### Public profiles focus on technical identity

Public profiles show avatar, nickname, bio, public articles, follow count, and follower count. This keeps the profile useful without adding heavier CSDN-style reputation systems.

### Personal center is a navigation hub

The personal center should expose profile management, articles, favorites, follows, followers, notifications, and account settings as entry points rather than combining all behavior into one large page.

### Follow relationships provide both UI value and recommendation signals

Follows support author discovery and can later boost recommended content for logged-in users.

### Favorites reuse article collection data

The favorites page lists collected articles instead of creating a separate bookmark model.

## Risks / Trade-offs

- Follow counts can drift if not updated transactionally → Mitigation: update relationship and counts together or derive counts consistently.
- Avatar upload overlaps with image validation → Mitigation: use shared upload validation rules from safety/governance.
- Personal center can grow too broad → Mitigation: keep it as entry points in v1.

## Migration Plan

Add profile fields, follow relationships, and any required counters through Prisma migrations. Reuse collection persistence from interactions for favorites.

## Open Questions

- Default avatar behavior can be finalized during implementation.
