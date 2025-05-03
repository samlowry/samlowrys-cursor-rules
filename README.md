# Samlowry's Cursor Rules

This repository contains custom rules and configurations for Cursor, an AI-powered code editor.

## Overview

This project helps maintain consistent coding practices and workflows when using Cursor. It includes:

- Custom instructions for AI assistants
- Git commit message formatting rules
- Code style guidelines
- Project setup practices

## Repository Structure

The repository is organized with all rules in the `rules/` directory at the root level:

```
samlowrys-cursor-rules/
├── rules/                # Directory containing all rule files
│   ├── docummenting-code.mdc     # Code documentation standards
│   ├── unit-tests-for-code.mdc   # Testing requirements and practices
│   ├── use-md-files-as-a-planning-memory.mdc  # Planning memory guidelines
│   └── you-are-sys-admin.mdc     # System administration practices
└── README.md
```

This structure makes it easier to:
- Manage and view rule files directly
- Add new rules in a central location
- Use the repository as a submodule in other projects

## Rules Description

### docummenting-code.mdc
Everything about adding and updating remarks in code comments - to improve LLM understanding of code.

### unit-tests-for-code.mdc
Guidelines for creating comprehensive unit tests and testing practices.

### use-md-files-as-a-planning-memory.mdc
How to use markdown files as planning memory for AI assistant workflows.

### you-are-sys-admin.mdc
System administration guidelines and best practices for configuration management.

## Installation

To use these rules in your project:

```bash
# Add as a submodule
git submodule add https://github.com/samlowry/samlowrys-cursor-rules.git .cursor/rules

# Update the submodule when needed
git submodule update --remote .cursor/rules
```

## Important Common Guidelines

- Never touch any parts of code not related to the current task. If you found some critical error not related to current task - just inform me before doing something
- Always use UTF-8 encoding
- Always use English in code and code comments! For any Russian interface texts always use separate language files
- Prefer iteration and modularization over code duplication. Always explore code for existing related logic
- Do not introduce new dependencies before making sure we don't already use a different library or framework
- Design services to be stateless; leverage external storage and caches (e.g., Redis) for state persistence
- When editing - always make sure you're not removing code unrelated to the edit
- Always use "docker compose" not outdated "docker-compose"
- Never install packages separately without adding them to requirements.txt or package.json

## Git Emoji Commit Message Format

Commits should follow this format:

```
<emoji> <description>
```

### Common Commit Types with Emojis

- ✨ (sparkles): New feature or enhancement
- 🐛 (bug): Bug fix
- 📚 (books): Documentation changes
- 💄 (lipstick): UI/style/formatting updates
- ♻️ (recycle): Code refactoring
- ✅ (white_check_mark): Adding or updating tests
- 🔧 (wrench): Configuration changes or tooling
- 🚀 (rocket): Performance improvements
- 🔒 (lock): Security fixes
- 🧹 (broom): Code cleanup or removing dead code
- 📦 (package): Dependency updates

### Guidelines

- Use imperative mood in the description (e.g., "Add" not "Added")
- First letter of description should be capitalized
- No period at the end of the description
- Keep the description under 50 characters
- For more details, add a blank line after the description and then provide a longer explanation

## Usage

This repository is designed to be included as a submodule in other projects to maintain consistent practices across multiple codebases. The structure with rules at the root level makes it easy to manage while still functioning correctly when imported as a submodule.
