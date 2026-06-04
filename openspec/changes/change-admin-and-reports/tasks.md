## 1. Data Model and Permissions

- [ ] 1.1 Add persistence models for reports, report targets, moderation actions, user ban state, and tag administration fields
- [ ] 1.2 Define article status transitions for public, taken down, restored, and deleted governance states
- [ ] 1.3 Add administrator role checks for all admin and moderation procedures
- [ ] 1.4 Add audit fields for actor, target, action, reason, and timestamp on moderation actions

## 2. Report Submission

- [ ] 2.1 Implement authenticated article reporting for public articles
- [ ] 2.2 Implement authenticated comment reporting for public comments
- [ ] 2.3 Validate report target existence, target visibility, and report reason input
- [ ] 2.4 Record submitted reports with pending status for administrator handling
- [ ] 2.5 Prevent reporting hidden or deleted public targets where content is no longer publicly visible

## 3. Report Handling

- [ ] 3.1 Implement administrator report list with filters for pending, handled, and ignored reports
- [ ] 3.2 Implement report detail view showing reporter, target summary, reason, status, and history
- [ ] 3.3 Implement administrator action to mark a report as handled with result metadata
- [ ] 3.4 Implement administrator action to ignore a report without changing target visibility
- [ ] 3.5 Record handler and handled time for handled or ignored reports

## 4. Article Governance

- [ ] 4.1 Implement administrator article list with status and report-count filters
- [ ] 4.2 Implement article takedown action that hides public content while preserving author edit access
- [ ] 4.3 Implement eligible article restore action for taken-down articles when governance allows restoration
- [ ] 4.4 Implement administrator article deletion for severe violations
- [ ] 4.5 Implement second-report deletion for articles that were taken down, republished, and reported again
- [ ] 4.6 Record deletion reasons for governance-triggered article deletion

## 5. User, Comment, and Tag Administration

- [ ] 5.1 Implement administrator user list and user detail views
- [ ] 5.2 Implement ban and unban actions that affect login and authenticated actions
- [ ] 5.3 Implement administrator comment list and deletion action
- [ ] 5.4 Implement tag rename action while preserving article associations
- [ ] 5.5 Implement tag merge action that moves affected article associations to the target tag
- [ ] 5.6 Implement tag disable action that prevents future article selection while preserving historical associations

## 6. Public Visibility and Integration

- [ ] 6.1 Exclude taken-down and deleted articles from public article lists, search results, recommendations, and detail pages
- [ ] 6.2 Exclude deleted comments from public comment surfaces
- [ ] 6.3 Block banned users from authenticated mutations
- [ ] 6.4 Ensure report and moderation changes invalidate affected public and admin queries

## 7. Verification

- [ ] 7.1 Add unit tests for report validation and report status transitions
- [ ] 7.2 Add unit tests for article governance state transitions, including second-report deletion
- [ ] 7.3 Add authorization tests for administrator-only procedures
- [ ] 7.4 Add integration tests for report submission and administrator handling flows
- [ ] 7.5 Manually verify admin report handling, article takedown, author republish, second-report deletion, user ban, comment deletion, and tag management flows
