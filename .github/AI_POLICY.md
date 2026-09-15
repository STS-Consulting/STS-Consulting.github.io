# Artificial Intelligence (AI) Usage Policy & Disclosure

## 1. Overview & Purpose
This repository recognizes and supports the responsible and ethical use of Artificial Intelligence (AI) assistance tools—such as GitHub Copilot, Google Gemini, Anthropic Claude, OpenAI ChatGPT, and Amazon Q—to aid in code generation, refactoring, documentation, and quality assurance.

Following transparency frameworks and disclosure practices established across the software industry (including guidelines from Microsoft, Google, Amazon, and the open-source community), this document outlines our policy on AI usage, governance, provenance, and human accountability across all contributions.

This policy applies to all markup, scripts, stylesheets, assets, configurations, workflows, tests, and documentation contributed to this repository.

---

## 2. Permitted & Recommended Use Cases
AI assistance tools are encouraged as authoring aids and pair-programming assistants for tasks such as:

- **Web Scaffolding & Boilerplate:** Generating initial HTML page structures, semantic sections, CSS stylesheets, layout grids, and workflow configurations.
- **Refactoring & Optimization:** Identifying opportunities to improve performance, accessibility (a11y), responsive design, readability, and maintainability.
- **Documentation & Technical Writing:** Drafting page annotations, accessibility statements, README files, guides, and change summaries.
- **Quality Assurance & Verification:** Synthesizing link checks, accessibility test cases, boundary conditions, and responsiveness checks.
- **Troubleshooting & Analysis:** Explaining layout quirks, diagnosing CSS cascade issues, resolving cross-browser discrepancies, and identifying edge cases.

---

## 3. Core Principles & Governance

### 3.1 100% Human Oversight & Accountability
AI tools are authoring assistants, not autonomous decision-makers or independent authors.
- **Full Human Accountability:** Human authors and contributors retain 100% accountability for the correctness, safety, performance, and accessibility of all committed content.
- **Comprehension Requirement:** Contributors must thoroughly understand every line of AI-generated or AI-assisted code they submit. Do not commit code or markup you cannot explain or support.
- **No Autonomous Deployments:** AI systems must never autonomously commit code, merge pull requests, execute production deployments, or mutate infrastructure without explicit human review and authorization.

### 3.2 Code Quality & Verification Standards
All contributions involving AI-assisted logic must undergo standard validation prior to committing or merging:
- **Human Code Review:** Every AI suggestion must be read, evaluated, and edited for correctness, semantic integrity, and style.
- **Static Analysis & Linting:** Markup, stylesheets, workflows, and scripts must satisfy repository linting and formatting standards without suppression of valid warnings.
- **Accessibility Verification:** All web contributions must be reviewed against WCAG 2.2 Level AA guidelines for contrast, semantic structure, keyboard navigation, and screen reader compatibility.
- **Security Auditing:** Code must be reviewed for common vulnerabilities, injection risks, insecure CDN references, and unvalidated inputs.

### 3.3 Security, Privacy & Data Protection
- **No Sensitive Data in Prompts:** Contributors must never submit proprietary secrets, credentials, API keys, private tokens, internal infrastructure identifiers, or Personally Identifiable Information (PII) to public, unvetted, or third-party AI models.
- **Package & Dependency Hallucination Defense:** Always verify that any libraries, frameworks, or external resources suggested by AI tools actually exist in official registries before adding them to project manifests or web pages.

### 3.4 Licensing & Intellectual Property Compliance
- **License Alignment:** Generated snippets must comply with this repository's licensing terms (Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International - CC BY-NC-SA 4.0) and must not infringe upon third-party copyrights or patents.
- **Avoid Verbatim Ingestion:** Contributors must avoid prompting AI tools to reproduce copyrighted proprietary or restrictive-licensed third-party code verbatim.
- **Duplication Filters:** Where available (e.g., GitHub Copilot), configure tools to block suggestions matching public code.

---

## 4. Limitations & Risk Awareness
Consumers and contributors must remain mindful of the inherent limitations of generative AI models:

| Characteristic | Risk Factor | Mitigation Strategy |
| :--- | :--- | :--- |
| **Hallucination & Plausibility** | Models can produce markup and styles that look plausible, yet contain subtle accessibility flaws, invalid CSS attributes, or broken links. | Perform rigorous line-by-line human review and automated accessibility/linting checks. |
| **Stale Knowledge & Deprecation** | Models may recommend obsolete HTML tags, deprecated CSS properties, or outdated browser polyfills. | Cross-reference suggestions against current official web specifications (MDN, W3C, WHATWG). |
| **Edge-Case Blindness** | AI generation tends to focus on typical desktop screen views, missing narrow mobile viewports, high-contrast modes, or screen reader behaviors. | Deliberately test with responsive tools, screen readers, and keyboard-only navigation. |
| **Third-Party Trust Model** | AI-generated code should be treated like code from an unvetted third party. | Exercise the same diligence, skepticism, and review rigor as with external, untrusted pull requests. |

---

## 5. Transparency, Provenance & Attribution

Transparency allows maintainers and reviewers to allocate appropriate focus during code reviews and quality audits.

### 5.1 When Disclosure is Required
Explicit disclosure is required when AI tools have:
- Generated a significant or non-trivial portion of a pull request or commit.
- Authored core layout architecture or complex interactive features.
- Converted or refactored large segments of an existing page or stylesheet.

*Note: Routine inline auto-completions for trivial syntax, tag closures, or common CSS property names do not require explicit disclosure.*

### 5.2 Pull Request Disclosure Format
When submitting a Pull Request that includes AI-assisted work, include a brief disclosure in the PR description:

```markdown
### AI Assistance Disclosure
- **Tool(s) & Model(s):** [e.g., GitHub Copilot, Anthropic Claude 3.7 Sonnet, Google Gemini 2.5 Pro, OpenAI ChatGPT]
- **Scope:** [e.g., Scaffolding responsive grid layout, generating accessibility annotations]
- **Human Verification:** [e.g., Manually reviewed, verified keyboard tab order, tested across Chrome/Firefox/Edge]
```

### 5.3 Commit Messages & Metadata (Recommended)
Where practical, commit messages or changelogs may include an attribution tag or note:

```text
feat(layout): add responsive navigation bar

AI-Assisted: GitHub Copilot (Claude 3.7 Sonnet)
Reviewed-by: Contributor Name <contributor@example.com>
```

---

## 6. Contributor Pre-Submission Checklist

Before submitting a Pull Request containing AI-assisted or AI-generated contributions, confirm that you have:

- [ ] **Understood:** Reviewed every line of markup, style, or script and fully understand its behavior.
- [ ] **Cleaned Prompts:** Confirmed that no private keys, passwords, credentials, or proprietary secrets were transmitted to AI tools.
- [ ] **Verified Resources:** Confirmed that all suggested scripts, stylesheets, and CDN assets are genuine and actively maintained.
- [ ] **Tested:** Verified across multiple viewport widths and tested keyboard navigation and contrast.
- [ ] **Linted:** Ran local linters and validators, resolving all warnings or errors.
- [ ] **Disclosed:** Included the AI tool, model, and scope of assistance in the Pull Request description.

---

## 7. Inquiries & Feedback
If you have questions, suggestions, or concerns regarding AI usage or governance within this repository, please open an issue or contact the repository maintainers.
