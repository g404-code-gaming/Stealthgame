# Actions du personnage 

Nous allons rajouter quelques actions en plus pour notre personnage. Il est en effet déjà capable de se déplacer et de sauter, mais nous allons rajouter deux actions très commune dans les FPS, et qui vont ajouter de la profondeur et de la fluidité dans le jeu.

Pour cette partie, nous allons travailler dans le Blueprint du Personnage : le **BP_StealthgameCharacter** qui a été créé dans le chapitre précédente.

## S'accroupir

Dans un jeu d'infiltration comme Stealthgame, s'accroupir est une action très courante. Elle permet d'être plus discret tout en passant dans des endroits autrement inaccessibles. Cette action possède néanmoins une contrepartie : elle rend le personnage plus lent.

![image 1](https://github.com/g404-code-gaming/Stealthgame/blob/main/image/4_actionperso_1.JPG)

Pour implémenter l'action, il faut ajouter la touche correspondante dans les entrées du projet : Paramètres --> Paramètres du projet --> Entrée (*Input* en anglais).

![image 2](https://github.com/g404-code-gaming/Stealthgame/blob/main/image/4_actionperso_2.JPG)

Il faut également aller dans les **détails** du personnage pour permettre l'action.

![image 3](https://github.com/g404-code-gaming/Stealthgame/blob/main/image/4_actionperso_3.JPG)

Ensuite, il faut ajouter l'évènement au **Blueprint du personnage** : 
Lorsqu'on presse la touche de Crouch, il se passe des choses différentes en fonction de si on a appuyé sur la touche ou non auparavant : 
  - Si on n'a pas déjà activé la commande de Crouch, alors cette dernière est activée.
  - Si on a déjà activé la commande, alors le Crouch est désactivé et le personnage se remet à se déplacer normalement.

![image 4](https://github.com/g404-code-gaming/Stealthgame/blob/main/image/4_actionperso_4.JPG)

Testez le Crouch pour vérifier qu'il fonctionne. Vous pouvez modifier la vitesse de déplacement dans les détails si vous voulez que le personnage se déplace plus ou moins vite alors qu'il est accroupis.

## Course 

Le Sprint est une action permettant au personnage d'augmenter sa vitesse de déplacement. C'est un outil très utile pour parcourir rapidement de longue distances.

Comme pour le Crouch, implémentez l'action dans les Input du projet.

![image 5](https://github.com/g404-code-gaming/Stealthgame/blob/main/image/4_actionperso_5.JPG)

Ensuite, modifier le Blueprint du personnage pour ajouter la course. 

![image 6](https://github.com/g404-code-gaming/Stealthgame/blob/main/image/4_actionperso_6.JPG)

[5 - Cinématique et chargement de scène](https://github.com/g404-code-gaming/Stealthgame/blob/main/5%20-%20Cin%C3%A9matique%20et%20chargement%20de%20sc%C3%A8ne.md)

