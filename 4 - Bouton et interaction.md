# 4 - Bouton et Interaction

Nous avons des portes qui se referment lorsque l'alarme est sonnée. Désormais, il faut ajouter un moyen d'ouvrir les portes à nouveaux, pour permettre au joueur de recommencer le niveau sans avoir besoin de relancer tout le jeu.

![image 1]()

## Création du bouton 

Ajouter une nouvelle [classe]() **Bouton**. 

Cette classe consiste essentiellement en un **objet** rond sur le mur, qui est illuminé par une **lumière** et possède une box de collision.

La box de collision dois être placée devant le bouton pour que le joueur puisse la traverser.

![image 2]()

Lorsque le joueur se tient à cotés du bouton, il a la possibilité d'appuyer sur une touche d'interaction, ce qui active le bouton et ouvre toutes les portes.

## Interaction

Afin de compléter le blueprint, nous allons avoir besoin de paramétrer quelques touches supplémentaires : Il faut en effet choisir avec quel bouton on souhaite interagir.

Allez dans les **paramètres du projet**, trouver les **Entrées** (Input). Dedans, il faut ajouter une **nouvelle association** (Binding) : une action nommée **Interact**.

A vous de choisir quelle touche vous voulez assigner à l'interaction. Vous pourrez toujours la changer plus tard si nécessaire.

![image 3]()

Ensuite, nous allons ajouter un **BLueprint Interface**. 
Ce dernier sers à gérer les interactions entre les actions des paramètres et les objets de la scène.

![image 4]()

Dans cet interface, ajouter une fonction **interaction**. 

![image 5]()

Vous n'avez rien de plus à faire ici : tout le reste sera dans les Blueprints.

## Blueprint

Dans le Blueprint de votre personnage, qui a été créé dans le chapitre précédent, ajouter le graphique pour interragir avec les objets.

Ce graphique vérifie lorsque le personnage est en collision avec un objet qui a un interface implémenté. Le programme appelle alors la fonction d'interaction.

![image 6]()

Ensuite, ouvrez votre **Bouton**. Allez dans les **Class Settings** et implémentez le BP-Interface. 

![image 7]()

Dans le Blueprint du Bouton, ajouter les nodes permettants de reconnaître quand le bouton est pressé.

- (1) afficher un message au joueur pour qu'il sache quelle touche utilisée pour pressé le bouton.
- (2) Pour ce graphique, on utilise Gate, un outil permettant de déclencher des évènements en fonction de certaines conditions simples. En effet, l'évènement ne se déclenche que si on appuie sur le bouton ET qu'on est en collision avec le bouton.
- (3) Ajoutez un Event dispatcher Used qui servira plus tards dans le Level-Blueprint.
- (4) Lorsque le bouton est pressé, un indicateur lumineux s'éteint et se rallume pour indiquer au joueur que son action à réussis.

![image 8]()

Testez votre projet : ajoutez un bouton au niveau et passez devant pour voir si le message apparait. Vérifier que la lumière clignote si vous appuyer sur le bouton d'interaction. 

Lorsque tout ça a fonctionné, il faut désormais relier le bouton aux portes afin qu'il puisse toutes les ouvrir. 

Dans le **Level-Blueprint**, Créer un nouveau Custom **Event Initialyze Bouton Reset Alarme**, qui va liée tout les objets Boutons à un évent de Reset alarme. 
Cela fonctionne un peu comme la détection par les caméras : on prend tout les acteurs de type Bouton, et on leur crée un custom event spécial qui permet d'appeler la fonction Open Door. 

![image 9]()

Afin que les caméra puissent toujours refermer les portes, il faut réactiver l'évènement d'alarme. 

![image 10]()

Comme à chaque fois qu'on crée des custom event pour tout les objets, il faut initialiser la construction des évènements lors du BeginPlay. 

![image 11]()

Testez le jeu ! 

Désormais, vous avez les bases de la programmation par Blueprint en utilisant les classes. Vous savez créer des Classes d'acteurs, leur donner du script pour des fonctionnements de base, et même les relier entre eux grâce à des Events dispatcher.

[5 - Actions du personnage](https://github.com/g404-code-gaming/Stealthgame/blob/main/4%20-%20Actions%20du%20personnage.md)
