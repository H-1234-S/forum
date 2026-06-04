## Context

This change adds optional AI assistance to the article editor. The platform is focused on AI programming learning, so AI support should help users improve technical writing while keeping the user in control of final content.

## Goals / Non-Goals

**Goals:**
- Provide manually triggered title suggestions, summary suggestions, and content improvement suggestions.
- Keep AI output editable and never automatically published.
- Isolate AI provider details behind a configurable service boundary.
- Support future provider selection without changing user-facing requirements.

**Non-Goals:**
- No automatic full-article generation.
- No automatic replacement of user content.
- No automatic AI execution during typing or publishing.
- No provider-specific product behavior in the spec.

## Decisions

### Manual trigger only

AI assistance runs only after the user explicitly clicks an editor action. This avoids surprising edits, reduces cost, and keeps the author responsible for final content.

### Suggestions do not auto-replace content

The UI presents AI output as suggestions that users can review, edit, copy, or apply. Publishing still uses the user's final editor content.

### Provider boundary stays small

The server exposes title, summary, and improvement operations through one AI assistance boundary. Provider configuration can later use Claude API, OpenAI API, or another provider without changing article editor behavior.

### Validate inputs before AI calls

Article content inputs should be validated before calling the provider to avoid empty requests and unnecessary cost.

## Risks / Trade-offs

- AI output may be inaccurate → Mitigation: present output as suggestions and require user review before use.
- Provider cost can grow → Mitigation: manual trigger and input validation limit unnecessary calls.
- Provider choice may change → Mitigation: keep provider logic behind a service boundary.
- Long content may exceed provider limits → Mitigation: constrain request size during implementation.

## Migration Plan

Add configuration for the selected provider and implement the service boundary. No persistent data migration is required unless usage logging is later added.

## Open Questions

- The first AI provider is deferred and can be selected during implementation.
