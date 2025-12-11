# Superpowers for Codex

A stripped-down fork of [obra/superpowers](https://github.com/obra/superpowers) focused on skill authoring.

## Quick Install

Tell Codex:

```
Fetch and follow instructions from https://raw.githubusercontent.com/jsholmes/superpowers/refs/heads/main/.codex/INSTALL.md
```

## Manual Installation

### Prerequisites

- OpenAI Codex access
- Shell access to install files

### Installation Steps

#### 1. Clone Superpowers

```bash
mkdir -p ~/.codex/superpowers
git clone https://github.com/jsholmes/superpowers.git ~/.codex/superpowers
```

#### 2. Install Bootstrap

The bootstrap file is included in the repository at `.codex/superpowers-bootstrap.md`. Codex will automatically use it from the cloned location.

#### 3. Verify Installation

Tell Codex:

```
Run ~/.codex/superpowers/.codex/superpowers-codex find-skills to show available skills
```

You should see the available skills listed.

## Available Skills

- **writing-skills** - Guide for creating effective skills using TDD principles
- **brainstorming** - Refine ideas into designs through Socratic questioning
- **testing-skills-with-subagents** - Validate skills with pressure testing

## Usage

### Finding Skills

```
Run ~/.codex/superpowers/.codex/superpowers-codex find-skills
```

### Loading a Skill

```
Run ~/.codex/superpowers/.codex/superpowers-codex use-skill superpowers:brainstorming
```

### Personal Skills

Create your own skills in `~/.codex/skills/`:

```bash
mkdir -p ~/.codex/skills/my-skill
```

Create `~/.codex/skills/my-skill/SKILL.md`:

```markdown
---
name: my-skill
description: Use when [condition] - [what it does]
---

# My Skill

[Your skill content here]
```

Personal skills override superpowers skills with the same name.

## Tool Mapping

When skills reference Claude Code tools, substitute Codex equivalents:

- `TodoWrite` → `update_plan`
- `Task` with subagents → Do the work directly
- `Skill` tool → `superpowers-codex use-skill`
- File operations → Native Codex tools

## Updating

```bash
cd ~/.codex/superpowers
git pull
```

## Troubleshooting

### Skills not found

1. Verify installation: `ls ~/.codex/superpowers/skills`
2. Check CLI works: `~/.codex/superpowers/.codex/superpowers-codex find-skills`
3. Verify skills have SKILL.md files

### CLI script not executable

```bash
chmod +x ~/.codex/superpowers/.codex/superpowers-codex
```

## Getting Help

- Issues: https://github.com/jsholmes/superpowers/issues
- Original repo: https://github.com/obra/superpowers
