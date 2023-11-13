---
obsidianUIMode: preview
cssclasses: json5e-monster
tags:
- compendium/src/5e/erlw
- monster/cr/0
- monster/size/medium
- monster/type/humanoid/any-race
aliases: ["Magewright"]
---
# Magewright
*Source: Eberron: Rising from the Last War p. 318*  

In Khorvaire, magic is part of everyday life. A chef might use [prestidigitation](compendium/spells/prestidigitation.md) to heat and season food, while a blacksmith uses [mending](compendium/spells/mending.md) to perform minor repairs and [guidance](compendium/spells/guidance.md) to help inspire their work. Those who work minor magic into their labors are called magewrights.

Far more limited in magical power than a typical spellcaster, a magewright is dedicated to learning a handful of spells, and magewrights cast their non-cantrip spells as rituals—even spells that can't normally be cast in this way. Most magewright rituals take 10 minutes to perform, but certain complex rituals can take up to 1 hour. However long the ritual takes, it requires extra material components, usually in the form of dragonshards.

## Creating a Magewright

The magewright stat block provides the baseline statistics for a magewright. You then add to that baseline by choosing a specialty from the Magewright Specialties table, or roll for one. The specialty determines additional spells the magewright knows, including ones that can be cast only as rituals. The specialty also gives the magewright more proficiencies.

**Magewright Specialties**

| dice: d8 | Specialty | Spells | Proficiencies |
|----------|-----------|--------|---------------|
| 1 | Artisan | [Guidance](compendium/spells/guidance.md), [mending](compendium/spells/mending.md) | One type of artisan's tools |
| 2 | Entertainer | [Minor illusion](compendium/spells/minor-illusion.md), [thaumaturgy](compendium/spells/thaumaturgy.md). Ritual only: [disguise self](compendium/spells/disguise-self.md). | [Performance](rules/skills.md#Performance) (+3) |
| 3 | Healer | [Resistance](compendium/spells/resistance.md), [spare the dying](compendium/spells/spare-the-dying.md). Ritual only: [detect poison and disease](compendium/spells/detect-poison-and-disease.md), [lesser restoration](compendium/spells/lesser-restoration.md) (1 hour). | [Medicine](rules/skills.md#Medicine) (+4), [herbalism kit](compendium/items/herbalism-kit.md) |
| 4 | Lamplighter | [Light](compendium/spells/light.md). Ritual only: [continual flame](compendium/spells/continual-flame.md) (1 hour). | [Tinker's tools](compendium/items/tinkers-tools.md) |
| 5 | Locksmith | [Mending](compendium/spells/mending.md). Ritual only: [arcane lock](compendium/spells/arcane-lock.md) (1 hour), [knock](compendium/spells/knock.md). | [Thieves' tools](compendium/items/thieves-tools.md), [tinker's tools](compendium/items/tinkers-tools.md) |
| 6 | Mediator | [Guidance](compendium/spells/guidance.md). Ritual only: [comprehend languages](compendium/spells/comprehend-languages.md), [zone of truth](compendium/spells/zone-of-truth.md). | [Insight](rules/skills.md#Insight) (+4), [Persuasion](rules/skills.md#Persuasion) (+3) |
| 7 | Medium | [Minor illusion](compendium/spells/minor-illusion.md). Ritual only: [speak with dead](compendium/spells/speak-with-dead.md). | [Deception](rules/skills.md#Deception) (+3), [Religion](rules/skills.md#Religion) (+4) |
| 8 | Oracle | [Guidance](compendium/spells/guidance.md). Ritual only: [augury](compendium/spells/augury.md), [divination](compendium/spells/divination.md) (1 hour). | [History](rules/skills.md#History) (+4), [Religion](rules/skills.md#Religion) (+4) |
^magewright-specialties

## Statblock

```ad-statblock
title: Magewright
![](compendium/bestiary/humanoid/token/magewright.png#token)
*Medium humanoid (any race), Any alignment*

- **Armor Class** 11 
- **Hit Points** 9 (`2d8`)
- **Speed** 30 ft.

|STR|DEX|CON|INT|WIS|CHA|
|:---:|:---:|:---:|:---:|:---:|:---:|
|11 (+0)|13 (+1)|10 (+0)|14 (+2)|14 (+2)|12 (+1)|

- **Proficiency Bonus** +2
- **Saving Throws** ⏤
- **Skills** Arcana +4
- **Senses** passive Perception 12
- **Languages** Common plus any two languages
- **Challenge** 0

***Spellcasting.*** The magewright's spellcasting ability is Intelligence (spell save DC 12). To cast one of its rituals, the magewright must provide additional material components whose value in gold pieces is 20 times the spell's level. These components are consumed when the ritual is finished. The magewright knows the following spells:

**At will**: [mage hand](compendium/spells/mage-hand.md), [prestidigitation](compendium/spells/prestidigitation.md)

## Actions

***Dagger.*** *Melee or Ranged Weapon Attack:* +3 to hit, reach 5 ft. or range 20/60 ft., one target. *Hit:* 3 (`1d4 + 1`) piercing damage.
```
^statblock