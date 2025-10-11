# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Purpose

This is a prompts repository for storing and organizing AI assistant prompts used for:
- Creating and planning new projects
- Learning concepts and technologies
- Code reviews and refactoring
- Development workflows and best practices

## Repository Structure

```
prompts/
├── project-development/          # Sequential project planning workflow
│   ├── INITIAL_IDEA.md          # Template for capturing initial project concept
│   ├── 1. planning.md           # High-level project planning
│   └── 2. detailed-planning-implementation.md  # Detailed step-by-step breakdown
├── workflows/                    # Multi-step workflows for complex tasks
│   └── project-development/     # Symlink or reference to main workflow
├── templates/                    # Reusable prompt templates (future)
│   ├── architecture-review.md
│   ├── code-review.md
│   └── refactoring.md
├── projects/                     # Project creation prompts (future)
│   ├── web/
│   ├── backend/
│   ├── mobile/
│   └── infrastructure/
└── learning/                     # Educational prompts (future)
    ├── concepts/
    ├── tutorials/
    └── examples/
```

## Project Development Workflow

This repository's main workflow is a **sequential three-phase project planning process**:

### Phase 1: Initial Idea Capture
**File:** `project-development/INITIAL_IDEA.md`
- Template for documenting project concept, requirements, and constraints
- Captures functional and non-functional requirements
- Defines tech stack preferences and project constraints
- Establishes success criteria

### Phase 2: High-Level Planning
**File:** `project-development/1. planning.md`
- **Pre-requirement:** User creates filled-out INITIAL_IDEA.md in their project's `docs/` folder
- Reads from `docs/INITIAL_IDEA.md` to generate high-level implementation plan
- Creates project overview with tech stack and architecture approach
- Breaks down project into logical phases with milestones
- Defines quality gates (tests must pass, build must succeed)
- Keeps everything at a high level - no implementation details yet

### Phase 3: Detailed Step Documentation
**File:** `project-development/2. detailed-planning-implementation.md`
- Breaks down each phase from planning into detailed step-by-step documentation
- **This is still planning - no code is written yet**
- For each step, provides:
  - Specific tasks to complete
  - Files to create or modify
  - Testing requirements (unit, integration, e2e)
  - Configuration needs
  - Validation criteria
- User specifies which step/phase to document
- After all documentation is complete, actual coding can begin

### Key Principles

1. **Sequential Workflow**: INITIAL_IDEA.md → 1. planning.md → 2. detailed-planning-implementation.md → Coding
2. **Quality Gates**: Each step must have passing tests and successful builds before proceeding
3. **Documentation First**: Complete planning and documentation before any code is written
4. **Test-Driven Development**: Emphasizes writing tests as part of the workflow
5. **Incremental Progress**: Each phase builds on the previous one

## File Organization Guidelines

### Prompt File Structure
Every prompt file follows this template:
```markdown
# [Prompt Title]

## Purpose
Brief description of what this prompt accomplishes.

## Context
When and why to use this prompt.

## Pre-requirements (if applicable)
What needs to exist before using this prompt.

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

- **project-development/**: The main sequential workflow for project planning (INITIAL_IDEA.md → planning → detailed implementation)
- **workflows/**: Multi-step workflows for complex tasks (CI/CD, testing strategies, migrations)
- **templates/**: Reusable templates for common tasks (reviews, refactoring, documentation)
- **projects/**: Project creation prompts, organized by domain (web/backend/mobile/infrastructure)
- **learning/**: Educational prompts for understanding concepts, tutorials, and examples

### Naming Conventions

- Use kebab-case for filenames: `create-nextjs-app.md`, `learn-typescript-basics.md`
- Use numbers for sequential workflows: `1. planning.md`, `2. detailed-planning-implementation.md`
- Use descriptive names that indicate purpose
- Keep filenames concise but clear

## Important Principles

1. **No Code**: This repository contains only markdown documentation with prompts. Never create code files.
2. **Template Consistency**: All prompts follow the same structure (Purpose, Context, Prompt, Expected Output, Notes)
3. **Organization First**: When adding new prompts, always consider the right category and location
4. **Sequential Workflows**: Related prompts that form a workflow should be numbered and grouped together
5. **User Approval**: When creating or improving prompts, present the draft to the user for approval before saving
6. **Pre-requirements**: Clearly document what needs to exist before using a prompt (e.g., INITIAL_IDEA.md for planning)

## Working with This Repository

### When Creating New Prompts
1. Determine the appropriate category (project-development, workflows, templates, projects, learning)
2. Follow the standard prompt template structure
3. Add clear pre-requirements if the prompt depends on other files or steps
4. Use descriptive names and numbering for sequential prompts
5. Present the draft to the user before saving

### When Improving Existing Prompts
1. Read the existing prompt to understand its purpose and context
2. Maintain the template structure
3. Ensure pre-requirements are clearly documented
4. Update the workflow documentation if changes affect the sequence
5. Get user approval before saving changes

### Understanding the Main Workflow
- **INITIAL_IDEA.md** is a template - users fill this out in their project's `docs/` folder
- **1. planning.md** reads from `docs/INITIAL_IDEA.md` to create high-level plans
- **2. detailed-planning-implementation.md** breaks down each phase into detailed steps
- **No coding happens until all planning and documentation is complete**
- **Quality gates** ensure tests pass and builds succeed at each step

## Common Tasks

### Adding a New Sequential Workflow
- Create a new folder under `workflows/` or in the root
- Number files sequentially: `1. step-one.md`, `2. step-two.md`
- Document pre-requirements in each file
- Update this CLAUDE.md if it's a major workflow

### Adding a Template
- Create file in `templates/` directory
- Follow standard prompt structure
- Make it reusable with clear placeholders
- Document when and how to use it

### Adding Project-Specific Prompts
- Organize by domain: `projects/web/`, `projects/backend/`, etc.
- Include tech stack in the prompt
- Provide clear expected outputs
- Reference the project-development workflow for planning
