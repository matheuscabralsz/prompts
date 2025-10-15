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
│   ├── 0. initial-idea.md       # Template for capturing initial project concept
│   ├── 1. planning.md           # High-level project planning
│   ├── 2. progress-tracking.md  # Feature completion tracking template
│   └── 3. create-claude-md.md   # Generate CLAUDE.md for new projects
├── workflows/                    # Multi-step workflows for complex tasks
│   └── project-development/     # Symlink or reference to main workflow
├── templates/                    # Reusable prompt templates (future)
├── projects/                     # Project creation prompts (future)
└── learning/                     # Educational prompts (future)
```

## Project Development Workflow

A simple **4-phase project planning and tracking process**:

### Phase 0: Initial Idea Capture
**File:** `project-development/0. initial-idea.md`
- Template for documenting project concept and requirements
- User fills this out in their project's `docs/` folder as `initial-idea.md`
- Prerequisites: None (always the starting point)

### Phase 1: High-Level Planning
**File:** `project-development/1. planning.md`
- Prerequisites: Completed initial-idea.md in docs/ folder
- Reads initial-idea.md to generate implementation plan
- Creates phases with explicit dependencies or "None"
- Keeps everything high-level - no implementation details
- Defines quality gates (tests must pass, build must succeed)

### Phase 2: Progress Tracking
**File:** `project-development/2. progress-tracking.md`
- Prerequisites: Complete planning.md
- Creates docs/PROGRESS.md to track implementation status
- Uses checkboxes: [ ] not started, [~] in progress, [✓] complete
- **After creating tracker, actual coding can begin**

### Phase 3: Generate CLAUDE.md
**File:** `project-development/3. create-claude-md.md`
- Prerequisites: Complete initial-idea.md, planning.md, and PROGRESS.md
- Generates `.claude/CLAUDE.md` with project-specific guidance
- **After creating CLAUDE.md, actual coding can begin**

### Key Principles

1. **Workflow**: initial-idea.md → planning.md → progress-tracking.md → create-claude-md.md → Coding
2. **Phase Independence**: Design phases to be independent when possible
3. **Explicit Dependencies**: Each phase declares prerequisites or states "None"
4. **Parallel Execution**: Independent phases can be worked on in any order
5. **Quality Gates**: Tests pass and builds succeed before proceeding
6. **Documentation First**: Complete planning before writing code

## File Organization Guidelines

### Prompt File Structure
Every prompt file follows this template:
```markdown
# [Prompt Title]

## Purpose
Brief description of what this prompt accomplishes.

## Context
When and why to use this prompt.

## Prerequisites (if applicable)
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

- **project-development/**: Main workflow for project planning
- **workflows/**: Multi-step workflows (CI/CD, testing, migrations)
- **templates/**: Reusable templates (reviews, refactoring, docs)
- **projects/**: Project creation prompts (organized by domain)
- **learning/**: Educational prompts (concepts, tutorials, examples)

### Naming Conventions

- Use kebab-case: `create-nextjs-app.md`, `learn-typescript-basics.md`
- Number sequential workflows: `1. planning.md`, `2. progress-tracking.md`
- Use descriptive names that indicate purpose

## Important Principles

1. **No Code**: This repository contains only markdown documentation with prompts. Never create code files.
2. **Template Consistency**: All prompts follow the same structure
3. **Organization First**: Always consider the right category and location
4. **User Approval**: Present drafts to the user before saving
5. **Prerequisites**: Clearly document dependencies
6. **Independence First**: Design for parallel work when possible

## Working with This Repository

### When Creating New Prompts
1. Determine the appropriate category
2. Follow the standard prompt template structure
3. Add clear prerequisites if needed
4. Use descriptive names and numbering for sequential prompts
5. Present the draft to the user before saving

### When Improving Existing Prompts
1. Read the existing prompt to understand its purpose
2. Maintain the template structure
3. Ensure prerequisites are clearly documented
4. Update workflow documentation if sequence changes
5. Get user approval before saving changes

### Understanding the Main Workflow
- **0. initial-idea.md**: Template - users fill in their project's docs/ folder as `initial-idea.md`
- **1. planning.md**: Reads docs/initial-idea.md, creates phases with dependencies
- **2. progress-tracking.md**: Creates docs/PROGRESS.md to track implementation
- **3. create-claude-md.md**: Generates .claude/CLAUDE.md with project guidance
- **No coding until all planning documentation is complete**

## Common Tasks

### Adding a New Sequential Workflow
- Create folder under `workflows/` or in root
- Number files sequentially
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
