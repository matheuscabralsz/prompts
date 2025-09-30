# Prompts Repository

A curated collection of prompts for AI-assisted development, learning, and project creation.

## Repository Structure

### 🔄 workflows/
Multi-step workflows for complex development tasks.

- **project-development/** - Sequential project workflow from planning to implementation
  - `1. planning.md` - High-level project planning with phases and milestones
  - `2. detailed-planning-implementation.md` - Detailed step-by-step documentation before coding
- `ci-cd-setup.md` - Setting up continuous integration and deployment pipelines
- `testing-strategy.md` - Designing comprehensive testing strategies

### 📝 templates/
Reusable prompt templates for common development tasks.

- `architecture-review.md` - Analyze and evaluate codebase architecture
- `code-review.md` - Systematic code review for quality and security
- `refactoring.md` - Guide code improvements and refactoring opportunities

### 📁 projects/
Prompts for creating new projects (organized by type when populated).

- `web/` - Web applications
- `backend/` - Backend services
- `mobile/` - Mobile applications
- `infrastructure/` - DevOps and infrastructure

### 📚 learning/
Educational prompts for understanding concepts and technologies.

- `concepts/` - Learning specific concepts or patterns
- `tutorials/` - Step-by-step learning guides
- `examples/` - Generating example code

## How to Use

### Using Existing Prompts

1. **Browse** the appropriate category based on your need
2. **Read** the Purpose and Context sections to ensure it fits your use case
3. **Copy** the prompt from the Prompt section
4. **Customize** any placeholders (e.g., `[Step Number]`, `[Tech Stack]`)
5. **Use** with your AI assistant (Claude, ChatGPT, etc.)

### Example Workflow: Starting a New Project

1. Use `workflows/project-development/1. planning.md` to create high-level plan
2. Use `workflows/project-development/2. detailed-planning-implementation.md` to document each step in detail
3. Use `workflows/testing-strategy.md` to plan your testing approach
4. Use `workflows/ci-cd-setup.md` to set up automation

### Prompt File Structure

Each prompt follows a consistent template:

```markdown
# [Prompt Title]

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

## Adding New Prompts

When contributing new prompts:

1. **Choose the right category:**
   - `workflows/` for multi-step processes
   - `templates/` for reusable single-purpose prompts
   - `projects/` for project creation prompts (organize by type)
   - `learning/` for educational content

2. **Follow naming conventions:**
   - Use kebab-case: `create-react-app.md`, `learn-docker-basics.md`
   - Be descriptive and concise
   - Number files if they form a sequence (e.g., `1. planning.md`, `2. implementation.md`)

3. **Use the template structure:**
   - Include all sections: Purpose, Context, Prompt, Expected Output, Notes
   - Make prompts clear and actionable
   - Add examples where helpful

4. **Group related prompts:**
   - Create subfolders for sequential workflows
   - Keep related prompts together (e.g., `project-development/`)

## Tips for Effective Prompts

- **Be Specific**: Include relevant context and constraints
- **Use Placeholders**: Mark areas for customization with `[brackets]`
- **Define Output**: Clearly describe what you expect the AI to produce
- **Iterate**: Refine prompts based on actual usage and results
- **Document**: Add notes about when the prompt works best and any gotchas