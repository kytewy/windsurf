# Code Review Workflow

## Description
Structured approach to conducting thorough code reviews following best practices.

## Prerequisites
- [ ] PR description explains the changes and why they're needed
- [ ] CI/CD pipeline has passed
- [ ] Code coverage meets requirements

## Review Checklist

### Code Quality
- [ ] Follows project coding standards
- [ ] No commented-out code
- [ ] No console.log statements in production code
- [ ] Error handling is appropriate
- [ ] Input validation is present

### Security
- [ ] No hardcoded secrets
- [ ] Input is properly sanitized
- [ ] Authentication/authorization checks are in place
- [ ] Dependencies are up-to-date and secure

### Performance
- [ ] No unnecessary re-renders (frontend)
- [ ] Database queries are optimized
- [ ] Large data sets are handled efficiently
- [ ] Assets are optimized

### Testing
- [ ] Unit tests are present and pass
- [ ] Edge cases are covered
- [ ] Test coverage meets requirements
- [ ] Mocks/stubs are used appropriately

### Documentation
- [ ] Public APIs are documented
- [ ] Complex logic has comments
- [ ] README is updated if needed
- [ ] Breaking changes are documented

## Review Process

1. **First Pass**
   - [ ] Check overall architecture and approach
   - [ ] Look for potential issues or edge cases
   - [ ] Note any questions or concerns

2. **Detailed Review**
   - [ ] Review code line by line
   - [ ] Check for potential bugs
   - [ ] Verify error handling
   - [ ] Check for security vulnerabilities

3. **Documentation & Tests**
   - [ ] Verify tests cover new functionality
   - [ ] Check that documentation is clear and complete
   - [ ] Ensure comments explain why, not what

4. **Final Check**
   - [ ] All review comments have been addressed
   - [ ] Code meets all requirements
   - [ ] No new issues introduced

## Review Etiquette
- Be constructive and specific in feedback
- Explain the why behind suggestions
- Acknowledge good patterns and solutions
- Keep discussions focused and professional

## Approval Criteria
- [ ] All checklist items are completed
- [ ] All comments have been addressed
- [ ] Code meets project standards
- [ ] Tests are passing
- [ ] Documentation is updated
