## 1. AI Assistance Boundary

- [ ] 1.1 Define configurable AI provider settings for server-side use
- [ ] 1.2 Implement an AI assistance service boundary with title, summary, and content-improvement operations
- [ ] 1.3 Keep provider-specific request and response handling inside the AI assistance boundary
- [ ] 1.4 Fail clearly when the AI provider is not configured

## 2. Input Validation

- [ ] 2.1 Validate authenticated access before allowing AI writing assistance requests
- [ ] 2.2 Validate title generation input so empty or insufficient article content is rejected before provider calls
- [ ] 2.3 Validate summary generation input so empty or insufficient article content is rejected before provider calls
- [ ] 2.4 Validate content improvement input so empty or oversized content is rejected before provider calls
- [ ] 2.5 Add request-size limits that avoid provider context-limit failures for v1 usage

## 3. Server API

- [ ] 3.1 Implement a title suggestion procedure for authenticated users
- [ ] 3.2 Implement a summary suggestion procedure for authenticated users
- [ ] 3.3 Implement a content improvement suggestion procedure for authenticated users
- [ ] 3.4 Return suggestions without mutating article title, summary, body, or publish state
- [ ] 3.5 Surface provider errors to the editor without silently replacing user content

## 4. Article Editor UI

- [ ] 4.1 Add manual title generation action to the article editor
- [ ] 4.2 Add manual summary generation action to the article editor
- [ ] 4.3 Add manual content improvement action to the article editor
- [ ] 4.4 Display AI suggestions as reviewable content separate from the current editor fields
- [ ] 4.5 Allow the user to copy or apply a suggestion only after reviewing it
- [ ] 4.6 Ensure AI suggestions never publish automatically and never replace editor content without user action

## 5. Verification

- [ ] 5.1 Add unit tests for AI input validation
- [ ] 5.2 Add unit tests for AI assistance boundary behavior with a configured provider stub
- [ ] 5.3 Add API tests proving AI procedures require authentication
- [ ] 5.4 Add UI tests for manual trigger and review-before-apply behavior
- [ ] 5.5 Manually verify title suggestion, summary suggestion, content improvement, copy/apply, and no-auto-publish editor flows
