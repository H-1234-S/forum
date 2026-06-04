## Context

This change covers the shared technical and UI foundation for the AI programming community. The product is a Next.js full-stack application, so v1 needs a clear baseline for routing, typed server procedures, client async state, persistence, local development, uploads, and responsive UI.

## Goals / Non-Goals

**Goals:**
- Use Next.js App Router with TypeScript.
- Use tRPC for typed application procedures.
- Use TanStack Query for client async state.
- Use Prisma with PostgreSQL for persistence.
- Support local PostgreSQL development through Docker.
- Store v1 uploaded images on the local filesystem.
- Provide responsive layouts and dark mode with shadcn/ui and Tailwind CSS.
- Support infinite scrolling for the homepage recommendation feed.

**Non-Goals:**
- No separate backend service in v1.
- No object storage migration in v1.
- No dedicated mobile app in v1.
- No external search or recommendation infrastructure in this foundation change.

## Decisions

### Use Next.js App Router as the application shell

Public, authenticated, and admin routes should be served through the App Router structure so routing, layouts, and metadata remain consistent.

### Keep server procedures typed with tRPC

Application mutations and dynamic queries should use typed tRPC procedures to preserve type safety across server and client boundaries.

### Use TanStack Query for client async state

Client components should rely on TanStack Query for caching, refetching, loading states, and infinite scrolling behavior.

### Persist domain data with Prisma and PostgreSQL

Accounts, profiles, articles, tags, comments, interactions, notifications, reports, and moderation state should be persisted in PostgreSQL through Prisma models.

### Store v1 images locally

Local filesystem storage keeps v1 simple while persisted metadata leaves room for later object-storage migration.

### Build UI on shadcn/ui and Tailwind CSS

The UI foundation should support responsive layouts and dark mode without creating a custom component system from scratch.

## Risks / Trade-offs

- Local image storage does not scale horizontally → Mitigation: centralize upload logic and persist metadata for future migration.
- Next.js version-specific conventions may differ from prior versions → Mitigation: read the relevant local Next.js docs before implementation.
- Infinite scrolling can hide loading or empty states → Mitigation: include explicit loading, empty, and pagination-end UI states during implementation.

## Migration Plan

Add Prisma setup, PostgreSQL configuration, Docker development configuration, upload directory configuration, and shared UI providers during implementation.

## Open Questions

- Exact local upload directory structure can be finalized during implementation.
