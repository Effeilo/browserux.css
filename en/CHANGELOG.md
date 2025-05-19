**EN** | [FR](../fr/CHANGELOG.md)

<div>
  <img src="https://browserux.com/assets/images/browser-ui-logo-150x150.png" alt="logo Browser UX"/>
</div>

# 📦 Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/)  
and this project adheres to [Semantic Versioning (SemVer)](https://semver.org/).

---

<br>

## [1.2.0] – 2025-05-19

### ✨ Added

- Support for user contrast preferences (`prefers-contrast`)
  Introduced a @media (`prefers-contrast: more`) query to enhance visual accessibility in high contrast environments. This rule improves the visibility of elements that are typically rendered with reduced emphasis by default:
  - Improved contrast for placeholder text (`::placeholder`) and disabled form elements (`[disabled]`)
  - Removal of visual artifacts on text selection
  - Enhanced readability for italic and small-sized text
  
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

- Inline media alignment
  Added vertical alignment rule for media elements (`audio`, `canvas`, `iframe`, `img`, `svg`, `video`) to remove the default baseline gap when displayed inline:

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

### 🔧 Changed

- Scrollbar styling strategy
  Reworked the scrollbar styling system to better support modern WebKit-based browsers (Chrome > 120, Edge > 120, Safari > 18.1) by scoping the `scrollbar-color` property to Firefox only using a `@supports (-moz-appearance: none)` block. This allows WebKit pseudo-elements (`::-webkit-scrollbar`) to apply properly:
  - `scrollbar-color` is now scoped to Firefox via `@supports`
  - WebKit scrollbar styles (track, thumb, hover, corner) are preserved and fully effective
  - `::-webkit-scrollbar-thumb` now has `border-radius` for smoother appearance

<br>

---

<br>

## [1.1.0] – 2025-05-13

### 🔧 Changed

- Removed the `browserux.min.css` file from the npm package: 
  The project encourages customization through CSS variables, so users are now expected to handle minification during their own build process.
- Updated documentation and README to clarify the intended usage and remove references to the minified file

<br>

---

<br>

## [1.0.2] – 2025-05-12

### ✨ Added / Changed

- Removed hardcoded color values from the dark mode section in favor of CSS variables
- Fixed inconsistent indentation in `browserux.css`
- Corrected inaccurate comments in the CSS file

<br>

---

<br>

## [1.0.1] – 2025-05-05

### ✨ Added

- Initial stable release of **`browserux.css`**:
  - `browserux.css` (readable version)
  - `browserux.min.css` (minified version)

- Full coverage includes:
  - 🔄 Minimal Reset
  - ⚙️ Normalization (typography, native elements, forms…)
  - 🧩 Ergonomics (smooth scroll, tap, visible scrollbars…)
  - ♿ Accessibility (dark mode, focus-visible, accent-color…)

<br>

### 📘 Presentation

- Clear overview of project goals, installation methods, philosophy, and file structure
  - `README.md` (English)
  - `fr/README-FR.md` (French)

<br>

### 📚 Documentation

- Full documentation:
  - `en/DOC.md` (English)
  - `fr/DOC.md` (French)

<br>

---

<br>

## 📊 Version History

- [Compare `1.0.1` ↔ `1.0.2`](https://github.com/Effeilo/browserux.css/compare/1.0.1...HEAD)
- [View `1.0.1`](https://github.com/Effeilo/browserux.css/releases/tag/1.0.1)

<br>

---