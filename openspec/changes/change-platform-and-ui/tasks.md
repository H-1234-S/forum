## 1. Next.js Application Foundation

- [ ] 1.1 Read the relevant Next.js docs in `node_modules/next/dist/docs/` for this project version before implementation
- [ ] 1.2 Organize public, authenticated, and administrator route groups through App Router conventions
- [ ] 1.3 Configure shared layouts for public, authenticated, and administrator surfaces
- [ ] 1.4 Configure TypeScript settings needed for full-stack application code

## 2. Typed API and Client State

- [ ] 2.1 Add tRPC server setup for typed application procedures
- [ ] 2.2 Add tRPC client setup for frontend usage
- [ ] 2.3 Add TanStack Query provider setup
- [ ] 2.4 Connect client components to server data through tRPC and TanStack Query
- [ ] 2.5 Establish loading, error, empty, and pagination states for dynamic data surfaces

## 3. Persistence and Local Development

- [ ] 3.1 Add Prisma setup and client generation workflow
- [ ] 3.2 Configure PostgreSQL connection environment variables
- [ ] 3.3 Configure Docker PostgreSQL for local development
- [ ] 3.4 Add migration workflow for domain data models
- [ ] 3.5 Add seed entry point for initial local development data where needed

## 4. Local Image Storage

- [ ] 4.1 Configure local upload path environment variables
- [ ] 4.2 Implement local filesystem storage boundary for uploaded images
- [ ] 4.3 Persist image metadata for article images and avatars
- [ ] 4.4 Serve uploaded images through safe public access paths
- [ ] 4.5 Keep upload logic centralized for future object-storage migration

## 5. UI System

- [ ] 5.1 Configure shadcn/ui components used by v1 surfaces
- [ ] 5.2 Configure Tailwind CSS theme tokens
- [ ] 5.3 Add dark mode provider and theme switching behavior
- [ ] 5.4 Implement responsive layout primitives for mobile and desktop
- [ ] 5.5 Ensure public, authenticated, and administrator surfaces use consistent UI structure

## 6. Infinite Scrolling

- [ ] 6.1 Implement paginated data contract for homepage recommendation feed
- [ ] 6.2 Implement infinite scrolling trigger on the homepage feed
- [ ] 6.3 Display loading state while loading the next feed page
- [ ] 6.4 Display end-of-feed state when no more articles are available
- [ ] 6.5 Prevent duplicate page loads during active fetches

## 7. Verification

- [ ] 7.1 Add tests or smoke checks for tRPC procedure wiring
- [ ] 7.2 Add tests or smoke checks for TanStack Query provider usage
- [ ] 7.3 Verify Prisma connects to local PostgreSQL through Docker configuration
- [ ] 7.4 Verify local image storage writes metadata and serves valid files
- [ ] 7.5 Verify responsive layouts on mobile and desktop widths
- [ ] 7.6 Verify dark mode styling
- [ ] 7.7 Verify homepage infinite scrolling loads additional pages and handles end-of-feed state
