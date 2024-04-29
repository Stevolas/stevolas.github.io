```dataview
>table without id
>	"**" + link(file.path, name) + "**" as "Name",
>	embed(Art) as "Art",
>	"**" + race + "**" as "Race",
>	"**" + class + "**" as "Class"
>FROM "Character's"
>FLATTEN choice(Condition = "Alive", "<font style=color:green>**" + Condition + "**</font>",  "<font style=color:red>" + Condition + "</font>") as condition
>where contains(location, "Party")
>sort file.name asc

## Quests

```