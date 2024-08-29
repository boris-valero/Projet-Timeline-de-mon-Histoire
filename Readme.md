# Projet Timeline de mon Histoire

Ce projet est une page web qui affiche une timeline de ma passion pour l'informatique.

## Structure du projet

- `index.html` : Le fichier HTML principal qui contient la structure de la page.
- `script.js` : Le fichier JavaScript qui gère les animations de la timeline.
- `style.css` : Le fichier CSS qui contient les styles de la page.

## Détails des fichiers

### `index.html`

Ce fichier contient la structure de base de la page web. Il inclut les fichiers CSS et JavaScript nécessaires.

### `script.js`

Ce fichier contient le code JavaScript qui utilise l'API `IntersectionObserver` pour ajouter une classe CSS aux éléments de la timeline lorsqu'ils entrent dans la vue. Voici un extrait du code :

```js
const targets = document.querySelectorAll(".timeline ol li");
const threshold = 0.5;
const ANIMATED_CLASS = "in-view";
function callback(entries, observer) {
  // Logique de callback
}

const observer = new IntersectionObserver(callback, { threshold });
for (const target of targets) {
  observer.observe(target);
}
```

### [`style.css`]

Ce fichier contient les styles pour la page web, y compris les animations pour les éléments de la timeline. Voici un extrait du code :

```css
.timeline ol li.in-view .details p {
  transition-delay: 0.9s;
}

.page-footer {
  position: fixed;
  right: 0;
  bottom: 20px;
  display: flex;
  align-items: center;
  padding: 5px;
  background: rgba(255, 255, 255, 0.65);
}
.page-footer a {
  display: flex;
  margin-left: 4px;
}
```

## Installation

1. Clonez le dépôt.
2. Ouvrez [`index.html`] dans votre navigateur pour voir la page en action.

