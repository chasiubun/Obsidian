---
AssociatedGroup: Vindi
Gender: Female
Race: Half-Elf
Age: "27"
Class: Sorcerer, Wizard
Alignment: Neutral Good
Character-Role: 
Location: Colhen
NoteIcon: npc
---
[[sorcerer]] [![Evie's NPC Portrait](https://static.wikia.nocookie.net/vindictus_gamepedia/images/8/80/Evie_%28NPC_Icon%29.png/revision/latest/scale-to-width-down/300?cb=20200430035332)


<% tp.file.title %>
<% await tp.file.move("/2. Mechanics/Non-Player Characters/" + tp.file.title) %>

<%*
const hasTitle = !tp.file.title.startsWith("NewNPC");
let title;
if (!hasTitle) {
    title = await tp.system.prompt("Enter NPC Name");
    await tp.file.rename(title);
} else {
    title = tp.file.title;
}
_%>

> [!infobox]
> # `=this.file.name`
> 
> !
> https://static.wikia.nocookie.net/vindictus_gamepedia/images/8/80/Evie_%28NPC_Icon%29.png/revision/latest/scale-to-width-down/300?cb=20200430035332
> ###### Basic Information
> Type |  Stat |
> ---|---|
> Home | `=this.Location` |
> Group | `=this.AssociatedGroup` |
> Sex | `=this.gender` |
> Race | `=this.race` |
> Age | `=this.age` |
> Condition | Healthy |
> ###### Rules Info
> Type |  Stat |
> ---|---|
> Alignment | `=this.alignment` |
> Class | `=this.class` |
> Character Role | `=this.character-role` |

# `=this.file.name`
## Profile

<% tp.file.cursor() %>
**<Add description here, extend it with AI Text Generator using Ctrl J>**

> [!info] Statblock
> ```statblock
> name: Individual
> monster: Commoner
> columns: 1
> ```

```encounter-table
name: Individual
creatures:
 - 1: Commoner
```
