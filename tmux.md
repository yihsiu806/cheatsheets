# Tmux Cheatsheet

```
<prefix> + ?                  # List shorts
```

## Session
```
tmux                          # Start new session
tmux new -s name              # Start new session with a name
<prefix> + d                  # Detach
tmux ls                       # List all session
tmux attach -t name           # Attach
tmux kill-session -t name     # Kill session
<prefix> + s                  # List all session
<prefix> + $                  # Rename session
<prefix> + (                  # Move to previous session
<prefix> + )                  # Move to next session
<prefix> + $                  # Rename session
```

## Window
```
<prefix> + c                  # New window
<prefix> + n                  # Next window
<prefix> + p                  # Previous window
<prefix> + ,                  # Rename a window
<prefix> + w                  # List all windows
<prefix> + f                  # Find a window
<prefix> + &                  # Kill a window
```

## Pane
```
<prefix> + %                  # Split panes vertically
<prefix> + "                  # Split panes horizontally
<prefix> + arrow              # Switch between panes
<prefix> + ;                  # Toggle last active pane
<prefix> + o                  # Swap panes
<prefix> + {                  # Move pane left
<prefix> + }                  # Move pane right
<prefix> + q                  # Show pane number
<pfreix> + x                  # Kill pane
```

## Reference
https://www.hostinger.com/tutorials/tmux-beginners-guide-and-cheat-sheet/
https://www.shortcutfoo.com/app/dojos/tmux/cheatsheet
https://tmuxcheatsheet.com/