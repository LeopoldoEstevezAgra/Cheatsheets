# *Tmux cheatsheet*


## Session management

### New session

`tmux new -s {{sessionName}}` : Starts a new session with an specific name

### List sessions

`tmux ls`

### Attach to a session (If named)

`tmux a -t {{sessionName}}`

### Kill session

`tmux kill-session -t {{sessionName}}`: Kills an specific session

## Window management

*Note*: All commands are used with the prefix "ctrl + a " as leading keys

 `c`:  Create window

 `w`:  List windows

 `n`:  Next window

 `p`:  Previous window

 `f`:  Find window

 `,`:  Name window

 `&`:  Kill window

## Panel management

 `-`: Vertical split

 `_`: Horizontal split

 `x`: Kill panel

 `{``}`: Move panels to previous and next position.

 `!`: Move current panel into a new window

## Panel movement

 `directional arrows`: Move to the panel in the given direccion

 `o`: Move to the the next panel ( cycle )

 `q + panel number` : Shows panels numbers and if jump to them if pressed

