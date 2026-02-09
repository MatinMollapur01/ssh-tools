# ZSH Setup Guide

## Overview
This document provides a comprehensive guide to your ZSH setup, including installation, configuration, themes, plugins, and customization options. Your terminal has been transformed into a highly productive cyberpunk-themed environment.

## Installation Process

### Prerequisites
- Ubuntu/Debian-based system
- Git and curl installed
- Administrative privileges (for package installations)

### Initial Setup Steps
1. Install ZSH: `sudo apt install zsh`
2. Install Oh My Zsh framework: `sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`
3. Install powerline fonts for proper display of special characters
4. Configure cyberpunk theme and customizations
5. Install productivity applications and plugins

## Theme Configuration

### Agnoster Theme
- Selected as the primary theme for its futuristic look
- Features powerline-style segments showing system information
- Customized with cyberpunk color scheme (neon greens, cyans, and magentas)

### Custom Prompt Elements
- Username and hostname display
- Current working directory
- Git branch and status indicators
- Command execution status
- Time stamps

## Plugin Configuration

### Core Productivity Plugins

#### 1. git
- Enhanced git functionality with useful aliases
- Common git commands shortened for faster typing
- Git status indicators in the prompt

#### 2. zsh-syntax-highlighting
- Adds syntax highlighting to commands as you type
- Invalid commands shown in red
- Valid commands highlighted appropriately
- Improves accuracy and reduces typos

#### 3. zsh-autosuggestions
- Suggests commands based on history as you type
- Suggestions appear in gray at the end of your command
- Press right arrow to accept the suggestion
- Increases typing speed significantly

#### 4. history-substring-search
- Enhanced history search functionality
- Press Up/Down arrows to search through command history
- Type part of a command to filter history
- Makes finding past commands much easier

#### 5. colored-man-pages
- Colors the manual pages for better readability
- Syntax highlighting for man page sections
- Improves navigation and comprehension of documentation

#### 6. extract
- Easy extraction of compressed archives
- Single command works for multiple archive formats (.tar.gz, .zip, .rar, etc.)
- Simply type `x filename` to extract any archive

#### 7. sudo
- Quickly prepend sudo to your last command
- Press `Esc` followed by `sudo` to add sudo to the previous command
- Saves time when forgetting to use sudo initially

#### 8. command-not-found
- Suggests packages to install for unknown commands
- When a command is not found, suggests installation options
- Helps discover relevant packages quickly

### Development Plugins

#### 9. docker
- Docker aliases and completions
- Shortcuts for common Docker commands
- Tab completion for container names and images

#### 10. docker-compose
- Docker Compose aliases and completions
- Simplified commands for Docker Compose workflows
- Tab completion for service names

#### 11. kubectl
- Kubernetes CLI completion and aliases
- Context and namespace information in prompt
- Tab completion for resources and namespaces

#### 12. terraform
- Terraform aliases and completion
- Shortcuts for common Terraform commands
- Improved workflow for infrastructure management

#### 13. aws
- AWS CLI completion and aliases
- Helpful for AWS command completion
- Faster cloud operations

#### 14. node
- Node.js related aliases
- Version management helpers
- NPM shortcuts

#### 15. npm
- npm aliases and completion
- Faster package management
- Tab completion for package names

#### 16. yarn
- Yarn package manager completion
- Alternative to npm with similar benefits
- Project-specific shortcuts

### Utility Plugins

#### 17. rsync
- rsync aliases for easier file synchronization
- Common rsync command shortcuts
- Safer copying with improved defaults

#### 18. copyfile
- Copy file contents to clipboard
- Use `copyfile <filename>` to copy file contents
- Cross-platform compatibility

#### 19. copydir
- Copy current directory path to clipboard
- Use `copydir` to copy the current path
- Useful for sharing or referencing paths

#### 20. web-search
- Allows searching web from command line
- Search engines accessible via command
- Example: `ducky how to use zsh plugins`

## Tmux Integration

### Aliases Setup
- `tml` - List all active tmux sessions (`tmux list-sessions`)
- `tmn` - Create a new named tmux session (`tmux new-session -s`)
- `tma` - Attach to an existing tmux session (`tmux attach-session -t`)
- `tmd` - Delete a tmux session (`tmux kill-session -t`)

