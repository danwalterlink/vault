---
id: 08u3oqk0j5t5boj2iyl4xq4
title: Mechanics
desc: ''
updated: 1685133453325
created: 1684961188700
---
calculations: averages are rounded down
definitions:
  "per day" is synonymous with "per long rest" since you cannot take multiple long rests within 24 hours.
  effects with the same name don't stack.
  turn rate: per resource per turn

## default critical misses
  messing with resources adds to the messed with resource instead while losing your expended resource.

## resources
{interface}: "once per {length} rest" is equivalent to 1d2 dice, doubling in size per stacking instance.
heroic inspiration can be converted into resource dice.
future resource gains of the same type are cut in dice size until recuperating rest, rounded down.
ie. a d6 resource becomes a d2 resource becomes 1. A feature becomes an illegal action, if you can't pay its base costs, even if a trait allows you to pay alternate costs.
-> maintaining at least 1 resource die becomes very important -> recovery worsens drastically if you expend all of it.
-> damage you receive can be in the form of resources
-> hit dice on equipment becomes an available resource to spend
-> can take reactions only if you haven't expended your reaction.
  using your reaction does not need expend it. It may pose restrictions in the future: ie:
      elven bladesinging armor:
        hardening: as a reaction, you increase your ac by +2. Until the end of your next turn, spells you cast can only be of range:touch or less(self).
        (notice it doesn't say expend).
        rules note: effects of the same name don't stack.

- buy an additional roll with exhaustion
  -> oDnD exhaustion rules
## ability score
### ability score class
physical
  str
  con
  dex
mental
  wis
  int
  cha
(status
  renown
  sanity
### disfigurements
- lose a hand
- lose a foot
- mute
- deaf
- blind

## item hit dice
along the {{generic object}} table.
object[size[tiny,...,huge], ac[material[paper,11],...,[adamantine,23]],dice.size[d4,...,10], dice.amount[2,...,5], modifier:[craftingQuality, trait[resilient:2,fragile:1/2]]
-> retrieving arrows: arrow[1d4]

## status conditions
{{template}}: while {{status.condition}} you experience the following effect:
· {{effect}}: ….
### creatures
bloodied: at or below half hp
healthy: your current hit points are within your biggest maximized hit dice worth of hp from your maximum.
dazed: Can't take bonus actions or use reactions. You cannot concentrate. You can either
  · take an action
  · or move,
  not both.
### objects
damaged: at or below half hp
broken/torn: up to one maximized hit dice away from 0 hp.
shattered/ripped: 0 hp.

## trait doctoring
having traits with the same name in different categories and layering traits/features on top of them could be interesting:
  ie. mage slayer (focus: ); (weapon mastery); (spellcasting specialization)
  (generic improvement):slasher: enhances "mage slayer": a creature hit with the attack while casting or continuing a spell becomes vulnerable to {slashing} damage

## d20 tests
skill checks: modes of success:
  clear failure/success: -/+ 5 or more of DC
  (slight) failure/success: -/+ 4 or less of DC
saving throws
attack rolls

## action dice
your action dice size is equal to your proficiency dice's
-> resource system

## heroic actions
much like legendary creatures have access to additional actions in legendary actions, heroic actions may be taken by creatures if they expend heroic inspiration.
when you take a heroic action, you may

## heroic: action surge
you may spend/do up to double your turn rate, by trading:
- last turn's remaining resource at half the rate
- this turn's remaining resource at rate
- next turn's remaining resource at half the rate
(or unlimited, but usage prorates)
-> convert into action dice(?)
: traits have action dice usage templates/associations
-> tied to proficiency dice size, multiply and/or add with modifiers

action class: (more dex, yields more speed)
  reaction: speed

actions have different additional costs:
ie. spells somatic components require movement speed.
this means that some spells can be cast

minimal ritual:
- dc check to cast, fail to make less effective

## maneuver: power attack
((-1 attack roll := +2 damage)x up to weapon dice size/2)xup to prof mod

## maneuver: precision attack
((-1 attack roll)xweapon dice size/2 := expanded clean hit range // crit range)x up to prof mod

## focus: enhanced attack
concentrate on applying a maneuver to an attack without expending resources. If a feature allows you to expend additional resources, you may apply them at a rate of normal expenditure/prof mod (rounded down)
(this implies that if you lose concentration, you lose the attack advantage. you roll concentration checks as if concentrating on a spell.
similarly, a spellcaster that casts a spell that doesn't ask concentration, while casting, you still roll for concentration checks as if you were concentrating.)

## focus: mage slayer
  if a creature takes a magic action within your reach, you may expend your reaction to make an opportunity attack against that creature.
  the target rolls d20 tests made this way to maintain concentration on casting or continuing spells with disadvantage.

## trait: luck
if multiple dice in the same roll show the same face, you add one of these dice to your dice .
luck to the bold: legerdemain skill contest: you appropriate the dice and store it for a rainy day. Swap either the number or size of a dice roll with your stored dice.

## resources
modifiers can be converted to dice.
dice can be spent as resources to gain more, whenever an associated roll is called:
  attack
  check
  throw

resource changes and allocations add dice
(also, resource expenditure can be indicated by dice size)
-> generation of feature usage makes dice smaller (until size breakpoint)

### heroic inspiration
you can only ever have 1 heroic insiration.
heroic inspiration can replace ability costs paid in dice and is your proficiency dice size.
- you gain heroic inspiration whenever you roll a 20 on a d20 test.

### proficiency
dice size average is your proficiency modifier.
+2 is d4, etc. up to +6 = d12 increased every 4th level past 1st (5th, 9th…)

### spell points
you use spell slots, but can convert between spell slots at spell point rate.
2,3 5,6,7 9,10,11 13; points cost per spell level
can only convert 1 slot above 6th per spell level per day.

## feat: featuring
analogous to "ability score increase",
"featuring" allows you to choose a class feature from a class sharing your primary class type and of a level up to that cumulative class type level. traits gained this way have the "feature" type.

## modes of success
4 stage:
  clear/clean fail/success : by 5 or more
  fail/success
  also applies to hits: clean hit:
    clean hit: one additional hit dice, slight chance of resource replenishment
    sloppy? failure: minor mishap

3 stage: from binary
  dc ± 2:
  -> generally: spells that have binary outcome have a 3rd option, with either advantage or disadvantage for slight fail/success
  (flavoured: "catching failed attempts": try again with disadvantage by slight misses)

## criticals
1: roll on the associated minor mishap table
double 1 on disadvantage: major mishap table
critical success (if roll additional dice, resource replenish if rolled nice)

## magic
### magical fatigue
even the most mundane things work their magic. an ancient fireplace might kindle itself. using things infuses them with your being. magical weapons lose their edge when used as paperweights too often.
an arcane focus might alleviate the need of components, but it grows gaunt and its magics shallow if not
### infusions
traits of magical objects are treated as infusions. on use by non-proficient users, magical objects can lose charges or infusions in addition.

## grievous wounds
on receiving lethal strikes, you have a chance to sustain a grievous wound.
## crafting
