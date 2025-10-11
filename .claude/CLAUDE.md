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
│   ├── planning.md           # High-level project planning
│   ├── detailed-planning-implementation.md  # Detailed step-by-step breakdown
│   └── progress-tracking.md  # Feature completion tracking template
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

This repository's main workflow is a **flexible four-phase project planning and tracking process** with independent, modular phases:

### Phase 1: Initial Idea Capture
**File:** `project-development/INITIAL_IDEA.md`
- Template for documenting project concept, requirements, and constraints
- Captures functional and non-functional requirements
- Defines tech stack preferences and project constraints
- Establishes success criteria
- **Prerequisites:** None (always the starting point)

### Phase 2: High-Level Planning
**File:** `project-development/planning.md`
- **Prerequisites:** User creates filled-out INITIAL_IDEA.md in their project's `docs/` folder
- Reads from `docs/INITIAL_IDEA.md` to generate high-level implementation plan
- Creates project overview with tech stack and architecture approach
- Breaks down project into **independent phases** with explicit dependencies
- Each phase must declare: "Prerequisites: Phase [N]" OR "Prerequisites: None"
- Phases without dependencies can be worked on in parallel
- Defines quality gates (tests must pass, build must succeed)
- Keeps everything at a high level - no implementation details yet

### Phase 3: Detailed Step Documentation
**File:** `project-development/detailed-planning-implementation.md`
- **Prerequisites:** Optional - can be used for any step (with or without high-level plan)
- Breaks down any phase or step into detailed documentation
- **This is still planning - no code is written yet**
- Each step must explicitly declare prerequisites or state "None"
- Steps without prerequisites can be worked on independently
- For each step, provides:
  - Explicit prerequisites (or "None")
  - Specific tasks to complete (noting parallel opportunities)
  - Files to create or modify (with dependencies)
  - External dependencies and integrations
  - Testing requirements (unit, integration, e2e)
  - Configuration needs
  - Independent validation criteria
- User specifies which step/phase to document
- After all documentation is complete, create progress tracker before coding

### Phase 4: Progress Tracking
**File:** `project-development/progress-tracking.md`
- **Prerequisites:** Either `planning.md` OR `detailed-planning-implementation.md` (or both)
- Creates a `docs/PROGRESS.md` file in the project to track implementation status
- Uses checkbox format to mark completed/in-progress/not-started items
- Tracks phases, steps, subtasks, and quality gates
- Provides visual overview of project completion status
- Updated regularly during implementation phase
- Helps identify blockers and maintain momentum
- **After creating tracker, actual coding can begin**

### Key Principles

1. **Flexible Workflow**: INITIAL_IDEA.md → planning.md → detailed-planning-implementation.md → progress-tracking.md → Coding
2. **Phase Independence**: Phases and steps should be independent unless explicitly stated otherwise
3. **Explicit Dependencies**: Every phase/step must declare prerequisites or state "None (can start independently)"
4. **Parallel Execution**: Independent phases/steps can be worked on in parallel or any order
5. **Quality Gates**: Each phase must have passing tests and successful builds before proceeding
6. **Documentation First**: Complete planning and documentation before any code is written
7. **Progress Visibility**: Track implementation status with checkboxes for accountability and momentum
8. **Test-Driven Development**: Emphasizes writing tests as part of the workflow
9. **Modular Progress**: Each phase can be completed and verified independently

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
- Use numbers for sequential workflows: `planning.md`, `detailed-planning-implementation.md`
- Use descriptive names that indicate purpose
- Keep filenames concise but clear

## Important Principles

1. **No Code**: This repository contains only markdown documentation with prompts. Never create code files.
2. **Template Consistency**: All prompts follow the same structure (Purpose, Context, Prompt, Expected Output, Notes)
3. **Organization First**: When adding new prompts, always consider the right category and location
4. **Sequential Workflows**: Related prompts that form a workflow should be numbered and grouped together
5. **User Approval**: When creating or improving prompts, present the draft to the user for approval before saving
6. **Pre-requirements**: Clearly document what needs to exist before using a prompt (e.g., INITIAL_IDEA.md for planning)
7. **Explicit Dependencies**: Every phase/step must declare prerequisites or state "None (can start independently)"
8. **Independence First**: Design phases and steps to be independent whenever possible to enable parallel work

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
- **planning.md** reads from `docs/INITIAL_IDEA.md` to create high-level plans with independent phases
- **Every phase must declare dependencies** - either "Prerequisites: Phase [N]" or "Prerequisites: None"
- **detailed-planning-implementation.md** can be used for any step (with or without a high-level plan)
- **Every step must declare prerequisites** - independent steps state "Prerequisites: None"
- **progress-tracking.md** creates `docs/PROGRESS.md` to track implementation status with checkboxes
- **Independent phases/steps** can be worked on in parallel or any order
- **No coding happens until planning, documentation, and tracking setup is complete**
- **Quality gates** ensure tests pass and builds succeed at each step
- **Progress tracking** provides visibility and accountability during implementation
- **Modular approach** allows flexible execution based on dependencies

## Common Tasks

### Adding a New Sequential Workflow
- Create a new folder under `workflows/` or in the root
- Number files sequentially: `step-one.md`, `step-two.md`
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
