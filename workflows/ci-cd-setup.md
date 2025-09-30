# CI/CD Setup Workflow

## Purpose
Set up continuous integration and deployment for a project.

## Context
Use this when initializing CI/CD pipelines for a new or existing project.

## Prompt
```
Please help me set up CI/CD for this project:

**Project Type**: [e.g., Node.js API, React app, Python service]
**Hosting Platform**: [e.g., AWS, Vercel, Heroku, self-hosted]
**CI/CD Platform**: [e.g., GitHub Actions, GitLab CI, Jenkins]

Please provide:

1. **Pipeline Configuration**: Complete CI/CD config file
2. **Build Steps**: Commands to build the project
3. **Test Steps**: How to run tests in CI
4. **Deployment Steps**: How to deploy to target environment
5. **Environment Variables**: Required secrets and configuration
6. **Branch Strategy**: When to build, test, and deploy
7. **Quality Gates**: Linting, testing, coverage requirements
8. **Rollback Strategy**: How to rollback failed deployments

Include best practices for [security/performance/reliability].
```

## Expected Output
Complete CI/CD configuration files with documentation.

## Notes
- Start with basic CI, then add CD incrementally
- Test the pipeline in a feature branch first
- Document all required secrets and permissions