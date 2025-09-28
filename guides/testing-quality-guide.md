
# Testing & Quality Guide

## Purpose
Outline the Candidate's approach to testing and code quality for the portfolio project, focusing on critical-path, scenario-based testing and practical quality practices.

## Testing Philosophy
- Emphasize critical-path testing for key features and flows.
- Prioritize end-to-end logical scenarios over exhaustive coverage.
- No strict minimum coverage percentage; focus on meaningful tests that reflect real user journeys.

## UI Testing (Angular)
- Use Jest for unit tests of components and services.
- Write tests for critical UI logic and user interactions.
- Example: Test that the project list renders correctly and handles empty states.
- Use ESLint for code quality and best practices.

## API Testing (Spring Boot)
- Use TestNG for unit tests, focusing on controller-level scenario tests that exercise business logic and data access layers.
- Write tests for main API endpoints and critical business flows.
- Example: Test that creating a new project via the API persists data and returns the correct response.
- Use static analysis tools (e.g., Checkstyle, SpotBugs) for code quality.

## CI/CD Integration
- Integrate all tests into GitHub Actions workflows.
- Run tests on every push and pull request.
- Fail builds if critical-path tests do not pass.

## Quality Practices
- Use ESLint for UI and equivalent static analysis for API.
- Enforce code formatting and linting before commits (pre-commit hooks recommended).
- Conduct code reviews for all major changes, even in personal projects, to maintain discipline.
- Document known limitations and areas not covered by tests.

## Additional Notes
- Focus on scenario-based, logical tests that reflect real-world usage.
- Keep the testing and quality process lightweight and maintainable.