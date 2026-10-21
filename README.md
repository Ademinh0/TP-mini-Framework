# Mini-Framework CSS

Mini-framework CSS léger écrit en **SCSS**, réalisé dans le cadre du TP de Gestion de projet.

Il fournit des composants prêts à l'emploi (grille, boutons, cartes) utilisables directement via des classes HTML, sans écrire de CSS.



## Fonctionnalités

- **Grille** :
- **Boutons** :
- **Cartes** :



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
    └── theme/          # Thèmes
```



## Équipe

- **Ardem**
- **Benjamin**
- **Ange**



## Licence

Ce projet est distribué sous licence **MIT**.
