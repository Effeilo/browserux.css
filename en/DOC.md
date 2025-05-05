**EN** | [FR](../fr/DOC.md)

<div>
  <img src="https://browserux.com/assets/images/browser-ui-logo-150x150.png" alt="logo Browser UX"/>
</div>

# 📘 Documentation — `browserux.css`

Welcome to the `browserux.css` documentation.

## 📚 Table of Contents

- 🧠 [I. Philosophy](#-i-philosophy)
  - 📌 [Goals](#-goals)
  - 📐 [Guiding Principles](#-guiding-principles)
- 🚀 [II. How to Use](#-ii-how-to-use)
  - 🔗 [Use the CDN](#-use-the-cdn)
  - 💾 [Download and Host Locally](#-download-and-host-locally)
  - 📦 [Use via npm](#-use-via-npm)
  - 📋 [Quick Summary](#-quick-summary)
  - 💡 [Notes](#-notes)
- 📄 [III. File Content](#-iii-file-content)
  - 🔣 [1. CSS Variables](#-1-css-variables)
    - 🎨 [Global Colors](#-global-colors)
    - ✅ [Form Validation Colors](#-form-validation-colors)
    - ⏳ [Progress Bar Colors](#-progress-bar-colors)
    - 🖍️ [Text Selection](#-text-selection-selection)
    - 🖱️ [Scrollbar](#%EF%B8%8F-scrollbar)
    - 🔤 [Typography](#-typography)
  - ⚙️ [2. Browser User Preferences](#2-%EF%B8%8F-browser-user-preferences)
    - 🌙 [Theme Preferences](#-theme-preferences-prefers-color-scheme)
    - 🎛️ [Animation Preferences](#%EF%B8%8F-animation-preferences-prefers-reduced-motion)
  - 🧩 [3. Browser Interface Theme](#3--browser-interface-theme)
    - 🖍️ [Text Selection](#%EF%B8%8F-text-selection-selection)
    - 🖱️ [Scrollbar](#%EF%B8%8F-scrollbars)
    - 📋 [Form Components](#-form-components)
    - 🔽 [Collapsible Interactive Components](#-collapsible-interactive-components)
    - 🎯 [Keyboard Focus Accessibility](#-keyboard-focus-accessibility)
  - 🧱 [4. Browser Default Styles](#4--default-browser-styles)
    - 🔧 [Spacing Reset](#-spacing-reset)
    - 📦 [Box Model](#-box-model)
    - 🧱 [HTML Root Element](#-html-root-element)
    - 📑 [Sections](#-sections)
    - 🗂️ [Content Grouping](#%EF%B8%8F-content-grouping)
    - ✏️ [Text-Level Semantics](#%EF%B8%8F-text-level-semantics)
    - 🖼️ [Embedded Content](#%EF%B8%8F-embedded-content)
    - 📊 [Tabular Data](#-tabular-data)
    - 🧾 [Forms](#-forms)
    - 🔽 [Interactive Elements](#-interactive-elements)
- 🌎 [IV. Browser Support](#-iv-browser-support)
- 🤝 [V. Contributing to the Project](#-v-contributing-to-the-project)
  - 🛠️ [Issues & Feedback](#%EF%B8%8F-issues--feedback)
  - 🔄 [How to Contribute](#-how-to-contribute)
  - ✅ [Best Practices](#-best-practices)
- ⚖️ [VI. License](#%EF%B8%8F-vi-license)

---

<br>

## 🧠 I. Philosophy

### 📌 Goals

- Provide a complete and lightweight base CSS file, designed from the start to improve user experience and accessibility.
- Offer a modern alternative to traditional base files (reset.css, normalize.css, etc.).

<br>

### 📐 Guiding Principles

- Use only native HTML elements, without relying on utility classes.
- Built around four fundamental pillars:
  - 🔄 Reset
  - ⚙️ Normalization
  - 🧩 Usability
  - ♿ Accessibility

---

<br>

## 🚀 II. How to Use

Whether you're building a static site or a modern front-end project, `browserux.css` integrates easily with any workflow.  
Here are three simple ways to add it to your project:

### 🔗 Use the CDN

You can include the latest version directly via jsDelivr:

#### Full version (with comments)

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/Effeilo/browserux.css/browserux.css">
```

- Full, readable version.  
- Ideal for learning, development, and understanding the structure.

#### Minified version (optimized for production)

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/Effeilo/browserux.css/browserux.min.css">
```

- Smaller file size.  
- Perfect for production websites where performance is key.

<br>

### 💾 Download and Host Locally

You can also download the following two files:

- `browserux.css` (full version with comments)  
- `browserux.min.css` (minified and compressed version)

Then include them locally in your project:

```html
<link rel="stylesheet" href="/path/to/browserux.css">
```

or

```html
<link rel="stylesheet" href="/path/to/browserux.min.css">
```
### 📦 Use via npm

You can also install `browserux.css` via npm for better integration with modern workflows (Vite, Webpack, Parcel, etc.):

```bash
npm install browserux.css
```

Once installed, you can import it into your project:

#### Direct link from `node_modules/` (in your HTML)

```html
<link rel="stylesheet" href="./node_modules/browserux.css/browserux.css">
```

or the minified version:

```html
<link rel="stylesheet" href="./node_modules/browserux.css/browserux.min.css">
```

#### Direct Import in JavaScript (Vite, Webpack, Parcel)

If your build tool supports CSS imports (like Vite, Webpack, etc.), you can directly import the CSS file in your JavaScript entry point:

```javascript
import 'browserux.css/browserux.css';
```

> This method ensures that the CSS is bundled with your final build and benefits from your build process (optimization, minification, etc.).

#### Why use npm?

- Easier project dependency management.  
- Automatic updates via your package manager.  
- Seamless integration with modern build tools and pipelines.

<br>

### 📋 Quick Summary

| Method           | File                            | Use Case                               |
|:----------------|:---------------------------------|:----------------------------------------|
| CDN (normal)     | `browserux.css`                 | Development, learning                   |
| CDN (minified)   | `browserux.min.css`             | Production, optimization                |
| Local (normal)   | `/assets/css/browserux.css`     | Custom development, modifications       |
| Local (minified) | `/assets/css/browserux.min.css` | Production deployment                   |
| npm install (normal) | `browserux.css` via node_modules | Integration with a bundler         |
| npm install (minified) | `browserux.min.css` via node_modules | Optimized production build      |

### 💡 Notes

- **Normal version**: ideal if you want to read, understand, and edit the file with comments.  
- **Minified version**: same functionality, reduced size (no comments), perfect for production environments.

---

<br>

## 📄 III. File Content

### 🔣 1. CSS Variables

The "CSS Variables" section of browserux.css centralizes all core values used throughout the stylesheet.  
This enables the creation of a consistent design system that is easily customizable (light/dark themes, accessibility, usability...).

The variables are declared in `:root`, which ensures global scope. Their purposes include:

- Centralizing style configuration  
- Simplifying customization (colors, typography, spacing)  
- Preparing for themes (e.g., prefers-color-scheme)  
- Supporting maintainability and visual consistency

<br>

#### 🎨 Global Colors

Variables used as the base for the overall theme: background colors, text colors, and primary/secondary accent colors.

| Variable               | Role                                      | Default Value     |
|------------------------|-------------------------------------------|-------------------|
| `--ui-page-bg`         | Main background color                     | `#eaeaea`         |
| `--ui-page-color`      | Main text color                           | `#121212`         |
| `--ui-color-primary`   | Primary color (accent/CTA)                | `#f05e0e`         |
| `--ui-color-secondary` | Secondary color (links, components)       | `#0e93f0`         |
| `--ui-transparent`     | Universal transparent value               | `transparent`     |

<br>

#### ✅ Form Validation Colors

Defines the colors used for valid/invalid form fields, as well as their corresponding placeholders.

| Variable                            | Usage                              | Default Value |
|-------------------------------------|-------------------------------------|----------------|
| `--ui-valid-border-color`           | Border of valid fields              | `#29b94c`      |
| `--ui-valid-bg-color`               | Background of valid fields          | `#f0fff5`      |
| `--ui-invalid-border-color`         | Border of invalid fields            | `#dc303e`      |
| `--ui-invalid-bg-color`             | Background of invalid fields        | `#fff0f0`      |
| `--ui-placeholder-color`            | Default placeholder color           | `#aaa`         |
| `--ui-invalid-placeholder-color`    | Placeholder color for invalid state| `#dc303e`      |

<br>

#### ⏳ Progress Bar Colors

Customizes the native `<progress>` element to match the theme interface.

| Variable                  | Description                          | Default Value |
|---------------------------|--------------------------------------|----------------|
| `--ui-progress-bar-bg`    | Background of the `<progress>` bar   | `#efefef`      |
| `--ui-progress-value-bg`  | Filled portion inside `<progress>`   | `#29b94c`      |

<br>

#### 📋 Text Selection (`::selection`)

Controls the appearance of text selected by the user.

| Variable                        | Description                        | Default Value           |
|---------------------------------|------------------------------------|--------------------------|
| `--ui-selection-bg`             | Background color for selection     | `var(--ui-page-color)`   |
| `--ui-selection-color`          | Text color for selection           | `var(--ui-page-bg)`      |
| `--ui-selection-text-shadow`    | Text shadow on selected text       | `none`                   |

<br>

#### 🖱️ Scrollbar

Enables customization of scrollbars for better visual integration (supported in WebKit/Blink).

| Variable                            | Role                                | Default Value               |
|-------------------------------------|-------------------------------------|------------------------------|
| `--ui-scrollbar`                    | Global scrollbar background color   | `var(--ui-page-bg)`         |
| `--ui-scrollbar-track`              | Track color                         | `#ddecf6`                   |
| `--ui-scrollbar-thumb`              | Thumb color                         | `var(--ui-color-secondary)` |
| `--ui-scrollbar-thumb-hover`        | Thumb hover color                   | `var(--ui-color-primary)`   |
| `--ui-scrollbar-vertical-width`     | Vertical scrollbar width            | `10px`                      |
| `--ui-scrollbar-horizontal-height`  | Horizontal scrollbar height         | `10px`                      |

<br>

#### 🔤 Typography

Base variables used to configure font, text size, and global line height.

| Variable                     | Role                                 | Default Value       |
|------------------------------|--------------------------------------|----------------------|
| `--ui-typo-font-family`      | Main document font                   | System + fallback    |
| `--ui-typo-mono-font-family` | Monospace font (for code, pre, etc.) | Standard monospace   |
| `--ui-typo-font-size`        | Base size (`rem`)                    | `1.6rem`             |
| `--ui-typo-line-height`      | Line height                          | `1.6`                |

---

<br>

### 2. ⚙️ Browser User Preferences

The `browserux.css` file takes into account certain system-level user preferences to improve ergonomics and accessibility — all without JavaScript.

<br>

#### 🌙 Theme Preferences (`prefers-color-scheme`)

Users can enable dark mode at the OS or browser level.  
This section dynamically adjusts CSS variables to reflect that preference.

```css
@media (prefers-color-scheme: dark) {
  :root {
    /* Exemples : */
    --ui-page-bg: #eaeaea;
    --ui-page-color: #121212;
    --ui-color-primary: #f05e0e;
    --ui-color-secondary: #0e93f0;
    /* etc. */
  }
}
```

- No JavaScript required.  
- The theme automatically follows the user’s system preferences.  
- Easy to customize through CSS variables.

> ♿ Accessibility and 🧩 Usability

<br>

##### Smooth Transition

Enables a soft transition when switching between light and dark themes (automatically or manually):

```css
body {
  transition: background-color 0.3s, color 0.3s;
}
```
> 🧩 Usability

<br>

#### 🎛️ Animation Preferences (`prefers-reduced-motion`)

Some users prefer reduced motion to avoid distractions or unpleasant effects caused by animations.

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

Effects applied:

| Property                      | Targeted Effect                       |
|------------------------------|----------------------------------------|
| `animation-duration: 0s`     | Disables animations                   |
| `animation-iteration-count: 1` | Stops infinite loops                |
| `scroll-behavior: auto`      | Disables smooth scrolling            |
| `transition-duration: 0s`    | Disables transition effects          |

> ♿ Accessibility

<br>

##### Smooth Scrolling (`scroll-behavior`)

If the user hasn’t disabled animations, smooth scrolling is enabled across the document (anchor links, navigation, etc.).

```css
@media (prefers-reduced-motion: no-preference) {
  :root {
    scroll-behavior: smooth;
  }
}
```
> 🧩 Usability

<br>

✅ These preferences are natively handled by CSS — no scripts needed — and contribute to a smooth, inclusive, and modern user experience.

---

<br>

### 3. 🧩 Browser Interface Theme

The "Browser UI Theme" section of `browserux.css` customizes several native browser elements — such as text selection, scrollbars, form components, or collapsible elements — to improve visual consistency, usability, and accessibility.

<br>

#### 🖍️ Text Selection (`::selection`)

Customizes the appearance of text selected by the user (background, color, shadow).

```css
::selection {
  background: var(--ui-selection-bg);
  color: var(--ui-selection-color);
  text-shadow: var(--ui-selection-text-shadow);
}
```
> 🧩 Usability

<br>

#### 🖱️ Scrollbars

Customizes native scrollbars to provide a more consistent appearance across browsers.  
Supports WebKit/Blink (Chrome, Safari, Edge Chromium) and Firefox (Gecko).

##### Main Style (WebKit / Blink)

```css
::-webkit-scrollbar {
  background: var(--ui-scrollbar);
  height: var(--ui-scrollbar-horizontal-height);
  width: var(--ui-scrollbar-vertical-width);
}

::-webkit-scrollbar-thumb {
  background-color: var(--ui-scrollbar-thumb);
}

::-webkit-scrollbar-thumb:hover {
  background-color: var(--ui-scrollbar-thumb-hover);
}
```
> Applied in Chrome, Safari, Edge Chromium

##### Firefox Support (Gecko)

```css
html {
  scrollbar-color: var(--ui-scrollbar-thumb) var(--ui-scrollbar-track);
  scrollbar-width: thin;
}
```
> Compatible with Firefox 64+

##### Visual Cleanup (WebKit / Blink)

Removes unnecessary buttons and corners for a cleaner appearance.

```css
::-webkit-scrollbar-button {
  display: none;
}

::-webkit-scrollbar-corner {
  background: transparent;
}
```

By aligning scrollbars with the global theme, visual consistency and user comfort are improved across all modern browsers.

> 🧩 Usability

<br>

#### 📋 Form Components

This section enhances the appearance and readability of native form components (checkbox, radio, range, select, progress, etc.) by customizing accent colors, validation states, placeholders, and sliders.  
It aims for better visual consistency without compromising accessibility.

<br>

##### Placeholder Color

Customizes the color of hint text in empty fields (`::placeholder`).

```css
::placeholder {
  color: var(--ui-placeholder-color);
}
```
> 🧩 Usability

<br>

##### Accent Colors (`accent-color`)

Applies the theme’s primary color to supported form elements.

```css
input[type="checkbox"],
input[type="radio"],
input[type="range"],
meter,
select {
  accent-color: var(--ui-color-primary);
}

progress {
  accent-color: var(--ui-progress-value-bg);
}
```
> 🧩 Usability

<br>

##### `range` Slider

Customizes the thumb (slider handle) of the `range` input component in WebKit and Firefox.

```css
input[type="range"]::-webkit-slider-thumb,
input[type="range"]::-moz-range-thumb {
  background: var(--ui-color-primary);
  border: none;
}
```
> 🧩 Usability

<br>

##### Field Validation States

Modifies the appearance of valid or invalid fields (border, background, placeholder).

```css
input:valid, 
textarea:valid, 
select:valid {
  background-color: var(--ui-valid-bg-color);
  border-color: var(--ui-valid-border-color); 
}

input:invalid, 
textarea:invalid, 
select:invalid {
  background-color: var(--ui-invalid-bg-color);
  border-color:  var(--ui-invalid-border-color);
}

input:invalid::placeholder, 
textarea:invalid::placeholder {
  color: var(--ui-invalid-placeholder-color);
}
```
> ♿ Accessibility and 🧩 Usability

<br>

##### Progress Bar (`progress`)

Unifies the native appearance of progress bars in WebKit and Firefox.

```css
progress::-webkit-progress-bar {
  background-color: var(--ui-progress-bar-bg);
  border-radius: 8px;
}

progress::-webkit-progress-value {
  background-color: var(--ui-progress-value-bg);
  border-radius: 8px;
}

progress::-moz-progress-bar {
  background-color: var(--ui-progress-bar-bg);
}
```
> 🧩 Usability

<br>

#### 🔽 Collapsible Interactive Components

This section improves the appearance of native HTML `details` and `summary` elements, often used to create accessible accordion-like components without JavaScript.  
It applies the theme’s accent color to maintain visual consistency with other form elements.

##### Accent Color (`accent-color`)

Applies the theme’s primary color to native arrows and markers (notably in Safari/Chrome).

⚠️ `accent-color` only works in Safari/macOS and iOS to style the `summary` arrow.  
Other browsers (Chrome, Edge, Firefox) ignore this property on these elements.  
For consistent cross-browser styling, use `summary::marker` or a custom icon via `::before`.

```css
details,
summary {
  accent-color: var(--ui-color-primary);
}
```
> 🧩 Usability

<br>

#### 🎯 Keyboard Focus Accessibility

This section manages the appearance of the `outline` focus ring to improve keyboard accessibility without interfering with mouse interactions.  
It uses the `:focus-visible` pseudo-class, which allows distinguishing keyboard navigation from mouse or touch input.

##### Removing Focus on Mouse Click

```css
:focus {
  outline: none;
}
```
> 🧩 Usability

<br>

##### Accessible Keyboard Focus (`:focus-visible`)

Displays a visible focus ring only during keyboard use, making accessible navigation easier.

```css
:focus-visible {
  outline: 2px solid var(--ui-color-primary);
  outline-offset: 2px;
}
```
> ♿ Accessibility

<br>

##### Result

- Keyboard users get a clear visual indicator.
- Mouse users don’t see unnecessary outlines after clicks.
- The style remains consistent thanks to theme CSS variables.

---

<br>

### 4. 🧱 Default Browser Styles

This section forms the ergonomic and typographic foundation of `browserux.css`.  
It draws inspiration from modern resets (like normalize.css), while going further in terms of usability, accessibility, and UX best practices.

<br>

#### 🔧 Spacing Reset

This section removes all default `margin` and `padding` applied by browsers to HTML elements.  
This creates a clean, predictable base — essential for any custom stylesheet.

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

#### 📦 Box Model

By default, browsers use `content-box`, which can make sizing unpredictable when borders and padding are involved.  
This section applies `border-box` globally, making dimension calculations more intuitive and consistent.

##### Inheriting `box-sizing`

Ensures that all elements inherit the value defined on `html`.

```css
*,
::before,
::after {
  box-sizing: inherit;
}
```
> 🔄 Reset

<br>

##### Global Application via the `html` Root Element

Makes width and height calculations more predictable throughout the entire document.

```css
html {
  box-sizing: border-box;
}
```
> ⚙️ Normalization

<br>

#### 🧱 `html` Root Element

This section sets the global behavior of the HTML document starting from the `html` element.  
It configures typography, minimum height, font rendering, scrolling, and mobile ergonomics to establish a stable, consistent, and accessible foundation.

```css
html {
  font-family: var(--ui-typo-font-family);
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

##### Consistent Typographic Base

Ensures uniform typography across browsers, instead of relying on the system default font which can vary between operating systems.

```css
font-family: var(--ui-typo-font-family);
```
> ⚙️ Normalization

<br>

Defines a base of 1rem = 10px to simplify calculations (e.g., 1.6rem = 16px).  
This is a readability convention, not a reset.

```css
font-size: 62.5%;
```
> 🧩 Usability and ♿ Accessibility

<br>

Improves readability of indentations (e.g., in `pre` or `code`) by setting the tab size to 4 spaces.

```css
tab-size: 4;
-moz-tab-size: 4;
```
> ⚙️ Normalization and 🧩 Usability

<br>

##### Stable Layout

Ensures the `html` element fills the full height of the viewport, making it easier to build 100vh layouts using flex or grid.  
This is not a native behavior in all browsers.

```css
min-height: 100%;
```
> 🧩 Usability

<br>

Forces the scrollbar to be visible even when there's no overflow, preventing layout "jumps" between pages with and without scrollbars.  
Very useful for visual stability.

```css
overflow-y: scroll;
```
> 🧩 Usability

<br>

##### Font Rendering Enhancement

Improves typography rendering consistency between macOS (or WebKit) and other platforms, especially to avoid blurry text.

```css
-moz-osx-font-smoothing: grayscale;
-webkit-font-smoothing: antialiased;
```
> ⚙️ Normalization and 🧩 Usability

<br>

##### Touch and Mobile Optimization

Removes the gray/blue "flash" that appears when tapping links or interactive elements on Android/iOS WebKit. Improves the touch experience.

```css
-webkit-tap-highlight-color: transparent;
```
> 🧩 Usability

<br>

Prevents iOS Safari from resizing text after rotation or zoom, while still respecting user zoom preferences.  
Unlike `user-scalable=no`, this method remains accessible.

```css
text-size-adjust: 100%;
-webkit-text-size-adjust: 100%;
```
> ♿ Accessibility

<br>

#### 📑 Sections

This section initializes the foundational styles of the page through the `body` element, which is considered a sectioning root in HTML.  
It sets up the visual base: background, text color, typography, and ensures a full-page minimum height — useful for layouts.

```css
body {
  background: var(--ui-page-bg);
  color: var(--ui-page-color);
  font-size: var(--ui-typo-font-size);
  line-height: var(--ui-typo-line-height);
  min-height: 100%;
}
```

<br>

##### Color Initialization

Applies the theme’s primary colors (light/dark) as soon as the page loads.

```css
background: var(--ui-page-bg);
color: var(--ui-page-color);
```
> 🧩 Usability

<br>

##### Typographic Base

Defines the base text size at the body level, which is then inherited by all child elements.  
Provides a consistent baseline across browsers using a CSS variable, instead of relying on inconsistent browser defaults.

```css
font-size: var(--ui-typo-font-size);
```
> ⚙️ Normalization

<br>

A good `line-height` ensures better reading comfort, especially for people with cognitive or visual impairments.

```css
line-height: var(--ui-typo-line-height);
```
> ⚙️ Normalization and ♿ Accessibility

<br>

##### Full-Height Layout

Ensures layouts using `100vh`, `flex`, `grid`, or a `sticky` footer work properly without the "blank page effect."

```css
min-height: 100%;
```
> 🧩 Usability

<br>

#### 🗂️ Content Grouping

This section focuses on HTML elements used to structure content in blocks: lists, blockquotes, code snippets, etc.  
It ensures these elements are visually consistent, accessible, and easy to style.

##### Prevents Horizontal Overflow

Prevents content like blockquotes (`blockquote`) or code blocks (`pre`) from overflowing their containers.

```css
blockquote,
pre {
  max-width: 100%;
}
```
> 🧩 Usability

<br>

##### Consistent Monospace Typography

Applies a consistent set of monospace fonts across all browsers, useful for `pre` blocks.

```css
pre {
  font-family: var(--ui-typo-mono-font-family);
}
```
> ⚙️ Normalization

<br>

##### Removes Default List Styles

Removes automatic bullets and numbering to allow for fully customized styling. This is a classic reset CSS technique!

```css
ol,
ul {
  list-style: none;
}
```
> 🔄 Reset

<br>

#### ✏️ Text-Level Semantics

This section applies to inline HTML elements used to structure semantic text: links, abbreviations, emphasis, subscript, code blocks, etc.  
It improves their readability, accessibility, typographic consistency, and touch behavior.

##### Links (`a`)

```css
a {
  outline: 0;
  text-decoration: none;
  text-decoration-skip-ink: auto;
  touch-action: manipulation;
}
```

<br>

Removes the focus outline (replaced elsewhere with `:focus-visible`)

```css
outline: 0;
```
> 🔄 Reset

<br>

Removes the default underline from links

```css
text-decoration: none;
```
> 🔄 Reset

<br>

Improves the underline to prevent collisions with letters

```css
text-decoration-skip-ink: auto;
```
> 🧩 Usability

<br>

Removes the 300ms delay on mobile (tap delay)

```css
touch-action: manipulation;
```
> 🧩 Usability

<br>

##### Abbreviations and Definitions (`abbr`, `dfn`)

```css
abbr[title],
dfn[title] {
  cursor: help;
  text-decoration: underline dotted;  
}
```

<br>

Changes the cursor to indicate that information is available

```css
cursor: help;
```
> ♿ Accessibility and 🧩 Usability

<br>

Adjusted underline to distinguish technical terms

```css
text-decoration: underline dotted;
```
> ⚙️ Normalization

<br>

##### Bold Text (`b`, `strong`)

Ensures that `b` and `strong` tags are displayed with a clearly visible weight, even if the font doesn’t handle it well natively.  
Provides a consistent appearance of bold text across browsers.

```css
b, 
strong {
  font-weight: bolder;
}
```
> ⚙️ Normalization

<br>

##### Code and Keyboard (`code`, `kbd`, `samp`)

Applies a consistent monospace font for all code blocks, keyboard input, and terminal examples.  
Ensures a readable and uniform display of code, regardless of browser or OS.

```css
code, 
kbd, 
samp {
  font-family: var(--ui-typo-mono-font-family);
}
```
> ⚙️ Normalization

<br>

`white-space` allows `code` blocks to preserve line breaks while enabling automatic line wrapping if the text is too long.  
Improves readability on mobile or small screens. `max-width` prevents overflow.

```css
code {
  max-width: 100%;
  white-space: pre-wrap;
}
```
> 🧩 Usability

<br>

##### Small Text (`small`)

Provides a consistent size for `small` elements, which are often too small or inconsistent across browsers.

```css
small {
  font-size: 80%;
}
```
> ⚙️ Normalization

<br>

##### Subscripts and Superscripts (`sub`, `sup`)

Fixes the vertical alignment and size of subscripts (`sub`) and superscripts (`sup`), which can cause line-height issues.  
Ensures a clean and readable appearance across all browsers.

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
> ⚙️ Normalization and ♿ Accessibility

<br>

#### 🖼️ Embedded Content

This section applies to HTML multimedia elements such as images (`img`), SVGs, videos, or clickable areas (`area`).  
It improves their responsiveness, touch usability, and graphical customization.

##### Touch Usability (`area`)

Removes the 300ms delay on clickable areas (`area`) in image maps for better mobile responsiveness.

```css
area {
  touch-action: manipulation;
}
```
> 🧩 Usability

<br>

##### Images, SVGs & Videos (`img`, `svg`, `video`)

Preserves the natural proportions of multimedia elements and prevents media from overflowing their container width.  
Together, these rules enable smooth and responsive scaling of images and videos, ensuring good adaptation on all types of screens.

```css
img, 
svg, 
video {
  height: auto;
  max-width: 100%;
}
```
> ⚙️ Normalization and 🧩 Usability

<br>

##### Preventing Image Selection

Removes the highlight effect (often purple/blue) when selecting text or dragging over an image.  
Prevents unwanted visual effects, especially when accidentally dragging an image.

```css
img::selection {
  background-color: var(--ui-transparent);
}
```
> 🧩 Usability

<br>

##### SVG Theming (`fill`)

Sets the fill color of SVGs from `color`, allowing SVG icons to be thematically styled automatically. SVGs automatically inherit the theme without needing specific inline styles.

```css
svg {
  fill: currentColor;
}
```
> ⚙️ Normalization

<br>

#### 📊 Tabular Data

This section improves the handling of `table` and `td` elements by fixing inconsistencies across browsers and preventing overflow on small screens.  
It ensures better readability, visual consistency, and mobile adaptability.

##### Fixing Inheritance and Indentation Bugs

Fixes a style bug where borders do not match the text color (Chrome/Safari) and removes the automatic text indentation in some versions of WebKit. These two rules correct native style inconsistencies in certain browsers.

```css
table {
  border-color: inherit;
  text-indent: 0;
}
```
> ⚙️ Normalization

<br>

##### Preventing Overflow

Prevents tables or cells from overflowing their container, especially on small screens. Improves responsiveness and prevents unwanted horizontal scrollbars.

```css
table, 
td {
  max-width: 100%;
}
```
> 🧩 Usability

<br>

#### 🧾 Forms

This section aims to standardize the appearance of form fields, improve mobile usability, and fix native inconsistencies across browsers.  
It deals with elements such as button, input, select, textarea, progress, etc.

##### Resetting Buttons

Removes the default style applied to buttons (background, border, etc.) and prevents accidental text selection during double-clicks.

```css
button {
  appearance: none;
  border: none;
  background: none;
  user-select: none;
}
```
> 🔄 Reset and 🧩 Usability

<br>

##### Mobile Responsiveness

Removes the touch delay of ~300ms on clickable elements (essential on mobile).

```css
button, 
input, 
label, 
select, 
textarea {
  touch-action: manipulation;
}
```
> 🧩 Usability

<br>

##### Inheriting Font Styles

Ensures typographic consistency between form fields and the rest of the site (same font, same size).

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
> ⚙️ Normalization

<br>

##### Remove Forced Uppercase

Disables automatic `uppercase` transformations imposed by certain browsers (Edge, Firefox).

```css
button,
select {
  text-transform: none;
}
```
> ⚙️ Normalization

<br>

##### Pointer Cursor for Clickable Elements

Displays a `pointer` cursor to reinforce the interactive nature of clickable elements.

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
> 🧩 Usability

<br>

##### iOS / Safari Compatibility

Forces buttons to render with their native appearance in Safari, while still maintaining CSS control.

```css
button,
[type="button"],
[type="reset"],
[type="submit"] {
  appearance: button;
  -webkit-appearance: button;
}
```
> ⚙️ Normalization

<br>

##### Handling Overflow

Prevents `input` and `textarea` elements from overflowing their container width.

```css
input, 
textarea {
  max-width: 100%;
}
```
> 🧩 Usability

<br>

##### Allow Text Selection

Allows the user to select text in fields (which is sometimes blocked by default).

```css
input, 
select, 
textarea {
  user-select: text;
}
```
> ♿ Accessibility

<br>

##### Search Fields (`type="search"`)

Fixes their style in Safari and Chrome to prevent extra outlines or decorations.

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
> ⚙️ Normalization

<br>

##### Aligning `progress`

Vertically aligns progress bars with the surrounding text.

```css
progress {
  vertical-align: baseline;
}
```
> ⚙️ Normalization

<br>

##### Vertical Resizing Only

Prevents horizontal resizing of `textarea` elements to avoid overflow and maintain mobile usability.

```css
textarea {
  resize: vertical;
}
```
> 🧩 Usability

<br>

##### Upload Button on iOS/Safari

Restores proper rendering of the file button (`input[type="file"]`) and inherits the correct font.

```css
::-webkit-file-upload-button {
  appearance: button;
  -webkit-appearance: button;
  font: inherit;
}
```
> ⚙️ Normalization

<br>

##### Spin Buttons in Numeric Fields

Fixes their alignment in Safari.

```css
::-webkit-inner-spin-button,
::-webkit-outer-spin-button {
  height: auto;
}
```
> ⚙️ Normalization

<br>

##### Firefox: Remove Internal Focus Style

Prevents the addition of a border or padding when a field is selected via keyboard.

```css
::-moz-focus-inner {
  border-style: none;
  padding: 0;
}
```
> ⚙️ Normalization

<br>

##### Firefox: Remove Invalid Field Styles

Removes the default red borders or shadows on invalid fields.

```css
:-moz-ui-invalid {
  box-shadow: none;
}
```
> ♿ Accessibility

<br>

#### 🔽 Interactive Elements

This section ensures that certain native elements like `summary` (within a `details`) or elements with `role="button"` behave consistently, smoothly, and accessibly across all browsers and devices.

##### Consistent Rendering of `summary`

By default, the visual behavior of `summary` varies across browsers. By forcing it to display as a list item (`list-item`), we improve its readability, accessibility, and compatibility with screen readers.

```css
summary {
  display: list-item;
}
```
> ⚙️ Normalization and ♿ Accessibility

<br>

##### Smooth Touch Behavior

Prevents text selection on elements that behave like buttons (such as a `summary` or an element with `role="button"`).  
This avoids unwanted visual effects during long presses or rapid clicks.

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

## 🌎 IV. Browser Support

- 🌈 Chrome (latest versions)  
- 🦊 Firefox (latest versions)  
- 🧭 Safari 13+  
- 📘 Edge Chromium  
- 🤖🌐 Modern Android browsers  
- 📱🧭 Safari on iOS 13+

> ⚡ No support for legacy browsers like IE11. A progressive enhancement approach ensures graceful and functional degradation.

---

<br>

## 🤝 V. Contributing to the Project

Contributions are welcome! Whether you'd like to report a bug, suggest an improvement, add a new feature, or fix a typo — feel free to get involved.

### 🛠️ Issues & Feedback

- Open an issue to:
  - Report a bug.
  - Suggest an improvement or new feature.
  - Discuss an idea before submitting a PR.
- All feedback is appreciated, even non-technical!

<br>

### 🔄 How to Contribute

1. Fork this repository.
2. Create a branch (`git checkout -b my-suggestion`).
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

## ⚖️ VI. License

**MIT License** — Free to use, modify, and distribute.

[Détails Licence MIT](./LICENCE.md)

---

<br>

#### Made with ❤️ by Effeilo
