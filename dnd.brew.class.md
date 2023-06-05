---
id: mche96l9m56hozf78zwul37
title: Class
desc: ''
updated: 1686000752874
created: 1684956724533
---

rebuild class system on:
  types
    generics
    traits

## typification / classification
archetype: martial(proficiency(with martical weapons)), caster(spellcasting)
  trait defined; if both: dual.
character (class) type: [single, mixed, multi]:
  total character class: cumulative type description
    total character class level: legacy character level
    derived character class level: cumulative character class level

martial: trait class:
  martial weapons
caster:
  spellcasting
specialist
hybrid

type:class: [warrior, expert, mage, priest, occult]
    warrior: [honed, sly, brute]
      attack [practiced, sneak, reckless]
      maneuver, focus, stance
      style
    expert: [artificer, pilferer, thaumaturge]
      expertise
    mage: [prepared, known, innate]
      spellcasting
      metamagic
      specialization
    priest: [divine, primal, eldritch]
      spellcasting
      channel

    crucible: [investiture, imbibe, pact]
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
_ {class}:
  adapter: {legacy}
  base: core
    un-subclassed: generic: supertype features
    paragon: non-derived: acquired feature types congruent with base class
  sub: supplemental
    derived: multiclass: replacements; resulting from multiclass;
    fighter -> monk: martial; mystic
  prestige: multi/core/supplemental/replacement
  paragon: improved scaling?

# base class template:
{one phrase description}
traits: [class type]
unified basic features: extended in subclasses
extending type class features: {}
paragon features: {}
base class feature: {}

