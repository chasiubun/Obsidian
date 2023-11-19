
> [!infobox]+
> # `=this.file.name`
> **Pronounced:**  "`=this.Pronounced`"
> ![[PlaceholderImage.png]]
> ###### Basic Information
>  |
> ---|---|
> **Aliases** | `=this.aliases` |
> **Base of Operations** | `=link(this.hq)` |
> **Associated Religion** | `=link(this.associatedreligion)` |
> **Alignment** | `=this.alignment` |
> **Type** | `=this.type` |

# **`=this.file.name`**
> [!metadata|overview]- Overview
The Paradisium Cult discovered relics of the nature of how the world was created. In order to attempt to re-establish what they call the first age, Paradise, the cult seeks to seize control of all civilizations away from the Aspects and to their own. Seeing one Aspect receive a cut from another during one of the Exhibitions, the cult reasoned that although the Aspects no longer aged, they could be injured, subjugated, and even killed. This small, yet effective cult operates undercover in most established societies, growing in control over those who occupy the higher echelons of society. Members of the cult are cold and calculating as they strive toward their goal. Each is accompanied by a Prism that operates as a weapon and as communication between members. The Prism is an objective tool that keeps each member in check while providing protection. Effects of the Prism also include a mind meld effect of conforming the minds of the members into one hive.

> [!metadata|settlements]- Locations
> `=link(this.location)`

> [!metadata|landmarks]- Landmarks
> [[🏰Landmark Database|🏰Add New Landmark]]
> ```dataview
table join(Type, ", ") AS Type, join(link(AffiliatedGroup), ", ") AS "Group(s)"
WHERE contains(AffiliatedGroup, this.file.name) AND contains(NoteIcon, "Landmark")
SORT file.name ASC

> [!metadata|pois]- Points of Interest
> [[❓ POI Database|📝Add New Point of Interest]]
> ```dataview
table join(Type, ", ") AS Type, join(link(AffiliatedGroup), ", ") AS "Group(s)"
WHERE contains(AffiliatedGroup, this.file.name) AND contains(NoteIcon, "POI")
SORT file.name ASC

> [!metadata|shops]- Shops
> [[Database_Shops and Services|📝Add New Shop/Service]]
> ```dataview
table join(Type, ", ") AS Type, join(link(AffiliatedGroup), ", ") AS "Group(s)"
WHERE contains(AffiliatedGroup, this.file.name) AND contains(NoteIcon, "Shop")
SORT file.name ASC

> [!metadata|characters]- Characters
> [[👨‍👩‍👧‍👦 NPC Database| 📝Add New NPC]]
> ```dataview
table Pronouns, join(Occupation, ", ") AS "Occupation(s)", join(link(AssociatedGroup), ", ") AS "Group(s)", join(link(AssociatedReligion), ", ") AS "Religion(s)"
WHERE contains(AssociatedGroup, this.file.name) AND contains(NoteIcon, "Character") AND !contains(Condition, "Dead")
SORT file.name ASC

## Culture
### Mission


### Conduct


### Recruitment & Training


### Ranks


### Uniforms & Equipment


## Acquaintances
### Allies:


### Rivals:


### Contacts:


## History


## Notes
### Plot Hooks


### Hidden Details


### General Notes

