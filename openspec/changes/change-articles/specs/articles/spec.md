## ADDED Requirements

### Requirement: Article publishing
The system SHALL allow authenticated users to publish text-plus-image technical articles.

#### Scenario: User publishes article
- **WHEN** an authenticated user submits a title, summary, body, 1-5 tags, and optional valid images
- **THEN** the system publishes the article publicly immediately

### Requirement: Article fields
The system SHALL store title, summary, body, images, author, tags, view count, like count, collection count, comment count, visibility status, created time, and updated time for each article.

#### Scenario: Article is created
- **WHEN** an article is published
- **THEN** the system persists all required article fields and initializes interaction counts

### Requirement: Article tags
The system SHALL require each article to have 1-5 tags and SHALL NOT require categories in v1.

#### Scenario: User submits article without tags
- **WHEN** an authenticated user submits an article without tags
- **THEN** the system rejects the article submission

#### Scenario: User submits article with category omitted
- **WHEN** an authenticated user submits an article with valid tags and no category
- **THEN** the system accepts the article if all other article fields are valid

### Requirement: Article image limits
The system SHALL allow each article to include up to 9 images, with each image no larger than 5MB and limited to JPG, PNG, or WebP.

#### Scenario: User uploads invalid article image
- **WHEN** an article image exceeds limits or uses an unsupported type
- **THEN** the system rejects the image upload

### Requirement: Article author management
The system SHALL allow article authors to edit and delete their own articles.

#### Scenario: Author edits article
- **WHEN** the author submits valid edits to their article
- **THEN** the system updates the article and refreshed updated time

#### Scenario: Author deletes article
- **WHEN** the author deletes their article
- **THEN** the system removes the article from public display

### Requirement: Publish-first moderation status
The system SHALL support article statuses for public, taken down, and deleted content.

#### Scenario: Article is published
- **WHEN** a user publishes an article
- **THEN** the system sets the article status to public

#### Scenario: Article is taken down
- **WHEN** an article is taken down by governance rules
- **THEN** the system hides the article from public surfaces while preserving it for author editing

#### Scenario: Author republishes taken-down article
- **WHEN** the author submits valid edits and republishes a taken-down article
- **THEN** the system sets the article status to public again

#### Scenario: Republished article is reported again
- **WHEN** the same article has been taken down, republished, and then reported again
- **THEN** the system deletes that article and prevents further author editing

### Requirement: Article detail page
The system SHALL provide SEO-friendly public article detail pages.

#### Scenario: Visitor opens article detail
- **WHEN** a visitor opens a public article detail page
- **THEN** the system displays title, summary, body, image carousel, author information, publish time, interaction counts, comments entry point, and related articles

### Requirement: Article view counting
The system SHALL count article views for public article detail visits.

#### Scenario: Visitor reads public article
- **WHEN** a visitor opens a public article detail page
- **THEN** the system records a view according to view-counting rules

### Requirement: Public visibility filtering
The system SHALL exclude taken-down and deleted articles from public article surfaces.

#### Scenario: Visitor opens taken-down article
- **WHEN** a visitor opens an article that is taken down or deleted
- **THEN** the system does not display the article content publicly
