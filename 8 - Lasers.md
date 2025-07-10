# 8 - Laser

En plus des caméras, le joueur peut se faire détecter par des **rayons laser**.

![image 1](https://github.com/g404-code-gaming/Stealthgame/blob/main/image/7_laser_1.png)

Nous allons voir dans ce chapitre comment créer ces rayons et comment les déplacer pour proposer un défi plus dynamique et difficile.

## Construction de la classe Laser

Créez la nouvelle [Classe](https://github.com/g404-code-gaming/UnrealEngine_cour/blob/main/Classes.md) **Laser**. 

Un Laser est composé de : 
  - Un objet physique pour représenter son origine : une boule, un carré, un canon, ....
  - Une lumière d'alarme (dont l'intensité de base est de 0, comme pour la caméra).

Il faut ajouter une **variable** à la classe : Target, qui servira à déterminer dans quel direction va partir le laser.

![image 2](https://github.com/g404-code-gaming/Stealthgame/blob/main/image/7_laser_2.png)

## Détection du joueur par le laser

Dans le [Blueprint](https://github.com/g404-code-gaming/UnrealEngine_cour/blob/main/Blueprint.md) du Laser, ajoutez l'évènement de détection.

Ce dernier fonctionne en deux parties : 

Premièrement, on trace une ligne entre le laser et sa target grâce au node **Line trace**. On récupère ensuite l'acteur qui est touché par cette ligne. 

![image 3](https://github.com/g404-code-gaming/Stealthgame/blob/main/image/7_laser_3.png)

Ensuite, on vérifie que l'acteur touché est bien le joueur. Si c'est le cas, alors on active la lumière d'alarme est on utilise un **event dispatcher** nommé Touched pour communiquer au niveau que le joueur est détecté.

![image 4](https://github.com/g404-code-gaming/Stealthgame/blob/main/image/7_laser_4.png)

Dans la scène, placez un laser et créez un objet **Target Point** qui sera la destination du rayon. Définissez la variable Target du laser pour qu'il reconnaisse votre TargetPoint.

![image 5](https://github.com/g404-code-gaming/Stealthgame/blob/main/image/7_laser_5.png)

Testez le jeu pour vérifier que le programme fonctionne. Si c'est le cas, votre laser allume la lumière d'alarme lorsque votre personnage traverse la ligne.

## évènements d'alarmes grâce au laser

Désormais, il faut relier la classe Laser au Level blueprint afin que les lasers activent les portes, comme les caméras le font déjà.

Ajoutez l'évènement qui permet de relier chaques Laser à la fonction de fermeture des portes. 

![image 6](https://github.com/g404-code-gaming/Stealthgame/blob/main/image/7_laser_6.png)

N'oubliez pas d'initialiser cette évènement au début du jeu. 

![image 7](https://github.com/g404-code-gaming/Stealthgame/blob/main/image/7_laser_7.png)

Il faut également ajouter une connexion entre l'évènement d'ouverture des portes et l'alarme des lasers : il faut que l'évènement soit réactivé lorsqu'on ouvre les portes.

![image 7](https://github.com/g404-code-gaming/Stealthgame/blob/main/image/7_laser_8.png)
![image 7](https://github.com/g404-code-gaming/Stealthgame/blob/main/image/7_laser_9.png)

Avec ces ajouts, les Laser fonctionnent maintenant comme des caméras : ils déclenchent l'alarme si le joueur entre en contact avec leur rayon.

Contrairement aux Caméras, qui sont surtout utilisée pour former une zone d'interdiction sur le sol, les lasers peuvent être utilisés pour former de véritable obstacles en 3D. Dans la partie suivante, nous allons créer du mouvement dans le jeu.

[9 - Animations](https://github.com/g404-code-gaming/Stealthgame/blob/main/9%20-%20Animation%201.md)

