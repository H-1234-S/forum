## Why

Articles are the core content unit of the AI programming community. v1 needs technical article publishing, image support, detail pages, SEO, view counts, author management, and publish-first moderation behavior.

## What Changes

- Add authenticated text-plus-image article publishing.
- Require each article to include title, summary, body, and 1-5 tags.
- Support up to 9 article images, 5MB per image, limited to JPG, PNG, and WebP.
- Store article images locally for v1.
- Publish articles publicly immediately without pre-review.
- Add article statuses for public, taken down, and deleted content.
- Allow authors to edit and delete their own articles.
- Allow authors to edit taken-down articles and republish them.
- Delete the same republished article when it is reported again after a prior takedown.
- Add SEO-friendly article detail pages, image carousel, view counts, and related article display.

## Capabilities

### New Capabilities
- `articles`: Text-plus-image article publishing, local image storage, publish-first moderation, SEO detail pages, view counts, author edit/delete, takedown/republish/delete states.

### Modified Capabilities

None.

## Impact

- Adds article routes, editor UI, detail UI, upload handling, tRPC procedures, Prisma models, status transitions, and author permissions.
- Interacts with tags, recommendations, comments, reports, notifications, safety validation, and local file storage.
