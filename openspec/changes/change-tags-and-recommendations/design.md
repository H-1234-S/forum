## Context

This change covers the tag and recommendation foundation for the AI programming community. v1 intentionally avoids article categories and uses tags as the primary organization and recommendation signal.

## Goals / Non-Goals

**Goals:**
- Require tags for articles and avoid categories in v1.
- Allow users to select existing tags and propose new tags.
- Allow administrators to normalize, rename, merge, and disable tags.
- Provide an infinite-scrolling homepage recommendation feed.
- Support guest lightweight personalization from local browsing tags.
- Support logged-in personalization from persisted behavior signals.
- Provide hot ranking and related article recommendations.

**Non-Goals:**
- No category system in v1.
- No machine-learning ranking model in v1.
- No vector recommendation infrastructure in v1.
- No paid promotion or ad ranking.

## Decisions

### Tags are the only v1 content taxonomy

Each article uses 1-5 tags and no category. Tags are flexible enough for technical topics and are useful for search, recommendations, and future personalization.

### User-proposed tags stay administratively normalizable

Users can add new valid tags while publishing, but administrators can later merge, rename, disable, and normalize tags to avoid long-term tag drift.

### Recommendation is rule-based in v1

The homepage feed should use public article visibility, tag matches, freshness, and interaction signals rather than a complex ML stack.

### Guests use local lightweight personalization

Guest personalization can boost articles matching recent locally stored browsing tags without requiring account identity.

### Logged-in personalization uses persisted behavior signals

Logged-in recommendations use views, likes, collections, comments, follows, and tags so future recommendation improvements have durable input data.

## Risks / Trade-offs

- Tag quality can degrade if users create duplicates → Mitigation: administrator normalization and merge flows.
- Rule-based ranking can feel less personalized than ML → Mitigation: capture durable signals so ranking can evolve later.
- Guest local history is limited to the browser → Mitigation: keep it lightweight and only use it as a boost.

## Migration Plan

Add tag, article-tag, tag status, and behavior-signal persistence needed for recommendation ranking. Seed an initial built-in tag list during implementation.

## Open Questions

- The initial built-in tag list can be finalized during implementation.
- The exact v1 hot-ranking formula can be tuned during implementation.
