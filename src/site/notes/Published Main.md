```dataview
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

```