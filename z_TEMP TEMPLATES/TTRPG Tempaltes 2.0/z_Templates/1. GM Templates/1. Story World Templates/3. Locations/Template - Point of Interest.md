---
tags:
  - "#Location"
  - "#POI"
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
> **Type** | `INPUT[POIType][inlineListSuggester:poitype]` |
> **Owner** | `INPUT[suggester(optionQuery(#Character), useLinks(false)):owner]` |
> **Staff** | `INPUT[suggester(optionQuery(#Character), useLinks(false)):staff]` |
> **Location** | `INPUT[suggester(optionQuery(#Location), useLinks(false)):location]` |
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
> **Staff** | `VIEW[{staff}][link]` |
> **Location** | `VIEW[{location}][link]` |
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

> [!metadata|characters]- Characters
> ```dataview
> TABLE join(aliases, ", ") AS Aliases, join(occupation, ", ") AS "Occupations", join(link(organization), ", ") AS "Organizations"
> WHERE econtains(location, this.file.name) AND contains(tags, "Character") AND !contains(condition, "Dead")
> SORT file.name ASC

## History


## GM Notes
### Hidden Details


### Notes

