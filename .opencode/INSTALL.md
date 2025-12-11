# Installing Superpowers for OpenCode

Quick setup to enable superpowers skills in OpenCode.

## Prerequisites

- [OpenCode.ai](https://opencode.ai) installed
- Node.js installed
- Git installed

## Installation Steps

### 1. Install Superpowers

```bash
mkdir -p ~/.config/opencode/superpowers
git clone https://github.com/jsholmes/superpowers.git ~/.config/opencode/superpowers
```

### 2. Register the Plugin

Create a symlink so OpenCode discovers the plugin:

```bash
mkdir -p ~/.config/opencode/plugin
ln -sf ~/.config/opencode/superpowers/.opencode/plugin/superpowers.js ~/.config/opencode/plugin/superpowers.js
```

### 3. Restart OpenCode

Restart OpenCode. The plugin provides `use_skill` and `find_skills` tools.

## Available Skills

- **writing-skills** - Guide for creating effective skills
- **brainstorming** - Refine ideas into designs through questioning
- **testing-skills-with-subagents** - Validate skills with pressure testing

## Usage

### Finding Skills

```
use find_skills tool
```

### Loading a Skill

```
use use_skill tool with skill_name: "superpowers:brainstorming"
```

## Getting Help

- Issues: https://github.com/jsholmes/superpowers/issues
- Original repo: https://github.com/obra/superpowers
