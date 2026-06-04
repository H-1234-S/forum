## 1. Search Data and Indexing

- [ ] 1.1 Identify article fields used for v1 search: title, summary, body, and tags
- [ ] 1.2 Identify user fields used for v1 search: nickname and bio
- [ ] 1.3 Add database indexes needed for article search queries
- [ ] 1.4 Add database indexes needed for user search queries

## 2. Article Search

- [ ] 2.1 Implement public article search procedure
- [ ] 2.2 Match article queries against title, summary, body, and tags
- [ ] 2.3 Return only public articles
- [ ] 2.4 Exclude taken-down and deleted articles from search results
- [ ] 2.5 Paginate article search results

## 3. User Search

- [ ] 3.1 Implement public user search procedure
- [ ] 3.2 Match user queries against nickname and bio
- [ ] 3.3 Return only public profile fields
- [ ] 3.4 Paginate user search results

## 4. Search UI

- [ ] 4.1 Add search input entry point in public navigation
- [ ] 4.2 Add search results page
- [ ] 4.3 Display article results and user results as distinct sections
- [ ] 4.4 Show empty states for no article or user results
- [ ] 4.5 Preserve the submitted query in the results UI

## 5. Verification

- [ ] 5.1 Add tests for article search matching title, summary, body, and tags
- [ ] 5.2 Add tests proving hidden articles are excluded from article search
- [ ] 5.3 Add tests for user search matching nickname and bio
- [ ] 5.4 Add tests for grouped search result output
- [ ] 5.5 Manually verify article search, user search, grouped results, pagination, and empty states
