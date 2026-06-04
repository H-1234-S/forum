## Why

The AI programming community needs account authentication and role-aware access before users can publish, interact, report content, or administer the platform. Email-based accounts provide a simple v1 foundation without adding social login complexity.

## What Changes

- Add email/password registration and login requirements.
- Add email verification and password reset requirements.
- Add banned-user blocking behavior.
- Add self-service account deletion behavior.
- Add guest, authenticated user, and administrator permission distinctions.

## Impact

- Affected capability: `auth-and-accounts`
- Enables authenticated publishing, comments, follows, interactions, reports, notifications, and administrator access.
