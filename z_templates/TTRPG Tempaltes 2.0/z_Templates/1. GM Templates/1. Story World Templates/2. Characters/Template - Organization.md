---
tags:
  - Organization
art: z_Assets/Misc/PlaceholderImage.png
---
> [!metadata|metadata]- Metadata 
> #### System
>  |
> ---|---|
> **Tags** | `INPUT[Tags][inlineListSuggester:tags]` |
> #### Info
>  |
> ---|---|
> **Art** | `INPUT[imageSuggester(optionQuery("z_Assets")):art]` |
> **Pronounced** |  `INPUT[textArea:pronounced]`
> **Aliases** | `INPUT[list:aliases]` |
> **Type** | `INPUT[SocietyType][inlineListSuggester:societytype]` |
> **Boss** | `INPUT[suggester(optionQuery(#Character), useLinks(false)):boss]` |
> **Manager** | `INPUT[suggester(optionQuery(#Character), useLinks(false)):manager]` |
> **Hierarchy** WIP | `INPUT[suggester(optionQuery("z_Canvas")):hierarchy]` | 
> **Religions** | `INPUT[inlineListSuggester(optionQuery(#Deity), useLinks(false)):religion]` |
> **HQ** | `INPUT[suggester(optionQuery(#Location), useLinks(false)):hq]` |
> **Operating Areas** | `INPUT[inlineListSuggester(optionQuery(#Location), useLinks(false)):location]` |

> [!infobox]+
> # `=this.file.name`
> `VIEW[!\[\[{art}\]\]][text(renderMarkdown)]`
> ###### Info
> ###### `=link(this.Hierarchy)` WIP
> | |
> ---|---|
> **Aliases** | `VIEW[{aliases}][text]` |
> **Type** | `VIEW[{societytype}][text]` |
> **Alignment** | `VIEW[{alignment}][text]` |
> **Boss** | `VIEW[{boss}][link]` |
> **Manager** | `VIEW[{manager}][link]` |
> **Religions** | `VIEW[{religion}][link]` |
> **HQ** | `VIEW[{hq}][link]` |
> **Operating Areas** | `VIEW[{location}][link]` |

# `=this.file.name` <span style="font-size: medium">"`VIEW[{pronounced}]`"</span>
> [!metadata|overview]- Overview
TBD

> [!metadata|landmarks]- Landmarks
> [[🏰Landmark Database|🏰Add New Landmark]]
> ```dataview
table join(Type, ", ") AS Type, join(link(AffiliatedGroup), ", ") AS "Group(s)"
WHERE econtains(society, this.file.name) AND contains(tags, "Landmark")
SORT file.name ASC

> [!metadata|pois]- Points of Interest
> [[❓ POI Database|📝Add New Point of Interest]]
> ```dataview
table join(Type, ", ") AS Type, join(link(AffiliatedGroup), ", ") AS "Group(s)"
WHERE econtains(society, this.file.name) AND contains(tags, "POI")
SORT file.name ASC

> [!metadata|shops]- Shops
> [[💲 Shop & Service Database|📝Add New Shop/Service]]
> ```dataview
table join(Type, ", ") AS Type, join(link(AffiliatedGroup), ", ") AS "Group(s)"
WHERE econtains(society, this.file.name) AND contains(tags, "Shop")
SORT file.name ASC

> [!metadata|characters]- Characters
> [[👨‍👩‍👧‍👦 NPC Database| 📝Add New NPC]]
> ```dataview
table Pronouns, join(Occupation, ", ") AS "Occupation(s)", join(link(organization), ", ") AS "Organization(s)", join(link(AssociatedReligion), ", ") AS "Religion(s)"
WHERE contains(organization, this.file.name) AND contains(tags, "Character") AND !contains(condition, "Dead")
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

