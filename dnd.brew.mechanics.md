---
id: 08u3oqk0j5t5boj2iyl4xq4
title: Mechanics
desc: ''
updated: 1685377748772
created: 1684961188700
---

calculations: averages are rounded down
definitions:
  "per day" is synonymous with "per long rest" since you cannot take multiple long rests within 24 hours.
  effects with the same name don't stack.
  turn rate: per resource per turn
  dice sizes are:
    d{2,4,6,8,10,12,20}
  swap dice according to:
  - 1d20 = 3d6
  - 3d6 = 7d2
  if you convert dice sizes pick the closest amount resulting in the same average

## categories
### type
types are additive, category-specific (non-commutative) and transitive.

#### type additions
##### item
minor, medior, major

##### spell level tier
cantrip(0), minor(1,2,3), medior(4,5), major(6,7,8), epic(9)

##### character level tier
(4) 0-2 novice, 3-6 master, 7-11 heroic, 12-16 grand, 17+ epic

alternate ways to unlock epic tier traits: increase an ability score above 20?

## default critical misses
  messing with resources adds to the messed with resource instead while losing your expended resource.

## resources
{interface}: "once per {length} rest" is equivalent to 1d2, doubling in size per stacking instance.
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

- buy a reroll with exhaustion
  -> oDnD exhaustion rules

### activity dice
translate fixed action economy into activity dice
[typed] - attack, move, magic {
- activity dice size = proficiency dice size -> conversions become more expensive in general, if you level up.
  spending activity dice allows you to exceed your action limit, not vice versa.
- whenever you expend resources, you can spend up to the amount stated.
- typed dice other than movement expire at the end of your round
expired dice appreciate, convert into activity dice and return to your activity dice pool
-> follow proration rules. leftovers fuse into dice( 3 depreciated d2s becomes 1s, add to d3 and round down to d2).
-> converting multiple instances of typed dice is very inefficient
-> spending slightly less can accrue significant mid-term value
(splitting dice, rogue: moving to 3d6, can expend)
receiving activity dice:
  interacting with objects uses movement (or magic dice)
  interacting with creatures uses attack dice}
- 1 action = 1 dice
- bonus action = 1/2 dice
- reaction = 1/2 dice
- base mvmt = 1 dice
(linear addition of resource accruement)
spending dice: (initial, prorate, max)
    grants additional effects?
    -> swifter attacks become less accurate
  action: (1, +2, 5)
  [cost modifiers]
  bonus: (1, +1, 2)
  reaction: (1, +1, 0) proration decreases for each turn you haven't used one
  -> reactions become cheaper when certain enemies are around
  concentrating: +.5
  -> war caster: letting you cast spells as reaction is way cheaper
  mvmt speed: 1 dice (doubling speed halves cost)
-> equivalent to halving movement speed = double dice cost
prorate:
  features like extra attack adapt to:
    - attack actions have lower initial proration.
    - attack actions cost less (minimal scaling)
    (2 attacks halves the cost, )
  some actions can have hybrid costs
  i.e. it's beneficial for users of costly actions, such as magic to be as stationary as possible.
total level class -> variant scaling: some
ways of gaining additional attacks:
  extra attack
  2 weapon
  + action surge

action class: (more dex, yields more speed)
  reaction: speed

actions have different additional costs:
ie. spells somatic components require movement speed.
this means that some spells can be cast

## ability score
### ability score type
#### physical
  str
  con
  dex

#### mental
  wis
  int
  cha

#### status
  renown
### disfigurements
- lose a hand
- lose a foot
- mute
- deaf
- blind

## trait
### metatrait
generics, apply if possible.
[core]
[adaptible] change type on trigger
[typecast] ability score association
[pilfering] assume type previous action
[aleatoric] dice shape {amount· size}, effects on combinations
[cunning] change action type {action, bonus action, reaction}
[precise] expanding beneficial ranges
[brutal] additional dice
[paragon] improve core
[heroic] surge; replaces action surge.
[epic] improve heroic actions;
[reactive] expend reaction for benefit, convert into reaction
[improved] add of type
[greater] additional effects
[deft] improve one type
[conserving] retains type
[common][lesser][greater][grand][epic] additional use
[canny] expertise
[adaptive] (re)selection
  - contextual:
    ie. hunter: horde breaker / colossus slayer
    -> species specialist?
    : intuition/wit: learn on the fly. -> [deferred]
    : leveling decision fixed :-> resets on long rest. [hesitant]
    : some choice made permanent on repeated choice without [honed]
    : honed abilities can be extended.
    -> size
    making similar distinction in martial classes that exists in casters:
      prepared/learned casters
