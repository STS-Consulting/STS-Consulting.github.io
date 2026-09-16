---
version: '2026.09.11.0846'
---

# GitHub Copilot Repository Instructions

Universal development guidance for **STS-Consulting/STS-Consulting.github.io**. This document sets the repository-wide behavioral, safety, accessibility, and coding standards for all AI-assisted workflows.

---

## 1. Autonomous Agent Directives

- **Autonomous Execution:** Work methodically through plans step-by-step. Validate each increment thoroughly before reporting completion.
- **Concise Communication:** Keep commentary direct and scannable. State what is being done or investigated in clear sentences.
- **Fail-Closed Validation:** Never declare a task complete if syntax errors, markup violations, broken links, or accessibility regressions remain.

---

## 2. Non-Negotiable Web & Accessibility Standards

All markup, styles, and assets in this repository target modern web standards and public GitHub Pages hosting.

### Semantic Markup & Structure
- **HTML5 Semantics:** Always use native semantic elements (`<header>`, `<nav>`, `<main>`, `<article>`, `<section>`, `<aside>`, `<footer>`) instead of generic nested `<div>` tags.
- **Heading Hierarchy:** Maintain a strict logical heading order (`<h1>` through `<h6>`). Never skip heading levels (e.g. do not jump from `<h2>` directly to `<h4>`). Every page must contain exactly one `<h1>`.
- **Landmarks & Page Structure:** Provide clear landmarks for assistive technology navigation. Use `<main id="main-content">` and include a skip-to-content mechanism.

### Accessibility (WCAG 2.2 Level AA)
- **Keyboard Operability:** Every interactive element must be reachable and operable using keyboard only (`Tab`, `Shift+Tab`, `Enter`, `Space`). Never trap focus.
- **Visible Focus Indicator:** Never suppress `:focus` outlines (`outline: none`) without providing an equivalent, highly visible custom focus indicator with at least 3:1 contrast against adjacent colors.
- **Color Contrast:** Text and images of text must maintain a contrast ratio of at least 4.5:1 for normal text and 3:1 for large text (18pt or 14pt bold). Non-text UI components and graphical objects must meet 3:1 contrast against adjacent background colors.
- **Text Alternatives:** All informative images must include concise, descriptive `alt` attributes. Purely decorative images must use empty `alt=""`.

### Responsive & Clean Styling
- **Fluid & Responsive:** Design mobile-first using flexible layouts (CSS Grid, Flexbox, relative units like `rem` and `ch`). Avoid fixed horizontal widths that cause viewport overflow.
- **No Inline Styles:** Maintain clean separation of concerns by keeping styling within stylesheets rather than inline `style="..."` attributes.
- **Vanilla & Maintainable:** Prioritize clean, modern vanilla CSS. Avoid excessive frameworks unless explicitly specified.

---

## 3. Mandatory Completion Gate

Before completing any page creation, edit, or refactor:
1. **Markup Validation:** Verify that all HTML tags are balanced, properly nested, and adhere to valid HTML5 syntax.
2. **Accessibility Audit:** Inspect contrast ratios, keyboard navigation paths, image `alt` attributes, and ARIA roles.
3. **Link & Reference Check:** Ensure all relative paths (images, stylesheets, markdown links) resolve accurately.
4. **No Dangling Artifacts:** Ensure no temporary debug code, placeholder lorem ipsum, or commented-out debris is left behind.

---

## 4. Conventional Commit & GitMoji Specification

Generate commit messages using the GitMoji specification tailored for web development:

```text
<emoji><type>[optional scope]: <description>
```

### Types & Emojis
- ✨ `feat`: New page, UI component, or site capability
- 🐛 `fix`: Bug fix in layout, markup, styling, or scripting
- ♿ `a11y`: Accessibility remediation or WCAG compliance enhancement
- 📚 `docs`: Markdown documentation, README, or technical guides
- 🎨 `style`: CSS formatting, layout alignment, typography styling
- ♻️ `refactor`: Structural markup refactoring without behavior changes
- ⚡ `perf`: Asset optimization, lazy loading, performance improvement
- 🖼️ `media`: Adding or updating images, icons, or visual media
- 🤖 `ci`: GitHub Actions workflows or automation
- 🧹 `chore`: Maintenance, link cleanup, file reorganization
- 🔒 `security`: Security hardening, CSP updates, header policies

### Scopes
`page`, `nav`, `layout`, `css`, `a11y`, `media`, `workflow`, `docs`

### Examples
- ✨ `feat(page): add portfolio showcase section with responsive grid`
- ♿ `a11y(nav): add skip-to-content link and visible focus indicators`
- 🐛 `fix(layout): resolve flex wrap overflow on mobile viewports`
- 📚 `docs(readme): add governance links and accessibility policy`
- 🎨 `style(css): adjust typography scale and color palette contrast`

---

## 5. Domain-Specific Custom Instructions

Contextual instructions are automatically loaded by GitHub Copilot based on active file types:

- **Accessibility & Inclusive UX:** [.github/instructions/a11y.instructions.md](file:///c:/Users/Scott.Surber/Source%20Code/GitHub/STS-Consulting/STS-Consulting.github.io/.github/instructions/a11y.instructions.md) (`**`)
- **Web Development Standards:** [.github/instructions/web-development.instructions.md](file:///c:/Users/Scott.Surber/Source%20Code/GitHub/STS-Consulting/STS-Consulting.github.io/.github/instructions/web-development.instructions.md) (`**/*.html, **/*.css, **/*.js`)
- **Markdown & Technical Docs:** [.github/instructions/markdown.instructions.md](file:///c:/Users/Scott.Surber/Source%20Code/GitHub/STS-Consulting/STS-Consulting.github.io/.github/instructions/markdown.instructions.md) (`**/*.md`)
- **CI/CD Best Practices:** [.github/instructions/github-actions-ci-cd-best-practices.instructions.md](file:///c:/Users/Scott.Surber/Source%20Code/GitHub/STS-Consulting/STS-Consulting.github.io/.github/instructions/github-actions-ci-cd-best-practices.instructions.md) (`.github/workflows/*.yml`)
- **Copilot Prompt Files:** [.github/instructions/prompt.instructions.md](file:///c:/Users/Scott.Surber/Source%20Code/GitHub/STS-Consulting/STS-Consulting.github.io/.github/instructions/prompt.instructions.md) (`**/*.prompt.md`)
- **Instruction Authoring Meta-Guide:** [.github/instructions/instructions.instructions.md](file:///c:/Users/Scott.Surber/Source%20Code/GitHub/STS-Consulting/STS-Consulting.github.io/.github/instructions/instructions.instructions.md) (`**/*.instructions.md`)


### Versioning Specification (Calendar Versioning - CalVer)
- **Strict Requirement:** All releases, module manifests, git tags, changelog entries, and instruction headers strictly adhere to **Calendar Versioning (CalVer)** using YYYY.MM.DD.HHmm (e.g., $exampleVer).
- **Prohibition:** Semantic Versioning (SemVer / MAJOR.MINOR.PATCH) is **strictly prohibited**.

