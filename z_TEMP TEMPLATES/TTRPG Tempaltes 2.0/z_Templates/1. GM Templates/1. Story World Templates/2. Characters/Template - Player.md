---
tags:
  - "#Character"
  - "#Player"
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
> **Character Sheet** |  `INPUT[textArea:charactersheet]`
> **Pronounced** |  `INPUT[textArea:pronounced]`
> **Aliases** | `INPUT[list:aliases]` |
> **Ancestry** | `INPUT[suggester(optionQuery(#Ancestry), useLinks(false)):ancestry]` |
> **Heritage** | `INPUT[suggester(optionQuery(#Heritage), useLinks(false)):heritage]` |
> **Gender** | `INPUT[Gender][:gender]` |
> **Pronouns** | `INPUT[Pronouns][:pronouns]`
> **Age** | `INPUT[Age][:age]` |
> **Sexuality** | `INPUT[Sexuality][:sexuality]` |
> **Alignment** | `INPUT[Alignment][:alignment]` |
> #### Info
>  |
> ---|---|
> **Occupations** | `INPUT[Occupation][inlineListSuggester:occupation]` |
> **Organizations** | `INPUT[inlineListSuggester(optionQuery(#Organization), useLinks(false)):organization]` |
> **Religions** | `INPUT[inlineListSuggester(optionQuery(#Deity), useLinks(false)):religion]` |
> **Owned Locations** | `INPUT[inlineListSuggester(optionQuery(#Location), useLinks(false)):ownedlocation]` |
> **Current Location** | `INPUT[suggester(optionQuery(#Location), useLinks(false)):location]` |
> **Which Party** | `INPUT[suggester(optionQuery(#Party), useLinks(false)):whichparty]` |
> **Condition** | `INPUT[Condition][:condition]` |

> [!infobox]+
> # `=this.file.name`
> `VIEW[!\[\[{art}\]\]][text(renderMarkdown)]`
> ###### `VIEW[\[Character Sheet\]({charactersheet})][text(renderMarkdown)]`
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
## Goals
### Short-term


### Long-term


## Ideals
### Loves


### Hates


## Traits
### Perks


### Flaws


## History
### Birth Location


### What was their childhood like growing up?


### Did they have a job before adventuring?


### What has happened between leaving home and the present day?


### What made them leave and what keeps them going?


### Do they know any of the party members before the start of the campaign?


### Do you follow a God, if so why?


## Notable Acquaintances
### Family


### Friends


### Rivals


## Events


## GM Notes
### Additional Notes From Players 


### Hidden Details


### Notes

