# Nouveau projet

Commençons par créer un projet avec le template **First Personn**

![image](https://github.com/g404-code-gaming/Stealthgame/blob/main/image/1_environnement_1.png)

Ensuite, dans notre projet, nous allons créer notre propre répertoire : créez le dossier **Stealthgame**, dans lequel nous mettrons un dossier pour nos images et créerons un niveau niveau.

![image](https://github.com/g404-code-gaming/Stealthgame/blob/main/image/1_environnement_2.png)

# Premiers objets et modélisation

Dans ce niveau, il n'y a rien pour le moment. Afin de voir ce que nous allons faire, il faut ajouter de la **lumière**.

![image](https://github.com/g404-code-gaming/Stealthgame/blob/main/image/1_environnement_3.png)

Créons maintenant nos premiers objets en utilise le mode **modélisation**. 

![image](https://github.com/g404-code-gaming/Stealthgame/blob/main/image/1_environnement_4.png)

Ce mode permet de créer rapidement de nouveaux objets à partir de formes géométriques simples ou d'outils supplémentaires. 
Une fois que vous avez créer un objet qui vous convient, il faut **valider** la création. 

Afin de construire très rapidement des niveaux, nous allons utiliser l'outil **CubeGrid**

![image](https://github.com/g404-code-gaming/Stealthgame/blob/main/image/1_environnement_5.png)

Cet outil permet de construire facilement des sols, murs, et formes géométriques personnalisés :
  - Sélectionner les cases de votre grille sur lesquelles vous voulez travailler.
  - utiliser **'E'** pour extraire des cubes et commencer à construire un mur ou un sol.
  - utiliser **'Q'** pour annuler votre action ou créer un trou dans votre objet.

Afin cet outil, notre première salle sera construite en un rien de temps. 

> Attention, une fois la modélisation validée, tout le travail en cours deviens un seul et unique objet.

### Texture

Les murs gris, c'est bien 5minutes, mais le projet rendrait mieux avec quelques **textures** : ajoutez une texture à votre salle.
Il existe des textures déjà existante dans Unreal Engine, mais vous pouvez ajouter vos propres textures en les important dans le dossier Image créé plus tôt.

![image](https://github.com/g404-code-gaming/Stealthgame/blob/main/image/1_environnement_6.png)

Avec ça, notre niveau commence à ressembler à quelque chose. 

Créez une **deuxième salle** qui servira de première épreuve.
Une fois que c'est fait, créez deux nouveaux objets : 
  - 📷 une **caméra**, qui va servir à détecter notre personnage et déclencher des alarmes.
  - 🚪 une **porte**, qui va bloquer le passage du joueur entre les salles et se refermer si l'alarme est sonnée. 

Nous pourrons ensuite commencer à créer les évènements d'alarme : 

[2 - Alarme et portes]()

