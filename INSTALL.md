# Claude Code Installation Guide

## Quick Install

### Option 1: Local Install (Recommended)

```bash
git clone https://github.com/nathanasimon/orsted.git
cd orsted/claude-code
claude --plugin-dir ./orsted
```

### Option 2: From Marketplace (when published)

```bash
/plugin marketplace add nathanasimon/orsted-marketplace
/plugin install orsted@orsted-marketplace
```

## Manual Install

1. **Clone the repository:**
   ```bash
   git clone https://github.com/nathanasimon/orsted.git
   cd orsted/claude-code
   ```

2. **Run Claude Code with plugin:**
   ```bash
   claude --plugin-dir ./orsted
   ```

3. **Set up project:**
   - Copy `.cursorrules` to your project root
   - Copy `templates/` to your project's `.orsted/` folder
   - Fill in `project_info.md` with your project details

## Project Setup

After installation:

1. **Copy `.cursorrules`** to your project root:
   ```bash
   cp .cursorrules /path/to/your/project/
   ```

2. **Create `.orsted/` folder** and copy templates:
   ```bash
   mkdir -p /path/to/your/project/.orsted
   cp templates/*.template /path/to/your/project/.orsted/
   ```

3. **Fill in `project_info.md`** with your project details

4. **Start working** — Orsted will automatically create `.orsted/` folders in directories where you work

## How It Works

Claude Code plugin uses:
- **`PreToolUse` hook** — Detects when reading CONTEXT.md files
- **`Stop` hook** — Updates context files after each session

## Requirements

- **Claude Code** (not Cursor IDE)
- Plugin system enabled

## Troubleshooting

### Plugin not loading
- Check that `orsted/` directory has `.claude-plugin/` folder
- Verify plugin structure: `ls -la orsted/.claude-plugin/`

### Hooks not firing
- Make sure Claude Code was started with `--plugin-dir` flag
- Check plugin logs for errors

## For Cursor Users

If you're using **Cursor IDE** (not Claude Code), see the `../orsted-cursor/` directory.