ie. barbarians(12) get brutal(1) on 9, brutal(2) on 13 and brutal(3) on 17

## item hit dice
along the {{generic object}} table.
object[size[tiny,...,huge], ac[material[paper,11],...,[adamantine,23]],dice.size[d4,...,10], dice.amount[2,...,5], modifier:[craftingQuality, trait[resilient:2,fragile:1/2]]
-> retrieving arrows: arrow[1d4]
using items without tracking individual hit dice:
  map hit dice to chanced traits that are rolled on interaction.

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
#### grievous wounds
on receiving lethal strikes, you have a chance to sustain a grievous wound.
### objects
damaged: at or below half hp
broken/torn: up to one maximized hit dice away from 0 hp.
shattered/ripped: 0 hp.

## trait doctoring
having traits with the same name in different categories and layering traits/features on top of them could be interesting:
  ie. mage slayer (focus: ); (weapon mastery); (spellcasting specialization)
  (generic improvement):slasher: enhances "mage slayer": a creature hit with the attack while casting or continuing a spell becomes vulnerable to {slashing} damage
#i -> replace typed concept with another concept of that type (not commutative!)

## d20 tests
skill checks: modes of success:
  clear failure/success: -/+ 5 or more of DC
  (slight) failure/success: -/+ 4 or less of DC
saving throws
attack rolls

## action economy
generic increases
-> hybrid d6/d20 system
turn rate: resource expenditure rate per turn
conversions prorate. whenever you convert activity dice, you either:
- remove one
- shrink dice size

## activity dice
your activity dice carry over.
you cannot store more than double your turn rate in dice
your action dice size is equal to your proficiency dice's
-> resource system

## heroic actions
much like legendary creatures have access to additional actions in legendary actions, heroic actions may be taken by creatures if they expend heroic inspiration.
you may take a heroic action on your as a by spending:
- heroic inspiration
- half your available hit dice, rounded up
- your activity dice maximum
you cannot take heroic actions if you
- cannot gain heroic inspiration
- if you are incapacitated
### heroic: surge
you may take an additional action.
: traits have action dice usage templates/associations
-> tied to proficiency dice size, multiply and/or add with modifiers

minimal ritual:
- dc check to cast, fail to make less effective

![[Martial|dendron://dnd/dnd.brew.martial]]
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

[mystical] alternate casting cost of differing type

### heroic inspiration
you can only ever have 1 heroic insiration, and gain it by:
- at least two dice rolls would have resulted in successes on contested d20 tests with disadvantage or worse, or if additonally one of those hits resulted in a critical hit for rolls made with advantage or better.
- rare demonstrations of cunning and character, occasionally.
you can spend heroic inspiration to:
- replace costs paid in dice. Your heroic inspiration dice is the same size as the cost it replaced, or your proficiency dice in size, whichever results in lesser effects.
- roll an additional dice for a d20 test, pick one to discard.

### proficiency
dice size average equals your proficiency modifier.
+2 is d4, etc. up to +6 = d12 increased every 4th level past 1st (5th, 9th…)

### spell points
you use spell slots, but can convert between spell slots at spell point rate.
2,3 5,6,7 9,10,11 13; points cost per spell level
can only convert 1 slot above 6th per spell level per day.

## epic feat: {spell school} master
(prereq: 5th level spells)
spells known of school/total spell level of 3rd level or higher
- {1}: master: conversion rebate to locked slots.
- {2}: grandmaster: diviner-like refueling
- {3}: legend: spellweaving {max slot lvl + mSl/4}

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

## crafting
innate abilities of creatures can be harvested.

## fighting styles
### great weapon fighting
additional damage dice: heavy weapons as if they had brutal(1)

### defensive
ac: +1, you gain access to the parrying stance