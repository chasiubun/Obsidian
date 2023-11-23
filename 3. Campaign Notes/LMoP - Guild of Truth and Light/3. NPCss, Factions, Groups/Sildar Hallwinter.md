---
tags:
  - "#Character"
  - "#NPC"
art: z_Assets/Misc/PlaceholderImage.png
Gender: Male
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
> **Pronounced** |  `INPUT[textArea:pronounced]` |
> **Aliases** | `INPUT[list:aliases]` |
> **Ancestry** | `INPUT[suggester(optionQuery(#Ancestry), useLinks(false)):ancestry]` |
> **Heritage** | `INPUT[suggester(optionQuery(#Heritage), useLinks(false)):heritage]` |
> **Gender** | `INPUT[Gender][:gender]` |
> **Pronouns** | `INPUT[Pronouns][:pronouns]` |
> **Age** | `INPUT[Age][:age]` |
> **Sexuality** | `INPUT[Sexuality][:sexuality]` |
> **Alignment** | `INPUT[Alignment][:alignment]` |
> #### NPC Info
>  |
> ---|---|
> **Occupations** | `INPUT[Occupation][inlineListSuggester:occupation]` |
> **Organizations** | `INPUT[inlineListSuggester(optionQuery(#Organization), useLinks(false)):organization]` |
> **Religions** | `INPUT[inlineListSuggester(optionQuery(#Deity), useLinks(false)):religion]` |
> **Owned Locations** | `INPUT[inlineListSuggester(optionQuery(#Location), useLinks(false)):ownedlocation]` |
> **Current Location** | `INPUT[suggester(optionQuery(#Location), useLinks(false)):location]` |
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
> **Ancestry** | `VIEW[{ancestry}][link]` |
> **Heritage** | `VIEW[{heritage}][link]` |
> **Gender** | `VIEW[{gender}]` |
> **Pronouns** | `VIEW[{pronouns}]` |
> **Age** | `VIEW[{age}]` |
> **Sexuality** | `VIEW[{sexuality}]` |
> **Alignment** | `VIEW[{alignment}]` |
> ###### Info
>  |
> ---|---|
> **Occupations** | `VIEW[{occupation}][text]` |
> **Organization** | `VIEW[{organization}][link]` |
> **Religions** | `VIEW[{religion}][link]` |
> **Owned Locations** | `VIEW[{ownedlocation}][link]` |
> **Current Location** | `VIEW[{location}][link]` |
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

