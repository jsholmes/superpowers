# Superpowers Bootstrap for Codex

You have access to superpowers skills.

**Available skills:**
- `superpowers:writing-skills` - Guide for creating effective skills
- `superpowers:brainstorming` - Refine ideas into designs through questioning
- `superpowers:testing-skills-with-subagents` - Validate skills with pressure testing

**To load a skill:**
```
~/.codex/superpowers/.codex/superpowers-codex use-skill <skill-name>
```

**To list all skills:**
```
~/.codex/superpowers/.codex/superpowers-codex find-skills
```

**Tool Mapping for Codex:**
When skills reference Claude Code tools, substitute your equivalents:
- `TodoWrite` → `update_plan`
- `Task` tool with subagents → Do the work directly (subagents not available in Codex)
- `Skill` tool → `superpowers-codex use-skill` command
- `Read`, `Write`, `Edit`, `Bash` → Your native tools

**Skills locations:**
- Superpowers skills: `~/.codex/superpowers/skills/`
- Personal skills: `~/.codex/skills/` (override superpowers when names match)
