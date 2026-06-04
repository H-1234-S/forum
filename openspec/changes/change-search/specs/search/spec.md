## ADDED Requirements

### Requirement: Article search
The system SHALL allow visitors to search public articles by title, summary, body, and tags.

#### Scenario: Visitor searches articles
- **WHEN** a visitor submits an article search query
- **THEN** the system returns matching public articles

### Requirement: User search
The system SHALL allow visitors to search users by nickname and bio.

#### Scenario: Visitor searches users
- **WHEN** a visitor submits a user search query
- **THEN** the system returns matching public user profiles

### Requirement: Search result grouping
The system SHALL separate article results and user results on the search results page.

#### Scenario: Visitor opens search results
- **WHEN** a visitor searches across the site
- **THEN** the system displays article results and user results as distinct sections
