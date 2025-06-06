[EN](../README.md) | **FR**

<div>
  <img class="has-dark" src="https://browserux.com/assets/img/logo/logo-browserux-css-250.png" alt="logo Browser UX v2.0.0"/>
</div>

# `browserux.css`

**`browserux.css`** est une **base CSS** minimaliste, centrée sur l’**expérience utilisateur** et l’**accessibilité**.
Conçu pour renforcer les comportements natifs de HTML et CSS, il offre une base **moderne et cohérente**, qui améliore l’**ergonomie sur tous les appareils**, avant même d’avoir recours à des classes utilitaires, à des frameworks lourds ou à JavaScript.

- [Documentation](./DOC.md)
- [Changelog](./CHANGELOG.md)

<br>

[![npm version](https://img.shields.io/npm/v/browserux.css.svg)](https://www.npmjs.com/package/browserux.css)
[![size](https://img.shields.io/bundlephobia/min/browserux.css)](https://bundlephobia.com/result?p=browserux.css)
[![License: MIT](https://img.shields.io/badge/license-MIT-green.svg)](https://opensource.org/licenses/MIT)

---

<br>

## 📚 Table of Contents

- ❓ [Pourquoi `browserux.css`](#-pourquoi-browseruxcss)
- 🧠 [Philosophie](#-philosophie)
- 🧬 [Structure du fichier](#-structure-du-fichier)
- ✨ [Fonctionnalités](#-fonctionnalités)
- 🚀 [Comment l’utiliser](#-comment-lutiliser)
- 🌎 [Support Navigateurs](#-support-navigateurs)
- 🤝 [Contribuer au projet](#-contribuer-au-projet)
- 🙏 [Remerciements](#-remerciements)
- ⚖️ [Licence](#%EF%B8%8F-licence)

---

<br>

## ❓ Pourquoi `browserux.css`

La plupart des projets front-end commencent avec un `reset.css` ou un `normalize.css`. Pourtant, malgré leurs intentions, notamment celle de Normalize, qui cherche à préserver les comportements utiles des navigateurs, on finit presque toujours par ajouter nos propres ajustements : suppression des marges, `box-sizing: border-box`, améliorations typographiques, etc.

Mais le web a évolué. L’expérience utilisateur est devenue un critère central, et les navigateurs modernes offrent désormais des capacités CSS natives souvent sous-utilisées : scrollbars personnalisables, gestion du focus clavier, prise en charge des préférences utilisateur comme le mode sombre ou la réduction des animations…

`browserux.css` va plus loin qu’un simple reset. Il propose une base moderne et légère, pensée pour améliorer l’ergonomie, l’accessibilité et la cohérence visuelle des éléments natifs du navigateur, sans JavaScript, sans classes utilitaires, et sans surcharge.

---

<br>

## 🧠 Philosophie

### 📌 Objectifs

- Fournir un fichier CSS de base complet et léger, pensé dès le départ pour améliorer l’expérience utilisateur et l’accessibilité.
- Proposer une alternative moderne aux fichiers de base traditionnels (reset.css, normalize.css, etc.).

<br>

### 📐 Ligne directrice 

- Utiliser exclusivement les éléments HTML natifs, sans recourir à des classes utilitaires.
- S’articuler autour de quatre piliers fondamentaux :
  - 🔄 Reset.
  - ⚙️ Normalisation.
  - 🧩 Ergonomie.
  - ♿ Accessibilité.

---

<br>

## 🧬 Structure du fichier

`browserux.css` est structuré en quatre parties logiques afin d’assurer clarté, évolutivité et facilité de maintenance :

### 🔣 1. Variables

L’utilisation des variables CSS garantit un système de design cohérent et permet une personnalisation facile du thème (mode clair/sombre, ajustements de couleurs, etc.).
Toutes les valeurs fondamentales sont définies ici :
- 🎨 Couleurs globales
- ✅ Couleurs des éléments de validation de formulaires
- ⏳ Couleurs de la barre de progression
- 🖍️ Sélection de texte
- 🖱️ Scrollbar
- 🔤 Typographie

### ⚙️ 2. Préférences utilisateur du navigateur

Gère les préférences propres à l’utilisateur, détectées via les media queries :
- 🌙 Préférences du thème.
- 🎛️ Préférences des animations.

### 🧩 3. Thème de l’interface navigateur

Applique une personnalisation visuelle aux éléments natifs du navigateur :
- 🖍️ Sélection de texte.
- 🖱️ Barre de défilement.
- 📋 Composants de formulaire.
- 🔽 Composants interactifs repliables.
- 🎯 Accessibilité du focus clavier.

### 🧱 4. Styles par défaut du navigateur

Intégration équilibrée des 4 axes fondamentaux, organisée de manière logique :
- 🔧 Réinitialisation des espacements
- 📦 Modèle de boîte
- 🧱 Élément racine HTML
- 📑 Sections
- 🗂️ Regroupement de contenu
- ✏️ Sémantique au niveau du texte
- 🖼️ Contenu embarqué
- 📊 Données tabulaires
- 🧾 Formulaires
- 🔽 Éléments interactifs

---

<br>

## ✨ Fonctionnalités

`browserux.css` est une base CSS moderne, légère et 100 % native (HTML/CSS pur), conçue pour répondre aux besoins des projets front-end actuels. Elle couvre les fondations essentielles pour garantir cohérence, accessibilité et ergonomie, dès le premier octet.

### 🔄 Reset

`browserux.css` applique un reset minimaliste pour supprimer les styles par défaut indésirables des navigateurs, tout en conservant les comportements utiles.

- Réinitialisation universelle des espacements (margin / padding à 0).
- Réinitialisation du modèle de boite à `border-box`.
- Suppression des styles de listes et des indentations de tableaux.
- Neutralisation des boutons et champs de formulaire.
- Éléments médias rendus réactifs.
- Nettoyage des bordures de focus par défaut sur Firefox.
- Neutralisation des styles de validation des champs.

### ⚙️ Normalisation

Standardise les éléments entre navigateurs pour garantir un comportement cohérent.

- Uniformisation de la typographie de base (taille, police, interligne)
- Uniformisation des comportements typographiques (`b`, `small`, `sub`, `sup`).
- Apparence des champs de formulaire harmonisée.
- Affichage unifié des listes et tableaux.
- Réactivité améliorée des contenus médias.
- Comportement des scrollbars cohérent.

### 🧩 Ergonomie

Optimise la fluidité des interactions UX et réduit les frictions sur tous types d’appareils.

- Défilement fluide (si l'utilisateur ne l’a pas désactivé via ses préférences).
- Optimisation du tap sur mobile (`touch-action: manipulation`).
- Empêche les contenus médias de déborder de leur conteneur.
- Désactivation de la sélection de texte non souhaitée sur les éléments interactifs.
- Affichage forcé des scrollbars pour éviter les sauts de layout.
- Amélioration des curseurs pour les éléments interactifs.

### ♿ Accessibilité 

Garantit que le site reste utilisable pour tous les utilisateurs, y compris ceux utilisant des technologies d’assistance.

- Respect des préférences système : mode sombre et réduction des animations.
- Contours de focus visibles au clavier via `:focus-visible`.
- Prise en charge de `accent-color` pour les champs de formulaire.
- Curseur d’aide sur les éléments contenant des infos supplémentaires (`abbr`, `dfn`).
- Styles de validation neutres (notamment sur Firefox).
- Scrollbars visibles et personnalisées, sans les masquer via des hacks CSS.

---

<br>

## 🚀 Comment l’utiliser

Que vous développiez un site statique ou un projet front-end moderne, `browserux.css` s’intègre facilement à tous les workflows.  
Voici trois méthodes simples pour l’ajouter à votre projet :

### 🔗 Utiliser le CDN

Vous pouvez inclure directement la dernière version via jsDelivr :

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/Effeilo/browserux.css/browserux.css">
```

### 💾 Télécharger et héberger localement

Vous pouvez également télécharger le fichier :

- `browserux.css`.

Puis l'inclure localement dans votre projet :

```html
<link rel="stylesheet" href="/path/to/browserux.css">
```

### 📦 Utilisation via npm

Vous pouvez aussi installer `browserux.css` via npm pour une meilleure intégration avec les workflows modernes (Vite, Webpack, Parcel, etc.) :

```bash
npm install browserux.css
```

Une fois installé, vous pouvez l’importer dans votre projet :

#### Lien direct depuis `node_modules/` (dans votre HTML)

```html
<link rel="stylesheet" href="./node_modules/browserux.css/browserux.css">
```

#### Import direct dans JavaScript (Vite, Webpack, Parcel)

Si votre outil de build prend en charge les imports CSS (comme Vite, Webpack...), vous pouvez importer directement le fichier CSS dans votre point d’entrée JavaScript :

```javascript
import 'browserux.css/browserux.css';
```

---

<br>

## 🌎 Support Navigateurs

- 🌈 Chrome (dernières versions)  
- 🦊 Firefox (dernières versions)  
- 🧭 Safari 13+ 
- 📘 Edge Chromium 
- 🤖🌐 Navigateurs Android modernes
- 📱🧭 Safari iOS 13+

> ⚡ Aucun support des anciens navigateurs comme IE11. Une approche d'amélioration progressive garantit une dégradation élégante et fonctionnelle.

---

<br>

## 🤝 Contribuer au projet

Les contributions sont les bienvenues ! Que vous souhaitiez signaler un bug, proposer une amélioration, ajouter une fonctionnalité ou corriger une coquille, n'hésitez pas à participer.

### 🛠️ Issues & feedback

- Ouvrez une issue pour :
  - Signaler un bug.
  - Suggérer une amélioration ou nouvelle fonctionnalité.
  - Discuter d’une idée avant de soumettre une PR.
- Toute remarque ou retour est apprécié, même non technique !

<br>

### 🔄 Comment contribuer

1. Forkez ce dépôt.
2. Créez une branche (`git checkout -b ma-proposition`).
3. Apportez vos modifications.
4. Faites un commit (`git commit -m 'Ajout : ma-proposition'`).
5. Poussez la branche (`git push origin ma-proposition`).
6. Ouvrez une Pull Request.

<br>

### ✅ Bonnes pratiques

- Restez fidèle à l’approche minimaliste, accessible et native du projet.
- Commentez votre code pour faciliter la relecture.
- Privilégiez des modifications claires, ciblées et documentées.
- Vérifiez vos changements dans les dernières versions des navigateurs modernes avant de proposer une PR.

---

<br>

## 🙏 Remerciements

Inspiré des bonnes pratiques de :

- [Modern Normalize](https://github.com/sindresorhus/modern-normalize)
- [Paul Irish's box-sizing border-box method](https://www.paulirish.com/2012/box-sizing-border-box-ftw/)
- [CSS Tricks Articles](https://css-tricks.com/)
- [WebAIM Accessibility Guidelines](https://webaim.org/)

---

<br>

## ⚖️ Licence

**Licence MIT**, Libre d’utilisation, de modification et de distribution.

- [Détails Licence MIT](./LICENCE.md)

---

<br>

#### Fait avec ❤️ par Effeilo
