# Contributing to Prompts Repository

Thank you for your interest in contributing! This document provides guidelines for adding new prompts, improving existing workflows, and maintaining quality standards.

## Table of Contents

- [How to Contribute](#how-to-contribute)
- [Prompt Template Standards](#prompt-template-standards)
- [File Naming Conventions](#file-naming-conventions)
- [Adding New Prompts](#adding-new-prompts)
- [Proposing New Workflows](#proposing-new-workflows)
- [Contributing Examples](#contributing-examples)
- [Code of Conduct](#code-of-conduct)

## How to Contribute

1. **Fork the repository** and create a new branch for your contribution
2. **Make your changes** following the guidelines below
3. **Test your prompts** to ensure they work as expected
4. **Submit a pull request** with a clear description of your changes

## Prompt Template Standards

All prompt files must follow this standardized structure:

```markdown
# [Prompt Title]

## Purpose
Brief description of what this prompt accomplishes (1-2 sentences).

## Context
When and why to use this prompt (1-2 paragraphs).

## Pre-requirements (if applicable)
What needs to exist before using this prompt:
- Bullet point list
- Be specific (file names, completed steps, etc.)
- Or state "None" if there are no prerequisites

## Prompt
```
The actual prompt text to use with AI assistants.
This should be copy-paste ready.
Include any necessary instructions or context.
```

## Expected Output
Description of what the AI should produce:
- File paths and names
- Content structure
- Success criteria

## Notes
- Additional tips or variations
- Common pitfalls to avoid
- Related prompts or next steps
```

### Template Requirements

- **Clarity**: Use clear, concise language
- **Actionability**: Prompts should produce concrete, measurable outputs
- **Specificity**: Include specific file names, paths, and examples
- **Completeness**: Cover all sections even if some are brief

## File Naming Conventions

### Sequential Workflows
- Number files sequentially: `0. initial-idea.md`, `1. planning.md`, `2. progress-tracking.md`
- Use a leading zero for single digits if the sequence may grow beyond 9 files
- Include a space after the number: `1. ` not `1.`

### Standalone Prompts
- Use kebab-case: `create-nextjs-app.md`, `learn-typescript-basics.md`
- Be descriptive: name should indicate the prompt's purpose
- Avoid abbreviations unless they're widely understood

### Directory Names
- Use kebab-case: `project-development/`, `code-review/`
- Be descriptive and specific
- Group related prompts together

## Adding New Prompts

### Before Adding a Prompt

1. **Check for duplicates**: Search existing prompts to avoid redundancy
2. **Identify the category**: Determine where it fits (workflows, templates, projects, learning)
3. **Plan dependencies**: Identify any pre-requirements or related prompts

### Steps to Add a Prompt

1. **Choose the right location**:
   - `project-development/`: Part of the main project workflow
   - `workflows/`: Multi-step development workflows
   - `templates/`: Reusable templates for specific tasks
   - `projects/`: Project creation prompts (organize by domain)
   - `learning/`: Educational prompts

2. **Create the file** following naming conventions

3. **Fill in the template** with all required sections

4. **Test the prompt**:
   - Try it with an AI assistant
   - Verify the output matches expectations
   - Ensure pre-requirements are accurate

5. **Update documentation**:
   - Add entry to the main README.md if it's a major addition
   - Update `.claude/CLAUDE.md` if it affects repository structure

6. **Submit a pull request** with:
   - Clear description of what the prompt does
   - Example usage or output (if applicable)
   - Rationale for why it's valuable

## Proposing New Workflows

Workflows are multi-step processes with interdependent prompts. When proposing a new workflow:

### Workflow Requirements

1. **Clear phases**: Define distinct steps with specific deliverables
2. **Explicit dependencies**: State what must be completed before each phase
3. **Quality gates**: Define success criteria for each phase
4. **Independence when possible**: Design phases to be parallelizable if feasible

### Workflow Structure

```
workflows/
└── workflow-name/
    ├── 0. first-step.md
    ├── 1. second-step.md
    ├── 2. third-step.md
    └── README.md          # Overview of the workflow
```

### Workflow README Template

```markdown
# [Workflow Name]

## Overview
Brief description of the workflow and its purpose.

## When to Use
Situations where this workflow is appropriate.

## Phases
1. **Phase 0**: [Name] - [Brief description]
2. **Phase 1**: [Name] - [Brief description]
3. **Phase 2**: [Name] - [Brief description]

## Prerequisites
What you need before starting this workflow.

## Expected Outcome
What you'll have when the workflow is complete.
```

## Contributing Examples

Examples demonstrate the workflows in action with realistic projects.

### Example Requirements

1. **Realistic**: Use a project you would actually build
2. **Complete**: Include all workflow files (initial-idea, planning, PROGRESS, CLAUDE.md)
3. **Diverse**: Choose different tech stacks from existing examples
4. **Detailed**: Show specific phases, dependencies, and quality gates
5. **In-progress**: Show realistic progress (not everything complete)

### Example Structure

```
examples/
└── project-name/
    ├── initial-idea.md
    ├── planning.md
    ├── PROGRESS.md
    ├── .claude/
    │   └── CLAUDE.md
    └── README.md (optional - if you want to add specific notes)
```

### Adding an Example

1. Create directory under `examples/`
2. Fill out all workflow files as if you were planning the project
3. Make PROGRESS.md realistic (some items complete, some in progress, some pending)
4. Ensure CLAUDE.md is specific to the project's tech stack
5. Update `examples/README.md` to list your example

## Code of Conduct

### Our Standards

- **Be respectful**: Treat all contributors with respect
- **Be constructive**: Provide helpful feedback and suggestions
- **Be collaborative**: Work together to improve the repository
- **Be inclusive**: Welcome contributors of all backgrounds and skill levels

### Expected Behavior

- Use welcoming and inclusive language
- Respect differing viewpoints and experiences
- Accept constructive criticism gracefully
- Focus on what's best for the community
- Show empathy towards other contributors

### Unacceptable Behavior

- Harassment, discrimination, or exclusionary behavior
- Trolling, insulting comments, or personal attacks
- Public or private harassment
- Publishing others' private information without permission
- Other conduct that would be inappropriate in a professional setting

## Questions?

If you have questions about contributing:
- Open an issue with the `question` label
- Review existing issues and discussions
- Check the main README.md for additional context

## Thank You!

Your contributions help make this repository more valuable for everyone. Whether you're fixing a typo, adding a new prompt, or proposing a major workflow, your effort is appreciated!
