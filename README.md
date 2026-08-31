# Оно тебе надо

> Responsive editorial landing page built from a visual specification with semantic HTML and modern CSS.

**Live demo:** https://nestlir.github.io/ono-tebe-nado/

## Overview

«Оно тебе надо» is an auction-themed editorial landing page focused on typography, composition and image-driven storytelling.

The project was originally created during Yandex Practicum frontend training. In 2026 it was revisited as a deliberate modernization exercise: the original visual concept was preserved while the codebase gained a cleaner responsive foundation, accessibility improvements, automated quality checks and CI/CD deployment.

## What the project demonstrates

- semantic HTML5 structure;
- meaningful document hierarchy;
- CSS Grid and Flexbox layouts;
- reusable visual primitives;
- responsive behavior for desktop, tablet and mobile screens;
- typography and spacing as part of a visual system;
- local font loading with `font-display: swap`;
- keyboard-visible focus states;
- reduced-motion support.

## Architecture

This is intentionally a **static HTML/CSS project**.

A framework was not introduced because the page does not have application state, reusable interactive components or runtime data. Keeping the implementation framework-free makes the architecture proportional to the problem while preserving readability.

```text
ono-tebe-nado/
├── .github/workflows/     # CI and GitHub Pages deployment
├── fonts/                 # Local web fonts
├── images/                # Visual assets
├── styles/                # Global and page styles
├── index.html             # Semantic document structure
└── package.json           # Quality tooling
```

## Quality tooling

The repository includes:

- **Prettier** for consistent formatting;
- **Stylelint** for CSS quality checks;
- **EditorConfig** for editor-independent conventions;
- **GitHub Actions** for automated CSS quality checks;
- **GitHub Pages** for deployment.

Run all checks:

```bash
npm install
npm run check
```

Format the project:

```bash
npm run format
```

## Local development

Clone the repository:

```bash
git clone https://github.com/nestlir/ono-tebe-nado.git
cd ono-tebe-nado
```

Install development tooling:

```bash
npm install
```

Then open `index.html` with a static server or your preferred development server.

## Accessibility

The modernization pass adds several baseline accessibility practices:

- semantic landmarks and heading hierarchy;
- descriptive alternative text for meaningful images;
- visible keyboard focus;
- motion reduction support;
- responsive layouts without a desktop-only minimum viewport.

## CI/CD

Every push and pull request runs automated CSS quality checks. Prettier is included for consistent local formatting.

Pushes to `main` trigger the GitHub Pages deployment workflow.

## Project evolution

**Version 1** — created as a Yandex Practicum training project.

**Version 2** — professional modernization focused on maintainability, responsive behavior, accessibility, automated quality gates and deployment.

The goal of the second iteration was not to hide the project's educational origin, but to make the engineering growth visible inside the repository itself.