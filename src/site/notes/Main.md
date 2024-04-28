---
{"dg-publish":true,"permalink":"/main/","tags":["gardenEntry"]}
---


![Bad Company.png](/img/user/Attachments/Bad%20Company.png)
<font size="10px" style="font-family: Segoe Print" color=beige><center>**Franzictini**</center></font>
```leaflet
id: leaflet-map
image: [[Attachments/Maps/franzictini.jpg]]
height: 720px
lat: 50
long: 50
minZoom: 7
maxZoom: 10
defaultZoom: 7
unit: meters
scale: 1
marker: default, 39.983334, -82.983330, [[Note]]
darkMode: false
recenter: true
```


### Table of Contents

- [[Main#Current Party\|Current Party]]
- [[Main#NPC's\|NPC's]]
- [[Main#Quests\|Quests]]
- [[Main#Locations\|Locations]]
- [[Main#Sessions\|Sessions]]

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
``` button
name New Quest
type command
action QuickAdd: New Quest
```
>[!cards|dvl no-strong]
>``` dataview
>LIST WITHOUT ID
>file.link + "<br>" + Objective 
>FROM "Quests" 
>WHERE file.name != "Quest Database" AND Tracked = true
>```

## Locations
```button
name New Location
type command
action QuickAdd: New Location
```

| Location                                         | Type      | Region       |
| ------------------------------------------------ | --------- | ------------ |
| [[Locations/Cities/Anaheim.md\|Anaheim]]         | \-        | South-West   |
| [[Locations/Cities/Cape Renozo.md\|Cape Renozo]] | Theocracy | South-West   |
| [[Locations/Cities/Covin.md\|Covin]]             | \-        | \-           |
| [[Locations/Cities/Irridanel.md\|Irridanel]]     | \-        | \-           |
| [[Locations/Hamlet/Boab.md\|Boab]]               | Isocracy  | Great Forest |
| [[Locations/Hamlet/Nellis.md\|Nellis]]           | \-        | \-           |
| [[Locations/Giorna.md\|Giorna]]                  | \-        | \-           |
| [[Locations/Metropolis/Brass.md\|Brass]]         | Monarchy  | Unknown      |
| [[Locations/Metropolis/Drovic.md\|Drovic]]       | Monarchy  | North-East   |
| [[Locations/Rectoro.md\|Rectoro]]                | \-        | \-           |
| [[Locations/Swallow.md\|Swallow]]                | \-        | \-           |
| [[Locations/Villages/Kelpon.md\|Kelpon]]         | \-        | \-           |
| [[Locations/Villages/Konoha.md\|Konoha]]         | \-        | \-           |
| [[Locations/Villages/Vindor.md\|Vindor]]         | Monarchy  | South-West   |
| [[Locations/Xorna.md\|Xorna]]                    | \-        | \-           |
| [[Locations/Whitwick.md\|Whitwick]]              | \-        | \-           |

{ .block-language-dataview}

## Sessions
```button
name New Session
type command
action QuickAdd: New Session
```
``` dataview
LIST WITHOUT ID
	file.link + "<br>" + Session_Date
FROM "Session Notes" 
WHERE file.name != "Session Database"
SORT Session_Date desc
```