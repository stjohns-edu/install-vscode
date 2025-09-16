# Installing Visual Studio Code on Ubuntu

This guide shows how to install Visual Studio Code on Ubuntu using the official Microsoft repository.

### Prerequisites

- Ubuntu system with sudo privileges
- Internet connection

### Installation Steps

1. Add Microsoft's GPG key:
   ```bash
   wget -qO- https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > packages.microsoft.gpg
   ```

2. Install the GPG key:
   ```bash
   sudo install -o root -g root -m 644 packages.microsoft.gpg /etc/apt/trusted.gpg.d/
   ```

3. Add the VS Code repository:
   ```bash
   sudo sh -c 'echo "deb [arch=amd64,arm64,armhf signed-by=/etc/apt/trusted.gpg.d/packages.microsoft.gpg] https://packages.microsoft.com/repos/code stable main" > /etc/apt/sources.list.d/vscode.list'
   ```

4. Update package list and install VS Code:
   ```bash
   sudo apt update
   sudo apt install code
   ```

### Launch VS Code

After installation, you can launch Visual Studio Code by:
- Running `code` command in the terminal
- Finding Visual Studio Code in your applications menu

### Automatic Updates

VS Code installed this way will receive automatic updates through Ubuntu's package manager when you run sudo apt update && sudo apt upgrade.

### Alternative Installation Methods

- Snap package: sudo snap install code --classic
- Download .deb package from the official VS Code website

### Troubleshooting

If you encounter permission issues, make sure your user has sudo privileges and try running the commands again.
