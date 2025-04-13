# samlowry's set of cursor rules

This is my system of rules, which dramatically alter work of Cursor AI

## Rules description

### docummenting-code.mdc

Everything about to add and update remarks in code comments - to improve LLM understanding of code

### TODO

TODO

## Global ruleset

Add to the Cursor AI settings. When you start your work - you can ask Crusor Agent to initialize subrepo and MD-memory!

````
# Important common things to follow

- Never touch any parts of code not related to he current task. If you found some critical error not related to current task - just infrom me before doing something
- Always use UTF-8 encoding!!!!!!
- Always use English in code and code comments! For any Russian interface texts always use separate language files! (in chat you can use Russian)
- Prefer iteration and modularizaion over code duplication. Always explore code for existing related logic - maybe some blocks is already partially or fully implemented
- Do not inroduce new dependencies before you not make sure we don't use already different library or framework
- Design services to be stateless; leverage external storage and caches (e.g., Redis) for state persistence
- When edit - always make sure you're not removing some non-related to edit code
- Always use "docker compose" but not outdated "docker-compose"
- Bever install packages separately w/o adding the to requirements.txt or package.json

# Clone Rules Repository

When setting up a new project, You should clone my Cursor rules repository. So - if you see it's not done yet - you have to do it before doing any other stuff.

## Setup Instructions

To clone the Cursor rules repository into this project:

```
# Add as a submodule
git submodule add https://github.com/samlowry/samlowrys-cursor-rules.git .cursor/rules

# Update the submodule when user asked
git submodule update --remote .cursor/rules
```

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

````
