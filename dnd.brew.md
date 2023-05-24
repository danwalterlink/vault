---
id: v6f9mvtfgh7cwyywakv89sz
title: dnd-6
desc: ''
updated: 1684919834738
created: 1684357294795
---
I believe it possible to build a "dnd 6" while being backwards compatible (even further back than 5th edition)
dnd brew -> yaml formatting
todo: integrate 5etools - mpmb
- rewrite current spells/features
- yml interchange format

general
tie regenerative capabilities to resources -> action surge regeneration to hit die / or other resources.
- give panic-options that are expensive. get cheaper during rests. -> active rests

character creation:
ABC: Ancestry, Background, Class
-> if more than one source grants you ability increases as base feature, pick one or bolster to +3 (+2 to one, +1 to another), unless a single source grants more, in which case you are allowed to choose the option granted.
action surge type restrictions?
-> cost backloading. action surge - attempt thing and then pay resources.

sharpshooter
you ignore half and 3/4 cover up to your prof mod amount of times.

healing:
: receiving over your biggest hit dice worth of hp in healing:
  - makes you hungry;
  - while hungry makes you starving.
  - while starved depletes hit dice a number of hit dice could have rolled (rounded up).
  - while starved and without adequate hit dice additionally gives you one level of exhaustion.

maneuvers for martials

weapon masteries, tool and crafting more important.
- exploits and boni tied to specific weapon family.

complexity creep
there's cost to smaller chunks. -> paper; more choices and prone to "bookkeeping"
more granular, pregens. classes work more like pregens, because I can essentially build classes and their amalgamations from these chunks.
[[residual ancestry]], [[trait doctoring]] and [[typecasting]] inverts and restricts this bottom up, extremely granular approach to retrofit the class structure presented in previous dnd editions.

degrees of success:
combat: critical failure/success
  slight failure: slight chance of minor weapon damage (knick, bend or tear),
  failure: failed by 5 or more: automatic minor weapon damage, slight chance of major weapon damage (rendering unusable or less effective). Can use reaction to mitigate.
  critical failure: automatic major weapon damage. Can use reaction to mitigate.

### feats
shared mind:
(becomes highly abusable with: one-sided telepathy block, sleeping potions or as torture)
arcane etchings back of head, willing participants rest back to back for one minute to implant their mind into the one not concentrating.
moving more than 30 ft apart from one another without other means of telepathy ends the bond.
unconscious or charmed creatures are considered willing.
  - without concentrating, either party hears the others thoughts as if they were their own
  - as an action, you can assume control of a willing party
  - either party makes concentration checks with disadvantage
  - either party takes psychic damage if any party takes psychic damage not received via this trait
  - you cannot rest

shield master
  {++}
  you can don a shield as your free item interaction.
  you may use armor class calculations that forbid using a shield with shields.
  shield bash: advantage on shove action
arcane notes
  if you discerned the makeup of an arcane spell, you may use generic spell components and magical ink to scribe the spell into your spellbook.
  there is a chance at least parts of the spell have escaped your scrutiny or intricacies have eluded your mind.
  For each 3 points you have missed the DC (10 + double the spells level) of the target spell
poisoner
- 1 dose = coating amount on dagger or 3 pieces of ammunition for it to show effects
- heavy dose = not deliverable via coating. consumes double the amount of poison and requires a special container
- craft 1 heavy dose by distilling 2 normal ones
- ignore resistance
- half damage as acid damage if immune

Potions
: healing potions restore health according to : minor healing potion (2d4 + constitution modifier) ||
: HoT: when you roll for healing of a potion and roll beneath half max, you heal for 1/2 max.
  anything over 1/2 is restored over time at (1/2 number of dice) hp/round.
(the following makes frequent cooking and/or magical food a necessity for adventurers)

Prestige Classes: when meeting criteria, your most advanced class becomes the base class for the prestige class. Future class advancements may not invalidate past choices.
  bonus features will unlock when cumulative class type levels reach thresholds.
  Advance in 2 Classes simultaneously up to a maximum.
  Mystic Theurge: 3+ Caster / 3+ Priest or higher, but still balanced levels. (eg. 2-Cleric, 2 Paladin, 3 Wizard), Max Level = Level of Base Class
    6/6/6

Partial class progression:
  pick features from a class belonging to the same type of the advancing class. The chosen class feature must be of a level less than half your total class type level.

Typecast:
  Class: Subclasses may alter class type.
  Ability association: when typecasting a feature, it, and all subfeatures thus gained, change their associated ability to another.
  #i features become less effective, the more centralized it becomes.
  -> uses of typecasting are inversely tied to diversity of ability scores.

Cumulative Subclasses:
  - Scaling features and sidegrades
  - typeclass scaling and incentives to return to classes

## feats
  enable power-fantasy of gwm-pom||shs-cbe, by enabling the core fantasy in more ways.
  -> generic power attack:
    gambling: scale: (-1 attack roll -> +2 dmg roll)xmaxPmod, 2->3, 3-4 (choose either attack or dmg mod, other gets calcd: rounded up.), can only go up in a turn.
  -> allow dynamic resource allocation
class passives:
  maneuvers for martial classes
  steal from ygp.
    overhaul:
      ranger
        lean into different playstyles
      barbarian
        pro/con rage, reckless attack
  figher: bake fighter/battlemaster into base class
  warlock: bake hexblade-features into base-class

smaller blocks with baked-in choice, backed by resource-interchange and interaction system.
-> small changes have potentially far-reaching effects.
along general type system, classes fulfill a more 'templative' role
warrior/expert(martial/expert);priest(divine/primal);caster(arcane/psionic);occult(pact/crucible)
  martial: monk? -> fighter/warrior
  expert: rogue/(alchemist)
  divine: cleric
  primal: druid
  arcane: wizard
  psionic: mystic
  pact: warlock
  crucible: witcher/blood hunter
  -- warrior
    + warrior: monk
  martial/expert: fighter -> battlemaster
  martial/primal: barbarian
  martial/divine: paladin
  martial/arcane: bladesinger/rune knight
  martial/psionic: psion/psi-warrior
  martial/pact: hexblade/eldritch knight/oath of vengeance
  martial/crucible: crucible knight
  --
  expert/expert: bard/rogue
  expert/martial: rogue/fighter
  expert/divine: thaumaturge??
  expert/primal: ranger
  expert/arcane: artificer/arcane trickster
  expert/psionic: soul knife
  expert/pact: ??
  expert/crucible: blood hunter(mutant)
  -- divine
  + divine : cleric
  + martial : war domain/forge domain
  + expert : trickery domain
  + primal : tempest domain
  + arcane : arcana domain
  + psi : ?
  + pact : twilight/death?
  + crucible : godeater
  -- primal
  + arcane
  -- arcane
  -- psi
  -- pact
  -- crucible