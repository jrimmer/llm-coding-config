# Claude Code User Configuration

Personal configuration directory for [Claude Code](https://claude.ai/code), Anthropic's CLI for Claude.

## Directory Structure

```
~/.claude/
├── commands/           # Custom slash commands
│   ├── claude/         # Meta commands (command-creator)
│   ├── git/            # Git commands (commit)
│   ├── github/         # GitHub commands (create-pr, review-pr-comment)
│   ├── localmemory/    # Memory commands (memorize, recall)
│   └── *.md            # Root commands (gather, reframe, truth, codereview, coverage-impl)
├── plugins/            # Installed plugins and marketplaces
├── projects/           # Project-specific configurations
├── settings.json       # Global settings
├── settings.local.json # Local overrides (not synced)
└── CLAUDE.md           # Instructions for Claude Code
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
| `/codereview` | Comprehensive code review with prioritized findings |
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
| `/create-pr` | Create branch, commit, and submit pull request |
| `/review-pr-comment [url]` | Review and implement PR feedback |

### Meta
| Command | Description |
|---------|-------------|
| `/command-creator` | Create new custom commands |

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
