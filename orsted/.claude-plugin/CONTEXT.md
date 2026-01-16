# CONTEXT.md - orsted/.claude-plugin

## What is this folder
Contains the plugin manifest (`plugin.json`) that defines metadata for the Orsted plugin in the Claude Code marketplace.

## Work Log

### 2026-01-15
- **Fixed `repository` field format**: Changed from object format `{"type": "git", "url": "..."}` to simple string format `"https://..."`. The marketplace requires `repository` to be a string, not an object.
- **Fixed repository URL**: Corrected the GitHub username from `nathansimon` to `nathanasimon` to match the actual repository location.
- **Fixed homepage URL**: Updated to use correct username `nathanasimon`.

## What Failed
- **Plugin validation failed**: The `repository` field was using npm's package.json object format, but the Claude marketplace plugin.json schema requires it to be a plain URL string. This caused validation/recognition issues.
- **Wrong GitHub username**: URLs pointed to non-existent `nathansimon` user instead of `nathanasimon`.

## Decisions
- **Repository format**: Used simple string format for `repository` field rather than object format. While less explicit about the VCS type, this matches the marketplace schema requirements.
- **Considered alternative**: Could have documented the git type elsewhere, but simplicity won out since the `.git` extension makes the type obvious.

## Status
🟢 Done
