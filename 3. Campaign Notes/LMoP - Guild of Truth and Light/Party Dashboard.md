---
tags:
  - "#Party"
---

![[Placeholderimage.png|banner-fade]]

> [!metadata|metadata]- Metadata 
> #### System
>  |
> ---|---|
> **Tags** | `INPUT[Tags][inlineListSuggester:tags]` |
> #### Bio
>  |
> ---|---|
> **Aliases** | `INPUT[list:aliases]` |
> **Alignment** | `INPUT[Alignment][:alignment]` |
> **Owned Locations** | `INPUT[inlineListSuggester(optionQuery(#Location), useLinks(false)):ownedlocation]` |

# **`=this.file.name`**
> [!metadata|party] Parties
>> [!cards|dataview 5] **Parties**
>>```dataview
TABLE WITHOUT ID
>>	embed(link(art)) AS "Art",
>>     "<span style='display: block; text-align: center; margin-bottom: 5px;'>" + link(file.link, Title) + "</span>" AS Title
WHERE econtains(whichparty, this.file.name) AND contains(tags, "Character") AND !contains(condition, "Dead")
>>SORT file.name asc
>>```

> [!metadata|sessionlogs]- Session Logs
📝[[📝 Session Note Database| New Session Log]]
>> [!cards|dataview 3]
>>```dataview
TABLE WITHOUT ID
>>     "<span style='display: block; border-bottom: 2px solid var(--accent); text-align: center; margin-bottom: 5px;'>" + link(file.link, Title) + "</span>" AS Title,
>>     "<span style='display: block; border-bottom: 2px solid var(--accent); text-align: center; margin-bottom: 5px;'>" + sessiondate + "</span>" AS SessionDate,
>>	quicknote AS "QuickNotes"
WHERE econtains(whichparty, this.file.name) AND contains(tags, "SessionNote")
>>SORT file.name desc LIMIT 9
>>```

> [!metadata|quests]- Quests
❗[[❗ Quest Database | New Main Quest]]
>> [!cards|dataview 3]
>>```dataview
TABLE WITHOUT ID
>>     "<span style='display: block; border-bottom: 2px solid var(--accent); text-align: center; margin-bottom: 5px;'>" + link(file.link, Title) + "</span>" AS Title,
>>     "<span style='display: block; border-bottom: 2px solid var(--accent); text-align: center; margin-bottom: 5px;'>" + Status + "</span>" AS Status,
>>	QuickNotes AS "QuickNotes"
WHERE contains(NoteIcon, "Quest") AND contains(WhichParty, "Party1") AND contains(status, "Active")
>>SORT file.name asc
>>```

> [!metadata|sidequests]- Side Quests
❓[[❗ Quest Database | New Side Quest]]
>> [!cards|dataview 3]
>>```dataview
TABLE WITHOUT ID
>>     "<span style='display: block; border-bottom: 2px solid var(--accent); text-align: center; margin-bottom: 5px;'>" + link(file.link, Title) + "</span>" AS Title,
>>     "<span style='display: block; border-bottom: 2px solid var(--accent); text-align: center; margin-bottom: 5px;'>" + Status + "</span>" AS Status,
>>	QuickNotes AS "QuickNotes"
WHERE contains(NoteIcon, "Side") AND contains(WhichParty, "Party1") AND contains(status, "Active")
>>SORT file.name asc
>>```

> [!metadata|servicerequests]- Service Requests
🏷️[[🎫 Service Request Database | New Service Request]]
>> [!cards|dataview 3]
>>```dataview
TABLE WITHOUT ID
>>     "<span style='display: block; border-bottom: 2px solid var(--accent); text-align: center; margin-bottom: 5px;'>" + link(file.link, Title) + "</span>" AS Title,
>>     "<span style='display: block; border-bottom: 2px solid var(--accent); text-align: center; margin-bottom: 5px;'>" + Status + "</span>" AS Status,
>>	QuickNotes AS "QuickNotes"
WHERE contains(NoteIcon, "ServiceRequest") AND contains(WhichParty, "Party1") AND contains(status, "Requested") OR contains(status, "In-Progress") OR contains(status, "Pending Pick-Up")
>>SORT file.name asc
>>```

> [!metadata|letters]- Letters
✉️[[✉️ Letter Database | New Letter]]
>> [!cards|dataview 3]
>>```dataview
TABLE WITHOUT ID
>>     "<span style='display: block; border-bottom: 2px solid var(--accent); text-align: center; margin-bottom: 5px;'>" + link(file.link, Title) + "</span>" AS Title,
>>     "<span style='display: block; border-bottom: 2px solid var(--accent); text-align: center; margin-bottom: 5px;'>" + Status + "</span>" AS Status,
>>	QuickNotes AS "QuickNotes"
WHERE econtains(whichparty, this.file.name) AND contains(tags, "Letter") AND !contains(condition, "Complete")
>>SORT file.name asc
>>```






## NPC Opinion
> [!column|3 no-title]
>> [!metadata] Ally
>> ```dataview
>> table
>> WHERE econtains(party1relation, "Ally")
>> SORT file.name ASC
> 
>> [!metadata] Lover
>> ```dataview
>> table
>> WHERE econtains(party1relation, "Lover")
>> SORT file.name ASC
> 
>> [!metadata] Family
>> ```dataview
>> table
>> WHERE econtains(party1relation, "Family")
>> SORT file.name ASC
> 
>> [!metadata] Friends
>> ```dataview
>> table
>> WHERE econtains(party1relation, "Friend")
>> SORT file.name ASC
> 
>> [!metadata] Dislike
>> ```dataview
>> table
>> WHERE econtains(party1relation, "Dislike")
>> SORT file.name ASC
> 
>> [!metadata] Enemy
>> ```dataview
>> table
>> WHERE econtains(party1relation, "Enemy")
>> SORT file.name ASC
> 





## **Notes**