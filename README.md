# Lumina — SaaS Dashboard UI

A responsive admin dashboard interface built with plain HTML, CSS, and JavaScript — no frameworks, no UI libraries. Built to practice mobile-first responsive design and CSS layout fundamentals before moving into JavaScript and React.

**[Live Demo](#)** · *https://sushildive012.github.io/SAAS-Responsive-Dashboard-UI/*

<br>

<p align="center">
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white" alt="HTML5">
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white" alt="CSS3">
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black" alt="JavaScript">
</p>

---

## Overview

Lumina is a fictional SaaS product's dashboard — the kind of screen a user sees after logging in: usage metrics, recent transactions, and account settings. The goal of this project was to go past "I can follow a CSS tutorial" and into understanding *why* a layout behaves the way it does at different screen sizes, without relying on a CSS framework to make those decisions for me.

## What this project focuses on

- **A single responsive navbar, two behaviors.** One `<nav>` element handles both the mobile slide-in menu and the desktop inline menu — no duplicated markup. A media query switches its `position`, `transform`, and layout direction rather than swapping out separate components.
- **Deliberate z-index layering.** The mobile nav panel, its dimming overlay, and the toggle button are stacked intentionally so each stays interactive and visible in the right order, instead of fighting each other.
- **CSS-only interactivity where possible.** The search bar darkens the rest of the page on focus using a `:has()` selector — no JavaScript needed for that interaction.
- **Fluid sizing with `clamp()`.** Font sizes, the logo, and component widths scale smoothly across breakpoints rather than jumping at fixed widths.
- **Small motion details.** A blinking status indicator (animated `::before` pseudo-element) and a subtle pulse on the subscription metric, used sparingly rather than everywhere.
- **Semantic, accessible markup.** Real `header`, `main`, `section`, `article`, and `footer` elements, labelled form fields, and descriptive `alt` text — not a wall of generic `div`s.

## Tech stack

| | |
|---|---|
| Structure | Semantic HTML5 |
| Styling | CSS3 — Flexbox, Grid, custom properties, media queries, `:has()` |
| Behavior | Vanilla JavaScript — DOM events only, no libraries |

## Project structure

```
lumina-saas-dashboard/
├── index.html
├── style.css          → base layout, components, animations
├── media.css           → desktop breakpoint overrides
├── assets/
│   ├── lumina.svg
│   ├── nav-icon.svg
│   ├── nav-close-icon.svg
│   ├── search-icon.svg
│   └── hero-bg-main.jpg
└── README.md
```

## Running locally

No build step — it's a static site.

```bash
git clone https://github.com/sushildive012/SAAS-Responsive-Dashboard-UI.git
cd SAAS-Responsive-Dashboard-UI
```

Then just open `index.html` in a browser, or use the VS Code "Live Server" extension for auto-reload while editing.

## Notes for next iteration

- Table data is currently static — once I cover JavaScript fetch/array methods, this becomes a good candidate to render from a JSON array instead of hardcoded rows.
- Would rebuild this as a React component breakdown later, once I'm past vanilla JS fundamentals.

---

*Built by Sushil Dive — BSc Computer Science, Nashik. One step in a structured, self-taught path toward becoming a MERN + AI developer.*
