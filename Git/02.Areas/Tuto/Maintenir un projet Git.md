---
banner: "![[GitLogo.png]]"
---
---
banner: "![[GitLogo.png]]"
Software: Git
Version: 
Type: Tuto
Auteur: PeterPan
DateCreation: 2024-12-09
WorkInProgress: false
tags: 
Sources: https://git-scm.com/book/en/v2/Git-Basics-Recording-Changes-to-the-Repository
cssclasses:
  - show_properties
---
Créé : `=this.file.ctime`
Dernière modification : `=this.file.mtime`

## Cycle de vie des fichiers d'un projet Git

![[lifecycle.png]]
Il existe deux types de fichiers dans un projet git :
- Les fichiers `Tracked`, qui sont présent dans la snapshot du projet : donc les fichiers `Unmodified`,`Modified` ou `Staged`
- Les fichiers `Untacked` qui correspond au reste, à savoir les fichiers créer localement sur la machine ou bien les fichiers qui ont été enlevés du projet

Pour connaître le status de chaque fichier dans ce cycle :

```bash
$ git status
```

Pour voir les différences entre la version `Staged` et la version `Modified` :

```bash
$ git diff
```

## Pour créer un commit

```bash
$ git commit -m "Story 182: fix benchmarks for speed"
```


