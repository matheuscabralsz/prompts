# Testing Strategy Workflow

## Purpose
Develop a comprehensive testing strategy for a project.

## Context
Use this when planning or improving the testing approach for a codebase.

## Prompt
```
Please help me design a testing strategy for this project:

**Project Type**: [e.g., REST API, SPA, microservices]
**Tech Stack**: [e.g., Node.js/Express, React/TypeScript]
**Current Coverage**: [e.g., 0%, 45%, none]

Please provide:

1. **Testing Pyramid**: Recommended distribution of unit/integration/e2e tests
2. **Unit Testing**: What to unit test and how (with examples)
3. **Integration Testing**: Key integration points to test
4. **E2E Testing**: Critical user flows to cover
5. **Test Framework**: Recommended tools and libraries
6. **Mocking Strategy**: How to mock dependencies
7. **Coverage Goals**: Realistic coverage targets
8. **Testing Patterns**: Best practices and patterns to follow
9. **CI Integration**: How to run tests in CI/CD

Focus on: [specify priorities, e.g., "quick wins", "critical paths", "high-risk areas"]
```

## Expected Output
Comprehensive testing strategy document with code examples.

## Notes
- Balance coverage with development velocity
- Start with high-value tests first
- Make tests maintainable and reliable
- Avoid testing implementation details