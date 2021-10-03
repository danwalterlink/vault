---
id: pwyctn6qdw862y56hldqhka
title: Keyboard Shortcuts
desc: ''
updated: 1665736224570
created: 1665736224570
---
## keys
  follows [[ahk syntax|vault://syntax.ahk]]
ctrl
shift
alt = opt
cmd = win

hypr = right {ctrl, opt, cmd}, and/or separate virtual modifier
lock/modal keys

## level hierarchy
os
  app launcher : <\#hypr(key)
    default functions per [[os.function]]

app
  cmd(key)

modal
  subapp
    +#($key)
  function
  meta
    hypr
      .navigation