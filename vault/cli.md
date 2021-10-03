---
id: txvyj875kh39rbr4bmcaf3r
title: CLI
desc: ''
updated: 1678360925213
created: 1636904252349
---
as a rule, keep defaults unless very necessary
eg. tmux default prefix

#feature normal-mode history navigation -> fzf popup

# themeing
follow system theme
make current state clear
  un/focus

# navigation
cli-encompassing leader-navigation
  vi-mode normal : space = leader
  -> vi-style tmux/tab navigation

## vim mode
tmux
  window
  tab
  pane
vim
  split
  tab
  buffer
emacs

# discovery
navigate/find commands bash/zsh
- apropos

# pager
- less/more
make separators newlines etc?

tr: translate char
pr: print
(g)awk

# upgrades
[n] ls : lsd

# escape sequences
2>&1

OSC, OSI, ESI, \e#######, ESC]]I, onFocus: windowFocusReporting: ]]ESC #?

[] vim-mode escaping, hyper-keys

VT100 xterm control sequence
  CSI PS SC q

# modal cli
## vi tmux
https://superuser.com/questions/685005/tmux-in-zsh-with-vi-mode-toggle-cursor-shape-between-normal-and-insert-mode
zsh-vi-mode omz plugin
tmux integration

#issue
tmux not displaying vi-mode cursor shapes
#resolved by --HEAD updating zsh-vi-mode omz plugin

#feature modal tmux
#feature per pane history
#f tmux : currently busy panes/windows | iterm integration: finished output
