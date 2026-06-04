## 1. Rate Limiting

- [ ] 1.1 Define rate-limit keys and windows for article publishing
- [ ] 1.2 Define rate-limit keys and windows for comments and replies
- [ ] 1.3 Define rate-limit keys and windows for reports
- [ ] 1.4 Define rate-limit keys and windows for repeated interactions
- [ ] 1.5 Apply rate-limit checks at protected mutation boundaries
- [ ] 1.6 Return clear errors when users exceed rate limits

## 2. Sensitive-Word Replacement

- [ ] 2.1 Add configurable sensitive-word source
- [ ] 2.2 Implement replacement of configured sensitive words with `***`
- [ ] 2.3 Apply replacement to article title, summary, and body before public display
- [ ] 2.4 Apply replacement to comment and reply content before public display
- [ ] 2.5 Ensure replacement runs before content is persisted or publicly returned according to implementation choice

## 3. Image Validation

- [ ] 3.1 Implement shared image type validation for JPG, PNG, and WebP where applicable
- [ ] 3.2 Implement avatar image size validation
- [ ] 3.3 Implement article image size validation with 5MB maximum
- [ ] 3.4 Implement article image count validation with 9-image maximum
- [ ] 3.5 Reject invalid image uploads before storing file metadata

## 4. Integration

- [ ] 4.1 Integrate rate limiting with article publishing
- [ ] 4.2 Integrate rate limiting with comment and reply creation
- [ ] 4.3 Integrate rate limiting with report submission
- [ ] 4.4 Integrate sensitive-word replacement with article publishing and editing
- [ ] 4.5 Integrate sensitive-word replacement with comment and reply publishing and editing
- [ ] 4.6 Integrate image validation with avatar and article image uploads

## 5. Verification

- [ ] 5.1 Add tests for publishing, comment, report, and interaction rate limits
- [ ] 5.2 Add tests for sensitive-word replacement in article fields
- [ ] 5.3 Add tests for sensitive-word replacement in comment fields
- [ ] 5.4 Add tests for avatar image validation
- [ ] 5.5 Add tests for article image type, size, and count validation
- [ ] 5.6 Manually verify rate-limit errors, sensitive-word replacement, invalid avatar rejection, and invalid article image rejection
