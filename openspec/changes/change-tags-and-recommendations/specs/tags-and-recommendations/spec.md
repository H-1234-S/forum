## ADDED Requirements

### Requirement: Tag-only article organization
The system SHALL organize articles with tags only and SHALL NOT require article categories in v1.

#### Scenario: User publishes tagged article
- **WHEN** a user publishes an article
- **THEN** the system requires 1-5 tags and no category

### Requirement: Tag selection and proposals
The system SHALL allow users to select existing tags and propose new tags during publishing.

#### Scenario: User proposes new tag
- **WHEN** a user enters a valid new tag that does not exist
- **THEN** the system associates the proposed tag with the article and makes it available for administrator normalization

### Requirement: Tag administration
The system SHALL allow administrators to merge, rename, disable, and normalize tags.

#### Scenario: Administrator merges duplicate tags
- **WHEN** an administrator merges duplicate tags
- **THEN** the system moves affected article associations to the target tag

### Requirement: Recommendation feed
The system SHALL provide an infinite-scrolling homepage recommendation feed.

#### Scenario: Visitor opens homepage
- **WHEN** a visitor opens the homepage
- **THEN** the system displays public articles from a recommendation feed

### Requirement: Guest lightweight personalization
The system SHALL personalize guest recommendations using recent locally stored browsing tags when available.

#### Scenario: Guest has recent browsing tags
- **WHEN** a guest with recent local tag history opens the homepage
- **THEN** the system boosts public articles matching those tags

### Requirement: Logged-in personalization
The system SHALL personalize logged-in recommendations using persisted behavior signals.

#### Scenario: Logged-in user has behavior history
- **WHEN** a logged-in user opens the homepage
- **THEN** the system uses views, likes, collections, comments, follows, and tag matches to rank recommended articles

### Requirement: Hot ranking
The system SHALL provide a hot ranking based on article views, likes, collections, and comments.

#### Scenario: Visitor opens hot ranking
- **WHEN** a visitor opens the hot ranking page
- **THEN** the system displays public articles ordered by the hot ranking formula

### Requirement: Related article recommendations
The system SHALL recommend related public articles on article detail pages.

#### Scenario: Visitor reads article detail
- **WHEN** a visitor opens a public article detail page
- **THEN** the system displays related articles using tag similarity and hotness signals
