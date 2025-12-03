# Contributing

Guidelines for adding and maintaining custom commands in this configuration.

## Adding New Commands

### 1. Choose Location

```
commands/
├── {category}/     # Grouped commands (git/, github/, localmemory/)
└── {name}.md       # Standalone commands
```

Use subdirectories for related commands; root level for standalone utilities.

### 2. Command File Format

```markdown
## /{command-name}

Brief description of what the command does.

**Process:**
1. Step one
2. Step two

**Output:**
```
Expected output format
```
```

### 3. Naming Conventions

- Use lowercase with hyphens: `my-command.md`
- Subdirectory commands: `/git/commit` from `commands/git/commit.md`
- Keep names short but descriptive

## Command Patterns

### Question-Gathering Pattern
See `/gather` - generates structured questions before starting work.

### Confirmation Pattern
See `/reframe` - presents understanding and waits for confirmation.

### Analysis Pattern
See `/codereview` - scans codebase and produces prioritized findings.

### Workflow Pattern
See `/commit` - multi-step process with decision points.

## Testing Commands

1. Create command file in `commands/`
2. Start new Claude Code session
3. Type `/{command-name}` to test
4. Iterate on the prompt

## Updating CLAUDE.md

When adding commands that affect Claude's behavior globally:
1. Add rules to appropriate section in `CLAUDE.md`
2. Document the command in the "Available Slash Commands" section

## Best Practices

- Keep prompts concise; Claude Code has context limits
- Use structured output formats for consistency
- Include example output in command files
- Test commands in real scenarios before committing
