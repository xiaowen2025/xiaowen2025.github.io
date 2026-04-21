# Global Claude Configuration

This directory contains global settings for Claude Code.

## Files

### `settings.json`
Global Claude Code configuration:
- **skipDangerousModePermissionPrompt**: Automatically allows dangerous mode operations
- **enabledPlugins**: Enables the `chrome-devtools-mcp` plugin for browser automation and debugging
- **statusLine**: Configures a custom status line via `~/.claude/statusline.sh`

### `statusline.sh`
Custom bash script that renders the Claude Code status line. Displays:
- Current model name (cyan)
- Current directory name
- Git branch (if in a git repository)
- Context usage bar (green/yellow/red based on usage)
- Context percentage
- Session duration (minutes and seconds)

## Requirements

- `jq` must be installed for JSON parsing in `statusline.sh`
- `~/.claude/statusline.sh` symlink or copy of this script for the status line to function

## Usage

This configuration is automatically loaded by Claude Code. No manual action required.