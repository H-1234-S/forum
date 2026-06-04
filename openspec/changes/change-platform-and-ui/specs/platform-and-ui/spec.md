## ADDED Requirements

### Requirement: Next.js full-stack architecture
The system SHALL use Next.js App Router with TypeScript for the full-stack application.

#### Scenario: User opens application route
- **WHEN** a user opens a public or authenticated route
- **THEN** the system serves the route through the Next.js App Router structure

### Requirement: tRPC and TanStack Query data flow
The system SHALL use tRPC for typed application procedures and TanStack Query for client asynchronous state.

#### Scenario: Client loads dynamic data
- **WHEN** a client component needs server data
- **THEN** the system retrieves it through typed tRPC procedures and manages client state with TanStack Query

### Requirement: Prisma and PostgreSQL persistence
The system SHALL use Prisma with PostgreSQL for application persistence.

#### Scenario: Domain data is persisted
- **WHEN** the system stores accounts, profiles, articles, tags, comments, interactions, notifications, or reports
- **THEN** the system persists the data in PostgreSQL through Prisma models

### Requirement: Local Docker database
The system SHALL support running PostgreSQL locally through Docker for development.

#### Scenario: Developer starts local database
- **WHEN** the developer starts the configured Docker database
- **THEN** the application can connect to PostgreSQL for local development

### Requirement: Local image storage
The system SHALL store v1 uploaded images on the local filesystem.

#### Scenario: User uploads valid image
- **WHEN** a user uploads a valid article image or avatar
- **THEN** the system stores the file locally and persists its metadata

### Requirement: Responsive UI and dark mode
The system SHALL provide responsive layouts and dark mode using shadcn/ui and Tailwind CSS.

#### Scenario: User changes viewport or theme
- **WHEN** a user opens the application on mobile, desktop, or dark mode
- **THEN** the system displays usable layouts and theme-appropriate styling

### Requirement: Infinite scrolling
The system SHALL support infinite scrolling for the homepage recommendation feed.

#### Scenario: User reaches feed end
- **WHEN** a user scrolls near the end of the current homepage feed
- **THEN** the system loads the next page of recommended articles
