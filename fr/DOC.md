[EN](../en/DOC.md) | **FR**

<div>
  <img class="has-dark" src="https://browserux.com/assets/img/logo/logo-browserux-css-250.png" alt="logo Browser UX"/>
</div>

# 📘 Documentation de `browserux.css`

Bienvenue sur la documentation de `browserux.css`.

## 📚 Sommaire

- 🧠 [I. Philosophie](#-i-philosophie)
  - 📌 [Objectifs](#-objectifs)
  - 📐 [Ligne directrice](#-ligne-directrice)
- 🚀 [II. Comment l'utiliser](#-ii-comment-lutiliser)
  - 🔗 [Utiliser le CDN](#-utiliser-le-cdn)
  - 💾 [Télécharger et héberger localement](#-télécharger-et-héberger-localement)
  - 📦 [Utilisation via npm](#-utilisation-via-npm)
  - 📋 [Résumé rapide](#-résumé-rapide)
  - 💡 [Notes](#-notes)
- 📄 [III. Contenu du fichier](#-iii-contenu-du-fichier)
  - 🔣 [1. Variables CSS](#-1-variables-css)
    - 🎨 [Couleurs globales](#-couleurs-globales)
    - ✅ [Couleurs des éléments de validation de formulaires](#-couleurs-des-éléments-de-validation-de-formulaires)
    - ⏳ [Couleurs de la barre de progression](#-couleurs-de-la-barre-de-progression)
    - 🖍️ [Sélection de texte](#-sélection-de-texte-selection)
    - 🖱️ [Scrollbar](#%EF%B8%8F-scrollbar)
    - 🔤 [Typographie](#-typographie)
  - ⚙️ [2. Préférences utilisateur du navigateur](#2-%EF%B8%8F-préférences-utilisateur-du-navigateur)
    - 🌙 [Préférences du thème](#-préférences-du-thème-prefers-color-scheme)
    - 🎛️ [Préférences des animations](#%EF%B8%8F-préférences-des-animations-prefers-reduced-motion)
    - 🌓 [Préférences de contraste](#-preferences-de-contraste-prefers-contrast)
  - 🧩 [3. Thème de l'interface du navigateur](#3--thème-de-linterface-du-navigateur)
    - 🖍️ [Sélection de texte](#%EF%B8%8F-sélection-de-texte-selection)
    - 🖱️ [Barre de défilement](#%EF%B8%8F-barres-de-défilement)
    - 📋 [Composants de formulaire](#composants-de-formulaire)
    - 🔽 [Composants interactifs repliables](#-composants-interactifs-repliables)
    - 🎯 [Accessibilité du focus clavier](#-accessibilité-du-focus-clavier)
  - 🧱 [4. Styles par défaut du navigateur](#4--styles-par-défaut-du-navigateur)
    - 🔧 [Réinitialisation des espacements](#-réinitialisation-des-espacements)
    - 📦 [Modèle de boîte](#-modèle-de-boîte)
    - 🧱 [Élément racine HTML](#-élément-racine-html)
    - 📑 [Sections](#-sections)
    - 🗂️ [Regroupement de contenu](#%EF%B8%8F-regroupement-de-contenu)
    - ✏️ [Sémantique au niveau du texte](#%EF%B8%8F-sémantique-au-niveau-du-texte)
    - 🖼️ [Contenu embarqué](#%EF%B8%8F-contenu-embarqué)
    - 📊 [Données tabulaires](#-données-tabulaires)
    - 🧾 [Formulaires](#-formulaires)
    - 🔽 [Éléments interactifs](#-éléments-interactifs)
- 🌎 [IV. Support Navigateurs](#-iv-support-navigateurs)
- 🤝 [V. Contribuer au projet](#-v-contribuer-au-projet)
  - 🛠️ [Issues & feedback](#%EF%B8%8F-issues--feedback)
  - 🔄 [Comment contribuer](#-comment-contribuer)
  - ✅ [Bonnes pratiques](#-bonnes-pratiques)
- ⚖️ [VI. Licence](#%EF%B8%8F-vi-licence)

---

<br>

## 🧠 I. Philosophie

### 📌 Objectifs

- Fournir un fichier CSS de base complet et léger, pensé dès le départ pour améliorer l’expérience utilisateur et l’accessibilité.
- Proposer une alternative moderne aux fichiers de base traditionnels (reset.css, normalize.css, etc.).

<br>

### 📐 Ligne directrice 

- Utiliser exclusivement les éléments HTML natifs, sans recourir à des classes utilitaires.
- S’articuler autour de quatre piliers fondamentaux :
  - 🔄 Reset
  - ⚙️ Normalisation
  - 🧩 Ergonomie
  - ♿ Accessibilité

---

<br>

## 🚀 II. Comment l’utiliser

Que vous développiez un site statique ou un projet front-end moderne, `browserux.css` s’intègre facilement à tous les workflows.  
Voici trois méthodes simples pour l’ajouter à votre projet :

### 🔗 Utiliser le CDN

Vous pouvez inclure directement la dernière version via jsDelivr :

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/Effeilo/browserux.css/browserux.css">
```

<br>

### 💾 Télécharger et héberger localement

Vous pouvez également télécharger le fichier suivant :

- `browserux.css` (version normale commentée).

Puis l'inclure localement dans votre projet :

```html
<link rel="stylesheet" href="/path/to/browserux.css">
```

<br>

### 📦 Utilisation via npm

ous pouvez aussi installer `browserux.css` via npm pour une meilleure intégration avec les workflows modernes (Vite, Webpack, Parcel, etc.) :

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

> Cette méthode garantit que le CSS est intégré au bundle final et bénéficie de votre processus de build (optimisation, minification, etc.).

#### Pourquoi utiliser npm ?

- Gestion plus facile des dépendances du projet.
- Mises à jour automatiques via votre package manager.
- Intégration fluide avec les outils et pipelines de build modernes.

<br>

### 📋 Résumé rapide

| Method | File | Use case |
|:--|:--|:--|
| CDN | `browserux.css` | Development, apprentissage |
| Local | `/assets/css/browserux.css` | Développement personnalisé, modifications |
| npm install | `browserux.css` via node_modules | Intégration avec un bundler |

---

<br>

## 📄 III. Contenu du fichier

### 🔣 1. Variables CSS

La section "Variables CSS" de browserux.css centralise toutes les valeurs fondamentales utilisées dans la feuille de style.
Cela permet de créer un système de design cohérent, facilement personnalisable (thèmes clair/sombre, accessibilité, ergonomie…).

Les variables sont déclarées dans `:root`, ce qui garantit leur portée globale. Elles ont pour objectifs de :

- Centraliser la configuration des styles
- Simplifier la personnalisation (couleurs, typographie, espacements)
- Préparer les thèmes (ex. prefers-color-scheme)
- Favoriser la maintenabilité et la cohérence visuelle

<br>

#### 🎨 Couleurs globales

Variables servant de base au thème général : couleurs de fond, de texte, et couleurs principales (primaires/secondaires).

| Variable               | Rôle                                     | Valeur par défaut |
|------------------------|------------------------------------------|-------------------|
| `--bux-page-bg`         | Couleur de fond principale               | `#eaeaea`         |
| `--bux-page-color`      | Couleur du texte principal               | `#121212`         |
| `--bux-color-primary`   | Couleur primaire (accent/CTA)            | `#f05e0e`         |
| `--bux-color-secondary` | Couleur secondaire (lien, composant)     | `#0e93f0`         |
| `--bux-transparent`     | Valeur transparente universelle          | `transparent`     |

<br>

#### ✅ Couleurs des éléments de validation de formulaires

Définit les couleurs utilisées pour les champs valides/invalides, ainsi que les placeholders correspondants.

| Variable                            | Utilisation                          | Valeur |
|-------------------------------------|--------------------------------------|--------|
| `--bux-valid-border-color`           | Bordure des champs valides           | `#29b94c` |
| `--bux-valid-bg-color`               | Fond des champs valides              | `#f0fff5` |
| `--bux-invalid-border-color`         | Bordure des champs invalides         | `#dc303e` |
| `--bux-invalid-bg-color`             | Fond des champs invalides            | `#fff0f0` |
| `--bux-placeholder-color`            | Couleur par défaut du placeholder    | `#aaa` |
| `--bux-invalid-placeholder-color`    | Couleur du placeholder invalide      | `#dc303e` |

<br>

#### ⏳ Couleurs de la barre de progression

Personnalise les styles de l’élément natif `<progress>` pour l’adapter à l’interface du thème.

| Variable                  | Description                      | Valeur |
|---------------------------|----------------------------------|--------|
| `--bux-progress-bar-bg`    | Fond de la barre `<progress>`    | `#efefef` |
| `--bux-progress-value-bg`  | Valeur remplie dans `<progress>` | `#29b94c` |

<br>

#### 📋 Sélection de texte (`::selection`)

Contrôle l’apparence de la sélection de texte effectuée par l’utilisateur.

| Variable                        | Description                      | Valeur                       |
|---------------------------------|----------------------------------|------------------------------|
| `--bux-selection-bg`             | Couleur de fond sélectionné      | `var(--bux-page-color)`       |
| `--bux-selection-color`          | Couleur du texte sélectionné     | `var(--bux-page-bg)`          |
| `--bux-selection-text-shadow`    | Ombre sur texte sélectionné      | `none`                       |

<br>

#### 🖱️ Scrollbar

Permet de personnaliser les scrollbars pour une meilleure intégration visuelle (supporté par WebKit/Blink).

| Variable                            | Rôle                                 | Valeur par défaut |
|-------------------------------------|--------------------------------------|-------------------|
| `--bux-scrollbar`                    | Couleur de fond globale de la scrollbar | `var(--bux-page-bg)` |
| `--bux-scrollbar-track`              | Couleur du rail                      | `#ddecf6`         |
| `--bux-scrollbar-thumb`              | Couleur du curseur (thumb)           | `var(--bux-color-secondary)` |
| `--bux-scrollbar-thumb-hover`        | Couleur du curseur au survol         | `var(--bux-color-primary)` |
| `--bux-scrollbar-vertical-width`     | Largeur de la scrollbar verticale    | `10px`            |
| `--bux-scrollbar-horizontal-height`  | Hauteur de la scrollbar horizontale  | `10px`            |

<br>

#### 🔤 Typographie

Variables de base utilisées pour configurer la police, la taille de texte et l’interligne global.

| Variable                    | Rôle                                 | Valeur par défaut |
|-----------------------------|--------------------------------------|-------------------|
| `--bux-typo-font-family`     | Police principale du document        | Système + fallback |
| `--bux-typo-font-family-mono`| Police monospace (code, pre…)        | Monospace standard |
| `--bux-typo-font-size`       | Taille de base (`rem`)               | `1.6rem`          |
| `--bux-typo-line-height`     | Interligne                           | `1.6`             |

---

<br>

### 2. ⚙️ Préférences utilisateur du navigateur

Le fichier `browserux.css` prend en compte certaines préférences système de l’utilisateur pour améliorer l’ergonomie et l’accessibilité, le tout sans JavaScript.

<br>

#### 🌙 Préférences du thème (`prefers-color-scheme`)

L’utilisateur peut activer un thème sombre au niveau de son système d’exploitation ou de son navigateur.
Cette section ajuste dynamiquement les variables CSS pour refléter cette préférence.

```css
@media (prefers-color-scheme: dark) {
  :root {
    /* Exemples : */
    --bux-page-bg: #121212;
    --bux-page-color: #eaeaea;
    --bux-color-primary: #f05e0e;
    --bux-color-secondary: #0e93f0;
    /* etc. */
  }
}
```

- Aucun JavaScript requis.
- Le thème suit automatiquement les préférences de l’utilisateur.
- Facile à personnaliser via les variables CSS.

> ♿ Accessibilité et 🧩 Ergonomie
 
<br>

##### Transition fluide

Permet une transition douce lors du basculement entre thème clair et sombre (automatique ou manuel).

```css
body {
  transition: background-color 0.3s, color 0.3s;
}
```
> 🧩 Ergonomie

<br>

#### 🎛️ Préférences des animations (`prefers-reduced-motion`)

Certaines personnes préfèrent réduire les animations pour éviter les distractions ou les effets désagréables liés aux mouvements.

```css
@media (prefers-reduced-motion: reduce) {
  * {
    animation-duration: 0s !important;
    animation-iteration-count: 1 !important;
    scroll-behavior: auto !important;
    transition-duration: 0s !important;
  }
}
```

Effets appliqués :

| Propriété                 | Effet visé                            |
|---------------------------|----------------------------------------|
| `animation-duration: 0s`  | Supprime les animations                |
| `animation-iteration-count: 1` | Stoppe les boucles infinies    |
| `scroll-behavior: auto`   | Désactive le défilement fluide         |
| `transition-duration: 0s` | Supprime les effets de transition      |

> ♿ Accessibilité
 
<br>

##### Défilement fluide (`scroll-behavior`)

Si l’utilisateur n’a pas désactivé les animations, on active un défilement fluide dans tout le document (liens d’ancrage, navigation...).

```css
@media (prefers-reduced-motion: no-preference) {
  :root {
    scroll-behavior: smooth;
  }
}
```
> 🧩 Ergonomie

<br>

✅ Ces préférences sont nativement gérées par CSS, sans script, et contribuent à une expérience utilisateur fluide, inclusive et moderne.
 
<br>

#### 🌓 Préférences de contraste (prefers-contrast)

L’utilisateur peut spécifier une préférence pour un affichage à contraste renforcé, généralement via son système d’exploitation (Windows, macOS, etc.). Cette section CSS améliore la lisibilité des éléments d’interface trop discrets par défaut.

```css
@media (prefers-contrast: more) {
```
Active ce bloc uniquement si l'utilisateur a explicitement demandé un contraste plus élevé.

```css
::placeholder {
  color: rgba(16, 16, 16, 0.8);
  opacity: 1;
}
```

- `::placeholder` : cible le texte d’espace réservé dans les champs de formulaire (`input`, `textarea`, etc.).
- `color: rgba(16, 16, 16, 0.8);` : applique un gris foncé semi-opaque pour améliorer le contraste tout en gardant un ton visuellement distinct du contenu.
- `opacity: 1;` : certains navigateurs ajoutent une opacité réduite par défaut, cette ligne force une opacité maximale pour assurer une lisibilité constante.

```css
[disabled] {
  color: rgba(16, 16, 16, 0.8);
}
```

- `[disabled]` : cible tous les éléments HTML porteurs de l’attribut `disabled` (inputs, boutons, sélecteurs, etc.).
- `color: rgba(16, 16, 16, 0.8);` : évite que ces éléments paraissent trop estompés ou peu visibles, tout en conservant une apparence désactivée.

```css
::selection {
  text-shadow: none;
}
```

- `::selection` : modifie le rendu du texte sélectionné à la souris ou au clavier.
- `text-shadow: none;` : supprime tout effet de flou ou de halo (souvent utilisé en thème sombre) qui pourrait réduire la lisibilité du texte sélectionné en contraste élevé.

```css
em,
i,
small {
  font-weight: bold;
}
```

- `em`, `i` : ces balises représentent du texte mis en valeur (généralement en italique), mais leur style peut devenir peu lisible en environnement à contraste fort.
- `small` : rend le texte plus petit, donc potentiellement plus difficile à lire.
- `font-weight: bold;` : renforce visuellement ces textes pour améliorer leur accessibilité sans altérer leur signification sémantique.

✅ Résumé des bénéfices :
- Renforce la lisibilité des éléments normalement subtils ou visuellement atténués.
- Aucune dépendance JavaScript : pur CSS.
- Compatible avec tous les navigateurs modernes prenant en charge `prefers-contrast`.
- Se combine élégamment avec `prefers-color-scheme` pour un thème entièrement réactif aux préférences utilisateur.

> ♿ Accessibilité et 🧩 Ergonomie

<br>

---

<br>

### 3. 🧩 Thème de l'interface du navigateur

La section Browser UI Theme de `browserux.css` personnalise plusieurs éléments natifs du navigateur, tels que la sélection de texte, les barres de défilement, les composants de formulaire ou repliables, afin d'améliorer leur cohérence visuelle, leur ergonomie et leur accessibilité.

<br>

#### 🖍️ Sélection de texte (`::selection`)

Personnalise l’apparence du texte sélectionné par l’utilisateur (fond, couleur, ombre).

```css
::selection {
  background: var(--bux-selection-bg);
  color: var(--bux-selection-color);
  text-shadow: var(--bux-selection-text-shadow);
}
```
> 🧩 Ergonomie

<br>

#### 🖱️ Barres de défilement

Personnalise les barres de défilement natives pour offrir un rendu plus cohérent entre navigateurs.
Prend en charge WebKit/Blink (Chrome, Safari, Edge Chromium) et Firefox (Gecko).

##### Support Firefox (Gecko)

```css
@supports (-moz-appearance: none) {
  html {
    scrollbar-color: var(--bux-scrollbar-thumb) var(--bux-scrollbar-track);
    scrollbar-width: auto;
  }
}
```

##### Support WebKit / Blink (Chrome, Safari, Edge Chromium)

```css
::-webkit-scrollbar {
  background: var(--bux-scrollbar);
  height: var(--bux-scrollbar-horizontal-height);
  width: var(--bux-scrollbar-vertical-width);
}

::-webkit-scrollbar-thumb {
  background-color: var(--bux-scrollbar-thumb);
}

::-webkit-scrollbar-thumb:hover {
  background-color: var(--bux-scrollbar-thumb-hover);
}
```

Supprime les boutons et coins inutiles pour une apparence plus épurée.

```css
::-webkit-scrollbar-button {
  display: none;
}

::-webkit-scrollbar-corner {
  background: transparent;
}
```

En harmonisant les barres de défilement avec le thème global, on améliore à la fois la cohérence visuelle et le confort d’utilisation sur tous les navigateurs modernes.

> 🧩 Ergonomie

<br>

#### 📋Composants de formulaire

Cette section améliore l’apparence et la lisibilité des composants de formulaire natifs (checkbox, radio, range, select, progress, etc.) en personnalisant les couleurs d’accentuation, les états de validation, les placeholders et les sliders.
Elle vise une meilleure cohérence visuelle, sans compromettre l’accessibilité.

<br>

##### Couleur du placeholder

Personnalise la couleur du texte d’indice dans les champs vides (`::placeholder`).

```css
::placeholder {
  color: var(--bux-placeholder-color);
}
```
> 🧩 Ergonomie

<br>

##### Couleurs d’accentuation (`accent-color`)

Applique la couleur principale du thème sur les éléments de formulaire compatibles.

```css
input[type="checkbox"],
input[type="radio"],
input[type="range"],
meter,
select {
  accent-color: var(--bux-color-primary);
}

progress {
  accent-color: var(--bux-progress-value-bg);
}
```
> 🧩 Ergonomie

<br>

##### Curseur de type `range` (slider)

Personnalise le bouton de glissement du composant `range` dans WebKit et Firefox.

```css
input[type="range"]::-webkit-slider-thumb,
input[type="range"]::-moz-range-thumb {
  background: var(--bux-color-primary);
  border: none;
}
```
> 🧩 Ergonomie

<br>

##### États de validation des champs

Modifie l’apparence des champs valides ou invalides (bordure, fond, placeholder).

```css
input:valid, 
textarea:valid, 
select:valid {
  background-color: var(--bux-valid-bg-color);
  border-color: var(--bux-valid-border-color); 
}

input:invalid, 
textarea:invalid, 
select:invalid {
  background-color: var(--bux-invalid-bg-color);
  border-color:  var(--bux-invalid-border-color);
}

input:invalid::placeholder, 
textarea:invalid::placeholder {
  color: var(--bux-invalid-placeholder-color);
}
```
> ♿ Accessibilité et 🧩 Ergonomie

<br>

##### Barre de progression (`progress`)

Harmonise l’apparence native des barres de progression dans WebKit et Firefox.

```css
progress::-webkit-progress-bar {
  background-color: var(--bux-progress-bar-bg);
  border-radius: 8px;
}

progress::-webkit-progress-value {
  background-color: var(--bux-progress-value-bg);
  border-radius: 8px;
}

progress::-moz-progress-bar {
  background-color: var(--bux-progress-bar-bg);
}
```
> 🧩 Ergonomie

<br>

#### 🔽 Composants interactifs repliables

Cette section améliore l’apparence des éléments HTML natifs `details` et `summary`, souvent utilisés pour créer des composants repliables (accordéons) accessibles sans JavaScript.
Elle applique la couleur d’accentuation du thème pour rester cohérent visuellement avec les autres champs de formulaire.

##### Accentuation (`accent-color`)

Applique la couleur principale définie dans le thème sur les flèches et marqueurs natifs du navigateur (notamment sur Safari/Chrome).

⚠️ `accent-color` ne fonctionne que sur Safari/macOS et iOS pour personnaliser la flèche du composant `summary`. Les autres navigateurs (Chrome, Edge, Firefox) ignorent cette propriété sur ces éléments. Pour un style cohérent multiplateforme, utilisez `summary::marker` ou une icône personnalisée (`::before`).

```css
details,
summary {
  accent-color: var(--bux-color-primary);
}
```
> 🧩 Ergonomie

<br>

#### 🎯 Accessibilité du focus clavier

Cette section gère l’apparence du contour de focus (`outline`) pour améliorer l’accessibilité au clavier sans gêner les interactions à la souris. Elle s’appuie sur la pseudo-classe `:focus-visible`, qui permet de distinguer les navigations clavier des clics souris ou tactiles.

##### Suppression du focus au clic souris

```css
:focus {
  outline: none;
}
```
> 🧩 Ergonomie

<br>

##### Focus clavier accessible (`:focus-visible`)

Affiche un contour visible uniquement lors de l’usage du clavier, pour faciliter la navigation accessible.

```css
:focus-visible {
  outline: 2px solid var(--bux-color-primary);
  outline-offset: 2px;
}
```
> ♿ Accessibilité

<br>

##### Résultat

- Les utilisateurs au clavier bénéficient d’un repère visuel clair.
- Les utilisateurs à la souris ne voient pas de contour inutile après clic.
- Le style reste cohérent grâce aux variables CSS du thème.

---

<br>

### 4. 🧱 Styles par défaut du navigateur

Cette section constitue le socle ergonomique et typographique de `browserux.css`.  
Elle s’inspire des resets modernes (comme normalize.css) tout en allant plus loin sur l’ergonomie, l’accessibilité et les bonnes pratiques UX.

<br>

#### 🔧 Réinitialisation des espacements

Cette section supprime tous les `margin` et `padding` appliqués par défaut par les navigateurs sur les éléments HTML.
Cela permet de partir d’une base prévisible et cohérente, essentielle à toute feuille de style personnalisée.

```css
*,
*::before,
*::after {
  margin: 0;
  padding: 0;
}
```
> 🔄 Reset

<br>

#### 📦 Modèle de boîte

Par défaut, les navigateurs utilisent `content-box`, ce qui rend la gestion des dimensions imprévisible avec les bordures et le padding.
Cette section applique `border-box` globalement, ce qui rend le calcul des dimensions plus intuitif et cohérent.

##### Héritage du `box-sizing`

Assure que tous les éléments utilisent la valeur définie sur `html`.

```css
*,
::before,
::after {
  box-sizing: inherit;
}
```
> 🔄 Reset

<br>

##### Application globale via l’élément racine `html`

Rend le calcul des largeurs/hauteurs plus prévisible dans l’ensemble du document.

```css
html {
  box-sizing: border-box;
}
```
> ⚙️ Normalisation

<br>

#### 🧱 Élément racine `html`

Cette section configure le comportement global du document HTML à partir de l’élément `html`. Elle agit sur la typographie, la hauteur minimale, le rendu des polices, le scroll, et l’ergonomie mobile pour établir une base stable, cohérente et accessible.

```css
html {
  font-family: var(--bux-typo-font-family);
  font-size: 62.5%;
  min-height: 100%;
  overflow-y: scroll;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  -webkit-tap-highlight-color: transparent;
  tab-size: 4;
  -moz-tab-size: 4;
  text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%
}
```

<br>

##### Base typographique cohérente

Assure une typographie homogène entre navigateurs (plutôt que laisser la police système par défaut, variable d’un OS à l’autre).

```css
font-family: var(--bux-typo-font-family);
```
> ⚙️ Normalisation

<br>

Définit une base 1rem = 10px, pour faciliter les calculs (ex : 1.6rem = 16px). C’est une convention de lisibilité, pas un reset.

```css
font-size: 62.5%;
```
> 🧩 Ergonomie et ♿ Accessibilité

<br>

Rend les indentations (par ex. dans `pre` ou `code`) plus lisibles en fixant la taille des tabulations à 4 espaces.

```css
tab-size: 4;
-moz-tab-size: 4;
```
> ⚙️ Normalisation et 🧩 Ergonomie

<br>

##### Mise en page stable

Assure que l’élément `html` occupe toute la hauteur du viewport, ce qui facilite les layouts flex ou grid 100vh. Ce n’est pas un comportement natif à tous les navigateurs.

```css
min-height: 100%;
```
> 🧩 Ergonomie

<br>

Force l’affichage de la scrollbar même s’il n’y a pas de débordement évite les "sauts" de layout entre pages avec ou sans scroll. Très utile pour la stabilité visuelle.

```css
overflow-y: scroll;
```
> 🧩 Ergonomie

<br>

##### Amélioration du rendu des polices

Harmonise le rendu de la typographie entre macOS (ou WebKit) et les autres plateformes, notamment pour éviter le rendu flou du texte.

```css
-moz-osx-font-smoothing: grayscale;
-webkit-font-smoothing: antialiased;
```
> ⚙️ Normalisation et 🧩 Ergonomie

<br>

##### Optimisation tactile et mobile

Supprime le "flash" gris/bleu qui apparaît au tap sur les liens/interactions sur Android/iOS WebKit. Améliore l’expérience tactile.

```css
-webkit-tap-highlight-color: transparent;
```
> 🧩 Ergonomie

<br>

Empêche Safari iOS de modifier la taille du texte après rotation ou zoom, tout en respectant les préférences de zoom utilisateur. Contrairement à `user-scalable=no`, cette méthode reste accessible.

```css
text-size-adjust: 100%;
-webkit-text-size-adjust: 100%;
```
> ♿ Accessibilité

<br>

#### 📑 Sections

Cette section initialise les styles fondamentaux de la page via l’élément body, considéré comme une racine de sectionnement en HTML.
Elle pose les bases visuelles : fond, couleur du texte, typographie, et garantit une hauteur minimale pleine page, utile pour les layouts.

```css
body {
  background: var(--bux-page-bg);
  color: var(--bux-page-color);
  font-size: var(--bux-typo-font-size);
  line-height: var(--bux-typo-line-height);
  min-height: 100%;
}
```

<br>

##### Initialisation des couleurs

Applique les couleurs principales du thème (claire/sombre), dès le chargement de la page.

```css
background: var(--bux-page-bg);
color: var(--bux-page-color);
```
> 🧩 Ergonomie

<br>

##### Base typographique

Définit la taille de base du texte à l’échelle du body, héritée ensuite par tous les éléments enfants. Fournit une base cohérente dans tous les navigateurs via une variable CSS plutôt que laisser la taille par défaut (souvent incohérente d’un navigateur à l’autre).

```css
font-size: var(--bux-typo-font-size);
```
> ⚙️ Normalisation

<br>

Un bon `line-height` garantit un meilleur confort de lecture, notamment pour les personnes avec troubles cognitifs ou visuels.

```css
line-height: var(--bux-typo-line-height);
```
> ⚙️ Normalisation et ♿ Accessibilité

<br>

##### Mise en page pleine hauteur

Permet aux layouts utilisant `100vh`, `flex`, `grid` ou un footer `sticky` de fonctionner correctement, sans "effet de page vide".

```css
min-height: 100%;
```
> 🧩 Ergonomie

<br>

#### 🗂️ Regroupement de contenu

Cette section concerne les éléments HTML qui servent à structurer du contenu en bloc : listes, blocs de citation, extraits de code, etc.
Elle assure que ces éléments soient visuellement cohérents, accessibles et faciles à styliser.

##### Empêche les débordements horizontaux

Évite que les contenus comme les citations (`blockquote`) ou les blocs de code (`pre`) dépassent de leur conteneur.

```css
blockquote,
pre {
  max-width: 100%;
}
```
> 🧩 Ergonomie

<br>

##### Typographie monospace homogène

Applique une série de polices monospace cohérente pour tous les navigateurs, utile pour les blocs `pre`.

```css
pre {
  font-family: var(--bux-typo-font-family-mono);
}
```
> ⚙️ Normalisation

<br>

##### Suppression du style par défaut des listes

Supprime les puces et numérotations automatiques pour permettre un style totalement personnalisé. C’est un classique du reset CSS !

```css
ol,
ul {
  list-style: none;
}
```
> 🔄 Reset

<br>

#### ✏️ Sémantique au niveau du texte

Cette section s'applique aux éléments HTML inline utilisés pour structurer du texte sémantique : liens, abréviations, emphase, indices, blocs de code, etc.
Elle améliore leur lisibilité, leur accessibilité, leur cohérence typographique et leur comportement tactile.

##### Liens (`a`)

```css
a {
  outline: 0;
  text-decoration: none;
  text-decoration-skip-ink: auto;
  touch-action: manipulation;
}
```

<br>

Supprime le contour de focus (remplacé ailleurs avec `:focus-visible`)

```css
outline: 0;
```
> 🔄 Reset

<br>

Supprime le soulignement par défaut des liens

```css
text-decoration: none;
```
> 🔄 Reset

<br>

Améliore le soulignement pour éviter les collisions avec les lettres

```css
text-decoration-skip-ink: auto;
```
> 🧩 Ergonomie

<br>

Supprime le délai de 300ms sur mobile (tap delay)

```css
touch-action: manipulation;
```
> 🧩 Ergonomie

<br>

##### Abréviations et définitions (`abbr`, `dfn`)

```css
abbr[title],
dfn[title] {
  cursor: help;
  text-decoration: underline dotted;  
}
```

<br>

Change le curseur pour indiquer qu’une info est disponible

```css
cursor: help;
```
> ♿ Accessibilité et 🧩 Ergonomie

<br>

Soulignement adapté pour distinguer les termes techniques

```css
text-decoration: underline dotted;
```
> ⚙️ Normalisation

<br>

##### Texte en gras (`b`, `strong`)

Assure que les balises `b` et `strong` s’affichent avec un poids clairement visible, même si la police ne le gère pas bien nativement. Fournit une apparence cohérente du texte en gras entre navigateurs.

```css
b, 
strong {
  font-weight: bolder;
}
```
> ⚙️ Normalisation

<br>

##### Code et clavier (`code`, `kbd`, `samp`)

Applique une police monospace uniforme pour tous les blocs de code, saisie clavier et exemples de terminal. Permet un rendu lisible et homogène du code, quel que soit le navigateur ou l’OS.

```css
code, 
kbd, 
samp {
  font-family: var(--bux-typo-font-family-mono);
}
```
> ⚙️ Normalisation

<br>

`white-space` permet aux blocs `code` de conserver les sauts de ligne tout en autorisant le retour automatique à la ligne si le texte est trop long. Améliore la lisibilité sur mobile ou petits écrans. `max-width` empêche les débordements.

```css
code {
  max-width: 100%;
  white-space: pre-wrap;
}
```
> 🧩 Ergonomie

<br>

##### Texte réduit (`small`)

Fournit une taille cohérente pour les éléments `small`, souvent trop petits ou incohérents selon les navigateurs.

```css
small {
  font-size: 80%;
}
```
> ⚙️ Normalisation

<br>

##### Indices et exposants (`sub`, `sup`)

Corrige l’alignement vertical et la taille des indices (`sub`) et exposants (`sup`), qui peuvent provoquer des bugs d’interligne. Garantit une apparence propre et lisible, quel que soit le navigateur.

```css
sub, 
sup {
  font-size: 75%;
  line-height: 0;
  position: relative;
  vertical-align: baseline;
}

sub { bottom: -0.25em; }
sup { top: -0.5em; }
```
> ⚙️ Normalisation et ♿ Accessibilité

<br>

#### 🖼️ Contenu embarqué

Cette section s'applique aux éléments multimédias HTML tels que les images (img), SVG, vidéos, ou zones cliquables (area).
Elle améliore leur comportement en matière de réactivité, ergonomie tactile et personnalisation graphique.

##### Ergonomie tactile (`area`)

Supprime le délai de 300ms sur les zones cliquables (`area`) des cartes d’image, pour une meilleure réactivité mobile.

```css
area {
  touch-action: manipulation;
}
```
> 🧩 Ergonomie

<br>

##### Éléments multimédias en ligne (`audio`, `canvas`, `iframe`, `img`, `svg`, `video`)

Évite l’apparition d’un espace indésirable sous les éléments multimédias lorsqu’ils sont affichés dans un flux en ligne (`inline` ou `inline-block`). Ce comportement est dû à l’alignement par défaut sur la ligne de base du texte. En les alignant verticalement au milieu, on prévient ce décalage visuel et on assure une meilleure cohérence de rendu dans des contextes mixtes texte/média.

```css
audio,
canvas,
iframe,
img,
svg,
video {
  vertical-align: middle;
}
```
> ⚙️ Normalisation et 🧩 Ergonomie

<br>

##### Prévention de la sélection d’image

Supprime l’effet de surbrillance (souvent violet/bleu) lors de la sélection de texte ou d’un drag sur l’image. Évite des effets visuels indésirables, notamment en glissant une image par accident.

```css
img::selection {
  background-color: var(--bux-transparent);
}
```
> 🧩 Ergonomie

<br>

##### Images, SVG & vidéos (`img`, `svg`, `video`)

Préserve les proportions naturelles des éléments multimédias et empêche les médias de dépasser la largeur de leur conteneur. Ensemble, ces règles permettent une mise à l’échelle fluide et réactive des images et vidéos. Cela assure une bonne adaptation sur tous types d’écrans.

```css
img, 
svg, 
video {
  height: auto;
  max-width: 100%;
}
```
> ⚙️ Normalisation et 🧩 Ergonomie

<br>

##### Thématisation des SVG (`fill`)

Définit la couleur de remplissage des SVG à partir de `color`, ce qui permet de thématiser les icônes SVG automatiquement. Les SVG héritent automatiquement du thème sans avoir besoin de styles inline spécifiques.

```css
svg {
  fill: currentColor;
}
```
> ⚙️ Normalisation

<br>

#### 📊 Données tabulaires

Cette section améliore la gestion des éléments `table` et `td` en corrigeant les incohérences entre navigateurs et en évitant les débordements sur petits écrans.
Elle garantit une meilleure lisibilité, cohérence visuelle, et adaptabilité mobile.

##### Correction des bugs d’héritage et d’indentation

Corrige un bug de style où les bordures ne reprennent pas la couleur du texte (Chrome/Safari) et supprime le retrait automatique du texte dans certaines versions de WebKit. Ces deux règles corrigent des incohérences natives de style dans certains navigateurs.

```css
table {
  border-color: inherit;
  text-indent: 0;
}
```
> ⚙️ Normalisation

<br>

##### Prévention des débordements

Empêche les tableaux ou cellules de déborder de leur conteneur, notamment sur petits écrans. Améliore la responsivité et empêche les barres de défilement horizontales non désirées.

```css
table, 
td {
  max-width: 100%;
}
```
> 🧩 Ergonomie

<br>

#### 🧾 Formulaires

Cette section vise à normaliser l’apparence des champs de formulaire, améliorer leur ergonomie mobile, et corriger les incohérences natives entre navigateurs.
Elle traite des éléments comme button, input, select, textarea, progress, etc.

##### Réinitialisation des boutons

Supprime le style par défaut appliqué aux boutons (fond, bordure…) et empêche la sélection involontaire de texte lors des doubles clics.

```css
button {
  appearance: none;
  border: none;
  background: none;
  user-select: none;
}
```
> 🔄 Reset et 🧩 Ergonomie

<br>

##### Réactivité mobile

Supprime le délai tactile de ~300ms sur les éléments cliquables (essentiel sur mobile).

```css
button, 
input, 
label, 
select, 
textarea {
  touch-action: manipulation;
}
```
> 🧩 Ergonomie

<br>

##### Héritage des styles de police

Assure une cohérence typographique entre les champs et le reste du site (même police, même taille).

```css
button,
input,
optgroup,
select,
textarea {
  font-family: inherit;
  font-size: 100%;
}
```
> ⚙️ Normalisation

<br>

##### Supprimer les majuscules forcées

Désactive les transformations automatiques (`uppercase`) imposées par certains navigateurs (Edge, Firefox).

```css
button,
select {
  text-transform: none;
}
```
> ⚙️ Normalisation

<br>

##### Curseur pointer pour les éléments cliquables

Affiche un curseur `pointer` pour renforcer l’aspect interactif.

```css
button:not(:disabled),
[type=button]:not(:disabled),
[type=reset]:not(:disabled),
[type=submit]:not(:disabled),
label[for],
select {
  cursor: pointer;
}
```
> 🧩 Ergonomie

<br>

##### Compatibilité iOS / Safari

Force le rendu des boutons à leur apparence native dans Safari, tout en gardant le contrôle CSS.

```css
button,
[type="button"],
[type="reset"],
[type="submit"] {
  appearance: button;
  -webkit-appearance: button;
}
```
> ⚙️ Normalisation

<br>

##### Gestion des débordements

Empêche input et textarea de dépasser la largeur de leur conteneur.

```css
input, 
textarea {
  max-width: 100%;
}
```
> 🧩 Ergonomie

<br>

##### Sélection de texte autorisée

Permet à l’utilisateur de sélectionner le texte dans les champs (ce qui est parfois bloqué par défaut).

```css
input, 
select, 
textarea {
  user-select: text;
}
```
> ♿ Accessibilité

<br>

##### Champs de recherche (`type="search"`)

Corrige leur style dans Safari et Chrome, pour éviter l’outline ou décoration supplémentaire.

```css
[type="search"] {
  appearance: textfield;
  -webkit-appearance: textfield;
  outline-offset: -2px;
}

[type="search"]::-webkit-search-decoration {
  -webkit-appearance: none;
}
```
> ⚙️ Normalisation

<br>

##### Alignement du `progress`

Aligne verticalement les barres de progression avec le texte environnant.

```css
progress {
  vertical-align: baseline;
}
```
> ⚙️ Normalisation

<br>

##### Redimensionnement vertical uniquement

Empêche le redimensionnement horizontal des `textarea` pour éviter les débordements et conserver l’ergonomie mobile.

```css
textarea {
  resize: vertical;
}
```
> 🧩 Ergonomie

<br>

##### Bouton d’upload sur iOS/Safari

Rétablit un rendu correct du bouton de fichier (`input[type="file"]`) et hérite de la bonne police.

```css
::-webkit-file-upload-button {
  appearance: button;
  -webkit-appearance: button;
  font: inherit;
}
```
> ⚙️ Normalisation

<br>

##### Spin buttons dans les champs numériques

Corrige leur alignement sur Safari.

```css
::-webkit-inner-spin-button,
::-webkit-outer-spin-button {
  height: auto;
}
```
> ⚙️ Normalisation

<br>

##### Firefox : suppression du style interne au focus

Empêche l’ajout d’une bordure ou padding quand un champ est sélectionné au clavier.

```css
::-moz-focus-inner {
  border-style: none;
  padding: 0;
}
```
> ⚙️ Normalisation

<br>

##### Firefox : suppression des styles de champ invalides

Supprime les bordures ou ombres rouges par défaut sur les champs invalides.

```css
:-moz-ui-invalid {
  box-shadow: none;
}
```
> ♿ Accessibilité

<br>

#### 🔽 Éléments interactifs

Cette section s’assure que certains éléments natifs comme `summary` (dans un `details`) ou des éléments avec role="button" se comportent de manière cohérente, fluide et accessible sur tous les navigateurs et appareils.

##### Rendu cohérent du `summary`

Par défaut, le comportement visuel de `summary` varie selon les navigateurs. En le forçant à s’afficher comme un élément de liste (`list-item`), on améliore sa lisibilité, son accessibilité et sa compatibilité avec les lecteurs d’écran.

```css
summary {
  display: list-item;
}
```
> ⚙️ Normalisation et ♿ Accessibilité

<br>

##### Comportement tactile fluide

Empêche la sélection de texte sur les éléments qui se comportent comme des boutons (comme un `summary` ou un élément avec `role="button"`). Cela évite des effets visuels indésirables lors d’un appui prolongé ou de clics rapides.

```css
[role="button"],
details[open] summary,
summary {
  user-select: none;
}
```
> 🧩 Ergonomie

---

<br>

## 🌎 IV. Support Navigateurs

- 🌈 Chrome (dernières versions)  
- 🦊 Firefox (dernières versions)  
- 🧭 Safari 13+ 
- 📘 Edge Chromium 
- 🤖🌐 Navigateurs Android modernes
- 📱🧭 Safari iOS 13+

> ⚡ Aucun support des anciens navigateurs comme IE11. Une approche d'amélioration progressive garantit une dégradation élégante et fonctionnelle.

---

<br>

## 🤝 V. Contribuer au projet

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

## ⚖️ VI. Licence

**Licence MIT**, Libre d’utilisation, de modification et de distribution.

- [Détails Licence MIT](./LICENCE.md)

---

<br>

#### Fait avec ❤️ par Effeilo
