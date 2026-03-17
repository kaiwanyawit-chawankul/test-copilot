# Code Review Standards

When reviewing code, always check for the following points and provide actionable feedback:

## Code Quality Essentials

- Functions should be focused and appropriately sized
- Use clear, descriptive naming conventions
- Ensure proper error handling throughout

## Security Standards

- Never hardcode credentials or API keys
- Validate all user inputs
- Use parameterized queries to prevent SQL injection

## Documentation Expectations

- All public functions must include doc comments
- Complex algorithms should have explanatory comments
- README files must be kept up to date

## Security
*   **Secrets:** Ensure there are no hardcoded secrets, tokens, or connection strings.
*   **Input Validation:** All user input must be validated and sanitized before use.
*   **SQL Injections:** Parameterized statements should be used for all SQL queries.

## Reliability
*   **Error Handling:** All asynchronous operations must have proper `try/catch` or equivalent error handling.
*   **Network Logic:** Network calls should include appropriate timeouts and retry logic.
*   **Resource Cleanup:** Ensure resources are cleaned up in `finally` blocks or `using` statements.

## Maintainability
*   **Function Length:** Functions should ideally do one thing and be under 40 lines where practical.
*   **Naming Conventions:** Variable names must be descriptive and follow project conventions (e.g., use `camelCase` for variables, `PascalCase` for types).
*   **Dead Code:** No commented-out code should be left in place; use version control instead.

## Performance
*   **N+1 Queries:** Database interactions must avoid N+1 query patterns.
*   **Memory Usage:** Large collections should use streaming or pagination rather than loading everything into memory.
