# CDA Integration Front-end

Projet frontend pour la plateforme "English Game" - Une plateforme immersive d'apprentissage de l'anglais basée sur des challenges inter-écoles.

---

## Table des matières
- [Organisation du projet](#organisation-du-projet)
- [Choix techniques](#choix-techniques)
- [Stratégie responsive](#stratégie-responsive)
- [Difficultés rencontrées](#difficultés-rencontrées)
- [Axes d'amélioration](#axes-damélioration)

---

## Organisation du projet

Le projet est structuré de manière modulaire et scalable :

```
CDA-Integration-front-end/
├── index.html                 # Page principale HTML
├── package.json              # Dépendances et scripts
├── assets/                   # Ressources statiques
│   ├── icons/               # Icônes et images vectorielles
│   ├── mds.png              # Logo
│   └── avatar.jpg           # Avatar utilisateur
├── css/
│   └── style.css            # CSS compilé (généré à partir du SCSS)
└── scss/                     # Feuilles de style SCSS
    ├── main.scss            # Point d'entrée SCSS
    ├── abstracts/           # Variables et mixins
    │   ├── _variables.scss  # Couleurs, typographie, breakpoints
    │   └── _mixins.scss     # Utilitaires et mixins réutilisables
    ├── base/                # Styles de base
    │   ├── _reset.scss      # Reset CSS
    │   └── _typo.scss       # Typographie globale
    ├── components/          # Composants réutilisables
    │   ├── _buttons.scss    # Styles des boutons
    │   ├── _cards.scss      # Styles des cartes
    │   └── _navbar.scss     # Styles de la navigation
    └── layout/              # Sections principales
        ├── _challenge.scss  # Section Challenge
        ├── _hero.scss       # Section Hero
        ├── _learning.scss   # Section Learning
        ├── _project.scss    # Section Project
        └── _schedule.scss   # Section Planning
```

### Architecture SCSS 
Le projet utilise cette architecture :
- **abstracts** : Variables et fonctions réutilisables
- **base** : Styles globaux et resets
- **components** : Modules indépendants et réutilisables
- **layout** : Sections principales de la page

---

## Choix techniques

### Language & Markup
- **HTML5** : Sémantique moderne avec structure claire des sections
- **Fonts** : Inter (weights: 400, 600, 800) depuis Google Fonts pour une meilleure performance

### Styling
- **SCSS** : Préprocesseur CSS pour une meilleure organisation et maintenabilité
  - Variables pour les couleurs, espacements, typographie
  - Mixins pour les patterns répétitifs
  - Nesting pour une meilleure lisibilité
  - Modularisation par fonctionnalité

### Architecture CSS
- **BEM-inspired naming** : Convention de nommage claires (ex: `topbar__content`, `challenge__grid`)
- **CSS Grid & Flexbox** : Layouts modernes et flexibles
- **CSS Custom Properties** : Réutilisation de valeurs
- **Clip-path SVG** : Formes personnalisées sur les cartes learning

### Structure de la page
- **Navigation supérieure** : Barre de navigation sticky avec logo, menu principal et account
- **Navigation mobile** : Barre de navigation inférieure (`bottom-nav`) pour l'accessibilité mobile
- **Sections stratégiques** :
  - Hero : Présentation principale
  - Challenge : Propositions de valeur
  - Schedule : Planning de la semaine
  - Project : Livrables et gestion de fichiers
  - Learning : Ressources pédagogiques
  - Footer : Navigation secondaire et liens

---

## Stratégie responsive

### Breakpoints
Les breakpoints sont définis dans les variables SCSS et permettent une adaptation fluide sur tous les appareils.

### Approches responsive

#### 1. **Mobile-first Design**
- Styles mobile par défaut dans les fichiers SCSS
- Media queries pour augmenter les tailles d'écran
- Classes conditionnelles (ex: `.mobile`) pour masquer/afficher des éléments

#### 2. **Flexbox & Grid**
- Utilisation intensive de Flexbox pour les alignements flexibles
- CSS Grid pour les layouts complexes (ex: `challenge__grid`, `footer__grid`)
- Propriétés comme `flex-wrap` pour s'adapter à l'espace disponible

---

## Difficultés rencontrées

 - Passage du rendu téléphone à desktop sur certaine partie du projet.
 - Forme des cards de la section learning.

---

## Axes d'amélioration

 - Forme des cards de la section learning.
 - effet de hover, animations etc ...
 - dynamiser le rendu ( éviter des répétition de code mais nécéssite du JS)

---

## Pour démarrer

### Prérequis
- Un navigateur moderne (Chrome, Firefox, Safari, Edge)
- Node.js (si compilation SCSS en local)

### Installation
```bash
# Cloner le projet
git clone <repository-url>

# Installer les dépendances
npm install

# Compiler les fichiers SCSS
npm run sass
```

### Compilation SCSS
- Les fichiers SCSS se trouvent dans le dossier `scss/`
- Ils sont compilés en `css/style.css`
- Le fichier principal est `scss/main.scss`

---


