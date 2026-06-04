## 1. Tag Model and Validation

- [ ] 1.1 Add tag persistence with name, normalized name, status, and metadata fields
- [ ] 1.2 Add article-tag association persistence
- [ ] 1.3 Seed initial built-in technical tags
- [ ] 1.4 Enforce 1-5 tags per article
- [ ] 1.5 Ensure article publishing does not require categories

## 2. Tag Selection and Proposals

- [ ] 2.1 Implement existing tag lookup for article publishing
- [ ] 2.2 Implement valid new tag proposal during publishing
- [ ] 2.3 Associate proposed tags with published articles
- [ ] 2.4 Mark proposed tags for administrator normalization
- [ ] 2.5 Reject disabled tags for new article selection

## 3. Tag Administration

- [ ] 3.1 Implement tag list and filter views for administrators
- [ ] 3.2 Implement tag rename action
- [ ] 3.3 Implement duplicate tag merge action
- [ ] 3.4 Implement tag disable action
- [ ] 3.5 Preserve historical article associations when tags are disabled

## 4. Recommendation Feed

- [ ] 4.1 Implement public article feed query with pagination
- [ ] 4.2 Rank feed items using public visibility, tags, freshness, and interaction signals
- [ ] 4.3 Implement infinite scrolling for homepage recommendations
- [ ] 4.4 Exclude taken-down and deleted articles from recommendations

## 5. Personalization Signals

- [ ] 5.1 Track recent browsing tags locally for guest visitors
- [ ] 5.2 Boost guest feed articles matching recent local browsing tags
- [ ] 5.3 Persist logged-in behavior signals for views, likes, collections, comments, follows, and tag matches
- [ ] 5.4 Use logged-in behavior signals to rank recommendation feed results

## 6. Hot Ranking and Related Articles

- [ ] 6.1 Implement hot ranking formula using views, likes, collections, and comments
- [ ] 6.2 Add hot ranking page or section for public articles
- [ ] 6.3 Implement related article query using tag similarity and hotness signals
- [ ] 6.4 Display related public articles on article detail pages

## 7. Verification

- [ ] 7.1 Add tests for tag-only article validation and no-category publishing
- [ ] 7.2 Add tests for tag proposal, rename, merge, and disable behavior
- [ ] 7.3 Add tests for recommendation public visibility filtering
- [ ] 7.4 Add tests for guest tag-history boosting
- [ ] 7.5 Add tests for logged-in personalization signal ranking
- [ ] 7.6 Add tests for hot ranking and related article queries
- [ ] 7.7 Manually verify tag publishing, proposed tags, admin normalization, homepage feed, guest personalization, logged-in personalization, hot ranking, and related articles
