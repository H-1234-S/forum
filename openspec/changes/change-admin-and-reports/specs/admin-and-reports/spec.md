## ADDED Requirements

### Requirement: Report articles and comments
The system SHALL allow authenticated users to report public articles and comments.

#### Scenario: User reports article
- **WHEN** an authenticated user submits a report for a public article
- **THEN** the system records the report for administrator handling and governance rules

#### Scenario: User reports comment
- **WHEN** an authenticated user submits a report for a public comment
- **THEN** the system records the report for administrator handling

### Requirement: Report handling
The system SHALL allow administrators to process reports as pending, handled, or ignored.

#### Scenario: Administrator handles report
- **WHEN** an administrator marks a report as handled
- **THEN** the system records the handling result, handler, and handled time

#### Scenario: Administrator ignores report
- **WHEN** an administrator marks a report as ignored
- **THEN** the system records the ignored result without changing the reported target visibility

### Requirement: Article governance
The system SHALL allow administrators to view, take down, restore eligible articles, and delete articles.

#### Scenario: Administrator takes down article
- **WHEN** an administrator takes down a public article
- **THEN** the system hides the article from public surfaces and keeps it editable by the author

#### Scenario: Administrator deletes article
- **WHEN** an administrator deletes a severe-violation article
- **THEN** the system removes it from public display and prevents author republishing

#### Scenario: Republished article receives second report
- **WHEN** an article has been taken down, republished, and reported again
- **THEN** the system deletes that article and records the deletion reason

### Requirement: User management
The system SHALL allow administrators to view users and ban or unban user accounts.

#### Scenario: Administrator bans user
- **WHEN** an administrator bans a user
- **THEN** the system blocks that user from login and authenticated actions

#### Scenario: Administrator unbans user
- **WHEN** an administrator unbans a user
- **THEN** the system allows the user to log in and perform authenticated actions if otherwise eligible

### Requirement: Comment management
The system SHALL allow administrators to view and delete comments.

#### Scenario: Administrator deletes comment
- **WHEN** an administrator deletes a violating comment
- **THEN** the system removes the comment from public display

### Requirement: Tag management
The system SHALL allow administrators to merge, rename, disable, and normalize tags.

#### Scenario: Administrator merges duplicate tags
- **WHEN** an administrator merges duplicate tags into a target tag
- **THEN** the system moves affected article associations to the target tag

#### Scenario: Administrator disables tag
- **WHEN** an administrator disables a tag
- **THEN** the system prevents users from selecting it for new articles while preserving historical associations as needed

### Requirement: Moderation audit records
The system SHALL record administrator moderation actions for auditability.

#### Scenario: Administrator performs moderation action
- **WHEN** an administrator handles a report, changes article visibility, deletes a comment, changes a user ban, or changes a tag
- **THEN** the system records the actor, target, action, reason, and time
