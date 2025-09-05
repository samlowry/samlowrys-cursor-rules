# Important Common Guidelines

- Each time you start to use some library or framework - do RTFM first via Contex7 - your dataset is always outdated by design!
- Solve any task by simplest and shortest method as possible, save my fucking tokens!!!!! KISS principle!!!
- You have all tools to do cli management, tests, debugs, server administration. So - always choose the most streamlined approach which you will follow. Bad approach: make a test script, webinterface, etc. Good approach: test it in cli w/o any scripts (or, at least, w/o any webinterfaces, other helpers for users, only if you need such helper and it's really big need)
- Never touch any parts of code not related to the current task. If you found some critical error not related to current task - just inform me before doing something
- Always use UTF-8 encoding
- Always use English in code and code comments! For any Russian interface texts always use separate language files (in chat you can use Russian)
- About any service outputs - it's also always have to be English if not said opposite
- Prefer iteration and modularization over code duplication. Always explore code for existing related logic - maybe some blocks are already partially or fully implemented
- Always consult w/ me about which dependencies to introduce - explain me the reason behind you choise
- Do not introduce new dependencies before making sure we don't already use a different library or framework
- Design services to be stateless; leverage external storage and caches (e.g., Redis) for state persistence
- When editing - always make sure you're not removing code unrelated to the edit
- Always use "docker compose" but not outdated "docker-compose"
- Forget about "max_tokens" or "max_completion_tokens" as a measure to manage size of output text - it doesn't work like this! One can only request desired size of output text through prompt. max_tokens (old) and max_completion_tokens (new) simply cut output even if it had to be longer!
- Never install packages separately without adding them to requirements.txt or package.json

# Clone Rules Repository

When setting up a new project, you should clone my Cursor rules repository. If you see it's not done yet - you have to do it before doing any other stuff.

## Setup Instructions

To clone the Cursor rules repository into this project:

```bash
# Add as a submodule
git submodule add https://github.com/samlowry/samlowrys-cursor-rules.git .cursor/rules

# Update the submodule when needed
git submodule update --remote .cursor/rules
```

# Initialization Workflow

When starting work with a new project, you can trigger the initialization routines by using the keyword **INIT**. When you type "INIT" in the chat, Cursor AI will:

1. Check if the rules repository is already cloned as a submodule
2. Clone it if needed (following the setup instructions above)
3. Execute all initialization routines mentioned in the active rule files
4. Set up any required project structure or configuration
5. Initialize markdown-based planning memory for the project

This ensures that all best practices from the rules are applied from the beginning of your work on the project.

# Git Emoji Commit Message Format

Commits MUST be prefixed with an emoji that represents the type of change, followed by a short description.

## Common Commit Types with Emojis
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

## Format
<emoji> <description>

## Examples
- ✨ Add Polish language support
- 🐛 Fix array parsing issue with multiple spaces
- 📚 Correct spelling in CHANGELOG
- 💄 Format code according to style guide
- ♻️ Improve refresh token logic
- ✅ Add missing tests for promo reels
- 🔧 Update build configuration
- 🚀 Optimize image loading process
- 🔒 Fix XSS vulnerability in form
- 🧹 Remove unused variables
- 📦 Update dependencies to latest versions

## Guidelines
- Use imperative mood in the description (e.g., "Add" not "Added")
- First letter of description should be capitalized
- No period at the end of the description
- Keep the description under 50 characters
- For more details, add a blank line after the description and then provide a longer explanation 
