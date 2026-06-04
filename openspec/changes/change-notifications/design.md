## Context

This change covers user notifications for social and governance events in the AI programming community. Notifications help users respond to article discussion, follows, and moderation outcomes.

## Goals / Non-Goals

**Goals:**
- Create notifications for article comments.
- Create notifications for replies to comments.
- Create notifications for article likes.
- Create notifications for new followers.
- Create notifications when article moderation status changes.
- Track unread and read notification state.
- Provide a personal notification page.

**Non-Goals:**
- No real-time push delivery in v1.
- No email notification digest in v1.
- No private-message notifications because private messaging is deferred to v1.1.

## Decisions

### Persist notifications as user-owned records

Notifications should be stored per recipient so the notification page can display history and unread state reliably.

### Keep delivery in-app for v1

v1 only requires in-app notification display. This avoids WebSocket, push, and email-delivery complexity.

### Governance notifications are mandatory

Article authors should be notified when their article is taken down or deleted so publish-first moderation remains understandable.

## Risks / Trade-offs

- High-frequency likes can create noisy notifications → Mitigation: implementation can deduplicate or throttle if needed while preserving the requirement to notify.
- In-app only notifications may be missed → Mitigation: keep v1 simple and add email/push later if needed.

## Migration Plan

Add notification persistence with recipient, actor, event type, target metadata, read state, and timestamps.

## Open Questions

- Exact notification grouping/deduplication behavior can be refined during implementation.
