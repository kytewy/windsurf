# Tech Stack Guidelines

## Framework & Library Usage
- Only use technologies explicitly specified in `tech_stack.md`
- Prefer the exact versions mentioned in the tech stack documentation
- When adding new dependencies, update `tech_stack.md` first

## Code Style & Conventions
- Follow naming conventions: camelCase for variables, PascalCase for components
- Use feature-based file organization as outlined in project docs
- Import order: External libraries → Internal modules → Relative imports

## Database Guidelines
- Follow table naming: snake_case, plural nouns
- Column naming: snake_case format
- Foreign keys: use `table_name_id` format
- Always use migrations for schema changes

## API Development
- Follow the API style specified in `tech_stack.md` (REST/GraphQL/tRPC)
- Implement proper request validation using specified validation library
- Include comprehensive error handling for all endpoints
- Document all APIs according to the chosen documentation standard

## Environment Configuration
- Use environment variables for all configuration
- Never hardcode sensitive values like API keys
- Follow the environment variable naming patterns in `tech_stack.md`
- Validate required environment variables on application startup
