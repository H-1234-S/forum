## ADDED Requirements

### Requirement: Two-level comments
The system SHALL support top-level comments and one level of replies on public articles.

#### Scenario: User posts top-level comment
- **WHEN** an authenticated user submits a valid comment on a public article
- **THEN** the system publishes the comment under that article

#### Scenario: User replies to comment
- **WHEN** an authenticated user submits a valid reply to a top-level comment
- **THEN** the system publishes the reply under that comment

### Requirement: Comment author management
The system SHALL allow comment authors to edit and delete their own comments and replies.

#### Scenario: Author edits comment
- **WHEN** a comment author submits valid edits
- **THEN** the system updates the comment content and updated time

#### Scenario: Author deletes comment
- **WHEN** a comment author deletes their comment
- **THEN** the system removes the comment from public display according to comment deletion rules

### Requirement: Article likes
The system SHALL allow authenticated users to like and unlike public articles.

#### Scenario: User likes article
- **WHEN** an authenticated user likes a public article
- **THEN** the system records the like and increments the article like count

#### Scenario: User unlikes article
- **WHEN** an authenticated user unlikes a previously liked article
- **THEN** the system removes the like and decrements the article like count

### Requirement: Article collections
The system SHALL allow authenticated users to collect and uncollect public articles.

#### Scenario: User collects article
- **WHEN** an authenticated user collects a public article
- **THEN** the system records the collection and increments the article collection count

#### Scenario: User uncollects article
- **WHEN** an authenticated user uncollects a previously collected article
- **THEN** the system removes the collection and decrements the article collection count

### Requirement: Article sharing
The system SHALL provide a way to share public articles.

#### Scenario: User shares article
- **WHEN** a user invokes article sharing
- **THEN** the system provides a shareable article link and records a share signal when applicable
