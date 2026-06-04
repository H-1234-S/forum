## ADDED Requirements

### Requirement: Rate limiting
The system SHALL rate limit high-risk user actions including article publishing, comments/replies, reports, and repeated interactions.

#### Scenario: User exceeds publishing rate limit
- **WHEN** an authenticated user exceeds the article publishing rate limit
- **THEN** the system rejects additional publish attempts until the limit window resets

#### Scenario: User exceeds comment rate limit
- **WHEN** an authenticated user exceeds the comment or reply rate limit
- **THEN** the system rejects additional comment submissions until the limit window resets

### Requirement: Sensitive-word replacement
The system SHALL replace configured sensitive words with `***` before publishing user-generated text.

#### Scenario: Article contains sensitive words
- **WHEN** a user submits an article title, summary, or body containing configured sensitive words
- **THEN** the system replaces those words with `***` before public display

#### Scenario: Comment contains sensitive words
- **WHEN** a user submits a comment containing configured sensitive words
- **THEN** the system replaces those words with `***` before public display

### Requirement: Image validation
The system SHALL validate uploaded images by file type, size, and count according to the target usage.

#### Scenario: User uploads invalid avatar
- **WHEN** a user uploads an avatar with unsupported type or excessive size
- **THEN** the system rejects the upload

#### Scenario: User uploads too many article images
- **WHEN** a user uploads more than 9 images for one article
- **THEN** the system rejects images beyond the allowed count
