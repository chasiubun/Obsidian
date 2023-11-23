---
tags:
  - "#Location"
  - "#Settlement"
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
> **Type** | `INPUT[SettlementType][:settlementtype]` |
> **Theme** | `INPUT[Theme][inlineListSuggester:theme]` |
> **Terrain** | `INPUT[Terrain][inlineListSuggester:terrain]` |
> **Defences** | `INPUT[Defence][:defence]`
> **Country** | `INPUT[suggester(optionQuery(#Country), useLinks(false)):country]` |
> #### Info
>  |
> ---|---|
> **Rulers** | `INPUT[suggester(optionQuery(#Character), useLinks(false)):leader]` |
> **Leaders** | `INPUT[suggester(optionQuery(#Character), useLinks(false)):leader]` |
> **Government Type** | `INPUT[GovernmentType][inlineListSuggester:governmenttype]` |
> **Population** |  `INPUT[textArea:population]`
> **Religions** | `INPUT[inlineListSuggester(optionQuery(#Deity), useLinks(false)):religion]` |
> **Imports** | `INPUT[Goods][inlineListSuggester:import]` |
> **Exports** | `INPUT[Goods][inlineListSuggester:export]` |


> [!infobox]+
> # `=this.file.name`
> `VIEW[!\[\[{art}\]\]][text(renderMarkdown)]`
> ###### Info
>  |
> ---|---|
> **Aliases** | `VIEW[{aliases}][text]` |
> **Type** | `VIEW[{settlementtype}][text]` |
> **Theme** | `VIEW[{theme}][text]` |
> **Terrain** | `VIEW[{terrain}][text]` |
> **Defences** | `VIEW[{defence}]` |
> **Country** | `VIEW[{country}][link]` |
> ###### Demographics
>  |
> ---|---|
> **Rulers** | `VIEW[{ruler}][link]` |
> **Leaders** | `VIEW[{leader}][link]` |
> **Government Type** | `VIEW[{governmenttype}][text]` |
> **Population** | `VIEW[{population}][text]` |
> **Religions** | `VIEW[{religion}][link]` |
> ###### Commerce
>  |
> ---|---|
> **Imports** | `VIEW[{import}][text]` |
> **Exports** | `VIEW[{export}][text]` |

# **`=this.file.name`** <span style="font-size: medium">"`VIEW[{pronounced}]`"</span>
> [!recite]- Introduction
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

> [!metadata|districts]- Districts
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(districttype, ", ") AS Type
> WHERE econtains(location, this.file.name) AND contains(tags, "District")
> SORT file.name ASC

> [!metadata|pois]- Points of Interest
> ```dataview
> Table join(aliases, ", ") AS Aliases, join(poitype, ", ") AS Type
> WHERE econtains(location, this.file.name) AND contains(tags, "POI")
> SORT file.name ASC

> [!metadata|shops]- Shops
> ```dataview
> Table join(aliases, ", ") AS Aliases, join(shoptype, ", ") AS Type
> WHERE econtains(location, this.file.name) AND contains(tags, "Shop")
> SORT file.name ASC

> [!metadata|organizations]- Organizations
> ```dataview
> Table join(aliases, ", ") AS Aliases, join(societytype, ", ") AS Type
> WHERE econtains(location, this.file.name) AND contains(tags, "Organization")
> SORT file.name ASC

> [!metadata|characters]- Characters
> ```dataview
> Table join(aliases, ", ") AS Aliases, join(occupation, ", ") AS "Occupations", join(link(organization), ", ") AS "Organizations"
> WHERE econtains(location, this.file.name) AND contains(tags, "Character") AND !contains(condition, "Dead")
> SORT file.name ASC

## History


## Notes
### Plot Hooks


### Hidden Details


### General Notes

