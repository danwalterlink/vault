---
id: 5yhhcnht60pe79ozroen255
title: Bladesinger
desc: ''
updated: 1706718339766
created: 1686215581531
---

core: wi6:bsg
0: readiedAction: spirit shroud
1: b: bladesong, a: magic, r:, \c
2: def variant a: (attack, magic:bladeWard), b:, r:, \c
2: off

build options
enhancements:
- armor of agathys (arcane spell in UA)
or: Magic Initiate(Warlock)

race ? [elf:elven accuracy]
  elf:
    shadar-kai($src:MPMM) |- innate misty-step, trance:proficiency
    grugach:($src:UAESR) |- druidic cantrip
    kaladesh.vahadar($src:PSK)
  elf.half(any)

bkd:
  astral drifter: magic initiate(cleric): guidance(UA), resistance(UA), healing word

b1:
race: shadar-kai(mpmm) (+2 dex, +1 int)
bkd: astral drifter
as: pb33: int:17, dex: 17, con: 13, wis: 10

feat:
  4: elven accuracy(dex) (dex: 20)
  8: resilient[con] (con: 14)
  12: war caster UA:(int) (int: 19)
  16: observant UA:(int) (int: 20)
  19: ASI(+2 con) | metamagic adept

feat: if no UA war caster (race:(+2 int, +1 dex))
  4: elven accuracy(int) (int=20)
  8: resilient[con] (con: 14)
  12: war caster
  16: ASI(+2 dex)
  19: metamagic adept

variation
  artificer 3
  blood hunter 3
    mutant
    profane soul

### racial options
pass without trace

spirit guardians
  background: lorehold, orzov

goodberry
aid
  halfling: mark of hospitality

armor of agathys
  dwarf: mark of warding

healing word
aura of vitality
lesser restoration
  halfling: mark of healing