# nvm Installation Guide

## For macOS and Ubuntu

### Prerequisites
- macOS Catalina (10.15) or higher, or any recent version of Ubuntu
- Docker installed (optional, but recommended for those using Docker)
- Git installed (typically pre-installed on macOS and Linux)
- For Windows, ensure WSL 2 is installed

### macOS Specific Setup
#### Install Brew (if not installed)
1. Check if Brew is installed:
   ```
   whereis brew
   ```
2. If not installed, run:
   ```
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   ```

### Common Setup for macOS and Ubuntu
1. Update system package lists:
   - On Ubuntu:
     ```
     sudo apt update
     ```
   - On macOS:
     ```
     brew update && brew upgrade
     ```

2. Create and navigate to a directory for `nvm` installation:
   ```
   mkdir ~/your-project-directory
   cd ~/your-project-directory
   ```

### Install Node.js Using nvm
Node.js is a server-side JavaScript environment. `nvm` allows you to manage multiple Node.js versions.

1. Install nvm:
   ```
   curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash
   ```

2. Update system paths:
   ```
   source ~/.bashrc
   ```

3. Check available Node.js versions:
   ```
   nvm list-remote
   ```

4. Install a specific Node.js version (e.g., v12.22.0):
   ```
   nvm install v12.22.0
   ```

5. Use the installed Node.js version:
   ```
   nvm use v12.22.0
   ```
