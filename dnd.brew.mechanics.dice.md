---
id: 8u96zbrsosp3akd8i5i5wqz
title: Dice
desc: ''
updated: 1691494131310
created: 1685123129692
---

"common" dice:
(d2,) d4, d6, d20
d6/3 rounded up == d2
d6/2ro-1 == +1 avg

## size
d20(10.5)

7d2(10.5)
4d4(10) 5d4(12.5)
3d6(10.5)
2d8(9) 3d8(13.5)
2d10(11)
2d12(13)

## dice mechanics
make the game more "haptic"
-> choice:
  ? take average
  : roll
! averaged dice aren't being rolled.

hoarding physical tokens (dice, etc)
  typed (on tokens)

give your players "tokens" for in-game actions
- proficiency-dice (whenever you apply boni represented by dice, [you may "roll -, [tight]" to add the average, rounded down -, or [loose] to roll the dice and add the value to it.)
- poker-chips for instances of a power
  -> writable/mutable

- cards for special effects
  -> writable/mutable

- make accumulating resources during combat meaningful
-> bursting high-value targets becomes less enticing.
- [plan]: {{action.type:focus:{mental,con}}}; make certain future actions cheaper, by predetermining action;
- "pay" for effects
  - cumulative "world" resources vs party-resource-pool (extended lair)
  -> danger level represented by "world dice".
    ? agent can gain up to opposing danger level amount of action dice per round.
    : action dice decay into chips at the start of ones turn.

  - hit-dice convertible into action dice by max of prof bonus.
  - ability-points/adrenalin (higher-danger situations increase resource generation, multiplicative with threat (acc CR of interacting threats))
    - danger levels
      ( leger
      , tense
      , perilous
      , mortal
      )
    - exhaustion decreases resource generation, in addition to lowering throw-values. (alternate exhaustion rules)

  - action dice (half prof. dice)
    you increase action dice size either by character level, or associating action types with it.
    (place action dice on chips/cards, which may modify dice size)
    for action first, the action dice size category increases by 1 (0 -> d2 -> d4 -> d6,..).
    - power-attack/called attack
      you may cast your action dice when you take the attack action to "power attack":
      \-x to-hit penalty for +2x damage bonus, (these dice count as "thrown" for both attack and damage rolls)
    - an action dice can be spent on any qualifying action.
    - spending action dice prorates the resource usage by 1 dice per type in turn.

  - inspiration
    : additional spendable dice : d4

amount dice
  add
  subtract
  multiply
  floor
  explode additional roll if highest
  implode subtractional roll if lowest

converting dice
} roll more dice!
  dice can be upgraded/upshifted
  d4 == d6-1 (more variance!) || (1d6/2ro-1) + (1d6/3) || 2d6/3ro
  d8 == d6+1 || 1d6 + 1d4/2ro-1 || (d4xd4)/2ro || 4d6/3ro
  d10 == d6+2 || 1d20/2ro
  d12 == d6+3 || (d6xd6)/3ro
  ..
  d6+7 = d20 / 3d6
  reform min/max (d6 : 1,2 = -1; 3,4 = 0; 5,6 = +1)

  /2 ro -> halfed dice (1,1,2,2,3,3)
  /2 rd w/ flop -> d6/2rdf (3,1,1,2,2,3)

d6 avg ranges used to determine partial successes/misses
expending dice

## rolling modifiers
advantage: roll twice, take higher
disadvantage: roll twice, take lower
  stack additively
  4x advantage 1x disadvantage: roll 4 times, pick

choose to roll "straight" modifiers
if a feature has multiple straight modifiers, your choice affects all of them.
(ie. power attack)
