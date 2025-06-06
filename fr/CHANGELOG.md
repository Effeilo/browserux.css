[EN](../en/CHANGELOG.md) | **FR**

<div>
  <img class="has-dark" src="https://browserux.com/assets/img/logo/logo-browserux-css-250.png" alt="logo Browser UX"/>
</div>

# 📦 Changelog

Toutes les modifications notables de ce projet seront documentées dans ce fichier.

Le format est basé sur [Keep a Changelog](https://keepachangelog.com/fr/1.0.0/)  
et ce projet suit les recommandations de versionnage [SemVer](https://semver.org/lang/fr/).

---

<br>

## [2.0.0] – 06-06-2025

### 💥 Rupture

#### Changement de préfixe des variables CSS :

Afin d'améliorer la scalabilité du projet et d'éviter les collisions de noms avec d'autres bibliothèques ou systèmes de design, toutes les variables CSS précédemment préfixées par `--ui-` ont été renommées en `--bux-`.

Ce changement clarifie la portée du design system BrowserUX (Bux) et prépare le terrain pour une meilleure intégration dans des projets multi-sources.

Exemple :

```diff
- --ui-color-primary
+ --bux-color-primary
```

####  Action requise pour les utilisateurs :

- Si vous surchargez des variables CSS dans vos propres feuilles de style, renommez-les avec le préfixe `--bux-`
- Si vous utilisez un thème ou un système de tokens personnalisé basé sur `--ui-`, pensez à le migrer vers `--bux-`

**Astuce** : Vous pouvez temporairement ajouter des alias manuels pour garantir une compatibilité douce :

```css
:root {
  --ui-color-primary: var(--bux-color-primary);
  --ui-spacing-small: var(--bux-spacing-small);
}
```

<br>

---

<br>

## [1.2.0] – 19-05-2025

### ✨ Ajout

- Prise en charge du contraste élevé utilisateur (`prefers-contrast`)
  Mise en place d’une requête média @media (`prefers-contrast: more`) pour améliorer l’accessibilité visuelle dans les environnements à contraste renforcé. Cette règle augmente la lisibilité des éléments généralement atténués par défaut :
  - Amélioration du contraste des textes d’espace réservé (`::placeholder`) et des éléments désactivés (`[disabled]`)
  - Suppression des effets visuels parasites sur les sélections de texte
  - Accentuation du texte en italique ou de petite taille pour une meilleure lisibilité
  
```css
@media (prefers-contrast: more) {
  ::placeholder {
    color: rgba(16, 16, 16, 0.8);
    opacity: 1;
  }

  [disabled] {
    color: rgba(16, 16, 16, 0.8);
  }

  ::selection {
    text-shadow: none;
  }

  em,
  i,
  small {
    font-weight: bold;
  }
}
```

- Alignement vertical des médias en ligne
  Ajout d'une règle d’alignement vertical pour les éléments multimédias (`audio`, `canvas`, `iframe`, `img`, `svg`, `video`) afin de supprimer l’espace par défaut causé par l’alignement sur la ligne de base lorsque ces éléments sont utilisés en ligne :
  
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

### 🔧 Modification

- Stratégie de personnalisation des barres de défilement
  Refonte de la gestion des styles de scrollbar pour une meilleure compatibilité avec les navigateurs WebKit modernes (Chrome ≥ 120, Edge ≥ 120, Safari ≥ 18.1), en isolant la propriété `scrollbar-color` uniquement pour Firefox via `@supports (-moz-appearance: none)`. Cela permet aux pseudo-éléments WebKit (`::-webkit-scrollbar`) d’être pleinement appliqués :
  - `scrollbar-color` est désormais limité à Firefox via via `@supports`
  - Les styles WebKit (piste, poignée, survol, coin) restent actifs
  - Ajout d’un `border-radius` sur `::-webkit-scrollbar-thumb` pour un rendu plus doux

<br>

---

<br>

## [1.1.0] – 13-05-2025

### 🔧 Modification

- Suppression du fichier `browserux.min.css` du package npm :   
  Le projet étant conçu pour être personnalisé via les variables CSS, les utilisateurs doivent désormais effectuer eux-mêmes la minification lors de leur processus de build.
- Mise à jour de la documentation et du README pour clarifier l’usage recommandé et retirer les références à la version minifiée

<br>

---

<br>

## [1.0.2] – 12-05-2025

### ✨ Ajout / Modification

- Suppression des couleurs codées en dur dans la section dark mode au profit de variables CSS
- Correction des indentations incohérentes dans `browserux.css`
- Correction de commentaires erronés dans le fichier CSS

<br>

---

<br>

## [1.0.1] – 05-05-2025

### ✨ Ajout

- Première version stable de **`browserux.css`** :
  - `browserux.css` (version complète avec commentaires)
  - `browserux.min.css` (version minifiée pour la production)

- Fonctionnalités de base :
  - 🔄 Reset minimaliste
  - ⚙️ Normalisation (typographie, éléments natifs, formulaires…)
  - 🧩 Ergonomie (scroll fluide, tap, scrollbar visible…)
  - ♿ Accessibilité (dark mode, focus visible, accent-color…)

<br>

### 📘 Presentation

- Présentation claire des objectifs, de l’installation, de la philosophie et de la structure des fichiers : 
  - `README.md` (anglais)
  - `fr/README.md` (français)

<br>

### 📚 Documentation

- Documentation complète :
  - `en/DOC.md` (anglais)
  - `fr/DOC.md` (français)

<br>

---

<br>

## 📊 Historique des versions

- [browseruxcss v`2.0.0`](https://github.com/Effeilo/browserux.css/tree/v2.0.0)
- [browseruxcss v`1.2.0`](https://github.com/Effeilo/browserux.css/tree/v1.2.0)
- [browseruxcss v`1.1.0`](https://github.com/Effeilo/browserux.css/tree/v1.1.0)
- [browseruxcss v`1.0.2`](https://github.com/Effeilo/browserux.css/tree/v1.0.2)
- [browseruxcss v`1.0.1`](https://github.com/Effeilo/browserux.css/tree/v1.0.1)

<br>

---