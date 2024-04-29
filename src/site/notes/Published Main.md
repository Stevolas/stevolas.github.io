---
{"dg-publish":true,"permalink":"/published-main/","tags":["gardenEntry"],"noteIcon":""}
---


![Bad Company.png](/img/user/Attachments/Bad%20Company.png)
<font size="10px" style="font-family: Segoe Print" color=beige><center>**Franzictini**</center></font>
### Table of Contents

- [[Published Main#Current Party\|Current Party]]
- [[Published Main#NPC's\|NPC's]]
- [[Published Main#Quests\|Quests]]
- [[Published Main#Locations\|Locations]]

## Current Party

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