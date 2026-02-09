# Enhanced SSH Tools Setup

This document outlines the tools and configurations installed to improve your SSH experience on this Ubuntu VPS.

## 1. Session Management (Already Configured)

- **tmux**: Terminal multiplexer for maintaining persistent sessions
  - Start: `tmux new-session -s session_name`
  - List: `tmux list-sessions`
  - Attach: `tmux attach -t session_name`
  - Detach: `Ctrl+b` then `d`

## 2. File Management

- **ranger**: Vim-like file manager
  - Launch: `ranger`
  - Navigation: hjkl keys (vim-style)
  - Quit: `q`
  - More info: `ranger --help`

## 3. Text Editing

- **neovim**: Advanced text editor with IDE-like features
  - Launch: `nvim filename`
  - Configuration includes plugins for better usability
  - Vim-style navigation and commands

## 4. System Monitoring

- **htop**: Interactive process viewer
  - Launch: `htop`
- **btop**: Modern alternative to htop
  - Launch: `btop`
- **glances**: Comprehensive system monitor
  - Launch: `glances`
- **iotop**: I/O monitoring
  - Launch: `sudo iotop`
- **nethogs**: Network bandwidth monitor by process
  - Launch: `sudo nethogs`

## 5. Shell Enhancement Utilities

- **zoxide**: Smart cd command that learns your habits
  - Usage: `z directory_name` (faster than cd)
- **fzf**: Fuzzy finder for files, history, etc.
  - File search: `Ctrl+t`
  - History search: `Ctrl+r`
  - Directory search: `Alt+c`
- **ripgrep (rg)**: Fast search tool
  - Usage: `rg search_term`
- **fd**: Fast alternative to find
  - Usage: `fd pattern`

## 6. Git Enhancement Tools

- **tig**: Text-mode interface for Git
  - Usage: `tig` (shows git log), `tig status` (shows git status)
- **git-delta**: Syntax-highlighting pager for git
  - Automatically configured as git's default pager

## 7. SSH Optimizations

- **Client Configuration** (`~/.ssh/config`):
  - ServerAliveInterval: Keeps connection alive
  - ControlMaster: Enables connection reuse for faster subsequent connections
  - Compression: Reduces bandwidth usage

## 8. Utility Functions

Added to `~/bin/utils.sh` and sourced in `.bashrc`:

- `sysinfo`: Show system information
- `psview`: View processes (uses htop if available)
- `netstat_view`: Show network usage
- `disk_usage`: Show disk usage (uses btop/htop if available)
- `git_status`: Show git status in tig
- `rgf`: Search files with ripgrep
- `exls`: Enhanced ls command
- `tmux_new`: Create new tmux session
- `tmux_list`: List tmux sessions
- `tmux_attach`: Attach to tmux session

## 9. Aliases Added

- `fd`: Alias for `fdfind` (due to package naming)
- `tma`: Alias for `tmux attach -t`
- `tml`: Alias for `tmux list-sessions`
- `rg`: Configured with smart-case matching

## Getting Started

1. Reload your shell configuration:
   ```bash
   source ~/.bashrc
   ```

2. Try out the tools:
   - Use `z` to jump to frequently used directories
   - Use `ranger` for file management
   - Use `nvim` for advanced text editing
   - Use `htop` or `btop` to monitor system resources
   - Use `rg` to search for text in files
   - Use `tig` to browse git repositories
   - Start long-running tasks in `tmux` sessions

## Benefits

- **Reduced disconnections**: SSH keep-alive settings and tmux sessions help maintain your work
- **Faster navigation**: zoxide, fzf, and ripgrep speed up common tasks
- **Better visibility**: Enhanced monitoring tools give insight into system performance
- **Improved productivity**: Vim-style editors and file managers boost efficiency