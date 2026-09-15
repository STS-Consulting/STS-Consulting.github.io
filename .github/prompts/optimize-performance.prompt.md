---
description: 'Analyze and optimize web assets, images, and layout performance for Lighthouse best practices'
---

# Optimize Performance & Assets

Analyze HTML, CSS, and media assets in this repository to maximize Core Web Vitals and Lighthouse metrics.

## Focus Areas

1. **Cumulative Layout Shift (CLS):** Ensure all `<img>` tags specify explicit `width` and `height` dimensions or aspect ratio CSS.
2. **Media Optimization:** Verify images in `Media/` and `Resources/` are compressed, appropriately scaled, and use modern formats where possible.
3. **Render-Blocking Resources:** Audit `<head>` for stylesheet and script tags, ensuring scripts use `defer` or `type="module"`.
4. **Clean CSS:** Remove unused CSS selectors and minimize excessive specificity.
