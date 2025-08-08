# Project Guidelines

## Documentation Context
- Always read `prd.md` before writing any code
- Refer to all documents in the `/project-docs` directory for context before proceeding
- This project follows Sahar's AI coding methodology: 80% planning, 20% execution

## Code Quality Standards
- Always prefer strict types over 'any' in TypeScript
- Use meaningful variable and function names
- Write self-documenting code with clear comments for complex logic
- Follow established naming conventions in `tech_stack.md`

## Development Workflow
- For complex or critical tasks, ask clarification questions before proceeding
- Break large tasks into smaller, testable components
- Always implement proper error handling
- Include input validation for all user-facing functions

## Architecture Guidelines
- Follow component structure outlined in `app_flow.md`
- Adhere to database schema defined in `db_schema.md`
- Use only technologies specified in `tech_stack.md`
- Implement features according to timeline in `implementation_plan.md`

## Security & Performance
- Always sanitize user inputs to prevent XSS and injection attacks
- Implement proper authentication checks for protected routes
- Follow performance targets specified in `tech_stack.md`
- Use environment variables for sensitive configuration

## Testing Requirements
- Write unit tests for all utility functions
- Include integration tests for API endpoints
- Test error scenarios and edge cases
- Maintain minimum 80% code coverage

## Git Practices
- Make frequent, atomic commits with descriptive messages
- Follow conventional commit format: type(scope): description
- Create feature branches for new functionality
- Ensure all tests pass before committing
