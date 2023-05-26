---
id: v6f9mvtfgh7cwyywakv89sz
title: dnd-6
desc: ''
updated: 1685128197278
created: 1684357294795
---
## foreword
Options are fun. Being able to make meaningful choices between options is powerful.
While many proposed changes and additional options blow the door open to ultimate power creep, they are intended as radical empowerment to mechanically underline gameplay choices.

Interface, Implement, Interplay

I believe it possible to build "dnd 6" while backwards compatible (even further back than 5th edition), through "ports"
ports are interfaces (in essence) that translate rules verbiage from one edition to another.
within these ports, design decision will need to be made. This will boil down to having different versions for implementations, which will only really be an issue, if they're obtuse and hard to extract/change.
this issue already present's itself in current (5th) edition of dnd, where text in publications doesn't lockstep with similar features introduced in later publications, ie. double skill proficiency to expertise.
It is quite obvious that in earlier publications, expertise was privy to certain classes only. Later feats have adopted the expertise phrasing but earlier features didn't receive errata.
-> make abundantly clear, which version something is from and is trying to sync with.
-> if you want to play with "the good ol\' sharpshooter", you play < 5.2 (which would be XGE).
-> 5.5 (what is now the dndOne approach, ironing out kinks)
-> 6 : more fundamental changes that make "ports" more necessary : ie. moving from the "class" model to the "pregen" model and having radically smaller chunks with fewer restrictions between them, making choosing the real restriction.

