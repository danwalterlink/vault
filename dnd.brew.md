---
id: cr6c1y1bpckfo7fvx9xkqa6
title: dnd-6
desc: ''
updated: 1690696692737
created: 1684357294795
---

scaling, power
- centralising ideas: moving closer to "stem" of characters
- generally, more powerful options are specialising and repeatable, then try to apply that stack to as much as possible
- choices are empowering, so blowing the door open for more granular amalgamations of features will raise the roof of mechanical abilities, AND give access to new lows of synergy. So while, in an absolute sense, the gulf of power becomes more, rather than less, the difference between maximized and basic, "by-the-book" characters is intended to be much smaller, since the new lows are only accessible if you engage with the granular "build-it-yourself" system extensively.

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
-> "5.5", meaning, to 5th, what 3.5 was to 3rd. the dndOne approach, ironing out kinks, with as few major overhauls as possible. (5.5 in my nomenclature would be TCE, incidentally, the 5th supplement)
-> 6 : more fundamental changes that make "ports" more necessary: short: new base books (dmg, pm, mm)

## design maxims in contrast and reaction to 5e
iterative, generative and clear versioning/templating including errata ![[Tooling|dendron://dnd/dnd.brew.tooling]]
  -> not "stranding" old material
simple, theme-focused class-based design does not shackle to class-based design.
take a page from programming: "classical hierarchy" does not limit us to "classical inheritance", or in dnd terms: "subclass design" approach

the balancing will always be finnicky, but having options is inherently fun.
system-design collapses gracefully.
out of the box strong, interact with system as-wanted. Forego optimization losing small edges.

0. focus on meaningful differentiation, packaging in distinct classes; power level is secondary.
    0. my preferred ootB experience would be really strong mechanically early, and gets less optimal the farther you progress.
    Simply: character concept becomes more niche, and the likelyhood that niche fits the environ by default gets smaller.
    but also: players are more knowledgeable.

    1. powers for drawbacks. pack tactics. sunlight sensitivity. -4 STR.

1. the world IS magical. Even the most mundane thing works magic. Doing something repeatly steeps the location in this ritual. Fireplaces grow closer to the elemental flame by each kindling; ancient fireplaces might even spark themselves through sheer habit.
certain tankards fit snugly in dwarven hands while feeling off to a human with the same prints.

2. gambling rocks.
  Any feature that lets you wager is cool in my books.

3. rolling things means something, but you don't wanna punish for rolling on cool things.
    0. choice: pick average, rounded up, or gamble
    for permanent rolls: anything below average gets rounded to dice average (rounded down).
    1. roll away things

4. flexible resource interchange system
    players "dice" as resources they can "cast".
    looking more like poker, where they can "throw in" their resources.
    0. tie regenerative capabilities to resources
      ie. action surge regeneration to hit die / or other resources.
    1. give panic-options that are expensive. get cheaper during rests -> active rests
        - make the time spent during rests meaningful, ie. different choices; currently you always blow as many resources as you can get away with: rest casting etc.
        - have other ways of regenerating resources other than variable "cooldowns"
            ex: monk ki recharges{x} on actions taken with conditions.
        - certain interactions diminish resource availability
        - condition checks tied to resources default to #dnd.generics half or less.
    2. option 'load' determines resource value #?
      - half of unused resources from last turn, pay in current turn or restrict your next turn: up to double your turn maximum.
      - movement for reactions

## rest
(take a breather, short rest, long rest, recuperation)
taking a breather uses available minor consumables to
less punishing initial exhaustion effects.
recovering from exhaustion reduces:
1) total no. of hit dice
2) hit dice size
3) [restful] regaining hit dice {[rested]amount/size[fatigue]} vs [preparing] regenerating resources;
: a character counts as fatigued, if their current hit dice size lesser than half their maximum
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

