C|A
-|-
:w !sudo tee % | override readonly
:E | Open file explorer
`:!<cmd>` | run command in console
ctrl + Z, `<cmd>`, fg | run command in console

## Motions
C|A
-|-
w | word next
b | word prev
e | word end
O | line start
$ | line end
gg | file start
G | file end
`<num>`G | goto line
:`<num>` | goto line
ctrl+o | Back
ctrl+i | Forward
ctrl+G | print current line
% | goto matching parentheses ([{ }])

## Inserts
C|A
-|-
i | insert before cursor
A | insert after the line
o | insert line after
O | insert line before
cw | change word
C | change rest of line
D | delete rest of line
Shift+A | insert at the end of line

## Edit
C|A
-|-
ZZ | save and exit
u | undo
ctrl + r | redo
dG | Delete untill the end of the file

## Search
C|A
-|-
/ | start search 
n | next 
N | prev 
:%s/}/}\r/g | Add newline after "}" 

## Macros
C|A
-|-
q1 | start req to "1"
… q | stop req
10@1 | do ten times macros "1"