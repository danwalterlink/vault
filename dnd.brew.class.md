---
id: mche96l9m56hozf78zwul37
title: Class
desc: ''
updated: 1685279618285
created: 1684956724533
---

"action surge becomes a general feature -> [[]]
if you dont want feature to be readily accessible through multiclassing/trait doctoring, make it an amalgam feature (features that exist through layering if class features) and describe the fantasy/surrounding ideas through the closest (sub)class

![[Progressions|dendron://dnd/dnd.brew.class.progressions]]
## feature
feature can be untyped -> inaccessible by any other means!
[core, base, sub, paragon, prestige, origin, kiln]
  generally:
    - additional resource allocation
    - base class features are unspecific
    - abilities are preferably tied to resources, instead of binary cooldowns (per day)
artificer:= tinkerer
  [ infusion specialist
  , cobbled creations (cobble)
  , right tool for the job
  ] (armorer)
barbarian: (berserker/zealot, psion, )
  [ reckless attack
  , rage
  , crucible of ancients
  ] (totem, ancestral guardian)
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
  , paragon/champion (divine presence/aura)
  , lay on hands
  ] (vengeance)
( psion:
  [ psionics
  , raw talent
  , discipline
  ] -> awakened -> move to crucible -> improves arcane resource generation (or move into monk?))
ranger: (hunter/monster hunter/monster slayer, drake warden/beast master, trapper)
  [ pick: prowl(explorer, foe, awareness),
  , scavenge
  , primal preparation (+ability appropriation: primal)
  ] (gloom stalker)[adaptable]
rogue: (assassin/arc trickster/swashbuckler)
  [ cunning action (+ ability appropriation, moving actions into different action types)
  , magic hands (mage hand(can put objects on people), use of magical devices)
  , sneak: attack, focus,
  ] (thief)
sorcerer: (archfey, draconic, abyssal)
  [ metamagic - "intuitive" (additional metamagic: spell echo, living spell, partial/condensed spell)
  , font of magic
  , magical guidance
  ] (clockwork soul (expanded spell lists))
warlock: (patron powers, or mutate existing ones)
  [ pactsmith [meldmind]
  , eldritch arcana [unwanted inquiries]
  , invocations
  ] (hexblade hex/eldritch blast integration)
wizard: (evoker, )
  [ scholarly tradition[spellbook]
  , metamagic: acribic [scribe/alter/memorize metamagic options]
  , experimenter [attach spells to objects] -> spellskin: runic condensation of arcaneries inked on skin
  ] (scribe (scribe/alter/memorize))

## class types
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
subtype: "tone/primary" - power: essence
(passive, primary, secondary)
warrior(honed/wit/brute): fighting style, maneuvers, focus
caster(learned/innate/pact): spellcasting, metamagic, additional access
priest(divine/primal/eldritch): paragon, channel, invocations

subtype: "kiln/secondary" - power: source
innate: metamagic, intuit [crucible -> temporary innate]
learned: acribic, ritual casting
pact: living spell

subtype: "chord/tertiary" - power: origin
arcane: primary damage types: all/none
primal(prime material): primary damage types: elemental, physical [primordial]
divine: primary damage types: necroti/radiant

-> 27 3-subtype combinations
up to 3 components. multiclass combinations are cut to 3.
blood hunter (warrior, arcane, {mutant}:crucible || {profane soul}:priest)

pure classes (one of subtype) ie. wizard(caster, arcane)
  diverging subclasses: 2 tones ie. wiz::bladesinger(caster, warrior)
  focussing subclasses: count a subtype doubly ie. wizard[subclass](caster, caster, arcane)
focussing multiclasses? -> monk: you do not gain additional features, but you count your monk class levels as 3 levels for the purposes of gaining additional traits in your primary class
balanced multiclasses: lose primary class, gains an additional secondary class
mixed martial classes: style
  honed(flat boni, balanced, any style)
  wit(emphasize dex/precision, dice conversions and additional effects)
  brute(typecast certain ability score to str/con)
  -> intellect brute(psion!): typecast everything to intelligence
  adding subclass options that improve on the specific nature:
  -> speeding up spell progression (2/3rds caster): every 3 classes count as 2 additional as to spell progressions. Rest: 1, neglect. Rest 2 add another 1.

supertype: (spell slot progression, trait doctoring -> supplanting traits = grafting)
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

subclass-less: "pure"/generic class{archetype}: counts as a prestige and paragon class.
  - gains quicker progressions by foregoing subclass choice
  - more resources?
  - gains "featureless pilferer"
  other means of acquiring paragon traits: high level (sub)class feature

## paragon class type
paragon of:
  might (fighter/psion/barbarian)
  cunning (bard/rogue, through paragon pilfering)
  {deity}/{circle} (cleric/druid)
  power (fighter)
  arcana (wizard/sorcerer)
  {any: warlock}

warrior paragon -> champion/cavalier (warrior/warrior/warrior)
  fighter: typecast any martial ability [typecast]
priest paragon: choose invocations paragon progression (priest/priest/priest)
  primal paragon: channel: elemental wildshapes
  divine paragon:
caster paragon (caster/caster/caster)
  wizard
    scribe: typecast spell-like abilities into arcane spells
    onomant: drop material and somatic components, power words, smaller spell book
warlock doesn't advance any other progressions. typecast class
(hybrid classes aren't paragon classes)

## prestige
