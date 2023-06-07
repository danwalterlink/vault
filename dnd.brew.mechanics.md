---
id: 08u3oqk0j5t5boj2iyl4xq4
title: Mechanics
desc: ''
updated: 1686147123696
created: 1684961188700
---

or is inclusive, oor is exclusive, xor is not or
calculations are by default:
  rounded down
  exclusive
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

#### damage
force, physical(b,p,s),
necrotic, radiant
poison, acid
fire, cold, lightning, thunder

counterpunch: range longer: more force
- same type cancel out
- elemental vulnerabilities

#### type additions
##### item
minor, medior, major

###### generic
[spellcharge]({damage.type}) spell does {damage.type} gain charge.
  [discharge]

##### spell level tier
cantrip(0), minor(1,2,3), medior(4,5), major(6,7,8), epic(9)

##### character level tier
(4) 0-2 novice, 3-6 master, 7-11 heroic, 12-16 grand, 17+ epic

alternate ways to unlock epic tier traits: increase an ability score above 20?

# action
## attack
### default critical misses
  messing with resources adds to the messed with resource instead while losing your expended resource.

### roll
extraordinary fumble: min on at least 2 dice on disadvantage or worse: minor and major adverse
fumble: min attack dice size: minor adverse: nick your weapon
miss <=-3 to hit
graze (to hit and up to -2): minimal damage (1)
hit >= to hit
clean >=5 hit
critical >= max attack dice size

## resources
{interface}: "once per {length} rest" is equivalent to 1d2, doubling in size per stacking instance.
any trait that instances usage counts as a resource spent per instance.
resource refers to sources of those instances.
heroic inspiration can be converted into resource dice.
after a resource die is replenished, the source die shrinks a size, or to half it's size if the maximum amount was replenished.
  ie. a d6 resource becomes a d2 becomes 0.
