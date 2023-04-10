---
id: k50hz0cyu9tnfyudi6ibv5y
title: Tmux
desc: ''
updated: 1680608576560
created: 1636903106989
---

#? quickswap current pane/window to pane/window
-> :swapp -s -t
#? current tmux does not allow nesting panes in windows?

tmux settings:
define leader as $cmd

#todo <C-a ?> display cmds correctly

#todo integrations
+ term, $os.mac: iterm
  - themeing: semantic, dynamic
+ emacs
+ vim
+ tmux
-> navigation

:understanding pane/window/tab nesting in iterm
-> add attach sth to pane/window
-> breaking pane -> window as inverse 'breaking up the tree' of window -> pane

[] themeing
- default themeing uses ANSI-Colors from iterm2
## theme
~/.tmux.conf

#todo fix status line
- [ ] #fix emacs doom config
- [ ] #fix theme #extend

send to all panes #i
  Ctrl-b :setw synchronize-panes on
    cmd
    sync-panes off
