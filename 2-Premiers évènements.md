# 2 - Premiers évènements

Il est l'heure de programmer nos premiers évènements. 

## Portes et Alarmes

Notre objectif est de faire apparaître une porte à la fin du niveau lorsque le personnage entre dans le rayon d'action d'une caméra. 

![image](https://github.com/g404-code-gaming/Stealthgame/blob/main/image/2_evenement_1.png)

Voici ce qu'on souhaite faire, retraduit dans une forme plus "scrip" : 
  - Faire disparaître la porte par défaut pour que le personnage puisse passer au niveau suivant. Cela signifie que la porte est invisible, mais aussi qu'elle n'a pas de collision.
  - Reconnaître quand le personnage passe dans le rayon de détection de la caméra.
  - Faire fermer la porte lorsque la caméra vois le personnage. 

Commencez par 'ouvrir' la porte par défaut dans le [Level Blueprint](https://github.com/g404-code-gaming/UnrealEngine_cour/blob/main/Blueprint.md).

![image](https://github.com/g404-code-gaming/Stealthgame/blob/main/image/2_evenement_2.png)

Ensuite, on créer l'évènement qui reconnait quand le joueur entre dans le rayon d'action de la caméra. Cela allume une lumière d'alarme.

> N'oubliez pas de créer la Classe Caméra, dans laquelle dois figurer au moins une **sphère de colision** et une **lumière**.

![image](https://github.com/g404-code-gaming/Stealthgame/blob/main/image/2_evenement_3.png)

Tester le jeu pour voir si la lumière s'allume et s'éteint lorsque le joueur est vus par la caméra.

### Interaction entre les classes et le Level Blueprint : l'Event dispatcher

Nous voulons faire en sorte que la porte se ferme lorsque le joueur est révélé par la caméra. Néanmoins, comment faire cela alors que le script de détection par la caméra est dans un Class Blueprint, et que la porte ne fait pas partie de ce Blueprint. 

De plus, ce que nous avons fait dans le Level Blueprint ne fonctionne que pour une seule porte, et ne fonctionnera que pour une seule caméra. Nous voulons au contraire que n'importe quelle caméra peut déclencher l'alarme, et que l'alarme peut fermer toutes les portes.

Pour cela, nous allons utiliser un **Event Dispatcher** : une sorte de signal permettant aux Blueprint class de communiquer entre elles.

Dans le blueprint de la caméra, créer l'event **Reveal**, puis intégrez-le aux nodes en utilisant le node **Call**. 

![image](https://github.com/g404-code-gaming/Stealthgame/blob/main/image/2_evenement_4.png)

Ensuite, dans le Level Blueprint, nous allons créer des graphique de node conçus pour permettre à toutes les alarmes de fermer toutes les portes. 

Commençons par créer un graphique qui ferme toutes les portes, et un autre qui ouvre toutes les portes : 

![image](https://github.com/g404-code-gaming/Stealthgame/blob/main/image/2_evenement_5.png)

Ensuite, nous devons créer le graphique qui prend toutes les caméras et leur assigne un évènement qui ouvre la porte lorsque l'event dispatcher est appelé. 

![image](https://github.com/g404-code-gaming/Stealthgame/blob/main/image/2_evenement_6.png)

Maintenant que les graphiques sont fait, il reste à initialiser le graphique d'alarme et à ouvrir toutes les portes au debut du niveau. 

![image](https://github.com/g404-code-gaming/Stealthgame/blob/main/image/2_evenement_7.png)

## Bouton 

Puisque nous avons un système d'alarme qui ferme nos portes, nous allons désormais offrir au joueur l'opportunité de rattraper son erreur en stoppant l'alarme. Pour ça, nous allons créer une nouvelle classe : le **bouton**. 

Lorsque le personnage appuie sur une touche d'interaction en étant à proximité du bouton, il appuie sur ce dernier, ce qui ouvre les portes. 

Créez un nouvel objet Bouton. Ce dernier dois notammant contenir une boîte de colision pour qu'il puisse détecter le joueur proche. 



