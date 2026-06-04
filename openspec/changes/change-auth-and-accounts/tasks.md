## 1. Account Data and Configuration

- [ ] 1.1 Add account, profile seed fields, credential, session, role, verification token, password reset token, and ban-state persistence
- [ ] 1.2 Configure authentication secrets and email delivery settings
- [ ] 1.3 Define guest, authenticated user, and administrator permission boundaries
- [ ] 1.4 Add password hashing and credential validation utilities

## 2. Registration and Email Verification

- [ ] 2.1 Implement email/password registration with required profile fields
- [ ] 2.2 Create unverified accounts after valid registration
- [ ] 2.3 Send email verification messages after registration
- [ ] 2.4 Implement verification-link handling
- [ ] 2.5 Mark accounts verified after valid verification

## 3. Login, Sessions, and Password Reset

- [ ] 3.1 Implement login for verified non-banned users
- [ ] 3.2 Reject login for invalid credentials, unverified accounts, and banned accounts
- [ ] 3.3 Start and persist sessions after successful login
- [ ] 3.4 Implement password reset request flow
- [ ] 3.5 Implement password reset completion flow with valid reset token

## 4. Permission Enforcement

- [ ] 4.1 Require login for publishing, commenting, liking, collecting, following, reporting, and profile settings
- [ ] 4.2 Require administrator role for administrator surfaces and procedures
- [ ] 4.3 Block banned users from authenticated mutations
- [ ] 4.4 Ensure protected actions return clear access errors

## 5. Account Deletion

- [ ] 5.1 Implement authenticated account deletion confirmation
- [ ] 5.2 Delete or anonymize deleted account data according to v1 rules
- [ ] 5.3 Preserve existing comments as deleted-user content
- [ ] 5.4 End active sessions after account deletion

## 6. Verification

- [ ] 6.1 Add tests for registration, verification, login, and password reset flows
- [ ] 6.2 Add tests for banned-user login and authenticated-action blocking
- [ ] 6.3 Add authorization tests for guest, authenticated user, and administrator boundaries
- [ ] 6.4 Add account deletion tests proving comments remain anonymized
- [ ] 6.5 Manually verify registration, verification, login, password reset, ban, role access, and account deletion flows