A d0 is equivalent to 0dx.
If a base cost requirement cannot be met, even if another trait allows you to pay alternate costs, you cannot use that trait.
-> maintaining at least 1 resource die becomes very important -> recovery worsens drastically if you expend all of it.
-> damage you receive can be in the form of resources
-> hit dice on equipment becomes an available resource to spend
-> can take reactions only if you haven't expended your reaction.
  using your reaction does not need expend it. It may pose restrictions in the future: ie:
      elven bladesinging armor:
        hardening: as a reaction, you increase your ac by +2. Until the end of your next turn, spells you cast can only be of range:touch or less(self).
        (notice it doesn't say "use").
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
### generic
generics, apply if possible.
[adaptible] change on trigger
  adaptible(SR): change on short rest
[typecast] ability association
[pilfering] assume a type of same class type
[aleatoric] dice shape {amount· size}, effects on combinations
  aleatoric[n][n+1][n+2]: the target becomes poisoned
  aleatoric(max[min]): explode
    (if all dice rolled the minimum number: roll again)
  aleatoric[1,20][1,20]: choose
    (if you roll two of 1 or 20, choose any combination)
  aleatoric(odd[even]): {if odd dice number, for each even dice}:
    half or double
[cunning] change action type {action, bonus action, reaction}
[sly] additional benefit from advantage, hidden: default: activity dice
[precise] expanding ranges
[brutal] additional dice
[core] base feature, generally scaling with class type levels
[paragon] core expansion
[heroic] character level restriction; surge; replaces action surge.
[epic] level restriction; improve heroic actions;
[reactive] use other action types as reaction
[improved] add of type
[greater] additional effects
[deft] improve one type
[conserving] replenishing resources on use
[minor][lesser][greater][grand][epic]: level restriction
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
[recharge](num) regain use on roll num
[discharge](num) up to all and for each (num) stored charges on {trigger}
[echo](spell) choose the order of targets of each echo. create an instance of the spell each target, decrease its level by 1 for each instance.
  If you are concentrating on a spell, make a concentration check.
  You may concentrate on each instance of an echoed spell simultaneously as if spellweaving{x}.
[spellweave] {{magic.concentrate}} if you weave multiple spells, all activity beyond concentrating additionally warrants a concentration check.
[riposte]
[debilitate]: {{attack.sneak}} attack dice for effects # crit => more effects
[imbue]: {{attack.primal}}

[imbue]
## item
### hit dice
along the {{generic object}} table.
object[size[tiny,...,huge], ac[material[paper,11],...,[adamantine,23]],dice.size[d4,...,10], dice.amount[2,...,5], modifier:[craftingQuality, trait[resilient:2,fragile:1/2]]
-> retrieving arrows: arrow[1d4]
using items without tracking individual hit dice:
  map hit dice to chanced traits that are rolled on interaction.
tracking hitpoints per item is tedious,
  simple variant rules:
    post combat: \#rounds = dmg for used weapons
    armor gets damaged when hit

### status conditions
[blunt]: below half maxed half hit dice
  slashing: -1 dmg
  piercing: -1 atk
[sharp]: slashing: within num hit dice from full
  slashing: +1 dmg
  piercing: +1 atk

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
despaired: you become frightened of creatures that attack you. You cannot be inspired.
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
  critical failure/success -/+ 10 of DC
    nat 1/20 decrease/increase result category
  (slight) failure/success: -/+ 4 or less of DC
saving throws
attack rolls

### death saves
DC 10 + Death Save
: stay, until treated in 1 min medical treatment
without medical, during short rest: 1 hit dice = 1 death save
 with prof med kit: 3 death saves = 1 hit dice: you gain half in hp

or through magical means

## action economy
(call/check)
combat:
roll initiative (dex ab check)
round: (3 ticks)
  gain reaction (unless surprised)
  reverse order:
    announce intent (move destination, action)
    3 ticks: (2s/tick)
      1st: turn order: action, move (simultaneuous)
      2nd: ''
      3rd: ''
      : gain resources
-> hybrid d6/d20 system?

turn rate: resource expenditure rate per turn
(default max turn rate:
  1 action -> 4 activity die
  1 bonus action -> 2 activity die
  1 reaction -> 1 activity die per turn
  1 move -> 1 activity die/30ft (1/2 die per 15 ft remaining)
  1 item interaction -> no activity die needed
    : as part of action
    : using item generally uses either action
  speaking does not impede:
  ) -> cast activity type:
    first reaction per turn as an action: 4 activity die
    move out of turn: 5ft = 1 die
usage prorates
whenever you convert activity dice, you either:
at the end of your turn, you convert unexpended resources into activity dice.
can't expend more than double your turn rate?
-> more dextrous and faster characters can take more actions
-> complex actions cost more
-> taking "partial turns"

### action: defer
 use your reaction: you move your turn to after a friendly character.

## activity dice
your activity dice carry over.
you cannot store more than double your turn rate in dice.
your action dice size is equal to your proficiency dice's
-> resource system

## heroic actions
much like legendary creatures have access to additional actions in legendary actions, heroic actions may be taken by creatures if they expend heroic inspiration.
you cannot take heroic actions if you:
- are below 7th level and have used a heroic action this combat.
you may take a heroic action on your as a by spending:
- heroic inspiration
- half your available hit dice, rounded up
- your activity dice maximum
-> heroic inspiration store:
  inspiration:
  increase store: 1, 4, 7; 3 inspiration = 1 heroic inspiration
  heroic: 7, 11, 15; 3 heroic inspiration = 1 epic inspiration
  20: all inspirations = legendary

### heroic: surge
you may take an additional action.
: traits have action dice usage templates/associations
-> tied to proficiency dice size, multiply and/or add with modifiers
-> gain 4 activity dice?

### heroic: resistance
choose a damage type to gain resistance to until the end of your next turn.
heroic: the target of your next attack or spell either gains or loses resistance to the damage type until the end of its turn

### heroic: resilience
either:
- end the incapacitated, stunned or dazed condition, gain 1 activity dice.
- cast half your smallest hit dice size amount of dice in your biggest hit die. Regain that amount of hp.

### heroic: bulwark
- you gain +3 to your AC until the end of your next turn.
heroic: if an attack targeting you misses, you may use your reaction to make an opportunity attack.

### heroic: sentinel
hitting opportunity attacks replenish your reaction until the end of your next turn.
heroic: disengaging enemies still provoke opportunity attacks

minimal ritual:
- dc check to cast, fail to make less effective

![[Martial|dendron://dnd/dnd.brew.martial]]

## trait: luck
if multiple dice in the same roll show the same face, you may add a copy one of these dice to your lucky dice pool.
create your own luck: legerdemain skill contest: you appropriate the dice instead and store it for a rainy day. Swap either the result or size of a dice roll with your stored dice before or after, respectively.

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
you can only ever have 1 heroic inspiration, and gain it by:
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
2,3 5,6,7 9,10,11,13; points cost per spell level
can only convert 1 slot above 6th per spell level per day.

## feat
### featuring
analogous to "ability score increase",
"featuring" allows you to choose a class feature from a class sharing your primary class type and of a level up to that cumulative class type level. traits gained this way have the "feature" type.
-> type restriction from character

## unraveling weave
DC Spell level - closeness to spell: damage type - school
opposed types +5
if you fail the check, chaos bolt at creature within reach.
critical fail: arcane anomaly (DoD:225)
when a spell fizzles after it was cast within your reach, you may use your reaction to cast a spell that takes at most an action. If you cast a spell this way, reduce the needed spell slot by up to half the fizzled spells level.

## counterweave
- disergy
  add spell levels
- synergy
  remove spell levels
enhance next attack

## splitting spells
[spellweave: echo]
for each instance of additional damage a spell would gain, you may instead, either:
- copy the spell an equal number of times. You may choose new targets for the copy.

## [paragon] {spell school} practicioner
(prereq: 5th level spells, paragon of knowledge)
spells known of school/total spell level of 3rd level or higher
- {1}: practicioner: [enhances: arcane recovery] spell point cost decrease for {school} per paragon rank (min 1,3); additional spell points only usable for {school}
- {2}: master: [expert](school) {typecast(divination expert::school)}
- {3}: grandmaster: enhances:[spellweaver] {max slot lvl + mSl/4} majority {spell school}}
  if non-spellschool: every activity: concentration check

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
critical success: additional minor benefits
miraculous success: if you roll more than one dice, and at least two result in critical success, you either gain heroic inspiration or replenish a resource die spent during this action
critical hit: minor benefits, double damage
lethal hit: if you rolled at least two die and at least two would result in a critical hit, your hit is lethal.
  Choose up to the amount of critical hits that would've resulted from casting the die:
  - grow your die one size
  - critical hit
  - replenish expended resource or gain heroic inspiration
  - your hit is brutal

## magic
### magical fatigue
even the most mundane things work their magic. an ancient fireplace might kindle itself. using things infuses them with your being. magical weapons lose their edge when used as paperweights too often.
an arcane focus might alleviate the need of components, but it grows gaunt and its magics shallow if not
### infusions
traits of magical objects are treated as infusions. on use by non-proficient users, magical objects can lose charges or infusions in addition.

## crafting
innate abilities of creatures can be harvested.

## fighting styles
? technician / fighter
  once per turn, if you make an attack, you may make an additional attack.

### great weapon fighting
additional damage dice: heavy weapons as if they had brutal(1)

### defensive
ac: you gain access to the defender's focus:
  stance:
    reposition: safe mvmnt 5ft
    parrying maneuver,
    after successful parry:
      reposition
      riposte
      heighten: reaction proration -2

## weapon attack types
ranged attacks with melee weapons count as ranged weapon attacks for that attacks instance.
A ranged attack with melee weapon generates a ranged weapon attack instance for the purposes of fulfilling restrictions of traits.
(ie. thrown weapons work with feat.sharpshooter.phb.5.0)

## potent cantrip
typecast cleric feature for any mental ability

## lightning reflexes
