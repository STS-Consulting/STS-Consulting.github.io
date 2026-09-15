---
description: 'Frontend web development standards, HTML5 semantics, modern CSS architecture, responsive layout, and performance.'
applyTo: '**/*.{html,css,js}'
version: '2609.15.1000'
---

# Web Development Standards

Authoritative engineering and design guidance for all web assets in **STS-Consulting/STS-Consulting.github.io**.

---

## 1. HTML5 Architecture & Semantics

- **Valid & Standards-Compliant:** Every HTML document must begin with `<!DOCTYPE html>` and declare `<html lang="en">` with `<meta charset="UTF-8">` and `<meta name="viewport" content="width=device-width, initial-scale=1">`.
- **Landmark Elements:** Structure pages logically using `<header>`, `<nav>`, `<main id="main-content">`, `<section>`, `<article>`, `<aside>`, and `<footer>`.
- **Heading Order:** Single `<h1>` per page. Sub-headings must progress sequentially (`<h2>` -> `<h3>` -> `<h4>`) without skipping levels.
- **Button vs. Anchor Distinction:** Use `<button>` for actions that trigger script behavior or state changes; use `<a href="...">` exclusively for navigational links.

---

## 2. CSS Architecture & Responsive Design

- **Modern Vanilla CSS:** Leverage CSS Custom Properties (CSS variables) for color tokens, spacing scales, and typography.
- **Responsive Layouts:** Mobile-first responsive design using CSS Grid and Flexbox. Use media queries (`@media (min-width: ...)`) to progressively enhance layouts for wider viewports.
- **Fluid Typography:** Use relative units (`rem`, `ch`, `clamp()`) rather than fixed `px` to respect user font-size preferences and browser zoom settings.
- **Motion & Preferences:** Honor user preferences with `@media (prefers-reduced-motion: reduce)`.

---

## 3. Web Accessibility (WCAG 2.2 Level AA)

- Cross-reference with [.github/instructions/a11y.instructions.md](a11y.instructions.md).
- Ensure color contrast ratios meet or exceed 4.5:1 for normal text and 3:1 for large text / UI elements.
- Never set `outline: none` without providing a high-visibility replacement `:focus-visible` ring.
- Provide descriptive `alt` text for images and proper `aria-*` attributes for custom interactive components.

---

## 4. Performance & Asset Optimization

- Optimize all image formats (use WebP, SVG, or compressed JPEG).
- Include `width` and `height` attributes on `<img>` elements to eliminate Cumulative Layout Shift (CLS).
- Lazy load below-the-fold media with `loading="lazy"`.
