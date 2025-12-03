# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Attribution
- Never attribute any work, commit, code, doc, suggestion, or mention to Claude
- Never commit as Claude, always commit as the user

## Test Execution
- Don't run the entire test suite after every change
- After modifying code in a specific module, run ONLY tests for that module
  - Example: If you modify `src/auth/login.py`, run only `pytest tests/test_auth.py`
- Ask before running full test suite

## Git Behavior
- Don't automatically merge PRs; wait for explicit request
- Don't try to GPG sign commits
- Upon merge, delete both local and remote associated branches
- When reviewing PR recommendations: inventory items first as a table, address each, then render the final status table (fit within 120 char width)

## Engineering Guidelines
- New features should always be accompanied with appropriate unit tests

## Available Slash Commands

### Information Gathering & Analysis
- `/gather` - Generate 5-7 numbered questions to gather requirements before starting work
- `/reframe` - Synthesize understanding and present structured summary for confirmation
- `/truth` - Activate truth-first mode with evidence-based, quantified responses
- `/codereview` - Comprehensive code review with TASK.md management and prioritized findings
- `/coverage-impl` - Add unit tests to functions without 100% coverage, including edge cases

### Memory Management
- `/memorize` - Save conversation context to local memory with semantic tagging
- `/recall [id|tag|query]` - Restore saved context from local memory

### Git & GitHub
- `/commit` - Create well-formatted commits with emoji conventional commit messages, auto-splitting logical changes
- `/create-pr` - Create branch, format files with Biome, commit, push, and submit PR
- `/review-pr-comment [url]` - Inventory PR comment recommendations and prompt for implementation

### Meta
- `/command-creator` - Interactive assistant to create new Claude commands following established patterns
