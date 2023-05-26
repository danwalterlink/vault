---
id: mche96l9m56hozf78zwul37
title: Class
desc: ''
updated: 1685135560192
created: 1684956724533
---
"action surge becomes a general feature -> [[]]
if you dont want feature to be readily accessible through multiclassing/trait doctoring, make it an amalgam feature (features that exist through layering if class features) and describe the fantasy/surrounding ideas through the closest (sub)class
## type additions
### item
minor, medior, major
### spell
minor(0,1), medior(2,3,4,5), major(6+)
### character level tier
(4) 0-2 novice, 3-6 journey, 7-11 grand, 11-16 heroic, 17+ epic
## template
### progression
prof(4): 5, 9, 13, 17 [4]
feat(4*): (0), 4, 8, 12, 16, 19
  feat(3): 1, 4, 7, 10, 13, 16, 19 [7]
subclass feature: {subclass} choice,
feature(3): 2, 5, 8, 11, 14, 17
  improvements: +1
  feature(3): 2,5,8,11,14,17
subclass features(3): 3, 6, 9, 12, 15, 18
epic boon: 20, 21, 22,…
spell level(2): 1, 3, 5, 7, 9, 11, 13, 15
spell slots(1): sp
action economy: 0, 5, 10, 15
## class list
  class features
  generally:
    - additional resource allocation
    - base class features are unspecific
    - abilities are preferably tied to resources, instead of binary cooldowns (per day)
artificer:= tinkerer
  [ arcane infusions
  , spell creations
  , right tool for the job
  ] (armorer)
barbarian:
  [ reckless attack
  , rage
  , crucible of ancients
  ] (totem)
bard:
  [ bardic inspiration
  , magical secrets
  , (counter)charming
  ] (lore)
blood hunter:
  [ blood malediction
  , crimson rites
  , hemocraft
  ] (mutant)
cleric:
  [ emboldening bond
  , turn undead
  , domain expansion
  ] (peace)
druid:
  [ natural recovery
  , wildshape (shapes known, 12 statblocks)
  ,
  ] (moon)
fighter:
  [ martial mastery (weapon mastery, multiples, any class)
  , second wind(indomitable(unstun), additional movement, hp regen)
  , balanced training (additional feats, floating proficiency, improve action surge)
  ] (champion/cavalier)
monk:
  [ flurry of blows
  , stunning strike
  , ki
  ] (shadow)
( monster hunter:
  [ imbibe
  , prowl
  , quarry
  ] -> move into ranger; spellless)
( mystic:
  [ psionics
  , meditate
  , discipline
  ] -> immortal -> move into psion)
paladin:
  [ divine sense
  , aura presence
  , lay on hands
  ] (vengeance)
( psion:
  [ psionics
  , raw talent
  , discipline
  ] -> awakened -> move to crucible -> improves arcane resource generation (or move into monk?))
ranger: (environmentally oriented)
  [ prowl(explorer, foe, awareness)
  , scavenge clean
  , primal preparation (+ability appropriation: primal)
  ] -> gloom stalker
rogue:
  [ cunning action (+ ability appropriation)
  , magic hands (mage hand(can put objects on people), use of magical devices)
  , sneak attack
  ] (thief)
sorcerer:
  [ metamagic (additional metamagic: spell echo, living spell, partial/condensed spell)
  , font of magic
  , magical guidance
  ] -> clockwork soul (expanded spell lists)
warlock:
  [ pactsmith [meldmind]
  , eldritch arcana [unwanted inquiries]
  , invocations
  ] (hexblade hex/eldritch blast integration)
wizard:
  [ scholarly tradition[spellbook]
  , acribic arcaneries [additional doctorings for spell]
  , experimenter [attach spells to objects] -> spellskin: runic condensation of arcaneries inked on skin
  ] (scribe (scribe/alter/memorize))