## design maxims in contrast and reaction to 5e
iterative, generative and clear versioning/templating including errata ![[Tooling|dendron://dnd/dnd.brew.tooling]]
  -> not "stranding" old material

strengthen overarching idea that the world is inherently magical. Even the most mundane thing works magic. Doing something repeatly steeps the location in this ritual. Fireplaces grow closer to the elemental flame by each kindling; ancient fireplaces might even spark themselves through sheer habit.
certain tankards fit snugly in dwarven hands while feeling off to a human with the same prints.


- powers for drawbacks
- focus on meaningful differentiation, packaging in distinct classes; power level is secondary.

generally, roll for upsides:
  for permanent rolls: anything below average gets rounded to dice average (rounded down).
flexible resource interchange system
- half of unused resources from last turn, pay in current turn or restrict your next turn: up to double your turn maximum.
- movement for reactions

tie regenerative capabilities to resources -> action surge regeneration to hit die / or other resources.
- give panic-options that are expensive. get cheaper during rests. -> active rests
- have other ways of regenerating resources other than cooldowns
- certain interactions diminish resource availability

(take a breather, short rest, long rest, recuperation)
taking a breather uses available minor consumables to
less punishing initial exhaustion effects.
-> recovering from exhaustion reduces your total hit dice
- long rests without available hit dice only recovers a single hit dice instead of any other benefits.
- long rests with your current maximum hit dice are recuperative.
- a recuperative rest restores your hit dice maximum

complexity creep
there's cost to smaller chunks. -> paper; more choices and prone to "bookkeeping"
more granular, pregens. classes work more like pregens, because I can essentially build classes and their amalgamations from these chunks.
[[residual ancestry]], [[trait doctoring]] and [[typecasting]] inverts and restricts this bottom up, extremely granular approach to retrofit the class structure presented in previous dnd editions.

## character creation
new standard array (17, 15, 13, 12, 10, 8) or by using the resulting point-buy total (33).
ABC: Ancestry, Background, Class
+2 to any Ability Score. Ability Scores listed in the Ancestry description denote the most common association. This ability score modification is associated with your ancestry. Choose up to one different source granting ability score increases. You may increase an Ability Score that this source could increase by up to 1.
You may choose another source granting ability scores to apply instead.
If the total cumulative amount of ASI no more than 3, you may take a feat.
### Ancestry
- culural/heritage, vestigial, partial, mixed and transformation trait templates
  + cultural: traits are available to individuals growing up in a community centered around {{ancestry}}
  + vestigial: features from distant ancestry that atrophied to (near) disfunction (ie. vestigial wings that allow you to hover/fall gracefully, essentially)
  + partial: only some features of this trait are available. If there are multiple options, choose one. You choose for every instance.
  + mixed: pick any trait from ancestry. You may acquire up to two features via this trait.
  + transformation: Traits gained overwrite base ancestry.
  modifications targeting traits do so for one instance of your choice.
amalgam ancestry:
  pick up to 4 races as your closest ancestors, 2 of which may be considered your race. Choose up to one trait from among your closest ancestors per ancestral trait category to inherit.
  you may additionally choose to:
    - gain darkvision up to 60ft
    - gain a feat, eldritch invocation or innate infusion. You may change that choice whenever you gain a feat.
    - change your size by one category up to huge or down to small
    - gain + 1 in an ability score of your choice
    - choose a cantrip to gain at 1st level, and a spell of 1st and 2nd level to gain at 3rd and 5th level respectively as innate Spells known #dnd.templating . Choose a mental Ability Score as Spellcasting Ability Score associated with those spells. You may cast each of those Spells once per Long Rest without expending non-consumed Material Components or Spell Slots. You also know those Spells if you have a spellcasting trait.
    - gain resistance to a damage type of your choice.
    your total ability score increase gained this way is limited to 2.
    for each choice beyond the first, you:
    - subtract 1 from an AS of your choice
    (- gain up to one disfigurement/disability.)

### Background
  - basic: 2 skills, 1 tool(choice)
  - some gain other benefits instead
engaged backgrounds: mali for boni (usual feat choices)
additionally, you may choose to affiliate with an order, association, guild or other faction.

### Class
autodidact: meta-class; what amalgam ancestry is for ancestry; autodidact is for classes.
pick:

you are considered lvl0 for all (base) classes you haven't picked a level in
if something refers to class, it refers (its) base class unless noted otherwise.

fighter: bake fighter/battlemaster into base class #changes.5e
warlock: bake hexblade-features into base-class #changes.5e

## class types
smaller blocks with baked-in choice, backed by resource-interchange and interaction system.
-> small changes have potentially far-reaching effects.
along general type system, classes fulfill a more 'templative' role
warrior/expert(martial/expert);priest(divine/primal);caster(arcane/psionic);occult(pact/crucible)
  warrior: monk? -> fighter/warrior
  expert: rogue/(alchemist)
  divine: cleric
  primal: druid
  arcane: wizard
  psionic: mystic
  pact: warlock
  crucible: witcher/blood hunter
-> crucial distinction: no-spell-progression, half-spell-progression, full-spell-progression

##### caster
cast/concentrate/practice
  wizard: scribe/memorize/alter spell
    - scribe anything, artificing
  sorcerer: intuitive alter spell -> metamagic
    - multi-casting, volatile/wild spells
  warlock: make their patron's magic their own. #f? -> priest?
    - living spell, granting pacts

##### warrior
maneuver/focus/drill
- fighter: allrounder/technician
  + fighter:battlemaster:: all maneuvers/exploits
- rogue: dexterity
- barbarian: strength

##### priest
invoke|cast/concentrate/pray
- cleric: divine
- druid: primordial
- warlock: eldritch

--- auxiliary
##### crucible
mutate/concentrate/research
- apothecary
- blood hunter (completes the paladin/ranger trio) -> mixed base type?
- monster hunter
- living crucible

##### innate?
- sorcerer
- bard
- psion

##### expert
+/craft/focus/invent(flash of mind)
- artificer () - expert: arcane
- monk:
- bard

##### arcane
+ arcane = mystic
+ innate = sorcerer
+ caster = wizard

--- mixed
##### mixed
  associate your spellcasting to a mental ability stat
  associated spell-ability you can convert into abilities (like smite)
- paladin: divine (pick associated mental ability stat)
- ranger
- artificer/warlock?

-- warrior
  + warrior: monk
  + expert: fighter -> battlemaster
  + primal: barbarian
  + divine: paladin
  + arcane: bladesinger/rune knight
  + psionic: psion/psi-warrior
  + pact: hexblade/eldritch knight/oath of vengeance
  + crucible: crucible knight
-- expert
  + expert: bard/rogue
  + warrior: rogue/fighter
  + divine: thaumaturge??
  + primal: ranger
  + arcane: artificer/arcane trickster
  + psionic: soul knife
  + pact: ??
  + crucible: blood hunter(mutant)
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

#### subclasses
Typecast:
  Class: Subclasses may alter class type.
  Ability association: when typecasting a feature, it, and all subfeatures thus gained, change their associated ability to another.
  #i features become less effective, the more centralized it becomes.
  -> uses of typecasting are inversely tied to diversity of ability scores.

Cumulative Subclasses:
  - Scaling features and sidegrades
  - typeclass scaling and incentives to return to classes

#### prestige class
prestige classes are augmented versions of base classes if you meet criteria and work as stackable templates.
you may always only ever be member of one prestige class, advance in it if you meet its additional requirements and any level gained degrades into any one of its constituent classes, should you no longer fulfill those requirements, such as advancing in another prestige class.
example:
artificer(5)[5 acquirable prestige levels]: (Wizard/5, Dex:13, Crafting Rank: Master, Expertise at least one Arcane Tool and either Arcana or another Arcane Tool)

only one prestige class. any combination of base classes. newer choices trump old ones -> augmented class degrades into base class.
with several class types: raise trait tinkering level.
  Balanced:
dual subclass: counts as prestige class. 2nd(+mod3) subclass features as if half cumulative class type.
without prestige class level: every 3 cumulative shared class type levels other than the chosen class count as one level in its progression.
prestige class: you may take a level in a prestige class if you fulfill its requirements. The prestige class counts towards its base class' level progressions.
every prestige class level decays into any one of its base classes should you not meet their requirements when you next level up.

Prestige Classes: when meeting criteria, your most advanced class becomes the base class for the prestige class. Future class advancements may not invalidate past choices.
  bonus features will unlock when cumulative class type levels reach thresholds.
  Advance in 2 Classes simultaneously up to a maximum.
  Mystic Theurge: 3+ Caster / 3+ Priest or higher, but still balanced levels. (eg. 2-Cleric, 2 Paladin, 3 Wizard), Max Level = Level of Base Class
    6/6/6

Partial class progression:
  pick features from a class belonging to the same type of the advancing class. The chosen class feature must be of a level less than half your total class type level.

## optional rules
casting spells:
in reverse order of genericity(?)
magic action -> casting spell (includes innate casting, magical traits, reading scrolls etc)
cast (arcane/divine/primordial)
invoke -> contact to extraplanar entity involved

mastery trait level
  having used something (weapon, tool, armor) extensively, it is steeped in your essence.
  : 4th mastery
  : 9th grand mastery
  : 14th epic
  : 19th legendary
  incentivise upgrading, networking (finding craftsmen), collecting raw materials

weapon masteries, tool and crafting more important.
- exploits and boni tied to specific weapon family.

(field) crafting
  : giving plentiful options to harvest materials
  : known recipes
  : rewarding experimentation
  : maxim: if it is a trait of a monster, you can probably craft something out of it.
ie. containers are infusables

spellcasting:

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