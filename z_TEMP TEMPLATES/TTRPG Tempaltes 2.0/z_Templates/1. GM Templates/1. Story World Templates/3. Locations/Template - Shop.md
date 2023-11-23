---
tags:
  - "#Location"
  - "#Shop"
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
> **Type** | `INPUT[ShopType][inlineListSuggester:shoptype]` |
> **Owner** | `INPUT[suggester(optionQuery(#Character), useLinks(false)):owner]` |
> **Staff** | `INPUT[suggester(optionQuery(#Character), useLinks(false)):staff]` |
> **Location** | `INPUT[suggester(optionQuery(#Location), useLinks(false)):location]` |
> **Society** | `INPUT[inlineListSuggester(optionQuery(#Organization), useLinks(false)):organization]` |

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
> WHERE Location = this.file.name AND contains(NoteIcon, "Key")
> SORT file.name ASC

## History


## DM Notes
### Hidden Details


### Notes