## class types
class types are different than "caster - martial - channeler" character types that are tied to traits:
  if you have either
    spellcasting, maneuvers, or channel powers, you count as a caster, martial or channeler respectively.
other character types, such as alchemist, artificer or other professions are tied to proficiency in tools.
your proficiency bonus with tools can be increased by renown. See: Journeyman.

(invoke names, cast spells)
subtype: "tone/primary" - power: essence
warrior(honed/wit/brute): fighting style
caster(learned(ritual casting)/innate/pact): spellcasting
priest(divine/primal/eldritch): channel {{source}}
(rituals?)

subtype: "kiln/secondary" - power: source
crucible/pact: prolong temporary buffs, pact, living spell
innate: metamagic, improvise
learned: acribic, ritual casting

subtype: "chord/power/tertiary" - power: origin
arcane: damage types: all[elemental, raw=arcane=force, ], )
primal: damage types: elemental
divine: damage types: necrotic/radiant
material -> all damage types:

-> 27 3-subtype combinations
up to 3 components. multiclass combinations are cut to 3.
blood hunter (warrior, arcane, {mutant}:crucible || {profane soul}:priest)

pure classes (one of subtype) ie. wizard(caster, arcane)
  diverging subclasses: 2 tones ie. wiz::bladesinger(caster, warrior)
  focussing subclasses: count a subtype doubly ie. wizard[subclass](caster, caster, arcane)
focussing multiclasses? -> monk: you do not gain additional features, but you count your monk class levels as 3 levels for the purposes of gaining additional traits in your primary class
balanced multiclasses: lose primary class, gains an additional secondary class
mixed martial classes:
  - honed(fighter)
  ? artificer (warrior/arcane)
  - wit (apply generics through dice)
  - brute (typecast to a certain attribute/ability score)
  -> intellect brute(psion!): typecast everything to intelligence
  adding subclass options that improve on the specific nature:
  -> speeding up spell progression (2/3rds caster): every 3 classes count as 2 additional as to spell progressions. Rest: 1, neglect. Rest 2 add another 1.

supertype: (spell slot progression, trait tinkering)
- spellcaster(cantrips, spellcasting(+ritual), "meta"[metamagic, scribe, pact])
  + non-
    barbarian, fighter, rogue, monk, bh, mh
  + half- -> construct by stacking martial with caster?
    -> divine smite, nature's wrath, x-infused
    (paladin, ranger, artificer) third: [profane soul, arcane trickster, eldritch knight]
  + full-
    -> feature regaining slots (outside of short-resting)
    (bard, sorcerer, wizard)(warlock)
- martial
  + maneuvers (martial cantrips/spells)
  + focus (stances, requiring resources: concentration)
  + drills (minor buffs, debuff removal, equipment prep, spell-like effects)
- expert
  + expertise
  + stroke of genius
  + escape strangling specifics (enhances trait tinkering)
- hybrid type (mixed?)
  : feature converts spell slots into
  -- [armor, cantrip-type, weapon]
  warrior(honed) derived classes:
  -> "half-casters"
    spell-like ability, fueled by expending spell slots
      paladin (cha/wis)
      (medium armor, maneuvers, mastery(longsword), non-finesse martial melee weapons)
        -> convert smite spells into abilities
        channel - smite: if spell prepared, add a smite effect
          - aura: self and allies
      ranger (wis/int)
      (light armor, maneuvers, mastery(shortsword, longbow), finesse martial melee weapons, non-firearm martial ranged weapons)
        -> traps, consumables,
        channel - imbue: consumables, self-buff
          - triggers and traps -> traps
      artificer (int/cha)
      (heavy armor, mastery(tools), firearms)
        infuse: spell-like effects to equipment
          - aura: lasting on equipment

  monk(extreme dedication: double progression, no additional features), psion(raw arcane prodigy), mystic()
    psi/chi (psi -> chi: "bodied" psi)

closeness in type:
caster:
  bard - artificer - : both have "create" spells worldly

## prestige