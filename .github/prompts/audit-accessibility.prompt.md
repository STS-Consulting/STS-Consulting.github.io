---
description: 'Audit HTML and CSS assets against WCAG 2.2 Level AA accessibility standards'
---

# Audit Accessibility

Perform a rigorous accessibility audit on the specified HTML page or component in this repository.

## Instructions

1. Check for valid document structure (`lang="en"`, landmark elements, skip-to-content link).
2. Verify heading hierarchy: ensure there is exactly one `<h1>` and no skipped heading levels.
3. Validate keyboard navigation: confirm all interactive elements (`<a>`, `<button>`, `<input>`) are keyboard reachable with visible `:focus-visible` indicators.
4. Evaluate color contrast: ensure foreground text meets 4.5:1 (normal text) and 3:1 (large text / icons) against background colors.
5. Inspect all `<img>` tags: confirm informative images have concise, descriptive `alt` text and decorative images have `alt=""`.
6. Provide specific code snippets for any remediation required.
