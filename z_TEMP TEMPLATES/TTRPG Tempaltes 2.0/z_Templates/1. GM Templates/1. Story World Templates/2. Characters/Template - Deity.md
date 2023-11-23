---
tags:
  - "#Character"
  - "#NPC"
  - "#Deity"
art: z_Assets/Misc/PlaceholderImage.png
---

> [!metadata|metadata]- Metadata 
> #### System
>  |
> ---|---|
> **Tags** | `INPUT[Tags][inlineListSuggester:tags]` |
> #### Bio
>  |
> ---|---|
> **Art** | `INPUT[imageSuggester(optionQuery("z_Assets")):art]` |
> **Pronounced** |  `INPUT[textArea:pronounced]`
> **Aliases** | `INPUT[list:aliases]` |
> **Depiction** |  `INPUT[textArea:depiction]` |
> **Power** | `INPUT[Pronouns][:power]` |
> **Plane** | `INPUT[suggester(optionQuery(#Location), useLinks(false)):location]` |
> **Condition** | `INPUT[Condition][:condition]` |
> #### Party Info
>  |
> ---|---|
> **Traveling With** | `INPUT[suggester(optionQuery(#Party), useLinks(false)):whichparty]` |
> **Party 1 Relation** | `INPUT[Party1Relation][:party1relation]` |

> [!infobox]+
> # `=this.file.name`
> `VIEW[!\[\[{art}\]\]][text(renderMarkdown)]`
> ###### Bio
>  |
> ---|---|
> **Aliases** | `VIEW[{aliases}][text]` |
> **Depiction** | `VIEW[{depiction}]` |
> **Alignment** | `VIEW[{alignment}]` |
> **Power** | `VIEW[{power}]` |
> **Plane** | `VIEW[{plane}][link]` |
> **Condition** | `VIEW[{condition}]` |



# **`=this.file.name`** <span style="font-size: medium">"`VIEW[{pronounced}]`"</span>
> [!metadata|overview]- Overview 
> TBD

## Aspirations
### Example 


## Acquaintances
### Family:


### Friends:


### Rivals:


### Met:


## History


## GM Notes
### Plot Hooks


### Hidden Details


### General Notes

