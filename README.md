# nvm Installation Guide

## Introduction
This guide provides step-by-step instructions on how to install and manage multiple versions of Node.js using `nvm` (Node Version Manager). `nvm` is particularly useful for developers who need to switch between different Node.js versions across various projects. If you're managing multiple services that each require different versions of Node.js, consider using Docker to isolate and manage these environments effectively.

## Prerequisites
- macOS Catalina (10.15) or higher, or any recent version of Ubuntu, Debian, or Arch Linux
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

### Common Setup for macOS, Ubuntu, and Debian
1. Update system package lists:
   - On Ubuntu/Debian:
     ```
     sudo apt update && sudo apt upgrade
     ```
   - On macOS:
     ```
     brew update && brew upgrade
     ```

### Arch Linux Specific Setup
1. Ensure you have the necessary tools:
   ```
   sudo pacman -Syu git base-devel
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

   I'm told that latest stable version is 0.39.7. However, 0.38.0 is the one I use. In any case, all you have to do is replace the `v0.38.0` in the url able with `v0.39.7`, if so inclined.

2. Update system paths:
   - For bash users:
     ```
     source ~/.bashrc
     ```
   - For zsh users:
     ```
     source ~/.zshrc
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

### Additional Notes for WSL Users
If you are using Windows and have WSL installed to handle Linux-specific tasks, remember to run these commands within your WSL terminal. This environment allows you to use Linux tools and software directly in Windows, integrating seamlessly with your Windows file system and hardware.
