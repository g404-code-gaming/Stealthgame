# 8 - Animations

Les portes qui disparaissent et les lasers statiques, c’est amusant deux minutes, mais si on veut donner un peu plus de dynamisme et d’intérêt à notre jeu, nous allons devoir créer des animations.

## Animation des portes 

### Open Door

Nous allons commencer par apprendre les animations simples en modifiant nos portes : au lieu qu'elles disparaissent et réapparaissent, nous allons faire en sorte qu'elles s'ouvrent et se ferment.

Dans votre classe de **Porte**, ajoutez un Animator Sequencer parmi les composants. Renommez-le **Open** : c’est l’animation d’ouverture de nos portes.

![image 1]()

Dans l'animator, ouvrez le **sequenceur** en utilisant le bouton *Open in tab*.

![image 2]()

Dans notre animation, nous souhaitons que la porte s’ouvre en se levant vers le haut, comme une herse. Pour ce faire, suivez les étapes suivantes :

![image 3]()
![image 4]()
![image 5]()
![image 6]()

Vous pouvez lancer un aperçus depuis le séquenceur pour vérifier que l'animation se fait bien comme prévus. 

### Close Door et implémentation

Créez une nouvelle séquence **Close** en répétant les étapes de la partie précédente, mais en inversant le mouvement de l’animation (la porte part du haut puis descend) pour inclure votre animation de fermeture de porte.

Une fois que votre animation finale est faite, ajouter à votre porte une variable *Ouvert*, sers à déterminer si elle est ouverte ou fermée.

![image 7]()

Désormais, dans le **level blueprint**, il faut modifier les customs events d'ouverture et de fermeture des portes pour inclure les nouvelles animations : au lieu de rendre (in)visible et (in)tangible les portes, on va directement déclencher leur animation. 

Puisqu'on ne veux pas que les portes s'ouvre/ferme plusieurs fois d'affilées (par exemple, si le joueur se fait repérer plusieurs fois de suite par une caméra), nous ajoutons un vérification de la variable *Ouvert* : Si Ouvert est faux, alors les portes sont donc fermée et ne peuvent pas se refermée. A l'inverse, si la variable est vraie, c'est que les portes sont déjà ouvertes et ne peuvent pas s'ouvrir à nouveau : seulement se fermer.

![image 8]()

