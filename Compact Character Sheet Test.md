---
Proficiency: 1
totalLevel: ""
art: z_Assets/Torston1.png
sca_temp: 0
sca: ""
---
`VIEW[round(floor(({totalLevel}+7)/4),0)][math(hidden):Proficiency]`

> [!metadata|]- Metadata 
> #### System
>  |
> ---|---|
> **Tags** | `INPUT[Tags][inlineListSuggester:tags]` |
> ##### `=this.file.name` Info
>  |
> ---|---|
>**Race** | `INPUT[suggester(optionQuery("z_compendium/races"), useLinks(false)):Race]` |
>**Class** | `INPUT[suggester(optionQuery(#class), useLinks(false)):Class]` |
>**SubClass** | `INPUT[suggester(optionQuery(#subclass), useLinks(false)):SubClass]`
>**Background** | `INPUT[suggester(optionQuery("z_compendium/background"), useLinks(false)):Background]` |
>| **Immunities** | `INPUT[inlineListSuggester(option(Blinded), option(Charmed), option(Deafened), option(Frightened), option(Grappled), option(Incapacitated), option(Invisible), option(Paralyzed), option(Petrified), option(Poisoned), option(Prone), option(Restrained), option(Stunned), option(Unconscious), option(Sleep), option(Magical Sleep), option(Fire), option(Cold), option(Thunder), option(Lightning), option(Acid), option(Necrotic), option(Radiant), option(Force), option(Poison)):Immunities]` |
>| **Resistance** | `INPUT[inlineListSuggester(option(Blinded), option(Charmed), option(Deafened), option(Frightened), option(Grappled), option(Incapacitated), option(Invisible), option(Paralyzed), option(Petrified), option(Poisoned), option(Prone), option(Restrained), option(Stunned), option(Unconscious), option(Sleep), option(Magical Sleep), option(Fire), option(Cold), option(Thunder), option(Lightning), option(Acid), option(Necrotic), option(Radiant), option(Force), option(Poison)):Resistance]` |
>**Languages** | `INPUT[inlineListSuggester(option(Common), option(Dwarvish), option(Elvish), option(Giant), option(Gnomish), option(Goblin), option(Halfling), option(Orc), option(Abyssal), option(Celestial), option(Draconic), option(Deep Speech), option(Infernal), option(Primordial), option(Sylvan), option(Undercommon)):Languages]`|
>**Armor Proficiency**| `INPUT[inlineListSuggester(option(Light Armor), option(Medium Armor), option(Heavy Armor), option(Shield)):ProfArmor]`|
>**Weapon Proficiency** | `INPUT[inlineListSuggester(optionQuery(#item/weapon), useLinks(false)):WeaponProf]` `INPUT[inlineListSuggester(option(Simple Weapons), option(Martial Weapons)):ProfWeaponType]`  |
>**Gear and Tool Proficiency** | `INPUT[inlineListSuggester(optionQuery(#item/gear), useLinks(false)):ProfGear]`|
> #### Bio
>  |
> ---|---|
> **Art** | `INPUT[imageSuggester(optionQuery("z_Assets")):art]` |
> #### Info
>  |
> ---|---|

