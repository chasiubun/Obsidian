---
tags:
  - "#Location"
  - "#Country"
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
> **Government Type** | `INPUT[GovernmentType][inlineListSuggester:governmenttype]` |
> **Theme** | `INPUT[Theme][inlineListSuggester:theme]` |
> **Terrain** | `INPUT[Terrain][inlineListSuggester:terrain]` |
> **Rulers** | `INPUT[inlineListSuggester(optionQuery(#Character), useLinks(false)):ruler]` |
> **Leaders** | `INPUT[inlineListSuggester(optionQuery(#Character), useLinks(false)):leader]` |
> **Planet** | `INPUT[suggester(optionQuery(#Planet), useLinks(false)):planet]` |
> **Religions** | `INPUT[inlineListSuggester(optionQuery(#Deity), useLinks(false)):religion]` |

> [!infobox]+
> # `=this.file.name`
> `VIEW[!\[\[{art}\]\]][text(renderMarkdown)]`
> ###### Info
>  |
> ---|---|
> **Aliases** | `VIEW[{aliases}][text]` |
> **Government Type** | `VIEW[{governmenttype}][text]` |
> **Theme** | `VIEW[{theme}][text]` |
> **Terrain** | `VIEW[{terrain}][text]` |
> **Rulers** | `VIEW[{ruler}][link]` |
> **Leaders** | `VIEW[{leader}][link]` |
> **Planet** | `VIEW[{planet}][link]` |
> **Religions** | `VIEW[{religion}][link]` |

# **`=this.file.name`** <span style="font-size: medium">"`VIEW[{pronounced}]`"</span>
> [!metadata|overview]- Overview
TBD

> [!metadata|map]- Map
> ```leaflet
> id: TBD
> image: [[PlaceholderImage.png]]
> height: 600px
> width: 640px
> lat: 50
> long: 50
> minZoom: 1
> maxZoom: 5
> defaultZoom: 1
> unit: meters
> scale: 1
> darkMode: false
> ```

> [!metadata|regions]- Regions
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(districttype, ", ") AS Type
> WHERE econtains(location, this.file.name) AND contains(tags, "District")
> SORT file.name ASC

> [!metadata|landmarks]- Landmarks
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(poitype, ", ") AS Type
> WHERE econtains(location, this.file.name) AND contains(tags, "POI")
> SORT file.name ASC

> [!metadata|settlements]- Settlements
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, settlementtype AS Type, defence AS Defences
> WHERE econtains(country, this.file.name) AND contains(tags, "Settlement")
> SORT file.name ASC

> [!metadata|organizations]- Organizations
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(societytype, ", ") AS Type
> WHERE econtains(location, this.file.name) AND contains(tags, "Organization")
> SORT file.name ASC

## History


## Politics & Relations


## Current Events


## GM Notes
### Plot Hooks


### Hidden Details


### General Notes

