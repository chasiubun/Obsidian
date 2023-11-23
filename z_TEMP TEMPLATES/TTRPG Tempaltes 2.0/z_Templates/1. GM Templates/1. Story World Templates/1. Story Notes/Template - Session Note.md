---
tags:
  - "#SessionNote"
locations:
  - Template - Shop
  - Template - Settlement
  - Template - Point of Interest
misc: []
characters:
  - Template - NPC
  - Template - Player
whichparty: Template - Party Dashboard
aliases:
  - The best session
quicknote: something happened, it was the best
sessiondate: 10-11-2023
---
> [!metadata|metadata]- Metadata 
> #### System
>  |
> ---|---|
> **Tags** | `INPUT[Tags][inlineListSuggester:tags]` |
> #### Info
>  |
> ---|---|
> **Aliases** | `INPUT[list:aliases]` |
> **Which Party** | `INPUT[suggester(optionQuery(#Party), useLinks(false)):whichparty]` |
> **Session Date** | `INPUT[datePicker:sessiondate]`
> **Quick Notes** |  `INPUT[textArea:quicknote]`
> **Session Video** |  `INPUT[textArea:video]`
> #### Quick References
>  |
> ---|---|
> **Character** | `INPUT[inlineListSuggester(optionQuery(#Character), useLinks(false)):characters]` |
> **Locations** | `INPUT[inlineListSuggester(optionQuery(#Location), useLinks(false)):locations]` |
> **Miscellaneous** | `INPUT[inlineListSuggester(optionQuery("3. Campaign"), useLinks(false)):misc]` |

#  `=this.file.name` "`=this.aliases`" (`=link(this.WhichParty)`)
## Prep
### To Do


### Plan


### Quick References
> [!column|3 no-title]
>> [!metadata|characters] People
>> `VIEW[{characters}][link]`
>
>> [!metadata|places] Places
>> `VIEW[{locations}][link]`
>
>> [!metadata|misc] Misc
>> `VIEW[{misc}][link]`

## During
### Events


### Travel & Rest (Remember Calendar)


### Loot, Rewards & Purchases


## Post
### New Creations


### Date & Time


### End of Session Notes