> [!infobox|]+
> # Stats
> Stat| \# | Stat | \# |
> ---|---|---|---|
>💪 STR|`INPUT[number(class(my-mb-css)):Strength]`|🧠 INT|`INPUT[number(class(my-mb-css)):Intelligence]`|
>🤸‍♂️ DEX|`INPUT[number(class(my-mb-css)):Dexterity]`|🦉 WIS|`INPUT[number(class(my-mb-css)):Wisdom]`|
>🍖 CON|`INPUT[number(class(my-mb-css)):Constitution]`|😎 CHA|`INPUT[number(class(my-mb-css)):Charisma]`|
> # Saving Throws
> Stat | Prof | \# | Stat | Prof | \# |
> ---|---|---|---|---|---|
> STR | `INPUT[toggle:Prof_Strength]` | `VIEW[round(floor(({Strength} - 10) / 2) + ({Prof_Strength} ? {Proficiency} : 0))]` | INT | `INPUT[toggle:Prof_Intelligence]` | `VIEW[round(floor(({Intelligence} - 10) / 2) + ({Prof_Intelligence} ? {Proficiency} : 0))]`| 
> DEX | `INPUT[toggle:Prof_Dexterity]`    | `VIEW[round(floor(({Dexterity} - 10) / 2) + ({Prof_Dexterity} ? {Proficiency} : 0))]` | WS | `INPUT[toggle:Prof_Wisdom]` | `VIEW[round(floor(({Wisdom} - 10) / 2) + ({Prof_Wisdom} ? {Proficiency} : 0))]`| 
> CON | `INPUT[toggle:Prof_Constitution]` | `VIEW[round(floor(({Constitution} - 10) / 2) + ({Prof_Constitution} ? {Proficiency} : 0))]` | CHA | `INPUT[toggle:Prof_Charisma]` | `VIEW[round(floor(({Charisma} - 10) / 2) + ({Prof_Charisma} ? {Proficiency} : 0))]`| 
> # Skills
> Skill |  | # | Skill |  | # |
> ---|---|---|---|---|---|
> Acro | `INPUT[toggle:Prof_Acrobatics]`| `VIEW[round(floor(({Dexterity} - 10) / 2) + ({Prof_Acrobatics} ? {Proficiency} : 0))]` | Med | `INPUT[toggle:Prof_Medicine]` | `VIEW[round(floor(({Wisdom} - 10) / 2) + ({Prof_Medicine} ? {Proficiency} : 0))]`
> Ani | `INPUT[toggle:Prof_AnimalHandling]` | `VIEW[round(floor(({Wisdom} - 10) / 2) + ({Prof_AnimalHandling} ? {Proficiency} : 0))]` | Nat | `INPUT[toggle:Prof_Nature]`| `VIEW[round(floor(({Intelligence} - 10) / 2) + ({Prof_Nature} ? {Proficiency} : 0))]`   |
> Arc | `INPUT[toggle:Prof_Arcane]`   | `VIEW[round(floor(({Intelligence} - 10) / 2) + ({Prof_Arcane} ? {Proficiency} : 0))]` | Perc | `INPUT[toggle:Prof_Perception]`   | `VIEW[round(floor(({Wisdom} - 10) / 2) + ({Prof_Perception} ? {Proficiency} : 0))]` | 
> Ath | `INPUT[toggle:Prof_Athletics]`   | `VIEW[round(floor(({Strength} - 10) / 2) + ({Prof_Athletics} ? {Proficiency} : 0))]` | Perf | `INPUT[toggle:Prof_Performance]`   | `VIEW[round(floor(({Wisdom} - 10) / 2) + ({Prof_Performance} ? {Proficiency} : 0))]` |
> Dec | `INPUT[toggle:Prof_Deception]`   | `VIEW[round(floor(({Charisma} - 10) / 2) + ({Prof_Deception} ? {Proficiency} : 0))]` | Pers | `INPUT[toggle:Prof_Persuasion]`   | `VIEW[round(floor(({Charisma} - 10) / 2) + ({Prof_Persuasion} ? {Proficiency} : 0))]` |
> His | `INPUT[toggle:Prof_History]`   | `VIEW[round(floor(({Intelligence} - 10) / 2) + ({Prof_History} ? {Proficiency} : 0))]` | Rel | `INPUT[toggle:Prof_Religion]`   | `VIEW[round(floor(({Intelligence} - 10) / 2) + ({Prof_Religion} ? {Proficiency} : 0))]` |
> Ins | `INPUT[toggle:Prof_Insight]`  | `VIEW[round(floor(({Wisdom} - 10) / 2) + ({Prof_Insight} ? {Proficiency} : 0))]` | SoH |`INPUT[toggle:Prof_SleightOfHand]`  | `VIEW[round(floor(({Dexterity} - 10) / 2) + ({Prof_SleightOfHand} ? {Proficiency} : 0))]` |
> Int | `INPUT[toggle:Prof_Intimidation]`   | `VIEW[round(floor(({Charisma} - 10) / 2) + ({Prof_Intimidation} ? {Proficiency} : 0))]` | Ste | `INPUT[toggle:Prof_Stealth]`  | `VIEW[round(floor(({Dexterity} - 10) / 2) + ({Prof_Stealth} ? {Proficiency} : 0))]` |
> Inv | `INPUT[toggle:Prof_Investigation]`  | `VIEW[round(floor(({Intelligence} - 10) / 2) + ({Prof_Investigation} ? {Proficiency} : 0))]` | Sur | `INPUT[toggle:Prof_Survival]`  | `VIEW[round(floor(({Wisdom} - 10) / 2) + ({Prof_Survival} ? {Proficiency} : 0))]` |
>###### Passive
>|                                                               Passive Per                                                               |                                                                         Passive Inv                                                                         |                                                            Passive Ins                                                             |
>|:------------------------------------------------------------------------------------------------------------------------------------:|:------------------------------------------------------------------------------------------------------------------------------------------------------------:|:------------------------------------------------------------------------------------------------------------------------------:|
>| `VIEW[round(10 + floor(({Wisdom} - 10) / 2) + ({Prof_Wisdom} ? {Proficiency} : 0) + {Prof_Persuasion} * {Proficiency}, 0)]` | `VIEW[round(10 + floor(({Intelligence} - 10) / 2) + ({Prof_Intelligence} ? {Proficiency} : 0) + {Prof_Investigation} * {Proficiency}, 0)]` | `VIEW[round(10 + floor(({Wisdom} - 10) / 2) + ({Prof_Wisdom} ? {Proficiency} : 0) + {Prof_Insight} * {Proficiency}, 0)]` |
> # SpellCasting
> | |
> |---|---|
> Spellcasting Ability | `INPUT[inlineSelect(option(0, -), option(1, INT), option(2, WIS), option(3, CHA)):sca_temp]` `VIEW[{sca_temp} == 0 ? False : ({sca_temp} == 1 ? {Intelligence} : ({sca_temp} == 2 ? {Wisdom} : {Charisma}))][math(hidden):sca]`
> Spell Save DC | `VIEW[{sca_temp} == 0 ? "None" : 8+{Proficiency}+round(floor(({sca}-10)/2),0)]` |
> Spell Atk. Mod. | `VIEW[{sca_temp} == 0 ? "None" : {Proficiency}+round(floor(({sca}-10)/2),0)]`|


