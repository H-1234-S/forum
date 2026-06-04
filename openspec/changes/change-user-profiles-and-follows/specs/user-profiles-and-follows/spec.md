## ADDED Requirements

### Requirement: Public user profile
The system SHALL provide public profile pages for users.

#### Scenario: Visitor opens public profile
- **WHEN** a visitor opens a user's public profile
- **THEN** the system displays avatar, nickname, bio, published public articles, follow count, and follower count

### Requirement: Personal center
The system SHALL provide authenticated users with a personal center.

#### Scenario: User opens personal center
- **WHEN** an authenticated user opens the personal center
- **THEN** the system displays entry points for profile management, my articles, favorites, follows, followers, notifications, and account settings

### Requirement: Profile editing
The system SHALL allow users to edit their avatar, nickname, and bio.

#### Scenario: User updates profile
- **WHEN** an authenticated user submits valid profile changes
- **THEN** the system saves and displays the updated profile

### Requirement: Follow relationships
The system SHALL allow authenticated users to follow and unfollow other users.

#### Scenario: User follows another user
- **WHEN** an authenticated user follows another user
- **THEN** the system creates the follow relationship and updates follow/follower counts

#### Scenario: User unfollows another user
- **WHEN** an authenticated user unfollows another user
- **THEN** the system removes the follow relationship and updates follow/follower counts

### Requirement: Favorites page
The system SHALL provide users with a page listing their collected articles.

#### Scenario: User views favorites
- **WHEN** an authenticated user opens the favorites page
- **THEN** the system displays articles the user has collected
