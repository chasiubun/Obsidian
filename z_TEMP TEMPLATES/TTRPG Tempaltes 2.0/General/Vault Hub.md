![[Placeholderimage.png|banner-fade]]

# Vault Hub

> [!metadata|info]+ Guide
>  **Create A New Note:** CTRL + P > Search "QuickAdd: Run QuickAdd" (Press Q and it will be the first option) and enter. You can now select a template to use and it will automatically be added into the correct folder for you. (As long as you don't edit the structure. You are more than welcome to, but will need to edit the settings.)
>  **Searching Notes:** Using CTRL + SHIFT + F, or In the top left, use the 🔍 or 🏷️ buttons to search for anything you're looking for. All notes have tags to increase the power of this vault. All characters such as Players, NPCs and Deities have the ""#Character" tag. All locations like Settlements, Shops, etc. all have the ""#Location" tag, and so on. Some notes get broken down further such as NPCs with the ""#NPC" tag. Additionally, if you want to search for a NPC you know is in a certain settlement. Search for the Tag: ""#NPC" tag and the Property: 'SettlementName'. I recommend looking at the templates and see which notes have what tags to aid in your searching.

> [!metadata|party] Parties
>> [!cards|dataview 5] **Party**
>> ```dataview
>> TABLE WITHOUT ID
>> "<span style='display: block; text-align: center; margin-bottom: 5px;'>" + link(file.link, Title) + "</span>" AS Title,
>> embed(link(art)) AS "Art"
> FROM !"z_Templates"
>> WHERE contains(tags, "Party")
>> SORT file.name asc
>> ```







## To Do
> [!column|2 no-title]
>> [!metadata] Short Term
> TBD
> 
>> [!metadata] Long Term
> TBD
> 


## Random Notes
> [!cards|dataview 7]
> ```dataview
> TABLE WITHOUT ID
> "<span style='display: block; text-align: center; margin-bottom: 2px;'>" + link(file.link, Aliases) + "</span>" AS Aliases,
> embed(link(art)) AS "Art"
> FROM !"z_Templates"
> WHERE contains(tags, "Character")
> FLATTEN [ [(seed) => (seed * 1103515245 + 12345) % 2147483648]] AS random
> FLATTEN [number(dateformat(date("now"), "x"))] AS seed
> SORT random[0](seed + file.size)
> LIMIT 14