## 1. Data Model and Persistence

- [ ] 1.1 Add article persistence fields for title, summary, body, author, status, counts, created time, and updated time
- [ ] 1.2 Add article image persistence with article association, file metadata, order, size, MIME type, and storage path
- [ ] 1.3 Add article-tag associations supporting 1-5 tags per article
- [ ] 1.4 Add article status/history persistence for public, taken-down, and deleted states
- [ ] 1.5 Add view-count persistence needed by public article detail visits
- [ ] 1.6 Initialize view, like, collection, and comment counts when articles are created

## 2. Article Publishing

- [ ] 2.1 Implement authenticated article publishing with title, summary, body, 1-5 tags, and optional images
- [ ] 2.2 Validate required article fields at the API boundary
- [ ] 2.3 Reject article submission without tags
- [ ] 2.4 Accept article submission without category when tags and other fields are valid
- [ ] 2.5 Set newly published articles to public status immediately
- [ ] 2.6 Persist created and updated timestamps for published articles

## 3. Article Images

- [ ] 3.1 Implement local image upload handling for article images
- [ ] 3.2 Enforce a maximum of 9 images per article
- [ ] 3.3 Enforce a maximum image size of 5MB
- [ ] 3.4 Allow only JPG, PNG, and WebP image types
- [ ] 3.5 Persist image metadata and display order
- [ ] 3.6 Reject invalid image uploads without publishing invalid image metadata

## 4. Author Management

- [ ] 4.1 Implement author-only article editing for editable article states
- [ ] 4.2 Update article fields and refresh updated time when an author submits valid edits
- [ ] 4.3 Implement author deletion that removes the article from public display
- [ ] 4.4 Prevent author editing for deleted articles
- [ ] 4.5 Allow authors to edit and republish taken-down articles
- [ ] 4.6 Set republished taken-down articles back to public status after valid edits

## 5. Public Article Detail

- [ ] 5.1 Implement SEO-friendly public article detail route
- [ ] 5.2 Generate page metadata from article title and summary
- [ ] 5.3 Display title, summary, body, image carousel, author information, publish time, and interaction counts
- [ ] 5.4 Display comments entry point on the article detail page
- [ ] 5.5 Display related articles on the article detail page
- [ ] 5.6 Record a view when a visitor opens a public article detail page according to v1 view-counting rules

## 6. Public Visibility Filtering

- [ ] 6.1 Exclude taken-down articles from public article surfaces
- [ ] 6.2 Exclude deleted articles from public article surfaces
- [ ] 6.3 Prevent public article detail pages from displaying taken-down article content
- [ ] 6.4 Prevent public article detail pages from displaying deleted article content
- [ ] 6.5 Ensure public counts and related-article queries only use publicly visible articles

## 7. Verification

- [ ] 7.1 Add unit tests for article validation, including required tags and omitted category acceptance
- [ ] 7.2 Add unit tests for image count, size, and MIME type validation
- [ ] 7.3 Add authorization tests for author-only edit and delete behavior
- [ ] 7.4 Add tests for article status transitions: publish, takedown, republish, and deleted
- [ ] 7.5 Add integration tests for public visibility filtering
- [ ] 7.6 Manually verify publish, invalid tag rejection, invalid image rejection, edit, delete, republish, public detail, SEO metadata, view counting, and hidden-content behavior
