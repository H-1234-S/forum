## Why

The AI programming community needs administrator governance and report handling so publish-first content can remain public by default while still allowing fast moderation when users report articles or comments.

## What Changes

- Add administrator-only backend surfaces for reports, articles, comments, users, and tags.
- Add article and comment reporting by authenticated users.
- Add report states for pending, handled, and ignored outcomes.
- Add publish-first article governance: first takedown hides an article while preserving author edit/republish, and a second report after republish deletes that same article.
- Add administrator article takedown, eligible restore, and severe-violation deletion actions.
- Add user ban/unban management that blocks banned users from login and authenticated actions.
- Add comment deletion for violating comments.
- Add tag management for merge, rename, disable, and normalization.
- Add moderation/audit records for report handling and governance decisions.

## Capabilities

### New Capabilities
- `admin-and-reports`: Admin article/user/comment/report/tag management, report handling, publish-first takedown/delete behavior, and user ban/unban behavior.

### Modified Capabilities

None.

## Impact

- Adds admin-only routes, tRPC procedures, authorization checks, and database records for reports and moderation actions.
- Affects article visibility, comment visibility, user login eligibility, tag availability, and author notifications.
- Depends on existing or planned auth roles, article status, comment, tag, and notification models.
