# Workspace Setup

## 1. Install CLI Tools

```bash
# Install Claude Code
brew install anthropic/claude-code/claude
```

## 2. Copy Global Claude Settings

```bash
# Copy global Claude configuration
cp -r settings/global_claude ~/.claude/
chmod +x ~/.claude/statusline.sh
```

This includes:
- `settings.json` — skip dangerous mode prompt, Chrome DevTools MCP plugin, custom status line
- `statusline.sh` — shows model name, directory, git branch, context %, and session duration

```bash
# Configure permissions after install .claude/settings.local.json)
# {
#   "permissions": {
#     "defaultMode": "bypassPermissions"
#   }
# }

# Install CodeX (if available)
brew install codex

# Install Antigravity (if available)
brew install antigravity
```

## 3. GitHub Authentication

```bash
# Authenticate personal account
gh auth login

# Authenticate work account (if using multiple accounts)
gh auth login --hostname github.com
```

## 3. Clone Repositories and Create Environments

```bash
# Clone all required repositories
git clone git@github.com:username/repo1.git
git clone git@github.com:username/repo2.git
# ... clone remaining repos

# Create Python virtual environments
python3 -m venv .venv
source .venv/bin/activate

# Or use uv for faster dependency management
brew install uv
uv venv
uv sync
```

## 4. Install Docker

```bash
# Download from https://www.docker.com/products/docker-desktop/
# Not installed via Homebrew due to sudo requirements
```

## 5. Install Proton Pass

```bash
# Install Proton Pass
brew install --cask proton-pass
```

## 6. Set Up VSCode Extensions

```bash
# Core extensions
code --install-extension esbenp.prettier-vscode
code --install-extension ms-python.python
code --install-extension bradlc.vscode-tailwindcss

# Markdown Enhanced Preview
code --install-extension shdenzh.material-theme-vscode
code --install-extension alefragnani.vscode-copy-word
code --install-extension yzhang.markdown-all-in-one
code --install-extension docsmsft.docs-markdown
code --install-extension ms-vscode.markdown-language-features

# Preview markdown
code --install-extension mudrii.markdown-preview
```

## 7. Install and Configure Obsidian

```bash
# Install Obsidian
brew install --cask obsidian

# Configure vault and plugins as needed
```

## 8. Set Up Composio

```bash
# Install Composio CLI
curl -fsSL https://composio.dev/install | bash

# Authenticate and configure
composio login
```

## 9. Install Google Cloud SDK and Chrome Profiles

```bash
# Install Google Cloud SDK
brew install --cask google-cloud-sdk

# Initialize gcloud
gcloud init
```

## 10. Set Up Syncthing

```bash
# Install Syncthing
brew install syncthing  # CLI
brew install --cask syncthing

# Launch Syncthing (opens in browser at http://localhost:8384)
open -a Syncthing
```

## 11. Copy Global Claude Settings

```bash
# Copy global Claude configuration
cp -r settings/global_claude ~/.claude/
chmod +x ~/.claude/statusline.sh
```

This includes:
- `settings.json` — skip dangerous mode prompt, Chrome DevTools MCP plugin, custom status line
- `statusline.sh` — shows model name, directory, git branch, context %, and session duration
