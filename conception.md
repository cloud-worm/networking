# Conception du Site

## 1 Aspect graphique, Web Design

### 1.1 Mise en page

Pour une lisibilté otpimale, le texte du site est arrangé dans une grande colonne centrale, définie dans le css par la classe `.content_width`. Notons que ce n'est pas le `body` qui est arrangé de la sorte ; lui, en effet, voit son attribut `margin` mis à `0`. Ceci permet une insertion plus facile de balises horizontales dont la largeur est celle de l'écran (`hr`, `div#navbar`).

### 1.2 Spécifications sur la police

La police par défaut du paragraphe (balise `p`) est de `16px` ; les titres de niveau 2, utilisés courramment au sein du site, sont de police `24px`. D'autres titres sont présents, de tailles variables. Les liens présents dans la barre de navigation sont également de `24 px` ; ces valeurs sont majoritairement arbitraires, et ont simplement été choisies pour une bonne lisibilité/clareté.

La pose utilisée dans le site est _PT Sans_. Cette police est légérement plus fine et condensée que la _Sans Serif_ par défaut, ce qui a permi la conception d'une barre de navigation et de titres plus agréables.

Pour les liens en barre de navigation et au pied de la page, la police est en _small caps_.

### 1.3 Choix stylistiques

On remarque un style général minimaliste. Peu de couleurs sont présentes, mais celles qui le sont sont importantes : du texte noir sur un fond blanc, et des titres dégradés (`linear-gradient` orienté en diagonale allant du rose au cyan en passant par le vers, environ). Le dégradé des titres a été choisi pour créer un site unique et dont l'impacte stylistique est forte.

Quand aux images de la partie "Exemples", elle ont un `border-radius` de `10px`, car j'ai trouvé que cela allait mieux avec l'esthétique minimaliste du site.

Quelques sources d'inspiration sont le guide du _Material Design_ de Google et le style d'interface graphique d'Apple.

### 1.4 Organisation du contenu

Une page du site comporte quatre parties :
1. L'entête
2. La barre de navigation
3. Le contenu
4. Le footer

On remarque que la barre de navigation est _sticky_, c'est-à-dire qu'elle est maintenue en haut de l'écran même si l'utilisateur fais défiler le site. Ceci peut être utile si, à la fin d'une des pages, l'utilisateur veut instantanément changer de page du site sans effort. C'est une optimisation de l'expérience utilisateur, qui a en même temps un rôle stylistique important.

## 2 Programmation du site

### 2.1 Organisation du code

Le code du site peut paraître chaotique, notamment vis-à-vis du nom des classes. En effet, il m'est arrivé de créer une classe ou une ID pour un élément spécifique que j'ai fini par réutiliser autre part, sans me préoccuper d'un changement de nom, pour plus d'efficacité. Ceci a pu mener à des noms qui paraissent incohérents, tels que "TL", "TXL", "SMT" pour désigner différents types de titres.

Mis à part ceci, le code est relativement bien organisé et cohérent. Il y a quelques commentaires personnels dans le CSS.

### 2.2 Hiérarchie des fichiers

La racine du site (dossier `networking/`) contient les dossiers suivants : `media/` pour les ressources audiovisuelles, `un`, `deux`, et `trois` pour les chapitres correspondants, `exemples` pour la page correspondante, et `Fonts` pour la seule police du site, ce qui est un peu vain.

Il y a un fichier `index.html` dans la racine et dans chaque dossier de page, afin de créer un site internet dont les pages ne s'appellent pas `deux.html` mais simplement `/deux`, ce qui me semble plus professionnel.

La racine et chaque dossier de page contient son propre fichier CSS, même s'il est pratiquement identique entre les chapitres et la page des exemples.

### 2.3 Diverses techniques

Pour le dégradé des titres, j'utilise du _clipping_ de texte, qui affiche le fond d'écran d'un élément sur le texte à la place du fond-même. Il y a également des classes pour les titres qui me permettent d'adapter la taille du dégradé à la taille du titre (faisable en JavaScript, mais bon...).

La barre de navigation _sticky_ fonctionne grâce à du CSS, tout simplement (cf. les fichiers sources CSS).

## Contenu

Le contenu textuel est totalement original. 
