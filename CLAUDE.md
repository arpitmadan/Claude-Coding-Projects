# CLAUDE.md

This file provides guidance to AI assistants (Claude and others) working in this repository.

## Repository Overview

**Repository:** arpitmadan/Claude-Coding-Projects
**Status:** Initial setup — no source code has been committed yet.

This is a fresh repository created to house coding projects. As projects are added, this file should be updated to reflect the current structure, tech stack, and conventions.

## Current State

The repository is empty aside from this documentation file. When project code is added:
1. Update the "Project Structure" section below
2. Update the "Tech Stack" section with actual dependencies
3. Add specific build/test/lint commands
4. Document any project-specific conventions

## Development Branch Conventions

- Feature branches follow the pattern: `claude/<description>-<session-id>`
- Always develop on the designated branch and push with:
  ```bash
  git push -u origin <branch-name>
  ```
- Never push to `main` or `master` directly without explicit permission

## Git Workflow

```bash
# Check current branch
git branch

# Stage and commit changes
git add <specific-files>
git commit -m "clear, descriptive commit message"

# Push to remote
git push -u origin <branch-name>
```

### Commit Message Style
- Use the imperative mood: "Add feature" not "Added feature"
- Keep the first line under 72 characters
- Reference issue numbers when applicable: `Fix #42: resolve auth bug`

## Project Structure

> To be updated when source code is added.

```
Claude-Coding-Projects/
├── CLAUDE.md           # This file
└── (projects to be added)
```

## Tech Stack

> To be updated when dependencies are established.

## Development Workflow

### Running the Project

> To be updated once a project is initialized.

### Running Tests

> To be updated once a test framework is configured.

### Linting and Formatting

> To be updated once linting tools are configured.

### Building

> To be updated once a build process is defined.

## Key Conventions

### Code Style
- Follow the conventions of the language/framework in use
- Keep functions small and single-purpose
- Avoid over-engineering — implement the minimum needed for the current task
- Do not add docstrings, comments, or type annotations to unchanged code
- Only validate at system boundaries (user input, external APIs)

### Security
- Never commit secrets, credentials, or API keys
- Do not introduce OWASP top 10 vulnerabilities (SQL injection, XSS, command injection, etc.)
- Validate and sanitize all external input

### File Management
- Prefer editing existing files over creating new ones
- Delete unused code rather than commenting it out or using backwards-compatibility shims
- Do not create documentation files unless explicitly requested

## AI Assistant Guidelines

When working in this repository:

1. **Read before modifying** — always read a file before editing it
2. **Minimal changes** — only change what is directly requested or clearly necessary
3. **No speculative features** — do not add error handling, fallbacks, or abstractions for hypothetical scenarios
4. **Confirm risky actions** — ask before force-pushing, deleting branches, or modifying shared infrastructure
5. **Update this file** — when significant new code, tooling, or conventions are added, update the relevant sections of this CLAUDE.md

## Getting Help

- Report issues at: https://github.com/anthropics/claude-code/issues
- Claude Code docs: `/help` in the Claude Code CLI
