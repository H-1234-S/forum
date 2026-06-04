## 1. Profile Data and Routes

- [ ] 1.1 Add profile fields for avatar, nickname, bio, follow count, and follower count
- [ ] 1.2 Add public profile route for user pages
- [ ] 1.3 Add personal center route for authenticated users
- [ ] 1.4 Add favorites route for collected articles

## 2. Public Profile

- [ ] 2.1 Display avatar, nickname, and bio on public profile pages
- [ ] 2.2 Display public published articles by the profile owner
- [ ] 2.3 Display follow and follower counts
- [ ] 2.4 Hide non-public articles from public profile pages

## 3. Personal Center

- [ ] 3.1 Display entry points for profile management and account settings
- [ ] 3.2 Display entry points for my articles and favorites
- [ ] 3.3 Display entry points for follows, followers, and notifications
- [ ] 3.4 Require authentication for personal center access

## 4. Profile Editing

- [ ] 4.1 Implement avatar update with valid image validation
- [ ] 4.2 Implement nickname update validation and persistence
- [ ] 4.3 Implement bio update validation and persistence
- [ ] 4.4 Refresh displayed profile data after successful updates

## 5. Follow Relationships

- [ ] 5.1 Add follow relationship persistence
- [ ] 5.2 Implement follow action for authenticated users
- [ ] 5.3 Implement unfollow action for authenticated users
- [ ] 5.4 Update follow and follower counts after follow changes
- [ ] 5.5 Prevent invalid follow relationships such as following oneself

## 6. Favorites

- [ ] 6.1 Display collected articles on the favorites page
- [ ] 6.2 Require authentication for favorites access
- [ ] 6.3 Exclude non-public articles from favorites display where public visibility rules require it

## 7. Verification

- [ ] 7.1 Add tests for public profile visibility and hidden article filtering
- [ ] 7.2 Add tests for personal center authentication
- [ ] 7.3 Add tests for profile editing validation
- [ ] 7.4 Add tests for follow and unfollow count updates
- [ ] 7.5 Add tests for favorites page article listing
- [ ] 7.6 Manually verify public profile, personal center, profile editing, follow/unfollow, and favorites flows
