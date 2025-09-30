# Refactoring Template

## Purpose
Guide the refactoring of existing code to improve quality and maintainability.

## Context
Use this when code needs improvement without changing its external behavior.

## Prompt
```
Please analyze this code and suggest refactoring opportunities:

1. **Code Smells**: Identify problematic patterns
2. **Design Patterns**: Suggest applicable design patterns
3. **DRY Violations**: Find and eliminate code duplication
4. **Naming**: Improve variable, function, and class names
5. **Complexity**: Reduce cyclomatic complexity
6. **Modularity**: Improve separation of concerns
7. **Testability**: Make code more testable

Prioritize refactorings by impact and effort.
```

## Expected Output
A prioritized list of refactoring suggestions with code examples.

## Notes
- Always ensure tests pass after refactoring
- Refactor incrementally, one change at a time
- Consider backwards compatibility requirements