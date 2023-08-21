---
id: mche96l9m56hozf78zwul37
title: Class
desc: ''
updated: 1691509344863
created: 1684956724533
---

rebuilt class system on:
  types
  generics
  traits

progressions grant [features] and [traits]
classes encapsulate
-> more granular progressions without sacrificing strong class/identity design
progressions along base class levels:
  {artificer..wizard}
  ++ custom/meta
  ++ base/un-subclassed

  gain features up to cumulative class type

[progression]
  [ character [cumulative]
  , profession [skill]
  , archetype [core]
  , class [type]
  ]

[tier]
  [ novice: ..0
  , master: 3..
  , heroic: 7..
  , grand: 11..
  , epic: 17..
  ]

## type trees
? class type |- m -| type class

: [type].:[type] -< trait >- class ->> class.derived

[ancestry]
[background]
[level] :: character ->> tier
  [tier]
  [character]
    [archetype] :: core ->> tier
      [martial] :: weapon mastery | fighting style | attack style
      [caster] :: spellcasting
        [off] :: magic.slot.progression.off==(1+lvl/5) max:4
        [half] :: magic.slot.progression.half==(1+lvl/3) max:5
        [full] :: magic.slot.progression.full==(1+lvl/2) max:9
        +[epic] :: magic.slot.progression.epic==() max:none

    [class] :: base ->> paragon
      [core] :: warrior, expert, priest, arcanist, occultist
      [base] :: {artificer,..,wizard}
      [sub] :: {..base.subclass}
      +[prestige] :: cast trait/generics
      +[paragon]

  [derived]
  [cumulative]
  [total]

traits and features have the types of their generators
[trait]
[feature]
  [class]
    [core]
    ..
  [feat]

type.class ? [warrior, expert, mage, priest, occult] :
    warrior ? [honed, sly, brute] :
      fighting style
      maneuver
        attack: [practiced, sneak, reckless]
        focus: [requires concentration]
        stance: [alters movement]
    expert ? [ magewright/tinkerer, pilferer, thaumaturge] :
      [ expertise, innovation]
    mage/arcanist ? [prepared, known, innate] :
      spellcasting
      metamagic
      countermagic
    priest: [divine, primal, arcane/eldritch]
      spellcasting
      channel
      invoke
    crucible: [investiture, imbibe, pact]
      host/channel
      invoke

class:type: [legacy, base, sub, derived, prestige, paragon]

feature type: [learned, pilfered, crucible]
  pilferer:
    fighter: martial
    rogue: skill/item
    artificer: item
    bard: spell
    warlock: everything

## class type features
supertypes: focused (+50% type scaling), dip, poly: paragon requirements
\_ {class}:
  adapter: {legacy}
  base: core
    un-subclassed: generic: supertype features
    paragon: non-derived: acquired feature types congruent with base class
  sub: supplemental
    derived: multiclass: replacements; resulting from multiclass;
    fighter -> monk: martial; mystic
  prestige: multi/core/supplemental/replacement
  paragon: improved scaling?

