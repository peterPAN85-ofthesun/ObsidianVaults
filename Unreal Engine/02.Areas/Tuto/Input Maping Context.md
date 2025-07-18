---
banner: "![[Unreal-Engine-5.webp]]"
Software: Unreal Engine
Version: v5.5
Type: Tuto
Auteur: PeterPan
DateCreation: 2024-12-30
WorkInProgress: true
tags:
  - Input
Sources: 
cssclasses:
  - show_properties
---

Créé : `=this.file.ctime`
Dernière modification : `=this.file.mtime`

# 1 - Créer des InputActions

>[!Blueprint]
>[[InputAction]]

![[04.Files/ScreenShot/Tuto/InputMapContext/InputAction.png]]

# 2 -Créer une InputMapContext

>[!Blueprint]
>[[InputMapingContext]]

![[04.Files/ScreenShot/Tuto/InputMapContext/InputMapingContext.png]]

Ce Bluerpint est une sorte de tableau associant des entrées physiques, comme les touches d'un clavier ou les joysticks d'une manette , à une `InputAction`, comme avancer ou sauter.

QUELQUES TIPS :
 - Le Modifier `DeadZone` permet du supprimer les approximations de valeurs notamment lorsqu'un joystick est au repos 
 - Pour les `InputAction` de type Vector, utiliser le modifier `SwizzleInputAxisVlalues` pour l'entrée affecte un autre axe que l'axe X (l'orde `YXZ` permet entre autre d'affecter l'axe Y)

# 3 - Implémenter le Blueprint


Dans le blueprint "contrôlé par le joueur", on associe à chaque changement de controller un InputMapContext
![[BPmapEnhancedInput.png]]

On peut maintenant implémenter des events Custom associé aux InputAction listées dans l'InputMapContext
![[ImplémentationBP.png]]