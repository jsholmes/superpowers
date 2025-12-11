# Superpowers for OpenCode

A stripped-down fork of [obra/superpowers](https://github.com/obra/superpowers) focused on skill authoring.

## Quick Install

Tell OpenCode:

```
Clone https://github.com/jsholmes/superpowers to ~/.config/opencode/superpowers, then create directory ~/.config/opencode/plugin, then symlink ~/.config/opencode/superpowers/.opencode/plugin/superpowers.js to ~/.config/opencode/plugin/superpowers.js, then restart opencode.
```

## Manual Installation

### Prerequisites

- [OpenCode.ai](https://opencode.ai) installed
- Node.js installed
- Git installed

### Installation Steps

#### 1. Install Superpowers

```bash
mkdir -p ~/.config/opencode/superpowers
git clone https://github.com/jsholmes/superpowers.git ~/.config/opencode/superpowers
```

#### 2. Register the Plugin

OpenCode discovers plugins from `~/.config/opencode/plugin/`. Create a symlink:

```bash
mkdir -p ~/.config/opencode/plugin
ln -sf ~/.config/opencode/superpowers/.opencode/plugin/superpowers.js ~/.config/opencode/plugin/superpowers.js
```

Alternatively, for project-local installation:

```bash
# In your OpenCode project
mkdir -p .opencode/plugin
ln -sf ~/.config/opencode/superpowers/.opencode/plugin/superpowers.js .opencode/plugin/superpowers.js
```

#### 3. Restart OpenCode

Restart OpenCode to load the plugin.

## Available Skills

- **writing-skills** - Guide for creating effective skills using TDD principles
- **brainstorming** - Refine ideas into designs through Socratic questioning
- **testing-skills-with-subagents** - Validate skills with pressure testing

## Usage

### Finding Skills

Use the `find_skills` tool to list all available skills:

```
use find_skills tool
```

### Loading a Skill

Use the `use_skill` tool to load a specific skill:

```
use use_skill tool with skill_name: "superpowers:brainstorming"
```

### Personal Skills

Create your own skills in `~/.config/opencode/skills/`:

```bash
mkdir -p ~/.config/opencode/skills/my-skill
```

Create `~/.config/opencode/skills/my-skill/SKILL.md`:

```markdown
---
name: my-skill
description: Use when [condition] - [what it does]
---

# My Skill

[Your skill content here]
```

### Project Skills

Create project-specific skills in your OpenCode project:

```bash
# In your OpenCode project
mkdir -p .opencode/skills/my-project-skill
```

Create `.opencode/skills/my-project-skill/SKILL.md` with similar structure.

## Skill Priority

Skills are resolved with this priority order:

1. **Project skills** (`.opencode/skills/`) - Highest priority
2. **Personal skills** (`~/.config/opencode/skills/`)
3. **Superpowers skills** (`~/.config/opencode/superpowers/skills/`)

You can force resolution to a specific level:
- `project:skill-name` - Force project skill
- `skill-name` - Search project → personal → superpowers
- `superpowers:skill-name` - Force superpowers skill

## Tool Mapping

When skills reference Claude Code tools, substitute OpenCode equivalents:

- `TodoWrite` → `update_plan`
- `Task` with subagents → OpenCode's `@mention` system
- `Skill` tool → `use_skill` custom tool
- File operations → Native OpenCode tools

## Updating

```bash
cd ~/.config/opencode/superpowers
git pull
```

Restart OpenCode to load the updates.

## Troubleshooting

### Plugin not loading

1. Check plugin file exists: `ls ~/.config/opencode/superpowers/.opencode/plugin/superpowers.js`
2. Check symlink: `ls -l ~/.config/opencode/plugin/superpowers.js`
3. Check OpenCode logs for plugin loading messages

### Skills not found

1. Verify skills directory: `ls ~/.config/opencode/superpowers/skills`
2. Use `find_skills` tool to see what's discovered
3. Check skill structure: each skill needs a `SKILL.md` file

## Getting Help

- Issues: https://github.com/jsholmes/superpowers/issues
- Original repo: https://github.com/obra/superpowers
- OpenCode docs: https://opencode.ai/docs/