## base class template
![[dendron://dnd/Progressions|dnd.brew.class.progressions]]
{one phrase description}
traits: [class type]
unified basic features: extended in subclasses
extending type class features: {}
paragon features: {}
base class feature: {}

## feature
feature can be untyped
[core, base, sub, paragon, prestige]
generally:
  additional resource allocation
  base class features are unspecific
    variants layer features on top
  abilities are preferably tied to resources, instead of binary cooldowns (per day)

whenever you choose character features, you can forego that choice and instead gain a feature that is at least as generic
!# class gets subtypes you can choose : a la cleric XUA22CO holy order
\-> 2 options + no choice.

%TAG ! tag:dnd.ddubl,class:
--- !base
![[artificer|dnd/Class|dnd.brew.class.artificer]]
  infuser, tinkerer : profession := magewright
![[barbarian|dnd.brew.class.barbarian]]
  |-[psion]
![[bard|dendron://dnd/dnd.brew.class.bard]]
![[witcher/blood hunter|dendron://dnd/dnd.brew.class.blood-hunter]]]
![[cleric|dendron://dnd/dnd.brew.class.cleric]]
![[druid|dendron://dnd/dnd.brew.class.druid]]
![[fighter|dendron://dnd/dnd.brew.class.fighter]]
![[monk|dendron://dnd/dnd.brew.class.monk]]
  |-[mystic]
![[paladin|dendron://dnd/dnd.brew.class.paladin]]
![[ranger|dendron://dnd/dnd.brew.class.ranger]]
  |-[hunter]: monster hunter
![[rogu|dendron://dnd/dnd.brew.class.rogue]]
![[sorc|dendron://dnd/dnd.brew.class.sorc]]
![[warlock|dendron://dnd/dnd.brew.class.warlock]]
![[wizard|dendron://dnd/dnd.brew.class.wizard]]

## class types
all class types have empty/generic variants.
\-> ie. pick: generic metaclass warrior:
[legacy]
obsolete class, superseded by a newer version
[derived]
beast master -> drakewarden

: variations/sub-subclasses
just syntactical sugar that makes inheritance-like models more apparent
[affix/prefix system?]
class types are different than "caster - martial - channeler" character types that are tied to traits:
  if you have either
    spellcasting, maneuvers, or channel powers, you count as a caster, martial or channeler respectively.
other character types, such as alchemist, artificer or other professions are tied to proficiency in tools.
your proficiency bonus with tools can be increased by renown. See: Journeyman.

(invoke names/entities, cast spells)
'{arche}type
subtype: "tone/primary" - power: essence
(passive, primary, secondary)
warrior(honed/wit/brute): fighting style, maneuvers, focus
caster(learned/innate/pact): spellcasting, metamagic, additional access ("steal" magic features)
priest(divine/primal/eldritch): paragon, channel, invocations

'{source}type
subtype: "kiln/secondary" - power: source
innate: metamagic, intuit [crucible -> temporary innate]
learned: acribic, ritual casting
pact: living spell

'{spell}type
subtype: "chord/tertiary" - power: origin
arcane: primary damage types: all/none
primal(prime material): primary damage types: elemental, physical [primordial]
divine: primary damage types: necroti/radiant

pure / non-subclassed // rule for class name alteration:
ie. wizard(caster, arcane)
  diverging subclasses: 2 tones ie. wiz::bladesinger(caster, warrior)
  focussing subclasses: count a subtype doubly ie. wizard[subclass]\(caster, caster, arcane)
focussing multiclasses? -> monk: you do not gain additional features, but you count your monk class levels as 3 levels for the purposes of gaining additional traits in your primary class
balanced multiclasses: lose primary class, gains an additional secondary class
mixed martial classes: style

### meta
#### warrior
##### training
  honed(balanced; any style)
    maneuver(acquired heroism)
    power attack(bonus or mastery)
    all Weapons

  sly(emphasize dex/precision; dice conversions and additional effects; precise styles)
    maneuver(debilitate)
    sneak attack
    finesse Weapons

  brute(rage; typecast certain ability score to str/con; brutal styles)
    maneuver(brutal)
    reckless attack
    oversized Weapons
    \-> intellect brute(psion!): typecast everything to intelligence

  adding subclass options that improve on the specific nature:
  \-> speeding up spell progression (2/3rds caster): every 3 classes count as 2 additional as to spell progressions. Rest: 1, neglect. Rest 2 add another 1.
/#####

super (spell slot progression, trait doctoring -> supplanting traits = grafting)
/####

### caster
cast(+ritual)
meta ([metamagic, scribe, pact])
counter < default: pit essence: wager hit-dice/ability-dice against spell; inefficient & undesirable >

- non-
  barbarian, fighter, rogue, monk, bh, mh

- half- construct by stacking martial with caster?
  -< smite / channel / invoke > variants
  (paladin, ranger, artificer) third: [profane soul, arcane trickster, eldritch knight]

- full-
  \-< recovery, meta, counter>
  (druid, cleric)(bard, sorcerer, wizard)(warlock)

- martial
  - maneuvers (martial cantrips/spells)
  - focus (requiring resources: concentration)
  - drills (resting activity, temporary buffs, debuff removal, equipment prep, spell-like effects)

- expert
  - expertise
  - stroke of genius
  - escape strangling specifics (enhances trait tinkering)

- hybrid type (mixed?)
  : feature converts spell slots into
  \-- [armor, cantrip-type, weapon]
  warrior, derived classes:
  \-> "half-casters"
    spell-like ability, fueled by expending spell slots

  paladin (cha/wis)
  (medium armor, maneuvers, mastery(longsword), non-finesse martial melee weapons)
    \-> convert smite spells into abilities
    channel divine - smite: if spell prepared, add a smite effect
  - aura: self and allies

  ranger (wis/int)
  (light armor, maneuvers, mastery(shortsword, longbow), finesse martial melee weapons, non-firearm martial ranged weapons)
    \-> traps, consumables, temporary enchantment
    channel nature - imbue: consumables, crucible
  - environment -> traps

  artificer (int/cha)
  (heavy armor, mastery(tools), firearms)
    channel arcane - infuse: spell-like effects to equipment
  - tinkerings: lasting on equipment

  monk(extreme dedication: double progression, no additional features),
  -> monk martial artist as fighter subclass
  psion(raw arcane(psychic force)){{monk prestige class}}
  mystic
  : chi/ki "bodied" -> psi
  subclass:
    crucible -> taking on vestiges of power in surroundings
    void/null -> walking anti-magic field. fueled by negating magic
    avatar -> elemental bender (psi or spells)

  - replace innate casting somatic component with an {unarmed strike}
  -> "overspecialization"
  : losing access to gained features to gain faster progressions

metaclass: "pick" mechanic : pure base class = class paragon
subclass-less: "pure"/generic class{archetype}: counts as paragon class and gains associated
- gains quicker progressions by foregoing subclass choice
- more resources?
- gains "featureless pilferer"
  other means of acquiring paragon traits: high level (sub)class feature

## paragon class type
warrior / priest
  exemplar - champion - paragon
caster / expert

  arch{class}

paragon of:
  might (fighter/psion/barbarian); primary ability score over 20
  cunning (bard/rogue, through paragon pilfering); over 5 different classes in traits
  {deity}/{circle} (cleric/druid); casting ability score priest over 20
  power (fighter/paladin);
  arcana (wizard/sorcerer); primary casting ability score caster over 20
  {any: warlock};

warrior paragon -> champion/cavalier (warrior/warrior/warrior)
  fighter: typecast any martial ability [typecast]
priest paragon: choose invocations paragon progression (priest/priest/priest)
  primal paragon: channel: elemental wildshapes
  divine paragon:
caster paragon (caster/caster/caster)
  wizard
    scribe: typecast spell-like abilities into arcane spells
    onomant: drop material and somatic components, power words, smaller spell book
warlock doesn't advance any other progressions. typecast class; crucible;

## meta-class
non-caster:
  warrior {honed, sly, brute}
  expert {artificer, thaumaturge, pilferer}
caster:
  priest(divine, primal, eldritch) { }
  arcanist(studied, innate(sorcerous, psionic), pact)
  occult(pact, host, crucible)
  \-> crucial distinction: no-spell-progression, half-spell-progression, full-spell-progression

### non-caster
core: maneuver/focus/drill
#### honed
fighter: allrounder/technician
- fighter:battlemaster:: all maneuvers/exploits

#### sly
rogue: dexterity

#### brute
barbarian: strength

### full-caster
core: spellcasting/magic tinkering/
  wizard: scribe/memorize/alter spell
- scribe anything, artificing

sorcerer: intuitive alter spell -> metamagic
- multi-casting, volatile/wild spells

bard: intuitive/honed
warlock: make their patron's magic their own. #f? -> priest?
- living spell, granting pacts

### priest
cast
channel
invoke
- cleric: divine
- druid: primordial
- warlock: eldritch

#### occult
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
\+/craft/focus/invent(flash of mind)

- artificer () - expert: arcane
- monk:
- bard

##### arcanist
- arcane = mystic
- innate = sorcerer
- caster = wizard

#### hybrid
hybrid mental ability requirements (as fighter has hybrid requirements)
physical ability requirement
- spell-slot fueled ability (divine/primal/arcane smite)
- gaining ways to interact with specific types of magic (divine/primal/arcane)

- paladin: (str,(wis/cha))
  · smite: divine (dmg, divine smite spell)
    (when an attack hits, you may cast a smite spell)
  · aura
  · invocations

- ranger: (dex,(int,wis))
  · smite: primal (dmg, primal smite spell)
  · imbue: self/bonded creatures/environs/weapons with primal magic;
  · melding/bonding: with environ/weapon/creature

- artificer
  · smite: arcane (dmg, arcane smite spell)
  · artificing, temporary and persisting item alterations.
    attaching spell-slots to items.
    pulling magic from items to fuel abilities.
    "arcane" smite
  · attunement

\-- warrior

- warrior: monk
- expert: fighter -> battlemaster
- primal: barbarian
- divine: paladin
- arcane: bladesinger/rune knight
- psionic: psion/psi-warrior
- pact: hexblade/eldritch knight/oath of vengeance
- crucible: crucible knight
  \-- expert
- expert: bard/rogue
- warrior: rogue/fighter
- divine: thaumaturge??
- primal: ranger
- arcane: artificer/arcane trickster
- psionic: soul knife
- pact: ??
- crucible: blood hunter(mutant)
  \-- divine
- divine : cleric
- martial : war domain/forge domain
- expert : trickery domain
- primal : tempest domain
- arcane : arcana domain
- psi : ?
- pact : twilight/death?
- crucible : godeater
  \-- primal
- arcane
  \-- arcane
  \-- psi
  \-- pact
  \-- crucible
