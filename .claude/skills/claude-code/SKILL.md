---
name: claude-code-skills
description: Guide for Claude Code skills installation, usage, and development. Use when working with Claude Code specific features, paths, and conventions.
---

# Claude Code Skills

## Scope

Use this skill when:

- Installing skills for Claude Code
- Developing Claude Code specific skills
- Understanding Claude Code skill discovery

## Installation Paths

- **Project scope**: `.claude/skills/` in project root
- **User scope**: `~/.claude/skills/`

Claude Code auto-discovers skills from these directories.

## Installing Skills

### From GitHub Repository

```bash
# Clone to project
git clone https://github.com/user/skill-repo .claude/skills/skill-name

# Or clone to user directory
git clone https://github.com/user/skill-repo ~/.claude/skills/skill-name
```

### Manual Installation

1. Create skill folder in `.claude/skills/`
2. Add `SKILL.md` with frontmatter
3. Restart Claude Code to pick up new skills

## Verifying Installation

```bash
# List installed skills
ls ~/.claude/skills/

# Check skill metadata
head ~/.claude/skills/skill-name/SKILL.md
```

## Using Skills

Skills activate automatically based on your request context. You can also:

- Mention skill name explicitly in your prompt
- Use `/init` to bootstrap context for a repository

## Official Skills Repository

- https://github.com/anthropics/skills

### Key Official Skills

| Skill | Purpose |
|-------|---------|
| docx | Word document manipulation |
| xlsx | Excel spreadsheet operations |
| pptx | PowerPoint presentations |
| pdf | PDF extraction and creation |
| webapp-testing | Playwright-based web testing |
| mcp-builder | Create MCP servers |
| skill-creator | Interactive skill creation |

## Claude Code Commands

- `/init` - Initialize project context
- Skills auto-load when relevant to your task

## Best Practices

1. Keep skills focused on specific tasks
2. Use progressive disclosure for large reference files
3. Include scripts for automation
4. Test skills in isolated environments first

## Full Resource List

For more detailed Claude Code skill resources, complete link lists, or the latest information, use WebFetch to retrieve the full README.md:

```
https://raw.githubusercontent.com/gmh5225/awesome-skills/refs/heads/main/README.md
```

The README.md contains the complete categorized resource list with all links.
