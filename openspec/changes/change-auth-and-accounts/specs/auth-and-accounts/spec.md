## ADDED Requirements

### Requirement: Email account authentication
The system SHALL allow users to register and log in with email and password.

#### Scenario: User registers with email
- **WHEN** a visitor submits valid email, password, and required profile fields
- **THEN** the system creates an unverified user account and sends an email verification message

#### Scenario: User logs in
- **WHEN** a verified non-banned user submits valid credentials
- **THEN** the system authenticates the user and starts a session

### Requirement: Email verification and password reset
The system SHALL support email verification and password reset for account recovery.

#### Scenario: User verifies email
- **WHEN** a user opens a valid verification link
- **THEN** the system marks the account email as verified

#### Scenario: User resets password
- **WHEN** a user completes a valid password reset flow
- **THEN** the system updates the password and allows login with the new password

### Requirement: Banned user blocking
The system SHALL prevent banned users from logging in or performing authenticated actions.

#### Scenario: Banned user attempts login
- **WHEN** a banned user submits valid credentials
- **THEN** the system rejects login and explains that the account is banned

### Requirement: Account deletion
The system SHALL allow users to delete their own accounts while preserving existing comments as anonymized content.

#### Scenario: User deletes account
- **WHEN** an authenticated user confirms account deletion
- **THEN** the system deletes or anonymizes the account and displays existing comments as from a deleted user

### Requirement: Role-aware access
The system SHALL distinguish guest, authenticated user, and administrator permissions.

#### Scenario: Guest accesses protected action
- **WHEN** a guest attempts to publish, comment, like, collect, follow, report, or manage profile settings
- **THEN** the system requires login before continuing
