---
banner: "![[Landscape.jpg]]"
Software: Unreal Engine
Version: v5.5
Type: Tuto
Auteur: PeterPan
DateCreation: 2024-11-30
WorkInProgress: true
tags:
  - Landscape
  - Modélisation
  - Material
Sources:
  - https://www.youtube.com/watch?v=aHkVinJ6-J8
cssclasses:
  - show_properties
---
Créé : `=this.file.ctime`
Dernière modification : `=this.file.mtime`

# 1 - La Modélisation

### a) Ouvrir le landscape mode depuis le level user

>[!shortcut]
>[[Turn to LandscapeMode]]

![[LandscapeMode.png]]

### b) Créer un landscape

>[!important]
>Penser à activer `Couches d'édition` pour éditer en différents matéiaux le landscape.

![[CreateLandScape.png]]

### c) Sculpter

![[Sculpter Add.png]]

---
>[!shortcut]
>[[Sculpt Landscape - remove]]

![[Sculpt Rumove.png]]

### d) Splines

![[Splines.png]]

Avec `Ctrl+LeftClick`, on ajoute des points.
>[!Shortcut]
>[[Splines Landscape - add point]]

![[Splines2.png]]

On valide la transformation avec `Toutes les splines`


![[Splines3.png]]
# 2 - Les Materials

### a) On créé un nouveau Matérial

![[NewMaterial.png]]

On assigne ce nouveau matériau comme matériau du Landscape

![[Assign Material.png]]

### b) On ajoute des layers à l'aide du node *LandscapeLayerBlend*

>[!Material]
> - [[LandscapeLayerBlend]]
> - [[Constant3vector]]

Penser à ajouter des les layers dans l'onglet `Properties`

![[LandscapeLayerBlend.png]]

### c) On applique les layer dans le level

En `LandscapeMode`, et dans le menu `Peinture` :

![[AssignLayer.png]]

![[AssignLayer2.png]]

### d) On peint les matériaux

On sélectionne le matériau qui nous intéresse puis on peint ensuite

![[Peinture.png]]