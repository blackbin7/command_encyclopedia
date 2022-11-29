# Command Line Collections
---
## Table of Contents
- [Terminal](#terminal)
  - [Directory operations](#directory-operations)
  - [File operations](#file-operations)
  - [Selection operations](#selection-operations)
  - [Security operations](#security-operations)
  - [Program operations](#program-operations)
  - [Process operations](#process-operations)
  - [Time operations](#time-operations)
  - [Network operations](#network-operations)
  - [Other operations](#other-operations)
- [Markdown](#markdown)
- [Git](#git)



File operations
---------------
'mv' - Move a file or directory
 - 'mv file1 file2' - Rename file1 to file2
 - 'mv file1 file2 file3 dir1' - Move file1, file2, file3 to dir1. If dir1 does not exist, it will be created.

 - For error '-bash: /bin/mv: Argument list too long':
   - use 'xargs' to split the command into smaller chunks:
     - 'find . -name "*.txt" | xargs mv -t dir1'
   - use 'find -exec' to execute the command for each file:
     - 'find . -name "*.txt" -exec mv {} dir1 \;'


Other operations
----------------
'tmux' - A terminal multiplexer. Tmux is the "unbinding" tool for sessions and windows, separating them completely from the terminal. It allows you to create multiple sessions, each with multiple windows, each with multiple panes. It also allows you to detach from a session and reattach later, and even to reattach from a different machine.
 - 'tmux new -s session_name' - Create a new session named session_name
 - 'tmux ls' - List all sessions
 - 'tmux attach -t session_name' - Attach to a session named session_name
 - 'tmux switch -t session_name' - Switch to a session named with specified names
 - 'tmux kill-session -t session_name' - Kill a session named session_name
 - 'tmux detach' - Detach from the current session
 - 'tmux rename-session -t old_name new_name' - Rename a session named old_name to new_name
 - 'tmux new-window -n window_name' - Create a new window named window_name
 - 'tmux rename-window -t old_name new_name' - Rename a window named old_name to new_name
 - 'tmux kill-window -t window_name' - Kill a window named window_name
 - 'tmux split-window -h' - Split the current window horizontally
 - 'tmux split-window -v' - Split the current window vertically
 - 'tmux select-pane -t session_name' - Select the sessions with specified names
 - 'tmux list-keys' - List all key bindings
 - 'tmux list-commands' - List all commands