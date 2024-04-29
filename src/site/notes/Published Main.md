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

- [[Quests/Main Quests/Search for Godsbane\|Search for Godsbane]]<br>Search for the remaining fragments of Godsbane
- [[Quests/Misc/Investigate Cult Activity in Drovic\|Investigate Cult Activity in Drovic]]<br>Investigate the cult that has been terrorizing the city

{ .block-language-dataview}

## Locations

``` dataview
TABLE WITHOUT ID
file.link as "Location",
type as "Type",
region as "Region"
FROM "Locations"
WHERE !contains(file.name, "Location Database")
```