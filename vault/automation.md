---
id: h4ilxta0jr3b0h7x5d82935
title: Automation
desc: ''
updated: 1681390171918
created: 1637080824781
---

timers/reminders

-> UI of $interface.active || $lighting.active

#do
## macos
iterm2 triggers for workspaces
themeing/color automation
-> export to variable via pythonAPI

#backup -> #dotfiles
iterm2
  { settings
  , snippets
  , profiles
  , colorKeys?
  }

## ios shortcut templates
#deps scriptable
, charty

modeled after ramda library and focussed around composition
  -> composable state-machine
- compose
  autocurried, variadic
- lens
    peer into structure, return structured ref
    struct ->
  find
