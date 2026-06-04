## 1. Data Model

- [ ] 1.1 Add comment persistence for top-level comments and one reply level
- [ ] 1.2 Add author, article, parent comment, content, deleted state, created time, and updated time fields for comments
- [ ] 1.3 Add article like persistence with unique user/article relationship
- [ ] 1.4 Add article collection persistence with unique user/article relationship
- [ ] 1.5 Add optional share-signal persistence when share actions are observable

## 2. Comments and Replies

- [ ] 2.1 Implement authenticated top-level comment submission on public articles
- [ ] 2.2 Implement authenticated reply submission to top-level comments
- [ ] 2.3 Prevent replies to replies beyond one level
- [ ] 2.4 Display comments and replies on public article detail pages
- [ ] 2.5 Increment article comment count when public comments or replies are created

## 3. Comment Author Management

- [ ] 3.1 Implement author-only comment and reply editing
- [ ] 3.2 Update comment content and updated time after valid edits
- [ ] 3.3 Implement author-only comment and reply deletion
- [ ] 3.4 Remove deleted comments from public display according to deletion rules
- [ ] 3.5 Update article comment count when deletion rules require count changes

## 4. Article Likes

- [ ] 4.1 Implement authenticated like action for public articles
- [ ] 4.2 Implement authenticated unlike action for previously liked articles
- [ ] 4.3 Keep article like count in sync with like and unlike actions
- [ ] 4.4 Prevent duplicate likes by the same user on the same article

## 5. Article Collections

- [ ] 5.1 Implement authenticated collect action for public articles
- [ ] 5.2 Implement authenticated uncollect action for previously collected articles
- [ ] 5.3 Keep article collection count in sync with collect and uncollect actions
- [ ] 5.4 Prevent duplicate collections by the same user on the same article

## 6. Article Sharing

- [ ] 6.1 Provide shareable public article links
- [ ] 6.2 Add article detail UI action for sharing
- [ ] 6.3 Record share signal when the app can observe a share action
- [ ] 6.4 Ensure sharing is only available for public articles

## 7. Verification

- [ ] 7.1 Add tests for top-level comments and one-level replies
- [ ] 7.2 Add tests preventing replies beyond one level
- [ ] 7.3 Add tests for comment author edit and delete permissions
- [ ] 7.4 Add tests for like/unlike count synchronization and duplicate prevention
- [ ] 7.5 Add tests for collect/uncollect count synchronization and duplicate prevention
- [ ] 7.6 Add tests for share link availability on public articles
- [ ] 7.7 Manually verify comments, replies, edit/delete, like/unlike, collect/uncollect, and sharing flows