![[Progressions|dendron://dnd/dnd.brew.class.progressions]]

## feature
feature can be untyped
[core, base, sub, paragon, prestige, origin, kiln]
generally:
  additional resource allocation
  base class features are unspecific
    variants layer features on top
  abilities are preferably tied to resources, instead of binary cooldowns (per day)

whenever you choose character features, you can forego that choice and instead gain a feature that is at least as generic
!# class gets subtypes you can choose : a la cleric XUA22CO holy order
-> 2 options + no choice.

### artificer
infuser, tinkerer
![[Class|dendron://dnd/dnd.brew.class.artificer]]

### barbarian
berserker, primal
  [ reckless attack
  , rage
  , crucible of ancients
  ] (totem, ancestral guardian)
(berserker/zealot, psion)

### bard
college: lore, sword
  [ bardic inspiration
  , magical secrets
  , (counter)charming
  ] (lore)

### blood hunter
covenant: witcher, warlock
  [ blood malediction
  , crimson rites
  , hemocraft
  ] (mutant)

### cleric
holy order, subclass: domain
    protector, scholar, thaumaturge {XUA22}
  [ emboldening bond
  , turn undead
  , domain expansion
  ] (peace)

### druid
  [ natural recovery
  , wildshape (shapes known, 12 statblocks)
  , channel: nature
  ] (moon)

- fighter
  academy: champion, cavalier, none
  [ martial mastery (weapon mastery, multiples, any class)
  , second wind(indomitable(unstun), additional movement, hp regen)
  , balanced training (additional feats, floating proficiency, improve action surge)
  ] (champion/cavalier)

  + champion
    expanded critical range
    exceptional athlete
    additional fighting style
    survivor

  + cavalier
    unwavering mark
    warding maneuver
    hold the line

### monk
  martial (artist), mental -> mystic
  . meditation > movement meditation: flurry of blows
  [ flurry of blows
  , stunning strike
  , ki
  ] (shadow)
[monastic] if you  you may replace somatic components with {monk weapon} strikes or meditation
if you use a ki ability via meditation, reduce it's ki-point cost by {amount}
: multi

### monster hunter
  [ imbibe
  , prowl
  , quarry
  ] -> move into ranger; spellless)

### mystic
applied, retreat
  [ psionics
  , meditate
  , discipline
  ] -> immortal -> move into psion)

### paladin
priest, warrior
  [ divine sense
  , paragon/champion (divine presence/aura)
  , lay on hands
  ] (vengeance)

### psion
derived class: typecast power source to psionic.
  [ psionics
  , raw talent
  , discipline
  ] -> awakened -> move to crucible -> improves arcane resource generation (or move into monk?))

### ranger
explorer, exploiter
  [ prowl(explorer, foe, awareness),
  , scavenge
  , primal preparation (+ability appropriation: primal)
  ] (gloom stalker)[adaptable]
(hunter/monster hunter/monsterslayer, drakewarden/beastmaster, trapper)

### rogue
duelist, infiltrator
  [ cunning action (+ ability appropriation, moving actions into different action types)
  , magic hands (mage hand(can put objects on people), use of magical devices)
  , sneak: attack, focus,
  ] (thief)
assassin, arcane trickster, swashbuckler

### sorcerer
explorer, exploiter
  [ metamagic - "intuitive" (additional metamagic: spell echo, living spell, partial/condensed spell)
  , font of magic
  , magical guidance
  ] (clockwork soul (expanded spell lists))
(archfey, draconic, fiend, divine)

### warlock
subtype -> patron
hexblade hex/eldritch blast integration
  [ pactsmith [meldmind]
  , eldritch arcana [unwanted inquiries]
  , invocations
  ]
(patron powers, or mutate existing ones)
elemental(genie), fey/fell, fiend, celestial, deep

### wizard
scribe, war
  +all added spells(scribe/memorize/alter spell)
features [1, 2, 7, 15, 18]
  [1] Arcane Recovery, Wizard's Spellbook, Scribe Spell
  [2] Academic, acribic metamagic: [1:scribe, 5:memorize, 7:modify, 9:create] spell
  []
  [] specialist/experimenter [attach spells to objects]
  spellskin: runic condensation of arcaneries inked on skin

subclasses: scholarly tradition [2, 6, 10, 14]
  {magic.school.adherent}: spell school features:
    (2) {school} savant: reduced cost spell scribing

    abjuration: [arcane ward, projected ward, improved abjuration, spell resistance]
    conjuration: [minor conjuration, benign transposition, focused conjuration, durable summons]
    divination: [portent, expert divinitation, the third eye, greater portent]
    enchantment: [hypnotic gaze, double target, instinctive charm, split enchantment, alter memories]
    evocation: [sculpt spell, potent cantrip, empowered evocation, overchannel]
    illusion: [improved minor illusion, malleable illusions, illusory self, illusory reality]
    necromancy: [grim harvest, undead thralls, inured to undeath, command undeath]
    transmutation: [minor alchemy, transmuter's stone, shapechanger, master transmuter]

  bladesinging
    +{core: replaces "song of victory"} you can choose to add your int ability modifier for melee weapon attacks made as part of casting a spell instead.
      heroic: for all weapon attacks while your bladesong is active.
    +{heroic} replace somatic components of spells that target a creature within your reach with an attack. You may change the spell's range to touch.
    +{grand}
      [Spellstain] When you mark a creature while casting a spell, that mark becomes a spellstained mark.
      [arcane maneuver: echoing spellstain]:
        You may either, when casting a spell with range touch:
        - echo the spell for each spellstained creature.
        - change the target of an effect targeting you to the creature you attack.
        - as a bonus action, teleport to an unoccupied space within reach of a marked creature.

    +{epic}
      [polyphony] you may choose other targets when making weapon attacks as part of casting a spell. For each target you may cast a spell of a level up to the number of targets.
      [arcane maneuver: finale -]: after an attack when casting a spell, you may end your bladesong. If you do so, either:
        [of devastation] you may recast a spell resulting in melee weapon attacks for each different target you cast during this bladesong. You may cast these spells using spell slots totaling half their cumulative level on each target.
        [reprise] regain spell points equal to half your expended spell points expended with spells resulting in melee weapon attacks.

## class types
all class types have empty/generic variants.
-> ie. pick: generic metaclass warrior:
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
caster(learned/innate/pact): spellcasting, metamagic, additional access
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
  focussing subclasses: count a subtype doubly ie. wizard[subclass](caster, caster, arcane)
focussing multiclasses? -> monk: you do not gain additional features, but you count your monk class levels as 3 levels for the purposes of gaining additional traits in your primary class
balanced multiclasses: lose primary class, gains an additional secondary class
mixed martial classes: style

### meta
#### warrior
  honed(balanced; any style)
    :maneuver, power attack; all Weapons
  sly(emphasize dex/precision; dice conversions and additional effects; precise styles)
    :maneuver, sneak attack; Dextrous Weapons
  brute(rage; typecast certain ability score to str/con; brutal styles)
    :maneuver, reckless attack; Strength Weapons
    -> intellect brute(psion!): typecast everything to intelligence

  adding subclass options that improve on the specific nature:
  -> speeding up spell progression (2/3rds caster): every 3 classes count as 2 additional as to spell progressions. Rest: 1, neglect. Rest 2 add another 1.

super (spell slot progression, trait doctoring -> supplanting traits = grafting)
- spellcaster(cantrips, spellcasting(+ritual), "meta"[metamagic, scribe, pact])

  + non-
    barbarian, fighter, rogue, monk, bh, mh

  + half- -> construct by stacking martial with caster?
    -> divine smite, nature's wrath, x-infused
    (paladin, ranger, artificer) third: [profane soul, arcane trickster, eldritch knight]

  + full-
    -> feature regaining slots (outside of short-resting)
    (druid, cleric)(bard, sorcerer, wizard)(warlock)

- martial
  + maneuvers (martial cantrips/spells)
  + focus (requiring resources: concentration)
  + drills (resting activity, temporary buffs, debuff removal, equipment prep, spell-like effects)

- expert
  + expertise
  + stroke of genius
  + escape strangling specifics (enhances trait tinkering)

- hybrid type (mixed?)
  : feature converts spell slots into
  -- [armor, cantrip-type, weapon]
  warrior, derived classes:
  -> "half-casters"
    spell-like ability, fueled by expending spell slots

    paladin (cha/wis)
    (medium armor, maneuvers, mastery(longsword), non-finesse martial melee weapons)
      -> convert smite spells into abilities
      channel divine - smite: if spell prepared, add a smite effect
      - aura: self and allies

    ranger (wis/int)
    (light armor, maneuvers, mastery(shortsword, longbow), finesse martial melee weapons, non-firearm martial ranged weapons)
      -> traps, consumables, temporary enchantment
      channel nature - imbue: consumables, crucible
      - triggers and traps -> traps

    artificer (int/cha)
    (heavy armor, mastery(tools), firearms)
      channel arcane - infuse: spell-like effects to equipment
      - aura: lasting on equipment

  monk(extreme dedication: double progression, no additional features),
  psion(raw arcane(psychic force)),
  mystic
    psi/chi (psi -> chi: "bodied" psi)
    - replace innate casting somatic component with an {unarmed strike}

metaclass: "pick" mechanic
subclass-less: "pure"/generic class{archetype}: counts as a prestige and paragon class.
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

## prestige

### meta
warrior {honed, sly, brute}
expert {artificer, thaumaturge, pilferer}
priest(divine, primal, eldritch)
caster(arcane, innate, psionic)
occult(pact, crucible)
-> crucial distinction: no-spell-progression, half-spell-progression, full-spell-progression

##### caster
core: spellcasting/magic tinkering/
  wizard: scribe/memorize/alter spell
    - scribe anything, artificing
  sorcerer: intuitive alter spell -> metamagic
    - multi-casting, volatile/wild spells
  bard: intuitive/honed
  warlock: make their patron's magic their own. #f? -> priest?
    - living spell, granting pacts

##### warrior
core: maneuver/focus/drill
- fighter: allrounder/technician
  + fighter:battlemaster:: all maneuvers/exploits
- rogue: dexterity
- barbarian: strength

##### priest
cast/channel/pray
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
+/craft/focus/invent(flash of mind)
- artificer () - expert: arcane
- monk:
- bard

##### arcane
+ arcane = mystic
+ innate = sorcerer
+ caster = wizard

#### mixed
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