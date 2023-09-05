---
id: vmhkkhezarm8t02cfe845k9
title: Types
desc: ''
updated: 1685986886867
created: 1685970682181
---

entity
  type
  condition

  character
    type: [caster,martial,crucible]
    ancestry
    background
    class
      type: [base, ]
      cast
        ? [warrior, expert, priest, mage, witcher]
          variant:
    ability
      score
        modifier

  object
    item

caster
  trait: spellcasting

feature
  ability
    spellcasting
    prowess

trait
  <intransitive,incommutative,associative>
  static|variable
    static: trigger only on acquisition
    variable: choice on trigger
  meta # applies to next trait
  generic # unselected sub-types

condition