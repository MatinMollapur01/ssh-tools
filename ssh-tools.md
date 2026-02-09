# SSH Tools and Terminal Enhancement Guide

## Overview
This document outlines the tools and configurations installed to enhance your terminal experience, transforming it into a powerful cyberpunk-themed environment with advanced functionality.

## Installed Applications

### File Management
1. **ranger** - A visual file manager with VI key bindings
2. **eza** - A modern replacement for ls with better visual output
3. **tree** - Display directory structure in a tree format

### Terminal Multiplexing
4. **tmux** - Terminal multiplexer for managing multiple terminal sessions

### File Viewing and Editing
5. **bat** - A cat clone with syntax highlighting and Git integration
6. **less/more** - Standard Unix paging utilities (pre-installed but enhanced)

### System Monitoring
7. **htop** - An interactive process viewer and system monitor
8. **glances** - Cross-platform system monitoring tool
9. **ncdu** - Disk usage analyzer with ncurses interface

### Search and Navigation
10. **ripgrep (rg)** - A fast search tool similar to grep
11. **fd** - A simple, fast and user-friendly alternative to find
12. **fzf** - A fuzzy finder for files, history, and more

### Network and HTTP Tools
13. **httpie** - User-friendly HTTP client with colorful output
14. **mosh** - Mobile shell that supports roaming and intermittent connectivity

### Data Processing
15. **jq** - Command-line JSON processor

### System Information
16. **neofetch** - System information tool with colorful output

### Entertainment and Fun
17. **cmatrix** - Shows a Matrix-style screen saver
18. **cowsay** - Generates ASCII pictures of a cow with speech bubbles
19. **figlet** - Creates large text banners with ASCII art fonts

### Session Recording
20. **asciinema** - Record and replay terminal sessions

## Tmux Configuration

### Aliases Setup
The following aliases have been added to your shell configuration:

- `tml` - List all active tmux sessions (`tmux list-sessions`)
- `tmn` - Create a new named tmux session (`tmux new-session -s`)
- `tma` - Attach to an existing tmux session (`tmux attach-session -t`)
- `tmd` - Delete a tmux session (`tmux kill-session -t`)

### Usage Examples
```bash
# List all sessions
tml

# Create a new session named "work"
tmn work

# Attach to a session named "work"
tma work

# Kill a session named "old_session"
tmd old_session
```

## Cyberpunk Theme Features

### Color Scheme
- Neon green/cyan/magenta color palette
- Enhanced syntax highlighting
- Custom prompt with cyberpunk aesthetics

### Visual Enhancements
- Powerline-patched fonts for special symbols
- Customized directory and file listings
- Enhanced command output formatting

## Quick Start Guide

### File Navigation
- Use `eza -la` instead of `ls -la` for enhanced file listings
- Use `tree` to visualize directory structures
- Use `ranger` for a visual file management experience

### Searching
- Use `fd pattern` instead of `find . -name pattern`
- Use `rg pattern` instead of `grep -r pattern .`

### System Monitoring
- Use `htop` for an interactive system monitor
- Use `glances` for comprehensive system stats
- Use `ncdu` to explore disk usage

### Session Management
- Use `tmux` to create persistent terminal sessions
- Use the aliases `tml`, `tmn`, `tma`, `tmd` for quick session management

## Useful Commands

### System Info
```bash
neofetch                    # Show system information
```

### File Preview
```bash
bat filename               # View file with syntax highlighting
```

### Network Testing
```bash
httpie example.com         # Make HTTP requests with colorful output
```

### Fun Commands
```bash
cowsay "Hello, Cyberpunk!" # ASCII art with message
figlet "HACKER"            # Large ASCII banner
cmatrix                    # Matrix-style falling characters
```

## Customization Tips

1. You can further customize your prompt by editing `~/.zshrc`
2. Ranger can be customized by creating a `~/.config/ranger/rc.conf` file
3. Tmux can be customized by editing `~/.tmux.conf`
4. Many of these tools have extensive configuration options - check their documentation

## Troubleshooting

- If colors don't appear correctly, ensure your terminal supports 256-color mode
- If special characters don't display properly, ensure powerline fonts are installed and active
- If aliases don't work, run `source ~/.zshrc` to reload your shell configuration

Enjoy your enhanced cyberpunk terminal experience!