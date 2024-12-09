From terminal `tmux <command>`  
From tmux `P + :, <command>`

tmux `<command>` | A
-|-
new -d -s `<session-name>` | + session (-d - do not attach)
kill-session -t `<session-name>` | - session `<session-name>`
ls | list sessions
a -t `<session-name>` | attach to `<session name>` 
new-window -n `<win-name>` -t `<session-name>` `<cmd>` | New window `<win-name>` in session `<session-name>`, command `<cmd>`
split-window -v[-h] [-f] -t `<session-name>` `<cmd>` | Split window vertically [horizontally] [stretch full size] with command `<cmd>`
select-window -t :`<win-name/num>` | Select window
select-pane -t `<num>` | Select pane
set-option -g remain-on-exit on | Global option: remain pane on exit

## Detach clients
`tmux list-clients`  
`tmux detach-client -t <client tty>` 