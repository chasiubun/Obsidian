---
tags:
  - "#Location"
  - "#Landmark"
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
> **Type** | `INPUT[LandmarkType][inlineListSuggester:landmarktype]` |
> **Owner** | `INPUT[suggester(optionQuery(#Character), useLinks(false)):owner]` |
> **Manager** | `INPUT[suggester(optionQuery(#Character), useLinks(false)):manager]` |
> **Country** | `INPUT[suggester(optionQuery(#Country), useLinks(false)):country]` |
> **Organization** | `INPUT[inlineListSuggester(optionQuery(#Organization), useLinks(false)):organization]` |

> [!infobox]+
> # `=this.file.name`
> `VIEW[!\[\[{art}\]\]][text(renderMarkdown)]`
> ###### Info
>  |
> ---|---|
> **Aliases** | `VIEW[{aliases}][text]` |
> **Type** | `VIEW[{shoptype}][text]` |
> **Owner** | `VIEW[{owner}][link]` |
> **Manager** | `VIEW[{manager}][link]` |
> **Country** | `VIEW[{country}][link]` |
> **Organization** | `VIEW[{organization}][link]` |

# `=this.file.name` <span style="font-size: medium">"`VIEW[{pronounced}]`"</span>
> [!recite]- Introduction
TBD

> [!metadata|overview]- Overview
> TBD

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
> defaultZoom: 2
> unit: meters
> scale: 1
> darkMode: false
> ```

> [!metadata|districts]- Keyed Locations
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, Key, join(type, ", ") AS Types
> WHERE econtains(location, this.file.name) AND contains(tags, "Key")
> SORT file.name ASC

> [!metadata|pois]- Points of Interest
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(poitype, ", ") AS Type
> WHERE econtains(location, this.file.name) AND contains(tags, "POI")
> SORT file.name ASC

> [!metadata|shops]- Shops
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(shoptype, ", ") AS Type
> WHERE econtains(location, this.file.name) AND contains(tags, "Shop")
> SORT file.name ASC

> [!metadata|characters]- Characters
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(occupation, ", ") AS "Occupations", join(link(organization), ", ") AS "Organizations"
> WHERE econtains(location, this.file.name) AND contains(tags, "Character") AND !contains(condition, "Dead")
> SORT file.name ASC

## History


## GM Notes
### Hidden Details


### Notes

