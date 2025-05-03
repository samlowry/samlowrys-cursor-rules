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
│   ├── docummenting-code.mdc
│   ├── unit-tests-for-code.mdc
│   ├── use-md-files-as-a-planning-memory.mdc
│   └── you-are-sys-admin.mdc
└── README.md
```

This structure makes it easier to:
- Manage and view rule files directly
- Add new rules in a central location
- Use the repository as a submodule in other projects

## Installation

To use these rules in your project:

```bash
# Add as a submodule
git submodule add https://github.com/samlowry/samlowrys-cursor-rules.git .cursor/rules

# Update the submodule
git submodule update --remote .cursor/rules
```

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

## Usage

This repository is designed to be included as a submodule in other projects to maintain consistent practices across multiple codebases. The structure with rules at the root level makes it easy to manage while still functioning correctly when imported as a submodule. 