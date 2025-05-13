**EN** | [FR](./fr/README.md)

<div>
  <img src="https://browserux.com/assets/images/browser-ui-logo-150x150.png" alt="logo Browser UX"/>
</div>

# `browserux.css`

**`browserux.css`** is a **minimal CSS foundation** focused on **user experience** and **accessibility**.
Designed to **enhance native HTML** and **CSS behaviors**, it provides a **clean**, **modern baseline** that **improves usability across all devices**, before relying on utility classes, heavy frameworks, or JavaScript.

- [Documentation](./en/DOC.md)
- [Changelog](./en/CHANGELOG.md)

<br>

[![npm version](https://img.shields.io/npm/v/browserux.css.svg)](https://www.npmjs.com/package/browserux.css)
[![size](https://img.shields.io/bundlephobia/min/browserux.css)](https://bundlephobia.com/result?p=browserux.css)
[![License: MIT](https://img.shields.io/badge/license-MIT-green.svg)](https://opensource.org/licenses/MIT)

---

<br>

## 📚 Table of Contents

- ❓ [Why `browserux.css`](#-why-browseruxcss)
- 🧠 [Philosophy](#-philosophy)
- 🧬 [File Structure](#-file-structure)
- ✨ [Features](#-features)
- 🚀 [How to Use](#-how-to-use)
- 🌎 [Browser Support](#-browser-support)
- 🤝 [Contributing to the Project](#-contributing-to-the-project)
- 🙏 [Credits](#-credits)
- ⚖️ [License](#%EF%B8%8F-license)

---

<br>

## ❓ Why `browserux.css`

Most front-end projects start with a `reset.css` or `normalize.css`. However, despite their intentions, especially Normalize’s goal to preserve useful browser behaviors, we almost always end up adding our own tweaks: removing margins, setting `box-sizing: border-box`, improving typography, etc.

But the web has evolved. User experience has become a key concern, and modern browsers now offer native CSS capabilities that are often underused: customizable scrollbars, keyboard focus management, support for user preferences like dark mode or reduced motion…

`browserux.css` goes beyond a simple reset. It provides a modern, lightweight foundation designed to improve usability, accessibility, and visual consistency of native browser elements, without JavaScript, without utility classes, and without bloat.

---

<br>

## 🧠 Philosophy

### 📌 Goals

- Provide a complete and lightweight base CSS file, designed from the ground up to enhance user experience and accessibility.
- Offer a modern alternative to traditional base files (reset.css, normalize.css, etc.).

<br>

### 📐 Guiding Principles

- Use only native HTML elements, without relying on utility classes.
- Built around four core pillars:
  - 🔄 Reset.
  - ⚙️ Normalization.
  - 🧩 Usability.
  - ♿ Accessibility.

---

<br>

## 🧬 File Structure

`browserux.css` is organized into four logical sections to ensure clarity, scalability, and maintainability:

### 🔣 1. Variables

Using CSS variables ensures a consistent design system and allows for easy theme customization (light/dark mode, color adjustments, etc.).
All foundational values are defined here:
- 🎨 Global colors
- ✅ Colors for form validation elements
- ⏳ Progress bar colors
- 🖍️ Text selection
- 🖱️ Scrollbar
- 🔤 Typography

### ⚙️ 2. User Preferences

Handles user-specific preferences detected via media queries:
- 🌙 Theme preferences.
- 🎛️ Animation preferences.

### 🧩 3. Browser Interface Theme

Applies visual customization to native browser elements:
- 🖍️ Text selection.
- 🖱️ Scrollbar.
- 📋 Form components.
- 🔽 Collapsible interactive components.
- 🎯 Keyboard focus accessibility.

### 🧱 4. Browser Default Styles

A balanced integration of the four core principles, organized logically:
- 🔧 Spacing reset
- 📦 Box model
- 🧱 HTML root element
- 📑 Sections
- 🗂️ Content grouping
- ✏️ Text-level semantics
- 🖼️ Embedded content
- 📊 Tabular data
- 🧾 Forms
- 🔽 Interactive elements

---

<br>

## ✨ Features

`browserux.css` is a modern, lightweight, and 100% native (pure HTML/CSS) base stylesheet, designed to meet the needs of today’s front-end projects. It covers the essential foundations to ensure consistency, accessibility, and usability, from the very first byte.

### 🔄 Reset

`browserux.css` applies a minimalist reset to remove unwanted default browser styles while preserving useful behaviors.

- Universal spacing reset (margin/padding set to 0).
- Box model reset to `border-box`.
- Removal of list styles and table indentations.
- Neutralization of default button and form field styles.
- Media elements made responsive.
- Cleansing of default focus outlines in Firefox.
- Neutralized browser field validation styles.

### ⚙️ Normalization

Standardizes elements across browsers to ensure consistent behavior.

- Unified base typography (size, font, line height).
- Standardized typographic behaviors (`b`, `small`, `sub`, `sup`).
- Harmonized appearance of form fields.
- Consistent rendering of lists and tables.
- Improved responsiveness of media content.
- Consistent scrollbar behavior.

### 🧩 Usability

Enhances the fluidity of UX interactions and reduces friction across all device types.

- Smooth scrolling (unless disabled by user preferences).
- Optimized tap handling on mobile (`touch-action: manipulation`).
- Prevents media content from overflowing its container.
- Disables unwanted text selection on interactive elements.
- Forces scrollbar visibility to avoid layout shifts.
- Improved cursor styles for interactive elements.

### ♿ Accessibility

Ensures the site remains usable for all users, including those relying on assistive technologies.

- Respects system preferences: dark mode and reduced motion.
- Visible keyboard focus outlines using `:focus-visible`.
- Support for `accent-color` on form fields.
- Help cursor on elements with additional information (`abbr`, `dfn`).
- Neutral validation styles (especially in Firefox).
- Visible and customizable scrollbars, without hiding them using CSS hacks.

---

<br>

## 🚀 How to Use

Whether you're building a static site or a modern front-end project, `browserux.css` integrates easily into any workflow.  
Here are three simple ways to add it to your project:

### 🔗 Use the CDN

You can include the latest version directly via jsDelivr:

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/Effeilo/browserux.css/browserux.css">
```

### 💾 Download and Host Locally

You can also download the following file:

- `browserux.css`.

Then include them locally in your project:

```html
<link rel="stylesheet" href="/path/to/browserux.css">
```

### 📦 Use via npm

You can also install `browserux.css` via npm for better integration with modern workflows (Vite, Webpack, Parcel, etc.):

```bash
npm install browserux.css
```

After installation, you can import the CSS file into your project:

#### Direct link from `node_modules/` (in your HTML)

```html
<link rel="stylesheet" href="./node_modules/browserux.css/browserux.css">
```

#### Import it directly in your JavaScript (Vite, Webpack, Parcel)

If your build tool supports CSS imports (like Vite, Webpack, etc.), you can directly import the CSS file into your JavaScript entry point:

```javascript
import 'browserux.css/browserux.css';
```

---

<br>

## 🌎 Browser Support

- 🌈 Chrome (latest versions)  
- 🦊 Firefox (latest versions)  
- 🧭 Safari 13+  
- 📘 Edge Chromium  
- 🤖🌐 Modern Android browsers  
- 📱🧭 Safari on iOS 13+

> ⚡ No support for legacy browsers like IE11. A progressive enhancement approach ensures graceful and functional degradation.

---

<br>

## 🤝 Contributing to the Project

Contributions are welcome! Whether you want to report a bug, suggest an improvement, add a feature, or fix a typo, feel free to get involved.

### 🛠️ Issues & Feedback

- Open an issue to:
  - Report a bug.
  - Suggest an improvement or new feature.
  - Discuss an idea before submitting a PR.
- Any feedback is appreciated, even non-technical!

<br>

### 🔄 How to Contribute

1. Fork this repository.
2. Create a new branch (`git checkout -b my-suggestion`).
3. Make your changes.
4. Commit your changes (`git commit -m 'Add: my-suggestion'`).
5. Push the branch (`git push origin my-suggestion`).
6. Open a Pull Request.

<br>

### ✅ Best Practices

- Stay true to the project's minimalist, accessible, and native-first approach.
- Comment your code to make reviews easier.
- Focus on clear, targeted, and well-documented changes.
- Test your changes in the latest versions of modern browsers before submitting a PR.

---

<br>

## 🙏 Credits

Inspired by great practices from:

- [Modern Normalize](https://github.com/sindresorhus/modern-normalize)
- [Paul Irish's box-sizing border-box method](https://www.paulirish.com/2012/box-sizing-border-box-ftw/)
- [CSS Tricks Articles](https://css-tricks.com/)
- [WebAIM Accessibility Guidelines](https://webaim.org/)

---

<br>

## ⚖️ License

**MIT License**, Free to use, modify, and distribute.

- [More details](./en/LICENSE.md)

---

<br>

#### Made with ❤️ by Effeilo
