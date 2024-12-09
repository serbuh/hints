
Prefix P = `Ctrl + b` 

C|A
-|-
P + ? | List commands 

### Create / kill
C|A
-|-
:kill-session | - Session
P + c | + window
P + & | - window
P + " | + pane h
P + % | + pane v
P + x | - pane 
Ctrl + d | - pane

### Nav
C|A
-|-
P + <num> | goto window <num>
P + <Arrow> | nav panes
P + n | next window
P + p | prev window
P + f | find window
P + q | List panes (numbers)
P + w | List sessions, windows
P + s | List sessions

### Rename
C|A
-|-
P + , | Rename window
P + $ | Rename session

### Move
C|A
-|-
P + { | Move pane left
P + } | Move pane right
P+: | Move pane to other window
join-pane -t <target-win> | / - /
P + ctrl-<arrow> | Resize
P + z | Zoom/unzoom pane
P + ! | Transform pane to window
P + space | switch layouts
P + ( | prev session
P + ) | next session