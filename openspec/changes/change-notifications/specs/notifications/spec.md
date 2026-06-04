## ADDED Requirements

### Requirement: Notification events
The system SHALL create notifications for important social and governance events.

#### Scenario: Article receives comment
- **WHEN** another user comments on an author's article
- **THEN** the system creates a notification for the article author

#### Scenario: Comment receives reply
- **WHEN** another user replies to a user's comment
- **THEN** the system creates a notification for the original comment author

#### Scenario: Article receives like
- **WHEN** another user likes a user's article
- **THEN** the system creates a notification for the article author

#### Scenario: User receives follower
- **WHEN** another user follows a user
- **THEN** the system creates a notification for the followed user

#### Scenario: Article moderation status changes
- **WHEN** an article is taken down or deleted by governance rules
- **THEN** the system creates a notification for the article author

### Requirement: Notification read state
The system SHALL track unread and read notification states.

#### Scenario: User marks notification as read
- **WHEN** an authenticated user marks a notification as read
- **THEN** the system updates the notification read state

### Requirement: Notification page
The system SHALL provide a personal notification page for authenticated users.

#### Scenario: User opens notification page
- **WHEN** an authenticated user opens the notification page
- **THEN** the system displays that user's notifications with unread/read state
