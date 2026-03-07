# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a **static HTML portfolio website** for Nguyen Tam Thanh, a Senior Software Engineer. It's a single-page application (SPA) with no build process, framework, or backend—just plain HTML, CSS, and vanilla JavaScript.

**Tech Stack:**
- HTML5
- CSS3 (with CSS variables for theming)
- Vanilla JavaScript (no frameworks)
- External libraries: Font Awesome icons, Iconify for tech stack icons
- Deployed via GitHub Pages

## Repository Structure

```
/
├── index.html              # Main page with all sections (hero, skills, education, experience, projects, contact)
├── css/
│   └── style.css           # All styling (responsive design, animations, theme variables)
├── js/
│   └── main.js             # DOM interactions and scroll effects
├── images/                 # Avatar and company logos
├── .gitignore
└── .git
```

## Key Features

The website showcases:
- **Responsive design**: Mobile-first layout with hamburger menu
- **Smooth scroll navigation**: Active link highlighting based on scroll position
- **Scroll animations**: Reveal effects for timeline items, project cards, and skill boxes
- **Dynamic year**: Footer displays current year automatically
- **Fixed header**: Shows shadow on scroll
- **Tech stack display**: Uses Iconify library for 30+ tech icons

## Common Development Commands

Since this is a static website, there are no build or test commands. Development is straightforward:

1. **Local development**: Open `index.html` in a browser or use any local server (e.g., `python -m http.server 8000`)
2. **Deployment**: Push to GitHub—pages are automatically deployed to `thanhdeveloper.github.io`

## Making Changes

### Adding/Editing Portfolio Content
Edit `index.html` directly:
- **Hero section** (#home): Introduction and social links
- **Skills section** (#skills): Tech stacks in "Development" and "Cloud & DevOps" categories
- **Education section** (#education): Education history and certifications
- **Experience section** (#experience): Timeline of work experience with company logos
- **Projects section** (#projects): Project showcases
- **Contact section** (#contact): Contact information

### Styling Changes
All styling is in `css/style.css` with:
- **CSS variables** at the top (`:root`) for colors, spacing, shadows, transitions
- **Mobile-first approach**: Base styles for mobile, media queries for larger screens
- **Key selectors**: `.container`, `.section`, `.nav-*`, `.header`, `.hero-*`, etc.

### JavaScript Interactions
The `js/main.js` file handles:
- **Navigation menu toggle**: Show/hide mobile menu on hamburger click
- **Active link highlighting**: Updates nav link active state during scroll
- **Header shadow**: Adds/removes shadow as user scrolls
- **Scroll reveal animations**: Fades in elements when scrolled into view
- **Smooth scroll**: Smooth navigation to section anchors
- **Dynamic year**: Sets `#current-year` element to current year

## Adding New Icons

The portfolio uses two icon libraries:

1. **Font Awesome** (social links, general icons):
   ```html
   <i class="fas fa-github"></i>
   ```

2. **Iconify** (tech stack icons):
   ```html
   <span class="iconify" data-icon="simple-icons:react" style="color: #61DAFB;"></span>
   ```

To add new tech icons, use Iconify's icon names from Simple Icons (e.g., `simple-icons:nodejs`, `simple-icons:postgresql`).

## Responsive Design

The website is mobile-first with breakpoints for:
- Small phones (320px+)
- Large phones (480px+)
- Tablets (768px+)
- Desktops (1024px+)

The `.container` max-width is `1400px` with `40px` padding on each side.

## Performance Considerations

- Lightweight images stored locally in `/images/` directory
- External scripts (Font Awesome, Iconify) loaded from CDNs
- No database or API calls
- Scroll event listeners throttled by browser (no explicit throttling needed for this simple use case)

## SEO & Meta Tags

Key meta tags in `<head>`:
- `description`: Professional summary
- `keywords`: Skills and technologies
- `author`: Developer name

Update these when refreshing the portfolio content.
