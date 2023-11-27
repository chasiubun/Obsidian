---
obsidianUIMode: preview
cssclasses: json5e-monster
tags:
- compendium/src/5e/mpmm
- monster/cr/9
- monster/environment/desert
- monster/environment/urban
- monster/size/medium
- monster/type/humanoid/cleric
aliases: ["War Priest"]
---
# War Priest
*Source: Mordenkainen Presents: Monsters of the Multiverse p. 254, Volo's Guide to Monsters p. 218*  

War priests worship deities of war, protection, and strategy. They plan tactics, lead soldiers into battle, confront enemy spellcasters, and tend to casualties. A war priest might command an army or serve as the right hand of a [warlord](b_warlord-mpmm.md) (appears in "this book") on the battlefield.

War priests typically adorn themselves with a symbol of their faith. You can roll on the War Priest Holy Symbols table below, or choose one that fits your campaign.

**War Priest Holy Symbols**

| dice: d8 | Holy Symbol |
|----------|-------------|
| 1 | Vial of iridescent liquid |
| 2 | Hilt of a broken sword |
| 3 | Piece of stained glass from a shrine |
| 4 | Clay figurine of a [ki-rin](2.%20GM%20Tools/5eTools%20Compendium%20&%20Rules/z_compendium/bestiary/celestial/b_ki-rin-mpmm.md) or another Celestial |
| 5 | [Torch](torch.md) carved so that a hand appears to be holding the flame |
| 6 | Circlet of woven reeds |
| 7 | Scrimshawed bone |
| 8 | Vessel such as a cup, a [jug](jug.md), an urn, or an amphora |
^war-priest-holy-symbols

```ad-statblock
title: War Priest
![](compendium/bestiary/humanoid/token/war-priest.png#token)
*Medium humanoid (cleric), Any alignment*

- **Armor Class** 18  ([plate](compendium/items/plate-armor.md))
- **Hit Points** 117 (`18d8 + 36`)
- **Speed** 30 ft.

|STR|DEX|CON|INT|WIS|CHA|
|:---:|:---:|:---:|:---:|:---:|:---:|
|16 (+3)|10 (+0)|14 (+2)|11 (+0)|17 (+3)|13 (+1)|

- **Proficiency Bonus** +4
- **Saving Throws** Constitution +6, Wisdom +7
- **Skills** Intimidation +5, Religion +4
- **Senses** passive Perception 13
- **Languages** any two languages
- **Challenge** 9

***Spellcasting.*** The war priest casts one of the following spells, using Wisdom as the spellcasting ability (spell save DC 15):

**At will**: [light](compendium/spells/light.md), [spare the dying](compendium/spells/spare-the-dying.md), [thaumaturgy](compendium/spells/thaumaturgy.md)

**1/day each**: [banishment](compendium/spells/banishment.md), [command](compendium/spells/command.md), [dispel magic](compendium/spells/dispel-magic.md), [flame strike](compendium/spells/flame-strike.md), [guardian of faith](compendium/spells/guardian-of-faith.md), [hold person](compendium/spells/hold-person.md), [lesser restoration](compendium/spells/lesser-restoration.md), [revivify](compendium/spells/revivify.md)

## Actions

***Multiattack.*** The war priest makes two Maul attacks, and it uses Holy Fire.

***Maul.*** *Melee Weapon Attack:* +7 to hit, reach 5 ft., one target. *Hit:* 10 (`2d6 + 3`) bludgeoning damage  plus *Hit:* 10 (`3d6`) radiant damage.

***Holy Fire.*** The war priest targets one creature it can see within 60 feet of it. The target must make a DC 15 Wisdom saving throw. On a failed save, the target takes 12 (`2d8 + 3`) radiant damage, and it is [blinded](rules/conditions.md#blinded) until the start of the war priest's next turn. On a successful save, the target takes half as much damage and isn't [blinded](rules/conditions.md#blinded).

## Bonus Actions

***Healing Light (Recharge 4-6).*** The war priest or one creature of its choice within 60 feet of it regains 12 (`2d8 + 3`) hit points.
```
^statblock

## Environment

desert, urban