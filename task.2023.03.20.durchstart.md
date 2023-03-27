---
id: igb3j8okbzz78mqo62d6n06
title: durchstart
desc: ''
updated: 1679908493514
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
  - [ ] default commit message on dendron: