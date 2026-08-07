# Job Application Form — Styled with CSS

A fully styled, mobile-first, responsive multi-page job application form built with semantic HTML and plain CSS. Features custom CSS selectors, pseudo-classes, nth-child/nth-of-type targeting, and a cohesive warm color palette.

**Author:** Jan Dexter Diaz  
**Course:** Fullstack Development — Lab Activity 2 (CSS)

---

## Table of Contents

- [Overview](#overview)
- [Project Structure](#project-structure)
- [CSS Techniques Used](#css-techniques-used)
- [Page Breakdown](#page-breakdown)
- [Design System](#design-system)
- [Responsive Breakpoints](#responsive-breakpoints)
- [How to Use](#how-to-use)
- [License](#license)

---

## Overview

This project builds on Lab Activity 1 (semantic HTML job application form) by adding a complete CSS stylesheet. The design uses a warm cream background (`#FFFCDF`), clean white card-based layouts, and a professional blue accent color — inspired by modern portfolio designs. All styling is done with **plain CSS only** (no frameworks, no Tailwind, no preprocessors).

---

## Project Structure

```
LabActivity2-Diaz-CSS/
├── personal-information.html   (Page 1)
├── position.html               (Page 2)
├── experience.html             (Page 3)
├── education-skills.html       (Page 4)
├── styles.css                  (Shared stylesheet)
└── README.md
```

---

## CSS Techniques Used

### CSS Selectors
- **Class selectors:** `.site-header`, `.progress-nav`, `.form-section`, `.form-group`, `.btn-primary`, `.btn-secondary`, `.btn-success`, `.checkbox-group`, `.radio-group`
- **Element selectors:** `body`, `html`, `h1, h2, h3, h4, h5`
- **Descendant selectors:** `.form-section fieldset legend`, `.progress-nav ol li a`
- **Attribute selectors:** `input[type="text"]`, `input[type="file"]`, `span[aria-label="required"]`
- **Universal selector:** `*, *::before, *::after` for CSS reset

### Pseudo-classes
- `:hover` — buttons, inputs, checkbox/radio rows
- `:active` — button press-down state
- `:focus` / `:focus-visible` — keyboard-accessible focus rings
- `:invalid:not(:placeholder-shown):not(:focus)` — validation error styling
- `:disabled` — disabled button state
- `:not(:last-child)` — progress bar connectors
- `:last-child`, `:first-child` — layout adjustments

### Pseudo-elements
- `::before` — step number counters in the progress nav
- `::after` — connector lines between progress steps
- `::placeholder` — custom placeholder text color

### nth-child / nth-of-type
- `.form-section fieldset > .form-group:nth-of-type(odd)` — alternating row backgrounds for form fields
- `.form-section fieldset > .form-group:nth-of-type(even)` — even row padding
- `fieldset .checkbox-group:nth-child(odd)` — striped checkbox list items
- `fieldset .radio-group:nth-child(odd)` — striped radio list items

### Other Techniques
- CSS Custom Properties (`--primary-color`, `--accent-color`, etc.)
- CSS Counters (`counter-reset`, `counter-increment`)
- Flexbox layout throughout
- `backdrop-filter: blur()` on header/footer
- CSS transitions and transforms for interactive feedback
- Google Fonts import (Poppins + Montserrat)

---

## Page Breakdown

| Page | File | Description |
|------|------|-------------|
| 1 | `personal-information.html` | Contact details, date of birth, citizenship, communication preference |
| 2 | `position.html` | Position title, department, salary, work location, cover letter, availability |
| 3 | `experience.html` | Current/previous positions, experience summary, resume upload |
| 4 | `education-skills.html` | Education, certifications, skills, competencies, languages, agreements |

---

## Design System

| Token | Value | Usage |
|-------|-------|-------|
| Background | `#FFFCDF` | Page background (warm cream) |
| Card BG | `#ffffff` | Form sections |
| Primary | `#0f172a` | Headings, dark elements |
| Accent | `#5883ef` | Buttons, links, focus rings |
| Success | `#22c55e` | Submit button, completed steps |
| Error | `#ef4444` | Required asterisks, validation |
| Text | `#0f172a` | Body text |
| Text Light | `#64748b` | Hints, secondary text |
| Border | `rgba(88, 131, 239, 0.2)` | Cards, fieldsets |
| Font Body | Montserrat | Body text |
| Font Heading | Poppins | Headings, buttons |

---

## Responsive Breakpoints

The stylesheet follows a **mobile-first** approach:

| Breakpoint | Target | Key Changes |
|-----------|--------|-------------|
| Base (< 576px) | Mobile phones | Single-column, stacked nav, stacked buttons, smaller fonts |
| ≥ 576px | Tablets | Horizontal nav with connectors, side-by-side buttons |
| ≥ 768px | Desktop | Larger padding, bigger inputs, increased font sizes |
| ≥ 1024px | Large screens | Extra padding, wider progress connectors |

---

## How to Use

1. Open `personal-information.html` in any web browser.
2. Fill in the required fields and click "Next" to advance.
3. Use the progress navigation links at the top to jump between pages.
4. On the final page, agree to the terms and click "Submit Application."

No build tools, servers, or dependencies required — just open the HTML files directly. The Google Fonts are loaded via CDN (requires internet for custom fonts; falls back to system fonts otherwise).

---

## License

&copy; 2026 Jan Dexter Diaz. All rights reserved.
