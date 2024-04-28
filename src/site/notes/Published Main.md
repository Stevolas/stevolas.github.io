---
{"dg-publish":true,"permalink":"/published-main/","tags":["gardenEntry"]}
---


![Bad Company.png](/img/user/Attachments/Bad%20Company.png)
<font size="10px" style="font-family: Segoe Print" color=beige><center>**Franzictini**</center></font>
### Table of Contents

- [[Published Main#Current Party\|Current Party]]
- [[Published Main#NPC's\|NPC's]]
- [[Published Main#Quests\|Quests]]
- [[Published Main#Locations\|Locations]]
- [[Published Main#Sessions\|Sessions]]

## Current Party
>[!cards|6 dataview] 
>``` dataview
>TABLE WITHOUT ID
>	"**" + link(file.path, name) + "**" AS "Name",
>	embed(Art) AS "Art",
>	"**" + race + "**" AS "Race",
>	"**" + class + "**" AS "Class"
>FROM "Character's"
>FLATTEN choice(Condition = "Alive", "<font style=color:green>**" + Condition + "**</font>",  "<font style=color:red>" + Condition + "</font>") as condition
>WHERE contains(location, "Party")
>SORT file.name asc

## Quests

``` dataview
LIST WITHOUT ID
file.link + "<br>" + Objective 
FROM "Quests" 
WHERE file.name != "Quest Database" AND Tracked = true
```

## Locations

``` dataview
TABLE WITHOUT ID
file.link as "Location",
type as "Type",
region as "Region"
FROM "Locations"
WHERE !contains(file.name, "Location Database")
```