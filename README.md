# Prompts Repository

A collection of prompts designed to help vibe coding personal project ideas with AI assistance.

## What is Vibe Coding?

This repository provides a structured workflow for rapidly turning project ideas into reality using AI assistants like Claude Code. Instead of getting stuck in analysis paralysis, these prompts help you document your idea, plan implementation, and start coding quickly.

## Quick Start

### Project Development Workflow

```
Phase 0          Phase 1           Phase 2              Phase 3            Ready to Code
┌─────────┐     ┌─────────┐      ┌──────────┐        ┌─────────┐         ┌──────────┐
│ Initial │ ──> │ Planning │ ──> │ Progress │ ────> │ CLAUDE  │ ─────> │ Start    │
│ Idea    │     │          │      │ Tracking │        │ .md     │         │ Coding   │
└─────────┘     └─────────┘      └──────────┘        └─────────┘         └──────────┘
Capture your    Generate         Create progress     Generate project    Begin
project         implementation   tracker with        guidance for        implementation
concept         phases           checkboxes          Claude Code
```

**The Workflow**:

1. **Phase 0 - Capture your idea**: Fill out `project-development/0. initial-idea.md` in your project's docs/ folder as `initial-idea.md`
2. **Phase 1 - Create a plan**: Use `project-development/1. planning.md` to generate implementation phases
3. **Phase 2 - Setup tracking**: Use `project-development/2. progress-tracking.md` to create a progress tracker
4. **Phase 3 - Generate guidance**: Use `project-development/3. create-claude-md.md` to create `.claude/CLAUDE.md`
5. **Start coding**: Begin implementation with full documentation in place

## Repository Structure

```
prompts/
├── project-development/          # Main workflow for vibe coding projects
│   ├── 0. initial-idea.md       # Template for capturing project concept
│   ├── 1. planning.md           # Generate implementation plan
│   ├── 2. progress-tracking.md  # Create progress tracker
│   └── 3. create-claude-md.md   # Generate CLAUDE.md guidance
└── examples/                     # Complete workflow examples
    └── todo-app/                 # Full-stack todo app example
        ├── initial-idea.md
        ├── planning.md
        ├── PROGRESS.md
        └── .claude/CLAUDE.md
```

Note: Additional prompt categories (workflows, templates, projects, learning) coming soon - see Roadmap below.

## How It Works

Each prompt file follows a simple structure:
- **Purpose**: What it does
- **Pre-requirements**: What you need first
- **Prompt**: Copy and use with your AI assistant
- **Expected Output**: What you'll get

Start with Phase 0 (`0. initial-idea.md`) and follow the numbered sequence. Each phase builds on the previous one to get you coding faster.

## Examples

Check out the `examples/` directory for complete walkthroughs:
- **todo-app**: Full-stack todo application showing all phases of the workflow
  - See how a simple idea becomes a structured plan
  - Observe phase dependencies and quality gates
  - Learn from realistic progress tracking

## Roadmap

Future additions planned for this repository:

### workflows/
Multi-step workflows for complex development tasks:
- CI/CD pipeline setup
- Database migrations
- Testing strategies
- Code refactoring workflows

### templates/
Reusable prompt templates:
- Code review checklists
- Documentation templates
- Refactoring guides
- Architecture decision records

### projects/
Project creation prompts organized by domain:
- `projects/web/` - Web applications (Next.js, React, Vue)
- `projects/backend/` - Backend services (Node.js, Go, Python)
- `projects/mobile/` - Mobile apps (React Native, Flutter)
- `projects/cli/` - Command-line tools

### learning/
Educational prompts for learning new concepts:
- Technology tutorials
- Concept explanations
- Best practices guides
- Code examples and patterns

## Contributing

Contributions are welcome! See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on:
- Adding new prompts
- Improving existing workflows
- Contributing examples
- Suggesting new categories

## License

MIT License - see [LICENSE](LICENSE) for details.