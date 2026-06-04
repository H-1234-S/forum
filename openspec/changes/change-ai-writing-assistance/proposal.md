## Why

The article editor should help users produce better technical content without making AI output automatic or mandatory. v1 needs a provider-flexible AI assistance boundary so the first provider can be selected later.

## What Changes

- Add manually triggered AI title suggestion from article content.
- Add manually triggered AI summary suggestion from article content.
- Add manually triggered AI content improvement suggestions.
- Keep AI suggestions reviewable and editable before users save or publish.
- Keep provider selection deferred behind a configurable service boundary.
- Do not automatically replace user content or publish AI-generated output.

## Capabilities

### New Capabilities
- `ai-writing-assistance`: Manually triggered title generation, summary generation, and content optimization assistance with provider selection deferred.

### Modified Capabilities

None.

## Impact

- Adds article editor UI controls, tRPC procedures, server-side AI assistance service boundary, provider configuration, and validation around article content inputs.
- May add dependency on a selected AI provider SDK during implementation, but the spec keeps provider choice outside product behavior.
