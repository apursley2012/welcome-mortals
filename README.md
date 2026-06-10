<!--
File: README.md
Document Title: Welcome, Mortals — Static Portfolio Theme
Author: Alysha Pursley
Date: June 6, 2026
-->

<div align="center">

# Welcome, Mortals — Static Portfolio Theme

**A theatrical haunted-house portfolio with orange highlights, eerie copy, custom cursors, and surprise spider energy.**

![Welcome, Mortals theme preview](images/screenshots/welcome-mortals-screenshot-01.png)

</div>

---

## Table of Contents

- [Theme Overview](#theme-overview)
  - [Purpose](#purpose)
  - [Intended Users](#intended-users)
  - [Design Style and Inspiration](#design-style-and-inspiration)
  - [Main Color Palette](#main-color-palette)
  - [Preview Screenshot](#preview-screenshot)
- [Pages Included](#pages-included)
- [Component Architecture](#component-architecture)
  - [Separated Static Components](#separated-static-components)
  - [Shared JavaScript Modules](#shared-javascript-modules)
- [File and Folder Structure](#file-and-folder-structure)
- [Static Conversion Notes](#static-conversion-notes)
- [Customization Guide](#customization-guide)
  - [Personal Information and Branding](#personal-information-and-branding)
  - [Biography and Life Story](#biography-and-life-story)
  - [Projects, Skills, Services, and Experience](#projects-skills-services-and-experience)
  - [Contact Information and Social Links](#contact-information-and-social-links)
  - [Images and Screenshots](#images-and-screenshots)
  - [Colors, Fonts, and Styling](#colors-fonts-and-styling)
- [GitHub Pages Deployment](#github-pages-deployment)
- [Accessibility and Browser Compatibility](#accessibility-and-browser-compatibility)
- [Repository Relationship](#repository-relationship)
- [Possible Future Enhancements](#possible-future-enhancements)
- [Copyright](#copyright)

---

## Theme Overview

### Purpose

**Welcome, Mortals** is a reusable static portfolio theme. Welcome, Mortals transforms a standard professional portfolio into a playful haunted attraction. The design uses a dark purple backdrop, Halloween-orange highlights, parchment-like text surfaces, lime accents, custom cursor treatment, and a spider-scare component. Its content structure remains practical: visitors can still find an introduction, biography, projects, skills, writing, case studies, testimonials, work history, and contact information. The theme is ideal for developers, designers, illustrators, horror fans, seasonal creators, and anyone whose portfolio benefits from a memorable spooky presentation.

This project is intentionally delivered as plain HTML, CSS, and Vanilla JavaScript. It can be opened locally, hosted on GitHub Pages, or adapted into a standalone repository without installing Node.js or running a build command.

### Intended Users

This theme is best suited to portfolio owners who want a site with a defined personality rather than a generic landing-page layout. It can be adapted for software development, design, technical writing, digital art, creative work, freelance services, coursework, personal projects, or a combination of professional and personal storytelling.

### Design Style and Inspiration

The theme borrows from haunted-house signage, Halloween party invitations, campy horror hosts, eerie storybook pages, and old web pages that were not afraid to surprise visitors. Its tone is spooky but playful rather than graphic or grim.

The theme should not be “cleaned up” into a different visual language when it is customized. The unusual interface choices are the point of the design. New content should be fitted into the existing structure while preserving the utility classes, spacing, layout, and palette unless the person reusing the theme intentionally decides to create a new variation.

### Main Color Palette

| Color | Hex | Primary Use |
| --- | --- | --- |
| Haunted Purple | #2A1B3D | Primary background |
| Pumpkin Orange | #FF7518 | Headings and Halloween accents |
| Parchment | #F4F1E8 | Readable story surfaces |
| Lawn Green | #7CFC00 | Unexpected neon accent |
| White | #FFFFFF | High-contrast readable text |

### Preview Screenshot

The included screenshot shows the theme’s default homepage presentation:

![Welcome, Mortals homepage preview](images/screenshots/welcome-mortals-screenshot-01.png)

---

## Pages Included

The original routed page architecture has been preserved as separate HTML documents. No pages were merged into a single file.

| Page | Purpose |
| --- | --- |
| `index.html` | Haunted welcome page that introduces the host and establishes the themed experience. |
| `pages/about.html` | Biography page titled Meet Your Host. |
| `pages/projects.html` | Project portfolio presented as The Crypt. |
| `pages/work.html` | Career history framed as Past Lives. |
| `pages/skills.html` | Skills collection titled Trick or Treat Bag. |
| `pages/blog.html` | Writing archive titled Tales from the Crypt. |
| `pages/case-studies.html` | Technical breakdowns presented as Field Reports. |
| `pages/testimonials.html` | Testimonials titled Eyewitness Reports. |
| `pages/contact.html` | Contact page titled Send a Message. |

`index.html` is the entry point for GitHub Pages. The remaining documents live inside `pages/` so that each original page continues to exist as its own independently editable static file.

---

## Component Architecture

### Separated Static Components

The original reusable React component boundaries have been retained as separated static files. Each original visual component has an HTML template and a matching Vanilla JavaScript module where behavior is needed.

| Static HTML Component | Vanilla JavaScript Module | Purpose |
| --- | --- | --- |
| `components/CustomCursor.html` | `js/components/CustomCursor.js` | Applies the themed cursor behavior. |
| `components/Layout.html` | `js/components/Layout.js` | Provides the consistent haunted page framing and navigation. |
| `components/SpiderScare.html` | `js/components/SpiderScare.js` | Creates the surprise spider interaction. |
| `components/SpookHost.html` | `js/components/SpookHost.js` | Renders the horror-host presentation element. |

Additional shared fragments such as `components/footer.html`, `components/navigation.html`, `components/copyright-footer.html`, and `components/source-utility-class-inventory.html` are included to keep the static project organized and to preserve the conversion audit trail.

### Shared JavaScript Modules

| Module | Responsibility |
| --- | --- |
| `js/site.js` | Initializes the theme after the static document loads. |
| `js/navigation.js` | Handles shared static navigation behavior. |
| `js/routes.js` | Stores route-aware logic without requiring React Router. |
| `js/animations.js` | Applies lightweight motion and transition behavior through browser APIs. |
| `js/interactions.js` | Collects general theme interactions that do not belong to a single component. |
| `js/component-loader.js` | Supports separated reusable static component fragments. |

### Theme-Specific Interactive Behavior

- The custom cursor and spider-scare behavior are implemented in Vanilla JavaScript.
- Navigation uses standard static links.
- Decorative effects are isolated from content so the site remains usable if JavaScript is unavailable.
- Entrance effects are handled through shared animation scripts.

---

## File and Folder Structure

```text
├── components/
│   ├── copyright-footer.html
│   ├── CustomCursor.html
│   ├── footer.html
│   ├── header.html
│   ├── Layout.html
│   ├── source-utility-class-inventory.html
│   ├── SpiderScare.html
│   └── SpookHost.html
├── css/
│   └── styles.css
├── images/
│   └── screenshots/
├── js/
│   ├── components/
│   │   ├── CustomCursor.js
│   │   ├── Layout.js
│   │   ├── SpiderScare.js
│   │   └── SpookHost.js
│   ├── source-modules/
│   │   ├── canvas.manifest.js
│   │   └── useScreenInit.js
│   ├── animations.js
│   ├── component-loader.js
│   ├── interactions.js
│   ├── navigation.js
│   ├── routes.js
│   └── site.js
├── layouts/
│   └── page-shell.html
├── pages/
│   ├── about.html
│   ├── blog.html
│   ├── case-studies.html
│   ├── contact.html
│   ├── projects.html
│   ├── skills.html
│   ├── testimonials.html
│   └── work.html
├── ARCHITECTURE-MAP.json
├── index.html
└── README.md
```

The folders work together as follows:

- `index.html` is the main entry page.
- `pages/` contains one static HTML document for each routed page from the original project.
- `components/` contains separated reusable HTML fragments that correspond to the original reusable interface pieces.
- `layouts/` contains the shared page shell.
- `css/styles.css` contains the complete standalone stylesheet.
- `js/` contains shared Vanilla JavaScript behavior.
- `js/components/` contains component-specific behavior modules.
- `images/screenshots/` contains readable preview-image filenames for documentation and repository browsing.
- `ARCHITECTURE-MAP.json` records the original React/Vite sources and their static equivalents.

---

## Static Conversion Notes

This version is designed to work as a true GitHub Pages-compatible static project.

The conversion follows these rules:

- React and Vite runtime files are not required in the deployed theme.
- Every original page component maps to an individual HTML file.
- Reusable components remain separated instead of being merged into one large HTML document.
- Tailwind utility classes remain on the live HTML elements so the original layout, margins, padding, grids, flex behavior, and theme styling are preserved.
- React Router links have been changed to standard HTML anchors.
- Framework-driven motion has been replaced with Vanilla JavaScript, browser-native animation behavior, or CSS transitions.
- The theme can be hosted directly from a repository without compiling source files first.

---

## Customization Guide

### Personal Information and Branding

Start with `index.html`. Replace the displayed portfolio-owner name, professional headline, homepage introduction, and any theme-specific labels that should reflect the new owner’s voice. Preserve the surrounding elements and class attributes while editing the words inside them.

### Biography and Life Story

Update the main biography inside `pages/about.html`. This is the best place to explain the portfolio owner’s background, goals, interests, career transition, education, creative influences, or personal approach to work. The copy can be detailed, but it should be broken into readable paragraphs that fit the theme’s existing card or window structure.

### Projects, Skills, Services, and Experience

Use the following files as the primary editing locations:

- `pages/projects.html` for featured portfolio work, repositories, screenshots, descriptions, and links.
- `pages/skills.html` for languages, frameworks, databases, tools, design capabilities, or service categories.
- `pages/work.html` when this theme includes a work-history page.
- `pages/case-studies.html` for detailed project breakdowns.
- `pages/blog.html`, `pages/articles.html`, or `pages/writing.html` when the theme includes writing content.

### Contact Information and Social Links

Edit `pages/contact.html` and any shared navigation or footer fragment that contains contact details. Replace email addresses, GitHub links, LinkedIn links, repository links, downloadable-resume links, and social profiles before publishing.

### Images and Screenshots

Store replacement images inside `images/` or a clearly named subfolder. Use readable filenames. Replace `images/screenshots/welcome-mortals-screenshot-01.png` after making changes so the repository documentation shows the customized design rather than the default screenshot.

### Colors, Fonts, and Styling

The original visual identity lives in `css/styles.css`. Search for the palette values documented above before changing colors. Make targeted changes rather than rewriting the stylesheet wholesale. This keeps the theme recognizable and prevents accidental layout drift.

### Theme-Specific Editing Checklist

1. Replace the host name and introduction in `index.html`.
2. Edit the personal story in `pages/about.html`.
3. Update crypt project cards in `pages/projects.html`, prior roles in `pages/work.html`, and contact copy in `pages/contact.html`.
4. Modify the scare behavior through `components/SpiderScare.html` and `js/components/SpiderScare.js`.
5. Change purple, pumpkin-orange, parchment, and green styling in `css/styles.css`.

---

## GitHub Pages Deployment

This project can be deployed as a standalone GitHub Pages site:

1. Create a new GitHub repository.
2. Upload the contents of this theme folder so `index.html` sits at the repository root.
3. Open the repository **Settings** page.
4. Select **Pages** from the sidebar.
5. Under **Build and deployment**, choose **Deploy from a branch**.
6. Select the branch containing the theme files, usually `main`.
7. Select the root folder and save the Pages configuration.
8. Wait for GitHub Pages to publish the repository.
9. Open the provided Pages URL and test every internal link.

Because the project uses relative paths and static files, it does not require a package installation step or a build pipeline.

---

## Accessibility and Browser Compatibility

### Accessibility Considerations

The spider surprise should remain decorative and should not obstruct navigation, trap focus, or flash rapidly. Test the theme with reduced motion enabled. Keep orange and lime accents for emphasis rather than long body text.

Before publishing a customized version, test keyboard navigation, link focus states, mobile width behavior, image alternative text, readable heading order, and reduced-motion preferences.

### Browser Compatibility

The static project is intended for current versions of Chrome, Firefox, Safari, and Edge. The design may imitate older browsers or operating systems, but the underlying files use modern static web standards. Test the final personalized version on both desktop and mobile screens because the theme’s decorative elements can make spacing changes more noticeable.

---

## Repository Relationship

This theme can be published as its own standalone repository:

- Standalone theme repository placeholder: `https://github.com/apursley2012/welcome-mortals`
- Main Portfolio Themes Templates collection: `https://github.com/apursley2012/portfolio-themes-templates`

When this theme is split into its own repository, the standalone README should keep a link back to the main collection so visitors can browse related designs. The collection repository should also link to the standalone theme repository and its live GitHub Pages demo.

---

## Possible Future Enhancements

- Add a visible reduced-motion option for visitors who prefer a calmer experience.
- Add seasonal alternate palettes.
- Create a themed 404 page that looks like a locked crypt door.

---

## Copyright

Copyright © 2026 Alysha Pursley. All rights reserved.

This theme documentation and converted static project are maintained by Alysha Pursley. Review the repository license and project-specific usage terms before redistributing modified versions.
