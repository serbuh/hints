C|A
-|-
`~/.tmux.conf` | Tmux config file
`tmux source-file ~/.tmux.conf` | Apply config
`:source-file ~/.tmux.conf` | Apply config 

Example config file: 
```
set -sg escape-time 0
set -g base-index 1
```
 
Add lines in file, or print that starting with `:` 
C|A
-|-
set -sg escape-time 0 | Disable "Esc" delay
set -g mouse on | Enable mouse (for resizes, highlights)
set -g history-limit 1000000 | Increase history size (from 2,000)
set -g base-index 1 | Start indexing windows from 1 instead of 0
set -g renumber-windows on | Renumber all windows when any window is closed

### Rebind prefix
```
unbind C-b
set -g prefix C-Space 
bind C-Space send-prefix 
```