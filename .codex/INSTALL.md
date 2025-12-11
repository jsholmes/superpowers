# Installing Superpowers for Codex

Quick setup to enable superpowers skills in Codex.

## Installation

1. **Clone superpowers repository**:
   ```bash
   mkdir -p ~/.codex/superpowers
   cd ~/.codex/superpowers
   git clone https://github.com/jsholmes/superpowers.git .
   ```

2. **Create personal skills directory**:
   ```bash
   mkdir -p ~/.codex/skills
   ```

3. **Test the CLI**:
   ```bash
   ~/.codex/superpowers/.codex/superpowers-codex find-skills
   ```

You should see the available skills listed.

## Available Skills

- **writing-skills** - Guide for creating effective skills
- **brainstorming** - Refine ideas into designs through questioning
- **testing-skills-with-subagents** - Validate skills with pressure testing

## Usage

To load a skill:
```
Run ~/.codex/superpowers/.codex/superpowers-codex use-skill superpowers:brainstorming
```

To list all skills:
```
Run ~/.codex/superpowers/.codex/superpowers-codex find-skills
```

## Getting Help

- Issues: https://github.com/jsholmes/superpowers/issues
- Original repo: https://github.com/obra/superpowers
