---
Proficiency: 1
totalLevel: ""
---
`VIEW[round(floor(({totalLevel}+7)/4),0)][math(hidden):Proficiency]`
`VIEW[{classLevel1}][math(hidden):totalLevel]`

> [!column| 3 no-t] At a Clance
>> [!metadata|bg-c-red] Info
>> 
>> |Type | # |
>>|---|----|
>>|🎚️ **Level** | `INPUT[inlineSelect(option(1), option(2), option(3), option(4), option(5), option(6), option(7), option(8), option(9), option(10), option(11), option(12), option(13), option(14), option(15), option(16), option(17), option(18), option(19), option(20)):classLevel1]` |
>>|🏹 **Race** | `INPUT[suggester(optionQuery("z_compendium/races")):Race]`  |
>>|⚔️ **Class** | `INPUT[suggester(optionQuery(#class)):Class]` |
>>| ⚔️**SubClass** | `INPUT[suggester(optionQuery(#subclass)):SubClass]`
>>|🌄 **Background** | `INPUT[suggester(optionQuery("z_compendium/background")):Background]` |
>>| 💖 **Health:** |  `INPUT[number(class(my-mb-css)):HP]` |
>>|💝**Temp Hp** | `INPUT[number(class(my-mb-css)):TempHP]` |
>>| 🛡️**AC:** | `INPUT[number(class(my-mb-css)):AC]` |
>>| ⏱️ **Initiative:** | `VIEW[floor(({Dexterity}-10)/2)]` |
>>| 🎲 **Hit Dice:** | `INPUT[text(placeholder(Hitdice), class(my-mb-css-text)):HitDice]` |
>>| 🎓**Proficiency:** | `VIEW[{Proficiency}]` |
>>| 🚶**Movement:** | `INPUT[number(class(my-mb-css)):Movement]` ft. |
>>| 🪽 **Flying** | `INPUT[number(class(my-mb-css)):Flying]` ft. |
>>| 🏊 **Swimming:** | `INPUT[number(class(my-mb-css)):Swimming]` ft.|
>>
>>| Defenses | Types |
>>|:---:|:----:|
>>| 🚫Immunities | `INPUT[inlineListSuggester(option(Blinded), option(Charmed), option(Deafened), option(Frightened), option(Grappled), option(Incapacitated), option(Invisible), option(Paralyzed), option(Petrified), option(Poisoned), option(Prone), option(Restrained), option(Stunned), option(Unconscious), option(Sleep), option(Magical Sleep), option(Fire), option(Cold), option(Thunder), option(Lightning), option(Acid), option(Necrotic), option(Radiant), option(Force), option(Poison)):Immunities]` |
>>| 🧱Resistance | `INPUT[inlineListSuggester(option(Blinded), option(Charmed), option(Deafened), option(Frightened), option(Grappled), option(Incapacitated), option(Invisible), option(Paralyzed), option(Petrified), option(Poisoned), option(Prone), option(Restrained), option(Stunned), option(Unconscious), option(Sleep), option(Magical Sleep), option(Fire), option(Cold), option(Thunder), option(Lightning), option(Acid), option(Necrotic), option(Radiant), option(Force), option(Poison)):Resistance]` |
>>
>>
>>|                                                               Passive Perception                                                               |                                                                         Passive Investigation                                                                         |                                                            Passive Insight                                                             |
>>|:------------------------------------------------------------------------------------------------------------------------------------:|:------------------------------------------------------------------------------------------------------------------------------------------------------------:|:------------------------------------------------------------------------------------------------------------------------------:|
>>| `VIEW[round(10 + floor(({Wisdom} - 10) / 2) + ({Prof_Wisdom} ? {Proficiency} : 0) + {PerPro} * {Proficiency}, 0)]` | `VIEW[round(10 + floor(({Intelligence} - 10) / 2) + ({Prof_Intelligence} ? {Proficiency} : 0) + {InvPro} * {Proficiency}, 0)]` | `VIEW[round(10 + floor(({Wisdom} - 10) / 2) + ({Prof_Wisdom} ? {Proficiency} : 0) + {InsPro} * {Proficiency}, 0)]` |
>>
>> |  Stat   |                  #                   |           Modifier            | Saving Throws | Prof 
>> |:-------:|:------------------------------------:|:-----------------------------:|:-----------------------------:|:-----------------------------:|
>> | 💪**STR** |   `INPUT[number(class(my-mb-css)):Strength]`   |   `VIEW[floor(({Strength}-10)/2)]`   | `VIEW[round(floor(({Strength} - 10) / 2) + ({Prof_Strength} ? {Proficiency} : 0))]` | `INPUT[toggle:Prof_Strength]`
>> | 🤸‍♂️**DEX** |  `INPUT[number(class(my-mb-css)):Dexterity]`   |  `VIEW[floor(({Dexterity}-10)/2)]`   | `VIEW[round(floor(({Dexterity} - 10) / 2) + ({Prof_Dexterity} ? {Proficiency} : 0))]` | `INPUT[toggle:Prof_Dexterity]`
>> | 🍖**CON** | `INPUT[number(class(my-mb-css)):Constitution]` | `VIEW[floor(({Constitution}-10)/2)]` | `VIEW[round(floor(({Constitution} - 10) / 2) + ({Prof_Constitution} ? {Proficiency} : 0))]` | `INPUT[toggle:Prof_Constitution]`
>> | 🧠**INT** | `INPUT[number(class(my-mb-css)):Intelligence]` | `VIEW[floor(({Intelligence}-10)/2)]` | `VIEW[round(floor(({Intelligence} - 10) / 2) + ({Prof_Intelligence} ? {Proficiency} : 0))]` | `INPUT[toggle:Prof_Intelligence]`
>> | 🦉**WIS** |    `INPUT[number(class(my-mb-css)):Wisdom]`    |    `VIEW[floor(({Wisdom}-10)/2)]`    | `VIEW[round(floor(({Wisdom} - 10) / 2) + ({Prof_Wisdom} ? {Proficiency} : 0))]` | `INPUT[toggle:Prof_Wisdom]`
>> | 😎**CHA** |   `INPUT[number(class(my-mb-css)):Charisma]`   |   `VIEW[floor(({Charisma}-10)/2)]`   | `VIEW[round(floor(({Charisma} - 10) / 2) + ({Prof_Charisma} ? {Proficiency} : 0))]` | `INPUT[toggle:Prof_Charisma]`
>
>> [!metadata|] Stats
>>
>>| Stat |   Skill    |                                  #                                   |                                                                   Prof/Exp                                                                    |              Adv               |              Dis               |
>>|:----:|:----------:|:--------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------------------------------:|:------------------------------:|:------------------------------:|
>> DEX  | Acrobatics | `VIEW[round(floor(({Dexterity}-10)/2) + {AcroPro}*{Proficiency},0)]` | `INPUT[slider(minValue(0), maxValue(2)):AcroPro]` `VIEW[{AcroPro} == 1 ? "Proficiency." : ({AcroPro} == 2 ? "Expertise": "No Proficiency.")]` | `INPUT[toggle:Adv_Acrobatics]` | `INPUT[toggle:Dis_Acrobatics]` |
>> WIS | Animal Handling       | `VIEW[round(floor(({Wisdom}-10)/2) + {AniPro}*{Proficiency},0)]` | `INPUT[slider(minValue(0), maxValue(2)):AniPro]` `VIEW[{AniPro} == 1 ? "Proficiency." : ({AniPro} == 2 ? "Expertise": "No Proficiency.")]` | `INPUT[toggle:Adv_AnimalHandling]` |  `INPUT[toggle:Dis_AnimalHandling]`
>> INT | Arcane       | `VIEW[round(floor(({Intelligence}-10)/2) + {ArcPro}*{Proficiency},0)]` | `INPUT[slider(minValue(0), maxValue(2)):ArcPro]` `VIEW[{ArcPro} == 1 ? "Proficiency." : ({ArcPro} == 2 ? "Expertise": "No Proficiency.")]` |`INPUT[toggle:Adv_Arcane]`  |`INPUT[toggle:Dis_Arcane]`
>> STR | Athletics       | `VIEW[round(floor(({Strength}-10)/2) + {AthPro}*{Proficiency},0)]` | `INPUT[slider(minValue(0), maxValue(2)):AthPro]` `VIEW[{AthPro} == 1 ? "Proficiency." : ({AthPro} == 2 ? "Expertise": "No Proficiency.")]` |`INPUT[toggle:Adv_Athletics]` |  `INPUT[toggle:Dis_Athletics]`
>> CHA | Deception       | `VIEW[round(floor(({Charisma}-10)/2) + {DecPro}*{Proficiency},0)]` | `INPUT[slider(minValue(0), maxValue(2)):DecPro]` `VIEW[{DecPro} == 1 ? "Proficiency." : ({DecPro} == 2 ? "Expertise": "No Proficiency.")]` |`INPUT[toggle:Adv_Deception]`  |`INPUT[toggle:Dis_Deception]`
>> INT | History       | `VIEW[round(floor(({Intelligence}-10)/2) + {HisPro}*{Proficiency},0)]` | `INPUT[slider(minValue(0), maxValue(2)):HisPro]` `VIEW[{HisPro} == 1 ? "Proficiency." : ({HisPro} == 2 ? "Expertise": "No Proficiency.")]` |`INPUT[toggle:Adv_History]`  |`INPUT[toggle:Dis_History]`
>> WIS | Insight      | `VIEW[round(floor(({Wisdom}-10)/2) + {InsPro}*{Proficiency},0)]` | `INPUT[slider(minValue(0), maxValue(2)):InsPro]` `VIEW[{InsPro} == 1 ? "Proficiency." : ({InsPro} == 2 ? "Expertise": "No Proficiency.")]` |`INPUT[toggle:Adv_Insight]`  |`INPUT[toggle:Dis_Insight]`
>> CHA | Intimidation       | `VIEW[round(floor(({Charisma}-10)/2) + {ItmPro}*{Proficiency},0)]` | `INPUT[slider(minValue(0), maxValue(2)):ItmPro]` `VIEW[{ItmPro} == 1 ? "Proficiency." : ({ItmPro} == 2 ? "Expertise": "No Proficiency.")]` |`INPUT[toggle:Adv_Intimidation]`  | `INPUT[toggle:Dis_Intimidation]`
>> INT | Investigation | `VIEW[round(floor(({Intelligence}-10)/2) + {InvPro}*{Proficiency},0)]` | `INPUT[slider(minValue(0), maxValue(2)):InvPro]` `VIEW[{InvPro} == 1 ? "Proficiency." : ({InvPro} == 2 ? "Expertise": "No Proficiency.")]` |`INPUT[toggle:Adv_Investigation]` | `INPUT[toggle:Dis_Investigation]`
>> WIS | Medicine      | `VIEW[round(floor(({Wisdom}-10)/2) + {MedPro}*{Proficiency},0)]` | `INPUT[slider(minValue(0), maxValue(2)):MedPro]` `VIEW[{MedPro} == 1 ? "Proficiency." : ({MedPro} == 2 ? "Expertise": "No Proficiency.")]` |`INPUT[toggle:Adv_Medicine]`  |`INPUT[toggle:Dis_Medicine]`
>> INT | Nature       | `VIEW[round(floor(({Intelligence}-10)/2) + {NatPro}*{Proficiency},0)]` | `INPUT[slider(minValue(0), maxValue(2)):NatPro]` `VIEW[{NatPro} == 1 ? "Proficiency." : ({NatPro} == 2 ? "Expertise": "No Proficiency.")]` |`INPUT[toggle:Adv_Nature]`  |`INPUT[toggle:Dis_Nature]`
>> WIS | Perception      | `VIEW[round(floor(({Wisdom}-10)/2) + {PerPro}*{Proficiency},0)]` | `INPUT[slider(minValue(0), maxValue(2)):PerPro]` `VIEW[{PerPro} == 1 ? "Proficiency." : ({PerPro} == 2 ? "Expertise": "No Proficiency.")]` |`INPUT[toggle:Adv_Perception]`  |`INPUT[toggle:Dis_Perception]`
>> CHA | Performance       | `VIEW[round(floor(({Wisdom}-10)/2) + {PrfPro}*{Proficiency},0)]` | `INPUT[slider(minValue(0), maxValue(2)):PrfPro]` `VIEW[{PrfPro} == 1 ? "Proficiency." : ({PrfPro} == 2 ? "Expertise": "No Proficiency.")]` |`INPUT[toggle:Adv_Performance]`  |`INPUT[toggle:Dis_Performance]`
>> CHA | Persuasion       | `VIEW[round(floor(({Charisma}-10)/2) + {PssPro}*{Proficiency},0)]` | `INPUT[slider(minValue(0), maxValue(2)):PssPro]` `VIEW[{PssPro} == 1 ? "Proficiency." : ({PssPro} == 2 ? "Expertise": "No Proficiency.")]`|`INPUT[toggle:Adv_Persuasion]`  |`INPUT[toggle:Dis_Persuasion]`
>> INT | Religion       | `VIEW[round(floor(({Intelligence}-10)/2) + {RelPro}*{Proficiency},0)]` | `INPUT[slider(minValue(0), maxValue(2)):RelPro]` `VIEW[{RelPro} == 1 ? "Proficiency." : ({RelPro} == 2 ? "Expertise": "No Proficiency.")]` |`INPUT[toggle:Adv_Religion]` | `INPUT[toggle:Dis_Religion]`
>> DEX | Sleight of Hand       | `VIEW[round(floor(({Dexterity}-10)/2) + {SohPro}*{Proficiency},0)]` | `INPUT[slider(minValue(0), maxValue(2)):SohPro]` `VIEW[{SohPro} == 1 ? "Proficiency." : ({SohPro} == 2 ? "Expertise": "No Proficiency.")]` |`INPUT[toggle:Adv_SleightOfHand]` | `INPUT[toggle:Dis_SleightOfHand]`
>> DEX | Stealth      | `VIEW[round(floor(({Dexterity}-10)/2) + {StlPro}*{Proficiency},0)]` | `INPUT[slider(minValue(0), maxValue(2)):StlPro]` `VIEW[{StlPro} == 1 ? "Proficiency." : ({StlPro} == 2 ? "Expertise": "No Proficiency.")]` |`INPUT[toggle:Adv_Stealth]`  |`INPUT[toggle:Dis_Stealth]`
>> WIS | Survival      | `VIEW[round(floor(({Wisdom}-10)/2) + {SurPro}*{Proficiency},0)]` | `INPUT[slider(minValue(0), maxValue(2)):SurPro]` `VIEW[{SurPro} == 1 ? "Proficiency." : ({SurPro} == 2 ? "Expertise": "No Proficiency.")]` |`INPUT[toggle:Adv_Survival]`  |`INPUT[toggle:Dis_Survival]`
>>
>
>> [!metadata| txt-c bg-c-green] Proficiencies
>> 
>> | Languages |
>> |:-------------:|
>> |`INPUT[inlineListSuggester(option(Common), option(Dwarvish), option(Elvish), option(Giant), option(Gnomish), option(Goblin), option(Halfling), option(Orc), option(Abyssal), option(Celestial), option(Draconic), option(Deep Speech), option(Infernal), option(Primordial), option(Sylvan), option(Undercommon)):Languages]` |
>>---
>> | [Light Armor](armor-and-shields-armor.md#^armor) | [Medium Armor](armor-and-shields-armor.md#^armor) | [Heavy Armor](armor-and-shields-armor.md#^armor) | [Shield](armor-and-shields-armor.md#^armor)
>> |:----:|:----:|:-----:|:----:|
>> | `INPUT[toggle:Has_LightArmorProf]` | `INPUT[toggle:Has_MediumArmorProf]` | `INPUT[toggle:Has_HeavyArmorProf]`| `INPUT[toggle:Has_ShieldProf]`
>>---
>> | Simple | Martial|
>> |:-----:|:----:|
>> |`INPUT[toggle:Has_SimpleWProf]`  | `INPUT[toggle:Has_MartialWProf]` |
>>---
>> | [Weapons](weapons.md#^Weapons) |
>> |:----:|
>> |`INPUT[inlineListSuggester(optionQuery(#item/weapon)):WeaponProf]` |
>>---
>> | [Tools](tools.md#^item-cost-weight) / [Gear](adventuring-gear.md#^adventuring-gear) |
>> |:----:|
>> |`INPUT[inlineListSuggester(optionQuery(#item/gear)):Gear]`  |
>>---
>>|                                                                                                                                                                        Senses                                                                                                                                                                         |
>>|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|
>>| `INPUT[inlineListSuggester(option(Darkvision), option(Superior Darkvision), option(Blindsight), option(Tremorsense), option(Truesight), option(Devils Sight), option(Feral Senses), option(Eldritch Sight), option(See Invisibility), option(Blindsense), option(Eyes of the Rune Keeper), option(Lay on Hands), option(Primeval Awareness)):Senses]` |
>
>> [!metadata|no-t bg-c-purple] 
>>**Armor**
>>
>>|  Type |  Armor  | AC |
>>|:--:|:-------:|:----:|
>>| **Light Armor** | `INPUT[inlineSelect(option(0, -), option(11.001, Padded), option(11.002, Leather), option(12.001, Studded Leather), option(12.003, +1 Padded), option(12.004, +1 Leather), option(13.002, +1 Studded Leather), option(13.004, +2 Padded), option(13.005, +2 Leather), option(14.005, +2 Studded Leather), option(14.006, +3 Padded), option(14.007, +3 Leather), option(15.005, +3 Studded Leather)):LightArmor]`| `VIEW[round({LightArmor})]` |
>>| **Medium Armor** | `INPUT[inlineSelect(option(0, -), option(12.002, Hide), option(13.001, Chain Shirt), option(14.001, Scale Mail), option(14.002, BreastPlate), option(15.001, Half Plate), option(13.003, +1 Hide), option(14.004, +1 Chain Shirt), option(15.002, +1 Scale Mail), option(15.003, +1 BreastPlate), option(16.002, +1 Half Plate), option(14.006, +2 Hide), option(15.005, +2 Chain Shirt), option(16.003, +2 Scale Mail), option(16.004, +2 BreastPlate), option(17.003, +2 Half Plate), option(15.006, +3 Hide), option(16.006, +3 Chain Shirt), option(17.004, +3 Scale Mail), option(17.006, +3 BreastPlate), option(18.003, +3 Half Plate)):MediumArmor]`  | `VIEW[round({MediumArmor})]` |
>>| **Heavy Armor** |  `INPUT[inlineSelect(option(0, -), option(14.003, Ring Mail), option(16.001, Chain Mail), option(17.001, Splint), option(18.001, Plate), option(15.004, +1 Ring Mail), option(17.002, +1 Chain Mail), option(18.002, +1 Splint), option(19.001, +1 Plate), option(16.005, +2 Ring Mail), option(18.003, +2 Chain Mail), option(19.003, +2 Splint), option(20.001, +2 Plate), option(17.005, +3 Ring Mail), option(19.002, +3 Chain Mail), option(20.002, +3 Splint), option(21.001, +3 Plate)):HeavyArmor]` | `VIEW[round({HeavyArmor})]`
>>|**Shield** | `INPUT[inlineSelect(option(0, -), option(2.001, Shield), option(3.001, +1 Shield), option(4.001, +2 Shield), option(5.001, +3 Shield)):Shield]` | `VIEW[round({Shield})]`
>>
>>|Stealth Dis | Armor On | Shield On
>>|:--:|:----:|:---:|
>>|`INPUT[toggle:Dis_Stealth]` | `INPUT[toggle:Armor_On]` | `INPUT[toggle:Shield_On]` | 
>>**Bag**
>>
>>| Weapons |
>>|---|
>>|`INPUT[inlineListSuggester(optionQuery(#item/weapon)):Has_Weapon]` |
>
>>[!metadata|bg-c-pink] Spells/Abilities
>>
>> | |
>> |---|---|
>> Spellcasting Ability | `INPUT[inlineSelect(option(0, -), option(1, INT), option(2, WIS), option(3, CHA)):sca_temp]` `VIEW[{sca_temp} == 0 ? False : ({sca_temp} == 1 ? {Intelligence} : ({sca_temp} == 2 ? {Wisdom} : {Charisma}))][math(hidden):sca]`
>> Spell Save DC | `VIEW[{sca_temp} == 0 ? "None" : 8+{Proficiency}+round(floor(({sca}-10)/2),0)]` |
>> Spell Atk. Mod. | `VIEW[{sca_temp} == 0 ? "None" : {Proficiency}+round(floor(({sca}-10)/2),0)]`|
>
>>[!metadata|bg-c-yellow] Currency
>>
>>| Type     | Input                         | 
>>| -------- | ----------------------------- |
>>| Copper   | `INPUT[number(class(my-mb-css)):CP]`   |
>>| Silver   | `INPUT[number(class(my-mb-css)):SP]`    | 
>>| Electrum | `INPUT[number(class(my-mb-css)):EP]` | 
>>| Gold     | `INPUT[number(class(my-mb-css)):GP]`     | 
>>| Platinum | `INPUT[number(class(my-mb-css)):PP]` |
>> Total gold: `VIEW[round(10*{PP}+{GP}+0.5*{EP}+0.1*{SP}+0.01*{CP},2)]`
>> 
>>**Gems**
>>`INPUT[inlineListSuggester(optionQuery(#item/wealth)):Gems]`
>>
>>[[Currency Calculator]]



>[!column|txt-s 4 no-t]  Spells
>> [!metadata|bg-c-orange] Cantrips
>> 
>> Spells |
>> -- |
>>`INPUT[inlineListSuggester(optionQuery(#spell/level/cantrip)):CantripSpells]` |
>
>> [!metadata|bg-c-orange] Level One Spells
>> 
>> Spells |
>> -- |
>>`INPUT[inlineListSuggester(optionQuery(#spell/level/1)):Level1Spells]` |
>>
>>Spell slots by level | Used                                                            |
>> | -------------------- | ---------------------------------------------------------------                     |
>> | 1st-level            | `INPUT[toggle(class(spell-slot)):Firstlevel1]` `INPUT[toggle(class(spell-slot)):Firstlevel2]` `INPUT[toggle(class(spell-slot)):Firstlevel3]` |
>
>> [!metadata|bg-c-orange] Level Two Spells
>> 
>> Spells |
>> -- |
>>`INPUT[inlineListSuggester(optionQuery(#spell/level/2)):Level2Spells]` |
>>
>>Spell slots by level | Used                                                            |
>> | -------------------- | ---------------------------------------------------------------                     |
>> | 2nd-level            | `INPUT[toggle(class(spell-slot)):Secondlevel1]` `INPUT[toggle(class(spell-slot)):Secondlevel2]` `INPUT[toggle(class(spell-slot)):Secondlevel3]` |
>
>> [!metadata|bg-c-orange] Level Three Spells
>> 
>> Spell |
>> -- |
>>`INPUT[inlineListSuggester(optionQuery(#spell/level/3)):Level3Spells]` |
>>
>>Spell slots by level | Used                                                            |
>> | -------------------- | ---------------------------------------------------------------                     |
>> | 3rd-level            | `INPUT[toggle(class(spell-slot)):Thirdlevel1]` `INPUT[toggle(class(spell-slot)):Thirdlevel2]` `INPUT[toggle(class(spell-slot)):Thirdlevel3]` |

