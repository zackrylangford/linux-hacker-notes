# Linux Commands

This section provides reference information for common Linux commands.

## Command Categories

- [**File Management**](file-management.md): Working with files and directories
- [**System Information**](system-info.md): Getting information about your system
- [**Networking**](networking.md): Network-related commands
- [**Text Processing**](text-processing.md): Manipulating text files

## Essential Commands

| Command | Description | Example |
|---------|-------------|---------|
| `ls` | List directory contents | `ls -la` |
| `cd` | Change directory | `cd /etc` |
| `pwd` | Print working directory | `pwd` |
| `cp` | Copy files or directories | `cp file.txt backup/` |
| `mv` | Move/rename files or directories | `mv old.txt new.txt` |
| `rm` | Remove files or directories | `rm -rf directory/` |
| `mkdir` | Create directories | `mkdir -p new/sub/dir` |
| `grep` | Search text using patterns | `grep "error" log.txt` |
| `find` | Search for files | `find / -name "*.conf"` |
| `chmod` | Change file permissions | `chmod +x script.sh` |
| `chown` | Change file owner | `chown user:group file.txt` |
| `ps` | Show process status | `ps aux` |
| `kill` | Terminate processes | `kill -9 1234` |
| `df` | Show disk space usage | `df -h` |
| `du` | Show directory space usage | `du -sh *` |
| `top` | Display running processes | `top` |
| `man` | Show manual pages | `man ls` |

## Command Structure

Most Linux commands follow this basic structure:

```
command [options] arguments
```

- **Command**: The program name (e.g., `ls`, `cp`)
- **Options**: Modify the command's behavior (e.g., `-l`, `--all`)
- **Arguments**: What the command acts upon (e.g., filenames, directories)

## Getting Help

There are several ways to get help with commands:

```bash
# View the manual page
man command_name

# Get brief help
command_name --help

# Get information about a command
info command_name

# Show a brief description
whatis command_name
```

## Command History

```bash
# Show command history
history

# Run previous command
!!

# Run command number 42 from history
!42

# Search command history
Ctrl+R
```

## Command Shortcuts

| Shortcut | Description |
|----------|-------------|
| `Tab` | Auto-complete commands and filenames |
| `Ctrl+C` | Interrupt (kill) the current process |
| `Ctrl+Z` | Suspend the current process |
| `Ctrl+D` | Exit the current shell |
| `Ctrl+L` | Clear the screen |
| `Ctrl+A` | Move cursor to beginning of line |
| `Ctrl+E` | Move cursor to end of line |
| `Ctrl+U` | Cut text from cursor to beginning of line |
| `Ctrl+K` | Cut text from cursor to end of line |
| `Ctrl+W` | Cut the word before the cursor |
| `Ctrl+Y` | Paste text that was cut |