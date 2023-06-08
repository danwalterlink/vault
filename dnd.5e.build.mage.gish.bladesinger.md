---
id: 85f08d5bq5xuis18o944liz
title: Bladesinger
desc: ''
updated: 1686260777060
created: 1686215581531
---

core: wi6:bsg
0: readiedAction: spirit shroud

1: b: bladesong, a: magic, r:, \c
2: def variant a: (attack, magic:bladeWard), b:, r:, \c
2: off

build options:
race ? [elf:elven accuracy]
  elf:
    shadar-kai($src:MPMM) |- innate misty-step, trance:proficiency
    grugach:($src:UAESR) |- druidic cantrip
    kaladesh.vahadar($src:PSK)
  elf.half(any)
