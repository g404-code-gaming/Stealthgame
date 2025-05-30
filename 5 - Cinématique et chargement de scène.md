# Cinématique et Chargement de scène

Nous allons ajouter quelques éléments de contrôle du niveau. Ces derniers sont utiles pour donner des indications au joueur ou gérer des éléments tels que la mort ou le retour au début du jeu.

## Cinématique

Les cinématiques sont souvent utilisées pour donner une information au joueur. Dans notre jeu, nous allons d'abord l'utiliser pour indiquer la sortie lorsque le joueur entre dans une nouvelle salle : lui montrant l'objectif à atteindre.

Ajouter une Caméra à votre scène.

![image 1]()

Pour contrôler facilement la caméra, nous allons utiliser des Macros. 

Créer la MacroLibrary pour votre projet. 

![image 2]() 

Les Macro sont des évènements préfaits qu'il est possible d'utiliser comme on le souhaite partout dans le projet. Cela simplifie grandement la programmation et permet de créer des évènements complexes et de les paramétrer facilement. 

Ajouter une Macro **OpenCinematic** qui va permettre de lancer le début d'une cinématique. 
Cet évènement consiste à désactiver les contrôles du personnage (pour éviter qu'il bouge pendant la cinématique), puis a changer la vue du joueur en choississant une caméra de la scène. 

![image 3]() 

Ajouter également la Macro **CloseCinematic** qui permet de stopper une cinématique et de reprendre les contrôles et la caméra du personnage. 

![image 4]() 

Voilà ! Avec ces Macros, nous pouvons très facilement créer des évènements de cinématiques simples. 

Si ce n'est pas déjà fait, ajouter dans le niveau une **Caméra** et un **Trigger box**. Le Trigger box servira à détecter le joueur pour déclencher la cinématique lorsqu'il passe la porte. 

Dans le **Level Blueprint**, ajouter l'évènement qui va utiliser les Macro pour déclencher une cinématique à l'aide de la caméra. 

![image 5]() 

Désormais, vous savez comment faire des cinématiques simples. 

## Chargement de niveau 

Dans ce jeu d'infiltration, nous allons rajouter un élément dangereux qui fait imédiatement perdre le joueur s'il le touche, par exemple, un trou, un lac d'acide, de la lave, ....

Lorsque le joueur "meurre", cela va directement relancer le niveau, lui donnant une chance de rejouer. 

Créer une nouvelle [classe](https://github.com/g404-code-gaming/UnrealEngine_cour/blob/main/Classes.md) **Vide** : un objet qui va tuer le personnage lorsqu'il le touche. 

![image 6]() 

Dans le graphique de cet objet, crée l'évènement qui fait recharger la scène lorsque le personnage entre en contact avec le vide.

![image 7]() 

Améliorez votre niveau de jeu pour ajouter le vide, et testez le pour voir si la "mort" du personnage fonctionne.