## Cyberpunk Visual Customization

### Color Scheme
- Primary: Neon Green (#00FF00)
- Secondary: Cyan (#00FFFF)
- Accent: Magenta (#FF00FF)
- Background: Dark theme for eye comfort

### Font Configuration
- Powerline-patched fonts for special characters
- Monospace font for consistent alignment
- Clear distinction between similar characters (0 and O, 1 and l)

## Additional Tools Installed

### File Management
- **ranger**: Visual file manager with VI key bindings
- **eza**: Modern replacement for ls with better visual output
- **tree**: Display directory structure in a tree format

### System Monitoring
- **htop**: Interactive process viewer and system monitor
- **glances**: Cross-platform system monitoring tool
- **ncdu**: Disk usage analyzer with ncurses interface

### Search and Navigation
- **ripgrep (rg)**: Fast search tool similar to grep
- **fd**: User-friendly alternative to find
- **fzf**: Fuzzy finder for files, history, and more

### Network Tools
- **httpie**: User-friendly HTTP client with colorful output
- **mosh**: Mobile shell that supports roaming and intermittent connectivity

### Data Processing
- **jq**: Command-line JSON processor

### System Information
- **neofetch**: System information tool with colorful output

### Entertainment
- **cmatrix**: Matrix-style screen saver
- **cowsay**: ASCII art with messages
- **figlet**: Large text banners with ASCII art fonts
- **asciinema**: Record and replay terminal sessions

## Configuration Files

### Location
- Main configuration: `~/.zshrc`
- Tmux configuration: `~/.tmux.conf` (if created)
- Oh My Zsh directory: `~/.oh-my-zsh/`

### Customization Options
- Edit `~/.zshrc` to modify theme, plugins, or aliases
- Add custom functions to the bottom of the file
- Reload configuration with `source ~/.zshrc`

## Productivity Tips

### Keyboard Shortcuts
- `Ctrl + R`: Search command history (if not overridden)
- `Up/Down Arrows`: Navigate command history
- `Tab`: Complete commands, filenames, etc.
- `Ctrl + A`: Move cursor to beginning of line
- `Ctrl + E`: Move cursor to end of line
- `Ctrl + U`: Clear entire line
- `Ctrl + K`: Clear from cursor to end of line

### Useful Commands
- `history`: View command history
- `which command_name`: Find the path of a command
- `man command_name`: View manual for a command
- `alias`: List all defined aliases
- `cd -`: Switch to previous directory

### Performance Optimization
- Disable unused plugins to improve startup time
- Use `time zsh -i -c exit` to measure shell startup time
- Consider lazy-loading for rarely used plugins

## Troubleshooting

### Common Issues
- If colors don't appear correctly, ensure your terminal supports 256-color mode
- If special characters don't display properly, ensure powerline fonts are installed and active
- If plugins don't load, run `source ~/.zshrc` to reload your shell configuration
- If autocomplete doesn't work, check that the relevant plugin is enabled in `.zshrc`

### Reset Configuration
- To reset to default, rename `~/.zshrc` to `~/.zshrc.backup` and reinstall Oh My Zsh
- To disable plugins temporarily, comment them out in `~/.zshrc`

## Updating

### Oh My Zsh
- Update Oh My Zsh: `upgrade_oh_my_zsh` command
- Updates include new themes, plugins, and fixes
- Automatic updates can be configured in `~/.zshrc`

### Plugins
- Most plugins update with Oh My Zsh
- Some plugins may have individual update mechanisms
- Check plugin documentation for specific update instructions

## Customization Ideas

### Theme Modifications
- Experiment with other Oh My Zsh themes
- Modify the agnoster theme colors
- Add custom segments to the prompt

### Plugin Additions
- Explore additional plugins in the Oh My Zsh repository
- Install community plugins from GitHub
- Create custom plugins for specific workflows

## Conclusion

Your ZSH environment is now optimized for productivity with a distinctive cyberpunk aesthetic. The combination of visual appeal, powerful plugins, and efficient shortcuts should significantly enhance your command-line experience. Take time to familiarize yourself with the new tools and shortcuts to maximize your productivity gains.

Remember to regularly update your system and Oh My Zsh to benefit from the latest features and security patches.