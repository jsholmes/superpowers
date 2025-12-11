# Superpowers (Stripped Fork)

A stripped-down fork of [obra/superpowers](https://github.com/obra/superpowers) focused on skill authoring.

This fork removes the full development workflow (TDD enforcement, code review, plan execution, git worktrees, etc.) and keeps only the skills for creating and testing new skills.

**For the full superpowers experience**, see the [original repository](https://github.com/obra/superpowers).

## What's Included

### Skills

- **writing-skills** - Guide for creating effective skills using TDD principles. Includes Anthropic's official best practices.
- **brainstorming** - Refine rough ideas into designs through Socratic questioning.
- **testing-skills-with-subagents** - Validate skills work under pressure using RED-GREEN-REFACTOR with subagents.

### Commands

- `/superpowers:brainstorm` - Start a brainstorming session

## Installation

### Claude Code

```bash
# Add marketplace (if not already added)
/plugin marketplace add obra/superpowers-marketplace

# Install this fork instead of the original
/plugin install superpowers@superpowers-marketplace
```

Or install directly from this repo if you've forked it.

### Codex

See [docs/README.codex.md](docs/README.codex.md)

### OpenCode

See [docs/README.opencode.md](docs/README.opencode.md)

## License

MIT License - see LICENSE file for details

## Acknowledgments

Original superpowers by [Jesse Vincent](https://github.com/obra). See the [original repo](https://github.com/obra/superpowers) for the full workflow.
