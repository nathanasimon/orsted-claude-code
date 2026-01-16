# ORSTED for Claude Code

**Persistent context system for Claude Code** — automatically tracks what you do, why you did it, and what failed.

## Quick Install

### Option 1: Local Install

```bash
git clone https://github.com/yourusername/orsted.git
cd orsted/claude-code
claude --plugin-dir ./orsted
```

### Option 2: From Marketplace (when published)

```bash
/plugin marketplace add yourusername/orsted-marketplace
/plugin install orsted@orsted-marketplace
```

## What It Does

ORSTED creates a `.orsted/` folder in each directory where you work, containing:

- **`claude.md`** — Working memory (current focus, work log, decisions)
- **`project_info.md`** — Project overview (tech stack, structure, conventions)
- **`critical_mistakes.md`** — Error prevention (learn from mistakes)
- **`full_context.md`** — Complete audit trail (auto-updated, rarely read)

All files update automatically after every session. No manual work required.

## How It Works

Uses Claude Code's plugin system with hooks:
1. **`PreToolUse` hook** — Detects when reading CONTEXT.md files
2. **`Stop` hook** — Updates context files after each session

Everything runs silently in the background. No notifications, no interruptions.

## Requirements

- **Claude Code** (not Cursor IDE)
- Plugin system enabled

## Installation

See `INSTALL.md` for detailed instructions.

## For Cursor Users

If you're using **Cursor IDE** (not Claude Code), see the `../orsted-cursor/` directory.
