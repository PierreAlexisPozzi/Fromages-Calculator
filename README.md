# 🧀 Fromage Calculator

Calculateur de quantités pour les repas fromagers : **raclette, fondue, tartiflette et croziflette**.
Indiquez le nombre de convives par appétit (😒 Éco, 😋 Normal, 🤤 Gourmand) et l'application calcule ce qu'il faut acheter.

[Edit in StackBlitz next generation editor ⚡️](https://stackblitz.com/~/github.com/PierreAlexisPozzi/Fromages-Calculator)

## Fonctionnalités

- **4 recettes** avec leur thème de couleurs, leurs fromages conseillés et leurs astuces
- **3 profils d'appétit** : Éco (80 %), Normal (100 %), Gourmand (120 %)
- **Quantités lisibles** : passage automatique en kg / litres au-delà de 1000 g / 1000 ml
- **Conversion en achats** : nombre de reblochons, bouteilles de vin, pots de crème, barquettes de lardons, paquets de crozets
- **Liste de courses** à copier ou partager (WhatsApp, SMS... via le partage natif sur mobile)
- **Quantités personnalisables** par personne, avec retour aux valeurs recommandées
- **Réglages mémorisés** dans le navigateur (localStorage, aucun cookie)
- **Lien direct par recette** : `…/#fondue`, `…/#tartiflette`, `…/#croziflette`
- Responsive (menu latéral sur PC, popup de saisie sur mobile), navigation au clavier, respect de `prefers-reduced-motion`

## Lancer en local

L'application est un unique fichier `index.html` sans build.

```bash
npm install
npm start   # serveur local avec rechargement automatique (servor)
```

Ou ouvrez simplement `index.html` dans un navigateur.

## Ajouter une recette

Dans `index.html`, ajoutez une entrée à l'objet `recipes` (titre, couleurs, ingrédients avec `baseValue` par personne en mode Normal, fromages, conseils), puis un lien `.recipe-option` avec le `data-recipe` correspondant dans le menu.
Pour afficher une conversion en conditionnement, ajoutez `pack: { size, singular, plural }` à l'ingrédient.
