# Claude Code User Configuration

Personal configuration directory for [Claude Code](https://claude.ai/code), Anthropic's CLI for Claude.

## Directory Structure

```
~/.claude/
├── commands/               # Custom slash commands
│   ├── claude/             # Meta commands (command-creator)
│   ├── git/                # Git commands (commit, review-branch)
│   ├── github/             # GitHub commands (create-pr, review-pr-comment)
│   ├── localmemory/        # Memory commands (memorize, recall)
│   └── *.md                # Root commands (listed below)
├── plugins/                # Installed plugins and marketplaces
│   └── marketplaces/       # Plugin marketplace sources
├── settings.json           # Global settings
├── settings.local.json     # Local overrides (not synced)
└── CLAUDE.md               # Instructions for Claude Code
```

## Available Commands

### Information Gathering
| Command | Description |
|---------|-------------|
| `/gather` | Generate requirements-gathering questions before starting work |
| `/reframe` | Synthesize and present structured summary for confirmation |
| `/truth` | Activate truth-first mode with evidence-based responses |

### Code Quality
| Command | Description |
|---------|-------------|
| `/codereview-to-beads` | Code review with findings tracked in Beads issue tracker |
| `/codereview-to-task` | Code review with findings tracked in TASK.md |
| `/coverage-impl` | Add unit tests to achieve 100% coverage |

### Memory
| Command | Description |
|---------|-------------|
| `/memorize` | Save conversation context to local memory |
| `/recall [query]` | Restore saved context from local memory |

### Git & GitHub
| Command | Description |
|---------|-------------|
| `/commit` | Create commits with emoji conventional commit format |
| `/commit-smart` | Smart commit with automatic change splitting |
| `/review-branch` | Multi-reviewer branch analysis |
| `/create-pr` | Create branch, commit, and submit pull request |
| `/review-pr-comment [url]` | Review and implement PR feedback |

### Meta
| Command | Description |
|---------|-------------|
| `/command-creator` | Create new custom commands |

## Installed Plugins

### Marketplaces
| Marketplace | Description |
|-------------|-------------|
| `anthropic-agent-skills` | Official Anthropic agent skills |
| `beads-marketplace` | Beads issue tracking plugin |
| `browser-tools` | Browser automation tools |
| `claude-plugins-official` | Official Claude plugins |
| `playwright-skill` | Playwright browser testing |
| `superpowers-marketplace` | Superpowers productivity plugins |

### Enabled Plugins
| Plugin | Source |
|--------|--------|
| `document-skills` | anthropic-agent-skills |
| `playwright-skill` | playwright-skill |
| `browser-automation` | browser-tools |
| `github` | claude-plugins-official |
| `supabase` | claude-plugins-official |
| `code-review` | claude-plugins-official |
| `pr-review-toolkit` | claude-plugins-official |
| `playwright` | claude-plugins-official |
| `vercel` | claude-plugins-official |
| `beads` | beads-marketplace |
| `double-shot-latte` | superpowers-marketplace |
| `superpowers` | superpowers-marketplace |

## Quick Start

1. Commands are available in any Claude Code session
2. Type `/` to see available commands
3. Use `/help` for built-in Claude Code help

## Configuration

- `CLAUDE.md` - Behavioral instructions applied to all sessions
- `settings.json` - Global Claude Code settings
- `settings.local.json` - Machine-specific overrides

## Resources

- [Claude Code Documentation](https://docs.anthropic.com/claude-code)
- [Report Issues](https://github.com/anthropics/claude-code/issues)
