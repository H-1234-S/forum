## Context

This change covers the account and permission foundation for the AI programming community. Most v1 features depend on distinguishing guests, authenticated users, administrators, verified accounts, and banned accounts.

## Goals / Non-Goals

**Goals:**
- Support email/password registration and login.
- Require email verification before normal authenticated usage.
- Support password reset.
- Block banned users from login and authenticated actions.
- Support user account deletion with anonymized comment preservation.
- Define role-aware access for public, authenticated, and administrator actions.

**Non-Goals:**
- No social login in v1.
- No enterprise SSO.
- No multi-factor authentication in v1.
- No private messaging access rules because private messaging is deferred to v1.1.

## Decisions

### Use email/password as the v1 account baseline

Email/password keeps v1 authentication understandable and avoids external OAuth provider setup during the initial platform build.

### Email verification gates account trust

New registrations create unverified accounts and send verification email. Verified, non-banned users can start sessions and perform authenticated actions.

### Bans are enforced at login and mutation boundaries

Banned users must be blocked from login and from authenticated procedures so active sessions cannot continue performing protected actions after a ban.

### Preserve comments as anonymized content after account deletion

Deleting an account should remove or anonymize the account while preserving existing comment threads as deleted-user content so article discussions remain coherent.

## Risks / Trade-offs

- Email delivery failures can block verification → Mitigation: expose resend verification behavior during implementation if needed.
- Account deletion can affect authored content ownership → Mitigation: define deletion behavior explicitly for comments in v1 and revisit article ownership behavior during implementation.
- Banned-session enforcement can be missed if only checked at login → Mitigation: check ban state at authenticated action boundaries.

## Migration Plan

Add user account, credential/session, verification, password reset, role, and ban-state persistence through Prisma migrations.

## Open Questions

- Final account deletion behavior for published articles can be refined during implementation.
