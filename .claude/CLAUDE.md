# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Purpose

This is a prompts repository for storing and organizing AI assistant prompts used for:
- Creating new projects
- Learning concepts and technologies
- Code reviews and refactoring
- Development workflows

## Repository Structure

```
prompts/
├── workflows/
│   ├── project-development/     # Sequential project workflow
│   │   ├── planning.md          # High-level project planning
│   │   └── detailed-planning-implementation.md  # Detailed step breakdown
│   ├── ci-cd-setup.md
│   └── testing-strategy.md
├── templates/                    # Reusable prompt templates
│   ├── architecture-review.md
│   ├── code-review.md
│   └── refactoring.md
├── projects/                     # Project creation prompts (organized by type)
│   ├── web/
│   ├── backend/
│   ├── mobile/
│   └── infrastructure/
└── learning/                     # Educational prompts
    ├── concepts/
    ├── tutorials/
    └── examples/
```

## File Organization Guidelines

### Prompt File Structure
Every prompt file follows this template:
```markdown
## Purpose
Brief description of what this prompt accomplishes.

## Context
When and why to use this prompt.

## Prompt
```
The actual prompt text to use with AI assistants.
```

## Expected Output
Description of what the AI should produce.

## Notes
Additional tips or variations.
```

### Where to Save Prompts

- **workflows/project-development/**: Sequential project development prompts (planning → detailed planning → implementation)
- **workflows/**: Multi-step workflows for complex tasks (CI/CD, testing strategies, migrations)
- **templates/**: Reusable templates for common tasks (reviews, refactoring, documentation)
- **projects/**: Project creation prompts, organized by domain (web/backend/mobile/infrastructure)
- **learning/**: Educational prompts for understanding concepts, tutorials, and examples

### Naming Conventions

- Use kebab-case for filenames: `create-nextjs-app.md`, `learn-typescript-basics.md`
- Use descriptive names that indicate purpose
- Keep filenames concise but clear

## Important Principles

1. **No Code**: This repository contains only markdown documentation with prompts. Never create code files.
2. **Template Consistency**: All prompts follow the same structure (Purpose, Context, Prompt, Expected Output, Notes)
3. **Organization First**: When adding new prompts, always consider the right category and location
4. **Sequential Workflows**: Related prompts that form a workflow should be grouped together in a subfolder
5. **User Approval**: When creating or improving prompts, present the draft to the user for approval before saving