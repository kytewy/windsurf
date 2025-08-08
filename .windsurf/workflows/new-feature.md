# New Feature Development Workflow

## Description
This workflow guides you through the process of developing a new feature following Sahar's 80% planning, 20% execution methodology.

## Prerequisites
- [ ] PRD is updated with the new feature requirements
- [ ] Implementation plan is updated in `project-docs/implementation_plan.md`
- [ ] Database schema is updated if needed (documented in `project-docs/db_schema.md`)

## Steps

### 1. Planning Phase
```markdown
1. Review the PRD section for this feature
2. Update `app_flow.md` with new screens/endpoints
3. Update database schema if needed in `db_schema.md`
4. Add implementation steps to `implementation_plan.md`
```

### 2. Implementation Phase
```typescript
// Example: Create a new React component
// 1. Create component file in appropriate directory
// 2. Implement basic structure following project conventions
// 3. Add TypeScript interfaces
// 4. Implement business logic
// 5. Add tests
```

### 3. Testing Phase
```bash
# Run unit tests
npm test

# Run integration tests
npm run test:integration

# Verify test coverage meets requirements (80%+)
npm run test:coverage
```

### 4. Documentation
- [ ] Update component documentation
- [ ] Add/update API documentation
- [ ] Update README if needed

### 5. Code Review
- [ ] Self-review changes
- [ ] Create pull request
- [ ] Address review comments

## Success Criteria
- [ ] All tests pass
- [ ] Code coverage meets requirements
- [ ] Documentation is updated
- [ ] PR is approved and merged
