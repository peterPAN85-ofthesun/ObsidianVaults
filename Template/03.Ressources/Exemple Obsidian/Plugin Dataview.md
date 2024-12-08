---
tags: 
 - Obsidian
 - Plugin
 - Dataview
---






### exemple dataview 1

Tableau à partir de la propriété "Date" des fichiers portant le tag #DayPlanners, avec les dates trié de manière descendante :

```dataview
table Date
from #DayPlanners 
sort Date desc
```

### exemple dataview 2

Liste des fichiers à l'intérieur de "01.Projects avec status="Done" :

```dataview
list from "01.Projects" where status="Done"
```

### exemple dataview 3

Tableau des fichiers dans "01.Projects" avec status = "Done", qui est publié par Marion (quelque soit la casse). Transformer le champ "published" en "Exporté". 

```dataview
table published as "Exporté" , collab from "01.Projects" where status="Done" and published=true and contains(upper(collab),"MARION")
```


### exemple dataview 4
La même chose sans le nom du fichier

```dataview
table WITHOUT ID published as "Exporté", collab from "01.Projects" where status="Done" and published=true and contains(upper(collab),"MARION")
```

### exemple dataview 5
Tableau des fichiers modifié il y a moins de 10 jours, trié par ordre décroissant

```dataview
table file.mtime, collab where file.mtime >= date(today) - dur(10 day) sort file.mtime desc
```
### Renvoyer la date de dernière modification 

Ce fichier a été modifié pour la dernière fois le `=this.file.mtime`

>[!Note]
>Information : `this` correspond au fichier courant. `file` correspond au fichier ciblé. Il existe plusieurs champs spécifiques pour `file`:
>- `file.name` : le nom du fichier
>- `file.tags` : les tags du fichier
>- `file.path` : le chemin du fichier
>- `file.size` : la taille du fichier
>- `file.ctime` : la date de création du fichier
>- `file.mtime` : la date de la dernière modification du fichier

