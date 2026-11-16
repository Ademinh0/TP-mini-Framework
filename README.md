# Mini-Framework CSS

Mini-framework CSS léger écrit en **SCSS**, réalisé dans le cadre du TP de Gestion de projet.

Il fournit des composants prêts à l'emploi (grille, boutons, cartes) utilisables directement via des classes HTML, sans écrire de CSS.



## Fonctionnalités

- **Grille** : 12 colonnes générées avec une boucle et un mixin.
- **Boutons** : primaire, secondaire, petit et grand.
- **Cartes** : image, titre, texte et bouton facultatifs.



## Prérequis

- [Node.js](https://nodejs.org/) (fournit `npx`)



## Commandes

### Compiler en continu (watch)

```bash
npx sass --watch scss/main.scss:css/style.css
```

### Compiler en version minifiée

```bash
npx sass scss/main.scss css/style.min.css --style=compressed --no-source-map
```



## Utilisation

Ouvrir `index.html` pour la démonstration. Les exemples HTML des composants sont dans ce README.

Charger `css/style.css` dans la page qui utilise le framework. Les couleurs, dimensions et espacements se règlent dans `scss/abstracts/_index.scss`.

La structure est séparée de l'apparence : `.btn` porte les règles communes et les modificateurs BEM définissent sa couleur ou sa taille. La grille peut contenir une carte sans que celle-ci dépende de sa largeur.

## Structure du projet

```
TP-mini-Framework/
├── index.html          # Planche des composants / documentation
├── css/                # CSS compilé (généré)
└── scss/
    ├── main.scss       # Point d'entrée
    ├── abstracts/      # Variables, mixins, fonctions
    ├── base/           # Reset, typographie
    ├── layouts/        # Grille, conteneurs
    ├── module/         # Composants
    ├── state/          # États
```



## Équipe

- **Ardem**
- **Benjamin**
- **Ange**



## Licence

Ce projet est distribué sous licence **MIT**.

## Gestion de projet

Product Owner : à désigner parmi les membres du groupe. Tableau Trello : à renseigner. Le PO priorise les cartes et valide leur passage en Terminé.

Les points ci-dessous sont une proposition pour le planning poker, à confirmer par l'équipe. Ils ne représentent pas un vote déjà réalisé. Pour chaque story, chacun propose une valeur parmi 1, 2, 3, 5 et 8, les écarts sont discutés, puis le groupe vote à nouveau.

### Backlog

#### Epic : structure et grille

**US01 — Variables et organisation — Must — 2 points**

En tant que développeur, je veux des variables et une organisation SCSS commune afin de modifier les styles au même endroit.

Acceptation : les valeurs de présentation sont dans `abstracts`, le SCSS compile et les styles sont répartis entre base, layouts, module et state.

**US02 — Grille — Must — 5 points**

En tant qu'intégrateur, je veux une grille de 12 colonnes afin de répartir mon contenu dans la page.

Acceptation : un mixin et une boucle génèrent les 12 tailles ; une ligne de 4 et 8 occupe toute la largeur ; les classes suivent BEM.

#### Epic : boutons

**US03 — Boutons — Must — 3 points**

En tant qu'intégrateur, je veux des boutons primaires, secondaires, petits et grands afin de distinguer les actions.

Acceptation : les quatre variantes sont affichées ; couleur et taille peuvent être combinées ; les boutons changent de teinte au survol.

#### Epic : cartes

**US04 — Carte — Must — 3 points**

En tant qu'intégrateur, je veux une carte avec des éléments facultatifs afin de présenter des contenus différents.

Acceptation : une carte complète contient une image, un titre, un texte et un bouton ; les versions sans image ou sans bouton fonctionnent avec les mêmes classes.

#### Epic : documentation et démonstration

**US05 — Documentation — Must — 2 points**

En tant qu'utilisateur du framework, je veux un exemple HTML pour chaque composant afin de savoir comment l'utiliser.

Acceptation : le README fournit du code copiable pour la grille, les quatre variantes de boutons et la carte ; les classes sont identiques aux exemples affichés dans la page.

**US06 — Démonstration — Must — 2 points**

En tant que visiteur, je veux voir les composants assemblés afin de vérifier leur rendu.

Acceptation : la page montre les 12 tailles de colonnes, les boutons et trois cartes disposées dans la grille ; l'image est fournie localement.

**US07 — Préparation de la revue — Must — 2 points**

En tant que membre de l'équipe, je veux un backlog, des règles de suivi et un support de revue afin de présenter le travail réalisé.

Acceptation : les stories ont une priorité, des points et un critère d'acceptation ; la Definition of Done, les limites WIP et le déroulé de revue sont écrits.

MoSCoW : ces sept stories sont Must car elles couvrent le sujet. Aucune story Should ou Could supplémentaire n'est retenue. Won't pour cette journée : responsive, qui n'est pas demandé.

### Definition of Done

- Le SCSS compile sans erreur.
- Les classes respectent BEM et utilisent les variables communes.
- Le composant est visible dans la page et son exemple HTML est fourni dans le README.
- Le rendu et les critères d'acceptation sont vérifiés sur ordinateur.
- Un autre membre du groupe relit le code.
- Le PO valide la story et la carte Trello est déplacée en Terminé.

### Kanban pour les six heures

Listes Trello : Backlog → À faire → En cours (WIP 2) → À valider (WIP 2) → Terminé.

Une carte par story : titre avec son code, sa priorité et ses points ; description avec la user story ; checklist avec ses critères d'acceptation. Une personne ne prend qu'une story à la fois. Si À valider est plein, on termine les validations avant de commencer autre chose. Le PO vérifie le tableau au début de la journée, à mi-parcours et avant la revue ; chacun déplace sa carte quand son état change.

Déroulé proposé : 30 minutes pour le PO, le backlog et le poker ; 4 heures pour réaliser et vérifier les composants ; 1 heure pour la documentation et les vérifications communes ; 30 minutes pour la revue et la rétrospective.

### Support de revue

1. Ouvrir `index.html`, montrer les colonnes, les variantes de boutons puis les trois cartes.
2. Montrer le mixin de colonne, la boucle et les variables, puis copier un exemple HTML du README.
3. Présenter le backlog final : code et documentation préparés ; compilation, largeurs des colonnes, liens et fichiers chargés vérifiés. Le rendu visuel sur ordinateur, la relecture par un membre du groupe et la validation du PO restent à faire. Les cartes ne sont pas déclarées validées à sa place.
4. Compléter en équipe ce qui n'a pas été terminé, les obstacles rencontrés et leurs raisons.
5. Rétrospective à discuter : garder les variables communes et les petites stories ; améliorer la coordination en fixant les noms de classes avant de répartir les composants.

Restent à renseigner en groupe : le PO, le lien Trello, les estimations issues du vrai planning poker et les validations de fin de journée.

## Exemples HTML

### Grille

```html
<div class="grid">
    <div class="col col--4">Colonne de 4</div>
    <div class="col col--8">Colonne de 8</div>
</div>
```

### Boutons

```html
<button type="button" class="btn btn--primary">Primaire</button>
<button type="button" class="btn btn--secondary">Secondaire</button>
<button type="button" class="btn btn--primary btn--small">Petit</button>
<button type="button" class="btn btn--primary btn--large">Grand</button>
```

### Carte

```html
<article class="card">
    <img class="card__image" src="meme.jpg" alt="Meme Distracted Boyfriend">
    <div class="card__body">
        <h3 class="card__title">Quand tu changes de framework</h3>
        <p class="card__text">Juste une image de meme dans la carte.</p>
        <a class="btn btn--primary" href="#grille">Voir la grille</a>
    </div>
</article>
```
