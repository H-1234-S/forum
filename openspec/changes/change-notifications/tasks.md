## 1. Notification Data Model

- [ ] 1.1 Add notification persistence with recipient, actor, event type, target metadata, read state, created time, and updated time
- [ ] 1.2 Define notification event types for comments, replies, likes, follows, and moderation changes
- [ ] 1.3 Add indexes for recipient notification listing and unread counts

## 2. Event Creation

- [ ] 2.1 Create notification when another user comments on an author's article
- [ ] 2.2 Create notification when another user replies to a user's comment
- [ ] 2.3 Create notification when another user likes a user's article
- [ ] 2.4 Create notification when another user follows a user
- [ ] 2.5 Create notification when an article is taken down or deleted by governance rules
- [ ] 2.6 Avoid notifying users for their own actions where not useful

## 3. Read State

- [ ] 3.1 Implement unread/read notification state
- [ ] 3.2 Implement mark-one-as-read action
- [ ] 3.3 Implement mark-all-as-read action if needed by the notification page
- [ ] 3.4 Expose unread notification count for authenticated users

## 4. Notification Page

- [ ] 4.1 Add authenticated notification page route
- [ ] 4.2 Display the current user's notifications only
- [ ] 4.3 Display unread/read state in the notification list
- [ ] 4.4 Add empty state for users with no notifications
- [ ] 4.5 Link notification items to relevant articles, comments, or profile pages when targets remain visible

## 5. Verification

- [ ] 5.1 Add tests for comment, reply, like, follow, and moderation notification creation
- [ ] 5.2 Add tests proving users cannot read another user's notifications
- [ ] 5.3 Add tests for mark-as-read behavior and unread count updates
- [ ] 5.4 Add tests for notification page query results
- [ ] 5.5 Manually verify notification creation, notification page display, unread/read state, and target links
