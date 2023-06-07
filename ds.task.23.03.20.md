---
id: ggsqotpj47qgv6pxv5m1x7i
title: durchstart
desc: ''
updated: 1679917039464
created: 1679305280166
status: ''
due: ''
priority: ''
owner: ''
TODO: durchstart
---

- [w] fixing escape sequences
  + [ ] git pulling upsream dotfile repos
    tmux.conf > .dotfiles/.tmux/.tmux.conf
    tmux.conf.local > yask
    - [ ] cherry pick commit/stash between branches
    - [ ] subproject in branch as submodule forked from off-project upstream
      submod points to correct branches
      -> git alias : from pull => (ownRemote --rebase --onto upstream.pull)
  ! git branch --remote : not indicating that branch tmux HEAD points to ddubl/tmux
  -> not possible in merge-redirects. : overwriting default function behaviour yields desired results
    - [ ] [[workflow.git]]
  - [ ] default commit message on dendron:
    changing dendron scripts : add '!squash' to non-tagged, non-flagged commits (ie. lifecycle commits)
      if flagged/tagged : add flag/tag to :intent
        add all files/links/resources added to task-graph
