# Animation 2

Nous avons vus le séquenceur, qui permet de créer des animations de manière expérimentale. Il est aussi possible de créer ses propres 'animations' en déplaçant plus simplement les objets du niveau. 

Ici, on souhaite faire en sorte que les Lasers puissent bouger, soit de manière **circulaire** (en tourant sur eux-même), soit de manière **linéaire** (glissant d'une position à l'autre).

(image 1) 

## Moving Actor 

Nous allons commencez par créer l'objet permettant le mouvement : le **Moving Actor**. 

Il s'agit d'une classe spéciale, invisible, qui peut bouger. Elle va contenir d'autres classes pour les déplacer.

Créez donc une nouvelle [classe]() **Moving Actor**. Cette classe va avoir besoin d'une certaine quantité de variables : 
  - **Rotate** : un Booléen qui détermine si l'objet doit tourner ou non.
  - **RotationValue** : la vitesse à laquelle l'objet tourne.
  - **Travel** : un Booléen qui détermine si l'objet doit se déplacer ou non.
  - **Reversed** : un Booléen qui détermine si l'objet qui se déplace doit aller dans le sens inverse ou non.
  - **Speed** : La vitesse de l'objet lorsqu'il se déplace.
  - **Target 1** : la 1ère cible de l'objet : il va se déplacer sur sa position.
  - **Target 2** : la 2ème cible de l'objet : il va se déplacer sur sa position après avoir atteint la 1ère cible.

Toutes les variables doivent être visible (l'oeil ouvert à coté), afin qu'il soit possible de les modifier directement depuis le niveau.

(image 2)

## Rotation du Moving Actor

Pour que l'objet puisse tourner sur lui-même, nous allons ajouter le graphique suivant dans son Blueprint : 
  Concrètement, on vérifie si la variable *Rotate* est vraie, et si c'est bien le cas, on fait tourner l'objet grâce à *add actor rotation*. 

(image 3)

Une fois que c'est fait, nous allons poser un Moving Actor sur la scène et mettre un laser à l'intérieur pour tester notre nouveau programme.

(image 4) 

Il faut bien intégrer le laser dans le Moving target, et ne pas oublier que le laser à besoin d'une target point sur laquelle tirer son rayon.
De plus, il faut vérifier que les paramètres du Moving Actor sont bien définis (si RotationValue es à 0, il ne tournera pas).

Lorsque tout ces éléments sont intégré au niveau, faites le test pour vérifier que le laser tourne.

## Déplacement linéaire du Moving Actor

Maintenant, on souhaite ajouter au Moving Actor la capacité de se déplacer d'un point à un autre, dans un mouvement de va-et-viens qui va apporter beaucoup de vivant et de challenge dans le jeu.

Ajouter le programme suivant au blueprint du Moving Actor :

(image 5) 

Ce programme permet de déplacer le Moving Actor d'une Target à une autre. 

Implémentez cette nouvelle fonction du Moving Actor dans le niveau. 

(image 6) 

Grâce aux déplacements d'objet du Moving Actor, nous pouvons désormais rajouter du vivant et de la difficulté dans le jeu.

## Pour aller plus loin 

Les Lasers ne sont pas les seuls objets que nous pouvons déplacer : les caméras ou même le sol peuvent être animés pour apporter de nouveaux défis au jeu. 

C'est désormais à vous de construire le jeu : vous avez les clés pour construire un jeu d'infiltration ! Ajoutez de nouvelles salles, inventez de nouveaux défis, et faites tester votre jeux aux autres apprenants pour vérifier qu'il est de bonne qualité !
