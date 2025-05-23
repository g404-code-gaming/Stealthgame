# Paramétrage et interface 

## Paramétrage 

Nous allons travailler un peu au paramétrage de notre projet : pour l'instant, nous utilisons des éléments issus du template FirstPerson, mais nous pourrions avoir besoin de les modifiers dans la suite du projet.
Pour éviter de modifier les classes déjà faite du projet, nous allons créer les notres : 

Dupliquer le Blueprint du personnage et le Gamemode à partir du dossier Firstperson. Renommez-les et placez-les dans votre propre dossier Stealthgame.

[image 1]()

Allez dans les paramètres du projet et changer de Gamemode pour choisir le votre.

[image 2]()

Désormais, ouvrez votre Gamemode et changer le Default Pawn Class : mettez votre personnage à la place de celui du FirstPerson. 

[image 2]()

Ainsi, nous pourrons modifier plus facilement le jeu. 

## Interface 

Il serait bien d'afficher dans le jeu les contrôles possibles : il faut, par exemple, que le joueur sache quelle touche utilisée pour interragir avec l'environnement.

Pour ça, nous allons créer un **UI** (User Interface). 

Créer le niveau **Widget blueprint** de votre UI.

[image 3]()

Dans ce niveau Widget, ajouter un Canvas Pannel et autant de text que nécessaire pour afficher tout les contrôles du jeu. 

[image 4]()

Pour chaque text, modifier le nom et le contenu pour qu'il affiche les contrôles. 

[image 5]()

Maintenant que le widget est préparé, il faut aller l'ajouter dans le **Level Blueprint** : Il faut créer un évènement qui ajoute le widget à la vue du joueur. 

[image 6]()

Ce nouvel évènement doit être appelé au lancement du jeu. 

[image 7]()

Désormais, notre personnage possède un interface sur lequel apparait les contrôles possible : Bravo ! 

[image 8]()
