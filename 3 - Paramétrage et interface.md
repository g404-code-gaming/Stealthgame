# Paramétrage et interface 

## Paramétrage 

Notre objectif est de faire apparaître une porte à la fin du niveau lorsque le personnage entre dans le rayon d'action d'une caméra. Nous allons travailler un peu au paramétrage de notre projet : pour l'instant, nous utilisons des éléments issus du template FirstPerson, mais nous pourrions avoir besoin de les modifier dans la suite du projet.
Pour éviter de modifier les classes déjà faites du projet, nous allons créer les nôtres :

Dupliquez le Blueprint du personnage et le Gamemode à partir du dossier FirstPerson. Renommez-les et placez-les dans votre propre dossier Stealthgame.

![image 1](https://github.com/g404-code-gaming/Stealthgame/blob/main/image/1%20-%20parametre%20et%20interface%20-%201.png)

Allez dans les paramètres du projet et changer de **Gamemode** pour choisir le votre.

![image 2](https://github.com/g404-code-gaming/Stealthgame/blob/main/image/1%20-%20parametre%20et%20interface%20-%202.png)

Désormais, ouvrez votre Gamemode et changer le **Default Pawn Class** : mettez votre personnage à la place de celui du FirstPerson. 

![image 3](https://github.com/g404-code-gaming/Stealthgame/blob/main/image/1%20-%20parametre%20et%20interface%20-%203.png)

Ainsi, nous pourrons modifier plus facilement le jeu. 

## Interface 

Il serait bien d'afficher dans le jeu les contrôles possibles : il faut, par exemple, que le joueur sache quelle touche utiliser pour interagir avec l'environnement.

Pour ça, nous allons créer un **UI** (User Interface).

Créez le niveau **Widget blueprint** de votre UI.

![image 4](https://github.com/g404-code-gaming/Stealthgame/blob/main/image/1%20-%20parametre%20et%20interface%20-%204.png)

Dans ce niveau Widget, ajouter un Canvas Pannel et autant de text que nécessaire pour afficher tout les contrôles du jeu. 

![image 5](https://github.com/g404-code-gaming/Stealthgame/blob/main/image/1%20-%20parametre%20et%20interface%20-%205.png)

Pour chaque text, modifiez le nom et le contenu pour qu'il affiche les contrôles. 

![image 6](https://github.com/g404-code-gaming/Stealthgame/blob/main/image/1%20-%20parametre%20et%20interface%20-%206.png)

Maintenant que le widget est préparé, il faut aller l'ajouter dans le **Level Blueprint** : Il faut créer un évènement qui ajoute le widget à la vue du joueur. 

![image 7](https://github.com/g404-code-gaming/Stealthgame/blob/main/image/1%20-%20parametre%20et%20interface%20-%207.png)

Ce nouvel évènement doit être appelé au lancement du jeu. 

![image 8](https://github.com/g404-code-gaming/Stealthgame/blob/main/image/1%20-%20parametre%20et%20interface%20-%208.png)

Désormais, notre personnage possède un interface sur lequel apparait les contrôles possible : Bravo ! 

![image 9](https://github.com/g404-code-gaming/Stealthgame/blob/main/image/1%20-%20parametre%20et%20interface%20-%209.png)
