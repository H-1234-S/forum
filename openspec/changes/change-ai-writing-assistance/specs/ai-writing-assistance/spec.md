## ADDED Requirements

### Requirement: Manual AI title generation
The system SHALL allow authenticated users to manually request AI-generated article title suggestions.

#### Scenario: User requests title suggestions
- **WHEN** an authenticated user manually triggers title generation from article content
- **THEN** the system returns title suggestions without automatically replacing the user's title

### Requirement: Manual AI summary generation
The system SHALL allow authenticated users to manually request AI-generated article summaries.

#### Scenario: User requests summary suggestion
- **WHEN** an authenticated user manually triggers summary generation from article content
- **THEN** the system returns a summary suggestion that the user can edit before publishing

### Requirement: Manual AI content improvement
The system SHALL allow authenticated users to manually request AI-assisted content improvement suggestions.

#### Scenario: User requests content improvement
- **WHEN** an authenticated user manually triggers content improvement
- **THEN** the system returns improved content suggestions without automatically publishing changes

### Requirement: User-controlled AI output
The system SHALL require users to review AI suggestions before saving or publishing them.

#### Scenario: AI suggestion is returned
- **WHEN** the system returns an AI writing suggestion
- **THEN** the article editor presents it as reviewable content and does not publish it automatically

### Requirement: Deferred AI provider
The system SHALL keep AI provider selection configurable and outside user-facing product requirements.

#### Scenario: AI provider is configured
- **WHEN** the application calls an AI writing assistance feature
- **THEN** the system uses the configured provider through the AI assistance boundary