> [!infobox]+
> ###### `=this.file.name` (Total level: `VIEW[{classLevel1}][:totalLevel]`)
>  |
> ---|---|
>|🎚️**Level** | `INPUT[inlineSelect(option(1), option(2), option(3), option(4), option(5), option(6), option(7), option(8), option(9), option(10), option(11), option(12), option(13), option(14), option(15), option(16), option(17), option(18), option(19), option(20)):classLevel1]` |
>|🏹**Race** | `VIEW[{Race}][link]` |
>|⚔️**Class** | `VIEW[{Class}][link]` |
>|⚔️**SubClass**| `VIEW[{SubClass}][link]` |
>|🌄**Background** | `VIEW[{Background}][link]` |
>|💖**Health:** |  `INPUT[number(class(my-mb-css)):HP]` |
>|💝**Temp Hp** | `INPUT[number(class(my-mb-css)):TempHP]` |
>|🛡**AC:** | `INPUT[number(class(my-mb-css)):AC]` |
>|⏱️**Initiative:** | `VIEW[floor(({Dexterity}-10)/2)]` |
>|🎲**Hit Dice:** | `INPUT[text(placeholder(Hitdice), class(my-mb-css-text)):HitDice]` |
>|🎓**Proficiency:** | `VIEW[{Proficiency}]` |
>|🚶**Movement:** | `INPUT[number(class(my-mb-css)):Movement]` ft. |
>|🪽**Flying** | `INPUT[number(class(my-mb-css)):Flying]` ft. |
>|🏊**Swimming:** | `INPUT[number(class(my-mb-css)):Swimming]` ft.|
> ###### Defenses
>| Defenses | Types |
>|:---:|:----:|
>|🚫Immunities | `VIEW[{Immunities}][text(renderMarkdown)]` |
>|🧱Resistance | `VIEW[{Resistance}][text(renderMarkdown)]` |
>
>| | |  |
>|:--:|:----:|---|
>|`INPUT[inlineSelect(option(0, -), option(11.001, Padded), option(11.002, Leather), option(12.001, Studded L), option(12.002, +1 Padded), option(12.003, +1 Leather), option(13.001, +1 Studded L), option(13.002, +2 Padded), option(13.003, +2 Leather), option(14.001, +2 Studded L), option(14.002, +3 Padded), option(14.003, +3 Leather), option(15.001, +3 Studded L), option(12.004, Hide), option(13.004, Chain Shirt), option(14.004, Scale Mail), option(14.005, BreastPlate), option(15.002, Half Plate), option(13.005, +1 Hide), option(14.006, +1 Chain Shirt), option(15.003, +1 Scale Mail), option(15.004, +1 BreastPlate), option(16.001, +1 Half Plate), option(14.007, +2 Hide), option(15.005, +2 Chain Shirt), option(16.002, +2 Scale Mail), option(16.003, +2 BreastPlate), option(17.001, +2 Half Plate), option(15.006, +3 Hide), option(16.004, +3 Chain Shirt), option(17.002, +3 Scale Mail), option(17.003, +3 BreastPlate), option(18.001, +3 Half Plate), option(14.008, Ring Mail), option(16.005, Chain Mail), option(17.004, Splint), option(18.002, Plate), option(15.007, +1 Ring Mail), option(17.005, +1 Chain Mail), option(18.003, +1 Splint), option(19.001, +1 Plate), option(16.006, +2 Ring Mail), option(18.004, +2 Chain Mail), option(19.002, +2 Splint), option(20.001, +2 Plate), option(17.006, +3 Ring Mail), option(19.003, +3 Chain Mail), option(20.002, +3 Splint), option(21.001, +3 Plate)):Armor]`|  |`VIEW[round({Armor})]`
>|`INPUT[inlineSelect(option(0, -), option(2.001, Shield), option(3.001, +1 Shield), option(4.001, +2 Shield), option(5.001, +3 Shield)):Shield]`| `INPUT[toggle:Shield_On]` | `VIEW[round({Shield})]`
>|Stealth Disadvantage |`INPUT[toggle:Dis_Stealth]` 
>###### Proficiencies
>| | |
>|---|---|
>| Languages | `VIEW[{Languages}][text(renderMarkdown)]`|
>| Armor | `VIEW[{ProfArmor}][text(renderMarkdown)]` |
>|Weapons | `VIEW[{WeaponProf}][text(renderMarkdown)]` `VIEW[{ProfWeaponType}][text(renderMarkdown)]` |
>|Gear / Tools| `VIEW[{ProfGear}][text(renderMarkdown)]`

> [!infobox]+
> # `=this.file.name`
> `VIEW[!\[\[{art}\]\]][text(renderMarkdown)]`
> ###### Bio
>  |
> ---|---|
> 
> ###### Info
>  |
> ---|---|


> [!metadata|]- Class Features
> `VIEW[!\[\[{Class}\]\]][text(renderMarkdown)]`

> [!metadata|]- SubClass Features
> `VIEW[!\[\[{SubClass}\]\]][text(renderMarkdown)]`