![[dendron://dnd/dnd.brew.ancestry]]

### Brief Background
baseline:
  : can give up skill and tool proficiencies to upgrade
  2 skills, 1 tool
  +variant: feat that entails some the above and give up the rest
  common + 1 regional language

  {background.custom}
- basic: 2 skills, 1 tool(choice)
- some gain other benefits instead

  mali for boni
additionally, you may choose to affiliate with an order, association, guild or other faction.

## Class
[autodidact] :=[custom class]: meta-class; what amalgam ancestry is for ancestry; autodidact is for classes.
mechanic:pick

you are considered lvl0 for all (base) classes you haven't picked a level in
if something refers to class, it refers (its) base class unless noted otherwise.

moving away from class-gated design
-> every feature a class has is a [feat]
fighter: bake fighter/battlemaster into base class #changes.5e
warlock: bake hexblade-features into base-class #changes.5e

### class types
[eclectic] picking from d
smaller blocks with baked-in choice, backed by resource-interchange and interaction system.
-> small changes have potentially far-reaching effects.
along general type system, classes fulfill a more 'templative' role

![[Class|dendron://dnd/dnd.brew.class]]

### subclasses
Typecast:
  Class: Subclasses may alter class type.
  Ability association: when typecasting a feature, it, and all subfeatures thus gained, change their associated ability to another.
  #i features become less effective, the more centralized it becomes.
  -> uses of typecasting are inversely tied to diversity of ability scores.

Cumulative Subclasses:
- Scaling features and sidegrades
- typeclass scaling and incentives to return to classes

### prestige class
prestige classes are augmented versions of base classes if you meet criteria and work as stackable templates.
you may always only ever be member of one prestige class, advance in it if you meet its additional requirements and any level gained degrades into any one of its constituent classes, should you no longer fulfill those requirements, such as advancing in another prestige class.
example:
artificer[5](5 acquirable prestige levels): (Wizard/5, Dex:13, Crafting Rank: Master, Expertise at least one Arcane Tool and either Arcana or another Arcane Tool)

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

### weapon masteries, tool and crafting more important
- exploits and boni tied to specific weapon family.

### (field) crafting
  : giving plentiful options to harvest materials
  : known recipes
  : rewarding experimentation
  : maxim: if it is a trait of a monster, you can probably craft something out of it.
ie. containers are infusables

spellcasting:
action surge type restrictions?
-> cost backloading. action surge - attempt thing and then pay resources.

## additional rules
### healing
: receiving over your biggest hit dice worth of hp in healing:
- makes you hungry;
- while hungry makes you starving.
- while starved depletes hit dice a number of hit dice could have rolled (rounded up).
- while starved and without adequate hit dice additionally gives you one level of exhaustion. h2

#### Potions
: healing potions restore health according to : minor healing potion (2d4 + constitution modifier) ||
: HoT: when you roll for healing of a potion and roll beneath half max, you heal for 1/2 max.
  anything over 1/2 is restored over time at (1/2 number of dice) hp/round.
(the following makes frequent cooking and/or magical food a necessity for adventurers)

### degrees of success
combat: critical failure/success
  slight failure: slight chance of minor weapon damage (knick, bend or tear),
  failure: failed by 5 or more: automatic minor weapon damage, slight chance of major weapon damage (rendering unusable or less effective). Can use reaction to mitigate.
  critical failure: automatic major weapon damage. Can use reaction to mitigate.

### feats
![[Brew|dendron://dnd/dnd.brew.feats]]

## setting
magic
weave not entirely separate. it's a "weave"
  blue/silver or spellfire are divine castings from mystra.

deities are avatars of their ideas.
moradin was created by the but also is creating the idea of dwarvenkin.
wrested and nestled a new corner into the multiverse through stout, hardy, collectives formed around their love of stone craft.
Separately, they grew their little corners, bending and twisting it slightly into different spaces, with different 'proto-muradins'.
And thus, slowly they grew, until suddenly they had been dwarves.
if you are suffused with a close-ish primordial soup, and onomatically cast yourself a dwarf,
is retroactively always having been moradin molding you to be a dwarf.

the collective of the multiverse partaking in onomancy is ao.
selune and shar danced the universe an upside-down, that begat stuff and the idea of difference.
In moments of uncaring strife between the twins, vague primordials formed, until, having been left to germinate into monstrosities by longer and longer altercations between light and dark.
The primordials grew, fueled by horror of difference into gargantuan calamities of entropy, and tempered in their constant struggle against one another, which culminated in a cataclysmic battle for supremacy, splitting realmspace, leaving proto-deities as victors.