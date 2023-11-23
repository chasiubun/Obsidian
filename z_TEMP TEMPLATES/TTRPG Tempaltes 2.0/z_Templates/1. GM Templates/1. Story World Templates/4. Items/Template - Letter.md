---
tags:
  - "#Letter"
aliases:
  - yes
  - no
quicknote: this is a letter
letterstatus: Sent
sender: Template - Player
receiver: Template - NPC
sentfrom: Template - Settlement
sentto: Template - Shop
cost: 5,000,000 gp
sentdate: today
deliverydate: today but a second later
response: Template - Letter
whichparty: Template - Party Dashboard
---

> [!metadata|metadata]- Metadata 
> #### System
>  |
> ---|---|
> **Tags** | `INPUT[Tags][inlineListSuggester:tags]` |
> #### Bio
>  |
> ---|---|
> **Aliases** | `INPUT[list:aliases]` |
> **Quick Notes** |  `INPUT[textArea:quicknote]`
> **Letter Status** | `INPUT[LetterStatus][:letterstatus]` |
> **Which Party** | `INPUT[suggester(optionQuery(#Party), useLinks(false)):whichparty]` |
> **Sender** | `INPUT[suggester(optionQuery(#Character), useLinks(false)):sender]` |
> **Receiver** | `INPUT[suggester(optionQuery(#Character), useLinks(false)):receiver]` |
> **Sent From** | `INPUT[suggester(optionQuery(#Location), useLinks(false)):sentfrom]` |
> **Sent To** | `INPUT[suggester(optionQuery(#Location), useLinks(false)):sentto]` |
> **Cost** |  `INPUT[textArea:cost]`
> **Sent Date** |  `INPUT[textArea:sentdate]`
> **Estimated Delivery Date** |  `INPUT[textArea:deliverydate]`
> **Response** | `INPUT[suggester(optionQuery(#Letter), useLinks(false)):response]` |

> [!infobox]
> # Info
> **Status** | <font color="#ffff00">`VIEW[{letterstatus}]`</font> |

# **To:** `VIEW[{receiver}][link]`  <span style="font-size: medium">**Sent to:** `VIEW[{sentto}][link]`</span> 
Letter contents that has been sent to the Character.

- <font color="#fac08f">**From:**</font> `VIEW[{sender}][link]`
- <font color="#fac08f">**Sent from:**</font> `VIEW[{sentfrom}][link]`

## Notes
Notes for anything to do with the letter being sent to the recipient.

---
<font color="#92cddc"><center>**Response:**</center></font>
<u><center>`VIEW[{response}][link]`</center></u>

----