## Context

This change covers discussion and article interaction features for the AI programming community. Comments, likes, collections, and shares are core CSDN-style v1 interactions and also provide behavior signals for recommendations.

## Goals / Non-Goals

**Goals:**
- Support top-level comments and one level of replies on public articles.
- Allow comment authors to edit and delete their own comments and replies.
- Allow authenticated users to like and unlike public articles.
- Allow authenticated users to collect and uncollect public articles.
- Provide a shareable public article link and record share signals when applicable.

**Non-Goals:**
- No deeply nested comment trees in v1.
- No comment likes in v1 unless added by a later change.
- No private messaging from comments in v1.
- No paid collection folders or advanced bookmark organization.

## Decisions

### Comments are limited to two levels

Top-level comments and one reply level keep discussion useful while avoiding the complexity of deeply nested threads.

### Interaction counts stay on articles

Article like, collection, and comment counts should be updated when interactions change so public lists and ranking formulas can use them efficiently.

### Collections power the favorites page

Collecting an article is the underlying behavior for the user's favorites page.

### Sharing stays lightweight

The system provides a shareable article link and records a share signal when applicable, without requiring external social-platform integrations in v1.

## Risks / Trade-offs

- Interaction counts can drift if mutations fail halfway → Mitigation: update interaction records and counts together.
- Comment deletion can break reply context → Mitigation: define public removal rules during implementation.
- Share tracking may be limited by browser capabilities → Mitigation: record only when the app can observe the share action.

## Migration Plan

Add comment, reply, like, collection, and optional share-signal persistence. Add counters to article persistence if not already present.

## Open Questions

- Exact comment deletion display text can be finalized during implementation.
